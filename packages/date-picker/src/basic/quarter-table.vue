<!--
 * @Descripttion: 季度组件面板
 * @Author: 19080088
 * @Date: 2020-11-24 10:49:51
 * @LastEditors: 19080088
 * @LastEditTime: 2020-12-24 17:55:22
-->
<template>
  <table @click="handleQuraterTableClick" class="el-quarter-table">
    <tbody>
      <tr>
        <td class="available" :class="getCellStyle([1, 2, 3])">
          <a class="cell">
            <p class="quarter-value">Q1</p>
            <p>1月 - 3月</p>
          </a>
        </td>
        <td  td class="available" :class="getCellStyle([4, 5, 6])">
          <a class="cell">
            <p class="quarter-value">Q2</p>
            <p>4月 - 6月</p>
          </a>
        </td>
      </tr>
      <tr>
        <td class="available" :class="getCellStyle([7, 8, 9])">
          <a class="cell">
            <p class="quarter-value">Q3</p>
            <p>7月 - 9月</p>
          </a>
        </td>
        <td class="available" :class="getCellStyle([10, 11, 12])">
          <a class="cell">
            <p class="quarter-value">Q4</p>
            <p>10月 - 12月</p>
          </a>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
  import { hasClass } from 'element-ui/src/utils/dom';
  import { arrayFindIndex, coerceTruthyValueToArray } from 'element-ui/src/utils/util';
  
  export default {
    name: 'QuraterTable',
    props: {
      date: {},
      value: {}
    },
    data() {
      return {
      };
    },
    methods: {
      getCellStyle(quarterList) {
        const style = {};
        const today = new Date();
        const year = this.date.getFullYear();
        style.today = today.getFullYear() === year && quarterList.includes(today.getMonth());
        style.current = arrayFindIndex(coerceTruthyValueToArray(this.value), date => date.getFullYear() === year && quarterList.includes(date.getMonth())) >= 0;
        console.log('quarterList: ', quarterList);
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
          'Q1': 2,
          'Q2': 5,
          'Q3': 8,
          'Q4': 11
        };
        this.$emit('pick', Number(transfromMonth[quarter]));
      }
    }
  };
</script>