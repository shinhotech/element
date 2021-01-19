<!--
 * @Descripttion: 季度组件面板
 * @Author: 19080088
 * @Date: 2020-11-24 10:49:51
 * @LastEditors: 19080088
 * @LastEditTime: 2021-01-19 14:40:13
-->
<template>
  <table @click="handleQuraterTableClick" class="el-quarter-table">
    <tbody>
      <tr>
        <td class="available" :class="getCellStyle([1, 2, 3])">
          <a class="cell">
            <p class="quarter-value">Q1</p>
            <p>{{ t('el.datepicker.months.' + months[0]) }} - {{ t('el.datepicker.months.' + months[2]) }}</p>
          </a>
        </td>
        <td  td class="available" :class="getCellStyle([4, 5, 6])">
          <a class="cell">
            <p class="quarter-value">Q2</p>
            <p>{{ t('el.datepicker.months.' + months[3]) }} - {{ t('el.datepicker.months.' + months[5]) }}</p>
          </a>
        </td>
      </tr>
      <tr>
        <td class="available" :class="getCellStyle([7, 8, 9])">
          <a class="cell">
            <p class="quarter-value">Q3</p>
            <p>{{ t('el.datepicker.months.' + months[6]) }} - {{ t('el.datepicker.months.' + months[8]) }}</p>
          </a>
        </td>
        <td class="available" :class="getCellStyle([10, 11, 12])">
          <a class="cell">
            <p class="quarter-value">Q4</p>
            <p>{{ t('el.datepicker.months.' + months[9]) }} - {{ t('el.datepicker.months.' + months[11]) }}</p>
          </a>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
  import { hasClass } from 'shinho-sh-ui/src/utils/dom';
  import Locale from 'shinho-sh-ui/src/mixins/locale';
  import { arrayFindIndex, coerceTruthyValueToArray } from 'shinho-sh-ui/src/utils/util';
  const datesInMonth = (year, month) => {
    const firstDay = new Date(year, month, 1);
    return [firstDay];
  };
  export default {
    name: 'QuraterTable',
    props: {
      disabledDate: {},
      date: {},
      value: {}
    },
    data() {
      return {
        months: ['jan', 'feb', 'mar', 'apr', 'may', 'jun', 'jul', 'aug', 'sep', 'oct', 'nov', 'dec']
      };
    },
    mixins: [Locale],
    methods: {
      getCellStyle(quarterList) {
        const style = {};
        const today = new Date();
        let year = this.date.getFullYear();
        let month = quarterList[0] - 1;
        style.disabled = typeof this.disabledDate === 'function'
          ? datesInMonth(year, month).every(this.disabledDate)
          : false;
        style.today = today.getFullYear() === year && quarterList.includes(today.getMonth() + 1);
        style.current = arrayFindIndex(coerceTruthyValueToArray(this.value), date => date.getFullYear() === year && quarterList.includes(date.getMonth() + 1)) >= 0;
        return style;
      },
      handleQuraterTableClick(event) {
        let target = event.target;
        if (target.tagName === 'P') {
          target = target.parentNode;
        }
        if (hasClass(target.parentNode, 'disabled')) return;
        const quarter = target.children[0] ? (target.children[0].textContent || target.children[0].innerHTML) : '';
        const transfromMonth = {
          'Q1': 0,
          'Q2': 3,
          'Q3': 6,
          'Q4': 9
        };
        this.$emit('pick', Number(transfromMonth[quarter]));
      }
    }
  };
</script>