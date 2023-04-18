<script setup>
import ComputerIcon from './icons/IconComputer.vue'
import InternetIcon from './icons/IconInternet.vue'
import PhoneIcon from './icons/IconPhone.vue'
import RocketIcon from './icons/IconRocket.vue'
import Modal from './Modal.vue'
</script>

<template>
  <img src="/home-header-graphics.webp" alt="new pic" class="bannerImage" width="auto" height="auto"/>
  <div class="bannerTextContainer">
    <div>
    <h1 class="bannerHeading pb-4 text-[#331B3B]">
      <span class="bannerSpecialWords">We Help you</span><br/>
      to grow your <span class="specialTextUnderline1"><span class="specialUnderline1"></span>Business</span>
    </h1>
    <p class="bannerText text-[#78697E]">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
    <button type="button" class="bannerButton pt-4">Get Started</button>
    </div>
  </div>
  <div class="section2">
    <img src="/ellipse.svg" class="ellipsebg" alt="background ellipse">
    <div class="bgCurve"></div>
    <div class="section2TitleContainer">
      <div>
      <h2 class="sectionTitle text-[#331B3B] pb-20"><span class="bannerSpecialWords">What We Do</span><br/>For Your 
        <span class="specialTextUnderline2"><span class="specialUnderline2"></span>Business</span>
      </h2>
      </div>
    </div>
    <div class="section2Grid">
      <div class="gridBox">
        <div class="cardContainer">
          <div class="iconContainer bg-[#FCE7F3]"><InternetIcon/></div>
          <div class="cardHeading">WEBSITE DESIGN</div>
          <div class="cardText">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</div>
        </div>
      </div>
      <div class="gridBox">
        <div class="cardContainer">
          <div class="iconContainer bg-[#FEF3C7]"><ComputerIcon/></div>
          <div class="cardHeading">WEB DEVELOPMENT</div>
          <div class="cardText">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</div>
        </div>
      </div>
      <div class="gridBox">
        <div class="cardContainer ">
          <div class="iconContainer bg-[#BAE6FD]"><PhoneIcon/></div>
          <div class="cardHeading">MOBILE APP DEVELOPMENT</div>
          <div class="cardText">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</div>
        </div>
      </div>
      <div class="gridBox">
        <div class="cardContainer">
          <div class="iconContainer bg-[#FEE2E2]"><RocketIcon/></div>
          <div class="cardHeading">MARKETING</div>
          <div class="cardText">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.</div>
        </div>
      </div>
    </div>
  </div>
  <div class="section3">
    <div class="section3ImageContainer">
      <img src="/about-graphics.webp"  class="section3Image" alt="Team sitting around enjoying a conversation" width="auto" height="auto">
    </div>
    <div class="section3Text">
      <h2 class="sectionTitle text-[#331B3B] pb-10"><span class="bannerSpecialWords">About Us</span><br/>Fake or 
        <span class="specialTextUnderline2"><span class="specialUnderline2"></span>Real</span>
        
      </h2>
      <p class="text-[#331B3B] pb-6">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>

      <p class="text-[#331B3B] pb-6">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
      <button type="button" class="bannerButton">Explore More</button>
    </div>
  </div>
  <div class="IndexFooter text-[#fff]">
    <div class="footerGrid">
      <div class="footerGridBox">
        <h1 class="text-[36px] pb-5 georgia font-[700]" >Dream Agency</h1>
        <p>Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries.</p>
      </div>
      <div class="footerGridBox justify-center flex ">
        <div>
          <p class="font-[700] text-18px">GET IN TOUCH</p>
          <Modal/>
        </div>
      </div>
      <div class="footerGridBox3"></div>
    </div>
  </div>
</template>

<style scoped>

.specialTextUnderline1{
  position: relative;
  display: flex;
  align-items: center;
}
.specialTextUnderline2{
  position: relative;
}
.specialUnderline1{
  z-index: -1;
  background-color: #FBBF24;
  width: 270px;
  height: 20px;
  position: absolute;
  bottom: 15px;
}
.specialUnderline2{
  width: 100%;
  height: 10px;
  z-index: -1;
  background-color: #FBBF24;
  position: absolute;
  bottom: 10px;

}
.bannerImage{
  position: absolute;
  z-index: -1;
  top: 0;
  right: 0;
  width: 800px;
}
.bannerTextContainer{
  width:550px;
  padding-left: 60px;
  height: 714px;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.bannerHeading{
  font-size: 72px;
}
.bannerSpecialWords{
  font-weight: 900;
}
.bannerButton{
  background-color: #331B3B;
  padding: 16px 32px;
  border-radius: 10px;
  color: white;
  margin-top: 30px;
  font-weight: 700;
}

.section2{
  position: relative;
  padding: 70px 10px;
  margin: 100px 0;
}
.section2TitleContainer{
  display: flex;
  justify-content: center;
  text-align: center;
}
.sectionTitle{
  font-size: 48px;
}
.bgCurve{
  width: 95%;
  height: 100%;
  background-color: #E0F2FE;
  border-radius: 0 400px 0 0;
  position: absolute;
  z-index: -1;
  left: 0;
  top:0;
}
.ellipsebg{
  position: absolute;
  right: 0;
  z-index: -1;
}
.section2Grid{
  display: grid;
  grid-template-columns: repeat(4, 300px);
  gap: 50px;
  justify-content: center;
}
.cardContainer{
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 0 9px 2px #0000000D;
}
.iconContainer{
  width: 50px;
  display: flex;
  justify-content: center;
  border-radius: 10px;
}
.cardHeading{
  color: #331B3B;
  font-weight: 700;
  padding:  10px 0;
}
.cardText{
  font-size: 14px;
  color: #78697E;
}
.section3{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 50px;
  padding: 50px 10px;
}
.section3Image{
  width: 800px;
}
.section3Text{
  width: 550px;
  padding: 10px;
}
.IndexFooter{
  background-color: #331B3B;
  border-radius: 0 120px 0 0;
  padding: 50px 10px 10px;
}
.footerGrid{
  display: grid;
  grid-template-columns: repeat(3, 33%);
  justify-content: space-between;
  align-items: flex-end;
}

@media screen and (max-width: 1300px){
  .bannerTextContainer{
    padding: 10px;
  }
}
@media screen and (max-width: 1430px) {
  .bannerImage{
    width: 50%;
  }
  .bannerTextContainer{
    width: 45%;
  }
  .section2Grid{
    grid-template-columns: repeat(3, 300px);
  }
  
}
@media screen and (max-width: 1080px) {
  .section2Grid{
    grid-template-columns: repeat(2, 300px);
  }
  .bannerImage{
    width: 100%;
    max-width: 450px;
    position: absolute;
    top: 0;
  }
  .bannerTextContainer{
    width: 100%;
    margin-top: 400px;
  }
  .section3{
    flex-direction: column;
  }
  .section3Image, .section3Text{
    width: 100%;
    max-width: 450px;
  }
  .IndexFooter{
    margin: 0 auto;
  }
  .footerGrid{
    grid-template-columns: auto;
    gap: 50px;
  }
  .footerGridBox3{
    display: none;
  }

}
@media screen and (max-width: 770px){
  .section2Grid{
    display: flex;
    flex-direction: column;
  }
}
</style>