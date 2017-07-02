<template>
  <header class="iblk clear w">
    <div class="iblk vt-base" style="margin-left: .15rem;">
      <img src="../assets/resume.png" class="logo">
    </div>
    <div class="tip iblk vt-base">
      <p v-for="tip in tips">
        {{ tip }}
      </p>
    </div>
    <hr class="trapezoid" style="margin: .2rem 0 0; border-bottom: none;"></hr>
  </header>
</template>

<script>
export default {
  name: 'head',
  data () {
    return {
      tips: ['Resume','学习是一种生活态度']
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import url('../../static/css/common.css');
  .logo{
    width: 1.3rem;
  }
  .tip{
    color: rgb(142,170,219);
    font-size: .28rem;
    margin-left: .18rem;
  }
</style>
