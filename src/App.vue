<template>
  <div id="app">
    <div class="nav">
      <h1>Care to Vote</h1>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>

body {
  overflow: hidden;
}

.clearfix:after {
  visibility: hidden;
  display: block;
  font-size: 0;
  content: " ";
  clear: both;
  height: 0;
}
.clearfix { display: inline-block; }
/* start commented backslash hack \*/
* html .clearfix { height: 1%; }
.clearfix { display: block; }
/* close commented backslash hack */

#app {
  font-family: -apple-system, BlinkMacSystemFont, "Helvetica Neue", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 44px;
  padding: 1em 0.5em;
}

.nav {
  padding: 0;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 10000;
  background: #FFFFFF;
  height: 44px;
  border-bottom: 1px solid #DDD;
  text-align: center;
  -moz-box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.1), 0px 1px 0px rgba(0, 0, 0, 0.1);
  -webkit-box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.1), 0px 1px 0px rgba(0, 0, 0, 0.1);
  box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.1), 0px 1px 0px rgba(0, 0, 0, 0.1)
}

.nav h1 {
  font-size: 18px;
  line-height: 18px;
  text-transform: uppercase;
  letter-spacing: 0.01em;
  color: #DA343C;
}

</style>
