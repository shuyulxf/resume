<template>
  <div class="rect" v-bind:class="bgColor">
    <i class="tip iblk font-14">{{tip}}</i>
  </div>
</template>

<script>
export default {
  name: 'rectangle',
  data () {
    return {
    }
  },
  computed: {
    bgColor: function () {

      return {
        'bg-color': this.bg ? false : true,
        'rect-bg': this.bg ? true : false
      }
    }
  },
  props: ['bg','tip'],
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import url('../../static/css/common.css');
  .rect {
    height: .36rem;
    font-size: 0;
  }
  .bg-color{
    background: white;
  }
  .rect-bg{

    background-color: rgb(218,227,243);
  }
  .tip {
    width: 1.05rem;
    height: .36rem;
    line-height: .36rem;
    background: rgb(143, 170, 220);
    color: rgb(204, 232, 207);
    text-align: center;
    font-style: normal;
  }
</style>
