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
  overflow-x: hidden;
  font-family: -apple-system, BlinkMacSystemFont, "Helvetica Neue", Helvetica, Arial, sans-serif;
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
  background: #FFFFFF;
  height: 44px;
  border-bottom: 1px solid #DDD;
  text-align: center;
  -moz-box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.1), 0px 1px 0px rgba(0, 0, 0, 0.1);
  -webkit-box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.1), 0px 1px 0px rgba(0, 0, 0, 0.1);
  box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.1), 0px 1px 0px rgba(0, 0, 0, 0.1);
}

.nav h1 {
  font-size: 18px;
  line-height: 18px;
  text-transform: uppercase;
  letter-spacing: 0.01em;
  color: #DA343C;
}

/* simple modal CSS */

.modal {
  opacity: 0;
  visibility: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  text-align: left;
  background: rgba(0,0,0, .9);
  transition: opacity .25s ease;
}

.modal__bg {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  cursor: pointer;
}

.modal-state {
  display: none;
}

.modal-state:checked + .modal {
  opacity: 1;
  visibility: visible;
}

.modal-state:checked + .modal .modal__inner {
  top: 0;
}

.modal.visible {
  opacity: 1;
  visibility: visible;
}

.modal.visible .modal__inner {
  top: 0;
}

.modal__inner {
  transition: top .25s ease;
  position: absolute;
  top: -20%;
  right: 0;
  bottom: 0;
  left: 0;
  width: 50%;
  margin: auto;
  overflow: auto;
  background: #fff;
  border-radius: 5px;
  padding: 1em 2em;
  min-height: 235px;
}

.modal__close {
  position: absolute;
  right: 1.5em;
  top: 1.5em;
  width: 1.1em;
  height: 1.1em;
  cursor: pointer;
}

.modal__close:after,
.modal__close:before {
  content: '';
  position: absolute;
  width: 2px;
  height: 2em;
  background: #ccc;
  display: block;
  transform: rotate(45deg);
  left: 50%;
  margin: -3px 0 0 -1px;
  top: 0;
}

.modal__close:hover:after,
.modal__close:hover:before {
  background: #aaa;
}

.modal__close:before {
  transform: rotate(-45deg);
}

@media screen and (max-width: 768px) {
  
  .modal__inner {
    width: 90%;
    height: 30%;
    box-sizing: border-box;
  }
}

/* end of simple modal CSS*/

</style>
