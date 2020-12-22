<!--
 * @Descripttion: 季度组件面板
 * @Author: 19080088
 * @Date: 2020-11-24 10:49:51
 * @LastEditors: 19080088
 * @LastEditTime: 2020-12-22 18:01:00
-->
<template>
  <table @click="handleQuraterTableClick" class="el-qurater-table">
    <tbody>
      <tr>
        <td class="available">
          <a class="cell">
            <p class="qurater-value">Q1</p>
            <p>1月 - 3月</p>
          </a>
        </td>
        <td  td class="available">
          <a class="cell">
            <p class="qurater-value">Q2</p>
            <p>4月 - 6月</p>
          </a>
        </td>
      </tr>
      <tr>
        <td class="available">
          <a class="cell">
            <p class="qurater-value">Q3</p>
            <p>7月 - 9月</p>
          </a>
        </td>
        <td class="available">
          <a class="cell">
            <p class="qurater-value">Q4</p>
            <p>10月 - 12月</p>
          </a>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
  import { hasClass } from 'element-ui/src/utils/dom';
  export default {
    name: 'QuraterTable',
    components: {},
    data() {
      return {
      };
    },
    computed: {},
    mounted() {},
    methods: {
      handleQuraterTableClick(event) {
        let target = event.target;
        if (target.tagName === 'P') {
          target = target.parentNode;
        }
        if (hasClass(target.parentNode, 'disabled')) return;
        const qurater = target.children[0] ? (target.children[0].textContent || target.children[0].innerHTML) : '';
        console.log('qurater: ', qurater);
        this.$emit('pick', qurater);
      }
    }
  };
</script>