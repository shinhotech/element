<!--
 * @Descripttion: 季度组件面板
 * @Author: 19080088
 * @Date: 2020-11-24 10:49:51
 * @LastEditors: 19080088
 * @LastEditTime: 2020-12-17 14:33:28
-->
<template>
  <table @click="handleQuraterTableClick" class="el-qurater-table">
    <tbody>
      <tr>
        <td class="available">
          <a class="cell">
            <p>Q1</p>
            <p>1月 - 3月</p>
          </a>
        </td>
        <td  td class="available">
          <a class="cell">
            <p>Q2</p>
            <p>4月 - 6月</p>
          </a>
        </td>
      </tr>
      <tr>
        <td class="available">
          <a class="cell">
            <p>Q3</p>
            <p>7月 - 9月</p>
          </a>
        </td>
        <td class="available">
          <a class="cell">
            <p>Q4</p>
            <p>10月 - 12月</p>
          </a>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
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
      console.log('event: ', event);
    }
  }
};
</script>

<style lang="scss" scoped>
</style>