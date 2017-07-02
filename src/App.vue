<template>
  <main id="app">
    <tip>
      
    </tip>
    <article>
      <baseInfo></baseInfo>
      <detailInfo></detailInfo>
    </article>
  </main>
</template>

<script>
import Tip from './components/Tip';
import BaseInfo from './components/BaseInfo';
import DetailInfo from './components/DetailInfo';

export default {
  name: 'app',
  components: {
    Tip,
    BaseInfo,
    DetailInfo
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #444;
  margin: 0.44rem auto;
  width: 100%;
  max-width: 900px;
  box-sizing: border-box;
  box-shadow: 0 0 5px #ddd;
  padding: 0.44rem;
}
.mobile #app {
  margin: 0;
}
</style>
