<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  name: 'App',
  data () {
    return {
      showModal: true
    }
  },
  setup () {

  }
})
</script>

<template>
<div id="app">
  <div class="icon-1" @click="showModal = true"> </div>
 <button class="button" @click="showModal = true">
  Show Modal
 </button>
<svg width="5cm" height="4cm" version="1.1" @click="showModal = true"
     xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
<image href="../assets/Facebook.svg" x="0" y="0" height="50px" width="50px"/>
</svg>
 <transition name="fade" appear>
  <div class="modal-overlay" v-if="showModal" @click="showModal = false"></div>
 </transition>
 <transition name="slide" appear>
  <div class="modal" v-if="showModal">
   <h1>Lorem Ipsum</h1>
   <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem provident explicabo accusamus laudantium voluptatum nobis sed nesciunt neque possimus molestiae?</p>
   <button class="button" @click="showModal = false">
    Close Modal
   </button>
  </div>
 </transition>
</div>

</template>

<style lang="scss" scoped>

.button-white{
 width: 100%;
  height:0;
  padding-bottom: 100%;
  border-radius: 50%;
  border:10px solid #cfdcec;
  overflow:hidden;
  background: #4679BD;
  box-shadow: 0 0 3px gray
}
* {
 margin: 0;
 padding: 0;
 box-sizing: border-box;
}

body {
 font-family: 'montserrat', sans-serif;
}

#app {
 position: relative;
  background-color: yellow;
 display: flex;
 justify-content: center;
 align-items: center;

 width: 100vw;
 min-height: 100vh;
 overflow-x: hidden;
}

.button {
 appearance: none;
 outline: none;
 border: none;
 background: none;
 cursor: pointer;

 display: inline-block;
 padding: 15px 25px;
 background-image: linear-gradient(to right, #CC2E5D, #FF5858);
 border-radius: 8px;

 color: #FFF;
 font-size: 18px;
 font-weight: 700;

 box-shadow: 3px 3px rgba(0, 0, 0, 0.4);
 transition: 0.4s ease-out;

 &:hover {
  box-shadow: 6px 6px rgba(0, 0, 0, 0.6);
 }
}

.modal-overlay {
 position: absolute;
 top: 0;
 left: 0;
 right: 0;
 bottom: 0;
 z-index: 98;
 background-color: rgba(0, 0, 0, 0.3);
}

.modal {
 position: fixed;
 top: 50%;
 transform: translate(-50%, -50%);
 z-index: 99;
 height: 900px;
 width: 1000px;
 background-color: #FFF;
 border-radius: 16px;

 padding: 25px;

 h1 {
text-align: right;
  color: #222;
  font-size: 32px;
  font-weight: 900;
  right: 1;
  margin-bottom: 15px;
 }

 p {
  color: #666;
  font-size: 18px;
  font-weight: 400;
  margin-bottom: 15px;
 }
}

.fade-enter-active,
.fade-leave-active {
 transition: opacity .5s;
}

.fade-enter,
.fade-leave-to {
 opacity: 0;
}

.slide-enter-active,
.slide-leave-active {
 transition: transform .5s;
}

.slide-enter,
.slide-leave-to {
 transform: translateY(-50%) translateX(100vw);
}
.icon-1{
position: absolute;
bottom: 108px;
right: 0;
display: block;
  text-indent: -9999px;
  width: 100px;
  height: 82px;
  background: url("../assets/Facebook.svg");
  background-size: 100px 82px;
  }
</style>
