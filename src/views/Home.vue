<script>

import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  name: 'App',
  data () {
    return {
      showModal: false
    }
  }
})
</script>

<template>
  <div class="home">
    <section class="hero">
      <div class="hero-text container">
        <div class="flexbox-container">
        <h2>
          Explore
        </h2>
        <svg width="5cm" height="4cm" version="1.1" @click="showModal = true" class="icon-click"
     xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
<image href="../assets/Plus.svg" x="0" y="0" height="30px" width="30px"/>
        </svg>
        <h3>
  More details
</h3>
             <transition name="fade" appear>
  <div class="modal-overlay" v-if="showModal" @click="showModal = false"></div>
 </transition>
 <transition name="slide" appear>
  <div class="modal cl-btn" v-if="showModal">
   <h1>Explore</h1>
   <p>Sed ut perspiciatis unde omnis iste natus error
     sit voluptatem accusantium doloremque laudantium,
     totam rem aperiam, eaque ipsa quae ab illo inventore
     veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi
     consequatur?
   </p>
   <button class="button-btg" @click="showModal = false">
    Read More
   </button>
  </div>
 </transition>
            <div class="icon-2">
</div>
      </div>

     <a href="https://facebook.com" target="_blank" rel="noopener">
     <div class="icon-1">
</div> </a>
             <a href="https://instagram.com" target="_blank" rel="noopener">
             <div class="icon">
</div>
</a>
       </div>
    </section>
  </div>
</template>

<style lang="scss" scoped>
.hero {
  background-image: url("../assets/Coding-Challenge-Image.png");
  background-size: cover;
  height: auto;
  background-attachment: fixed;
  position: relative;
  height: 100vh;
  font-family: 'EssonnesText', bold;
.flexbox-container{
     padding-top: 50px;
  padding-right: 300px;
  padding-bottom: 50px;
  padding-left: 80px;
  float: left;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  bottom: 0;
  display: flex;
  flex-direction: column;
  background-color: #611818;

}
.cl-btn{

}
h3{
   color: rgba(250, 250, 250, 0.863);
  position: absolute;
  top: 64%;
  right:0px;
 font-size: 30px;
}
h2{
 margin: 0;
  position: absolute;
  top: 60%;
  right:100px;
  left: 50%;
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}

.icon-click{
   color: rgba(250, 250, 250, 0.863);
  position: absolute;
  right: 20px;
  top:66%;
}
  .hero-text {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: #fff;
      padding-top: 50px;
    padding-right: 30px;
  padding-bottom: 50px;
  padding-left: 80px;

    h4 {
      text-transform: uppercase;
      font-size: 22px;
      padding-bottom: 4px;
    }

    h2 {
      font-size: 50px;
      @media (min-width: 1100px) {
        font-size: 200px;
      }
    }
  .modal {
 position: fixed;
 top: 50%;
 right: 50%;
 transform: translate(-50%, -50%);
 z-index: 99;
 height: 900px;
 width: 700px;
 left: 500px;
 background-color: #FFF;
 border-radius: 16px;
 @media (max-width: 1100px) {
        top: 60%;
        right: 50%;
         height: 550px;
        width: 400px;
        left: 200px;
         background-color: #FFF;
         padding: 0;
      }
.button-btg {
 appearance: none;
 outline: none;
 border: none;
 background: none;
 position: absolute;
 left: 0;
 cursor: pointer;
 display: inline-block;
 padding: 15px 25px;
 background-image: linear-gradient(to right, #CC2E5D, #611818);
 border-radius: 8px;

 color: #FFF;
 font-size: 25px;
 font-weight: 700;
 margin: 100px;

 box-shadow: 3px 3px rgba(0, 0, 0, 0.4);
 transition: 0.4s ease-out;
 &:hover {
  box-shadow: 6px 6px rgba(0, 0, 0, 0.6);
 }
  @media (max-width: 1100px) {
        margin: 10px;
        padding: 15px 25px;
         font-size: 15px;
         position: fixed;
         right: 100 100 ;
      }
}

.modal-overlay {
 position: fixed;
 top: 0;
 left: 0;
 right: 0;
 bottom: 0;
 z-index: 98;
 background-color: rgba(0, 0, 0, 0.3);
}
 h1 {
   text-align: left;
  color: #611818;
  text-decoration: underline;
  text-underline-position: under;
  font-size: 66px;
  font-weight: 900;
  margin-bottom: 10px;
    padding-top: 20px;
  padding-right: 20px;
  padding-left: 50px;
  @media (max-width: 1100px) {
     font-size: 30px;
     margin-bottom: 0px;
    padding-top: 0px;
      }
 }
 p {
   word-break: break-word;
   letter-spacing: 1px;
   line-height: 2;
  padding-top: 20px;
  padding-right: 30px;
  padding-bottom: 50px;
  padding-left: 50px;
  text-align: left;
  color: #666;
  font-size: 18px;
  font-weight: 400;

 }
}
.icon{
position: absolute;
bottom: 12px;
right: 0;
display: block;
  text-indent: -9999px;
  width: 100px;
  height: 82px;
  background: url("../assets/Instagram.svg");
  background-size: 100px 82px;
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
      @media screen and (max-width: 991px) {
    .icon{
       width: 40px;
   height: 62px;
   background-size: 40px 62px;
    }
      .icon-1{
       width: 40px;
   height: 62px;
   background-size: 40px 62px;
    }

}

@media screen and (max-width: 767px) {
.icon{
       width: 40px;
   height: 62px;
   background-size: 40px 62px;
    }
    .icon-1{
       width: 40px;
   height: 62px;
   background-size: 40px 62px;
    }
}

@media screen and (max-width: 500px) {
.icon{
       width: 40px;
   height: 62px;
   background-size: 40px 62px;
    }
    .icon-1{
   width: 40px;
   height: 62px;
   bottom: 55px;
   background-size: 40px 62px;
    }
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
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}

.slide-enter,
.slide-leave-to {
 transform: translateX(10px);
  opacity: 0;
}
@media screen and (max-width: 991px) {
.flexbox-container{
          padding-top: 50px;
  padding-right: 100px;
  padding-bottom: 50px;
  padding-left: 80px;
}
h3{
  font-size: 18px;
  top: 62%;
  right:0px;
}
.icon-click{
   top: 63%;
  right:100px;
  left: 25%;
}
}
@media screen and (max-width: 767px) {
.flexbox-container{
       padding-top: 50px;
  padding-right: 100px;
  padding-bottom: 50px;
  padding-left: 80px;
}
h3{
  font-size: 20px;
  color:white;
}
.icon-click{
   top: 64%;
  right:100px;
  left: 23%;
}
}

@media screen and (max-width: 480px) {
.flexbox-container{
       padding-top: 20px;
  padding-right: 50px;
  padding-bottom: 50px;
  padding-left: 80px;
}
h3{
  font-size: 16px;
  color:yellow;
}
.icon-click{
   top: 64%;
  right:100px;
  left: 10%;
}

}
}

</style>
