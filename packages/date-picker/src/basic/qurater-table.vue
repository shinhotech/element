<!--
 * @Descripttion: 季度组件面板
 * @Author: 19080088
 * @Date: 2020-11-24 10:49:51
 * @LastEditors: 19080088
 * @LastEditTime: 2020-12-04 16:12:27
-->
<template>
  <table @click="handleQuraterTableClick">
    <tbody></tbody>
  </table>
</template>

<script>
export default {
  components: {},
  data () {
    return {
    }
  },
  computed: {},
  mounted () {},
  methods: {
    handleQuraterTableClick (event) {
      console.log('event: ', event);
    }
  }
};
</script>

<style lang="scss" scoped>
</style>