<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavDropdown from './components/NavDropdown.vue'

</script>

<template>
  <header>
    <div class="flex align-center px-4 justify-between">
      <div class="flex justify-center align-center p-4">
        <p class="text-[24px] text-[#331B3B] font-[700] georgia">Dream Agency</p>
      </div>
      <div class="navDropdown">
        <NavDropdown/>
      </div>
      <div class="navLinksContainer flex align-center" >
        <RouterLink class="px-3 py-4 my-4 mx-4 navLinks"  to="/">Home</RouterLink>
        <RouterLink class="px-3 py-4 my-4 mx-4 navLinks" to="/about">About Us</RouterLink>
        <RouterLink class="px-3 py-4 my-4 mx-4 navLinks" to="">Services</RouterLink>
        <RouterLink class="px-3 py-4 my-4 ml-4 navLinks" to="">Contact Us</RouterLink>
      </div>
    </div>
      
  </header>

  <RouterView />
    <div class="footerBranding pt-[48px] text-[14px] text-[#fff]">
      © 2023 Dream Agency, Inc. All right reserved <span></span> Privacy Policy <span></span> Terms of Use
    </div>
</template>

<style scoped>
.navLinks:hover{
    background-color: aqua;
}
.navDropdown{
  display: none;
}
.footerBranding span{
border: solid 1px #FBBF24;
height: 16px;
margin: 0 3px;
}
.footerBranding{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  background-color: #331B3B;
  padding-bottom: 10px;
}
@media screen and (max-width: 700px){
  .navLinksContainer{
    display: none;
  }
  .navDropdown{
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
@media screen and (max-width: 530px){
  .footerBranding{
    display: block;
  }
}
</style>