<template>
  <ion-page>    
    <ion-content :fullscreen="true">
      <div class="top-bar" id="top">
        <ion-text class="bicara-ai-top">Bicara.ai</ion-text>
      </div>

      <div class="top-gradient">
        <div class="top-empty"></div>
        <div class="top-content">
          <ion-text class="title-top1">Improve your<br></ion-text>
          <ion-text class="title-top2" color="secondary">communication skills <br></ion-text>
          <div class="desc-top">
            <ion-text>Bicara.ai is an education platform. Bicara.ai aim to improve indviduals comunication skills with judgement free feedback from our AI-powered speech coach.</ion-text>
          </div>
          <div class="email-regist">
            <ion-img src="assets/icon/email.svg"></ion-img>
            <ion-input class="email-input" placeholder="Your email address"></ion-input>
            <ion-button size="large" color="notify" class="notify">Notify me</ion-button>
          </div>
        </div>
      </div>

      <div class="one">
        <h1>Why use Bicara.ai</h1>
        <ion-img id="num-backg" src="assets/img/1.svg" alt=""></ion-img>
        <ion-row>
          <ion-col size="2"></ion-col>
          <ion-col size="2">
            <ion-card class="card-one">
              <ion-img src="assets/icon/pronunciation.svg"></ion-img>
              <ion-card-title>Pronunciation</ion-card-title></ion-card>
          </ion-col>
          <ion-col size="2">
            <ion-card class="card-one">
              <ion-img src="assets/icon/intonation.svg" class="small"></ion-img>
              <ion-card-title>Intonation</ion-card-title>
            </ion-card>
          </ion-col>
          <ion-col size="2">
            <ion-card class="card-one">
              <ion-img src="assets/icon/eye.svg"></ion-img>
              <ion-card-title>Eye Detection</ion-card-title>
            </ion-card>            
          </ion-col>
          <ion-col size="2">
            <ion-card class="card-one">
              <ion-img src="assets/icon/grammar.svg"></ion-img>
              <ion-card-title>Grammar</ion-card-title>
            </ion-card>
          </ion-col>
          <ion-col size="2"></ion-col>
        </ion-row>
      </div>

      <div class="two">
        <h1>See our analysis example</h1>
        <div>
          <ion-img id="num-backg" src="assets/img/2.svg" alt=""></ion-img>
          <div class="video">
            <iframe width="560" height="315" src="https://www.youtube.com/embed/fpI8Jx65W18" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          </div>
        </div>
      </div>

      <div class="three">
          <ion-img id="num-backg" src="assets/img/3.svg" alt=""></ion-img>
          <h1>How it works</h1>
          <div class="green-bar">
            <ion-img src="assets/img/Union.png"></ion-img>
          </div>
          <ion-row>
          <ion-col size="2"></ion-col>
          <ion-col size="2">
            <p class="card-desc">Step 1</p>
            <ion-card class="card-three"></ion-card>
          </ion-col>
          <ion-col size="2">
            <p class="card-desc">Step 2</p>
            <ion-card class="card-three"></ion-card>
          </ion-col>
          <ion-col size="2">
            <p class="card-desc">Step 3</p>
            <ion-card class="card-three"></ion-card>            
          </ion-col>
          <ion-col size="2">
            <p class="card-desc">Step 4</p>
            <ion-card class="card-three"></ion-card>
          </ion-col>
          <ion-col size="2"></ion-col>
        </ion-row>
        <div class="center">
          <ion-text class="kucing">
              Are you ready to be <br>
              <div class="kelinci"><ion-text class="highlight">
                a better speaker
              </ion-text><ion-text>?</ion-text>
              </div>
          </ion-text>
          <div class="kucing">
              <ion-button class="to-top" size="large" color="im-in" href="#top">
                Yes I'm in
              </ion-button>
          </div>
        </div>
      </div>

      <div class="footer">
        <ion-text class="bicara-ai-bot">Bicara.ai</ion-text>
        <ion-text class="copyright">
          © 2022 Bicara.ai
        </ion-text>
      </div>

    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LandingPage',
  components: {
    IonContent,
    IonPage,
  }
});
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@500;700&family=Krona+One&display=swap');

.bicara-ai-top {
  background: #3F54D1;
  background: radial-gradient(70.14% 53.23% at 53.13% 91.67%, rgba(33,188,207,1) 10%, rgba(82,128,226,1) 79%, rgba(63,84,209,1) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-family: 'Krona One', sans-serif;
  align-self: center;
  font-size: 30px;
  line-height: 100px;
}

.top-bar {
  line-height: 56px;
  height: 100px;
  text-align: center;
}

.top-gradient {
  background: linear-gradient(180deg, rgba(21,205,203,1) -43.28%, rgba(243,244,248,1) 100%);
  height: 562px;
  font-family: 'Inter', sans-serif;
}

.top-content {
  padding-left: 50px;
}

.top-empty {
  height: 76px;
}

.title-top1 {
  font-style: normal;
  font-weight: 700;
  font-size: 40px;
  color: black;
}
.title-top2 {
  font-style: normal;
  font-weight: 700;
  font-size: 40px;
  color: #3F54D1;
}

.desc-top {
  padding-top: 20px;
  font-size: 20px;
  font-weight: 500;
  width: 550px;
  color: #6e7071;
}

.email-regist {
  display: flex;
  width: 468px;
  box-shadow: none;
  background-color: white;
  border-radius: 30px;
  margin-top: 45px;
  padding-left: 24px;
  margin-left: 0px;
  font-size: 20px;
  position: absolute;
}

.email-regist ion-img {
  height: 20px;
  margin:auto;
}

.email-input {
  margin : 0px;
  height: 56px;
  font-size: 20px;
  font-family: 'Inter', sans-serif;
  font-weight: 500;
  color: black;
  z-index: 0;
}

.notify {
  position: absolute;
  margin: 0 auto;
  left:60%;
  height: 56px;
  width: 216px;
  --border-radius: 30px;
  --line-height: 56px;
  --background-color: ;
}

.one {
  background-color: #f3f4f8;
  height: 800px;
}

.one h1 {
  color: #2c3b93;
  font-family: 'Inter', sans-serif;
  font-weight: 700;
  text-align: center;
  padding-top: 64px;
  z-index: 5;  
}

#num-backg {
  margin-top: 25px;
  height: 300px;
  z-index: -1;
}

.one ion-row {
  margin-left: auto;
  margin-right: auto;
}

.one ion-col {
  display: flex;
  justify-content: center;
}

.card-one {
  background-color: white;
  width: 156px;
  height: 248px;
  border-radius: 30px;
}

.card-one.small {
  margin-top: 84px;
  height: 150px;
}
.card-one ion-img {
  margin-top: 84px;
  height: 25px;
}

.card-one ion-card-title {
  color: black;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-weight: 700;
  text-align: center;
  font-size: 20px;
  margin-top: 12px;
}

.two {
  background:#2c3b93;
  height: 800px;
  padding-top: 90px;
}

.two h1 {
  color: #15cdcb;
  font-family: 'Inter', sans-serif;
  font-weight: 700;
  text-align: center;
  z-index: 1;
}

 .video{
  display: flex;
  justify-content: center;
  z-index: 1;
 }

 .three {
  height: 1156px;
 }

 .three-content {
  display: flex;
  justify-content: center;
 }

 .three h1 {
  position: relative;
  color: #2c3b93;
  font-family: 'Inter', sans-serif;
  font-weight: 700;
  text-align: center;
 }

 .green-bar  {
  width: 650px;
  display: block;
  margin-left: auto;
  margin-right: auto;
 }

 .three ion-text {
  font-family: 'Inter', sans-serif;
  font-size: 40px;
  font-weight: 700;
  color: black;
 }

 .highlight {
  background-color: #92ecd1;
 }

 .center {
  display: flex;
  justify-content: center;
  flex-direction: column;
 }

 .three ion-row ion-col {
  display: flex;
  justify-content: center;
  flex-direction: column;
 }

 .card-desc {
  font-size: 24px;
  font-weight: 700;
  color: black;
  text-align: center;
 }

 .card-three {
  background-color: #c8d6da;
  width: 90px;
  height: 84px;
  border-radius: 25px;
  align-self: center;
 }

 .kucing {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: auto;
  margin-top: 20px;
  text-align: center;
 }

 .kelinci {
  text-align: center;
  margin-bottom: 20px;
 }

.to-top {
  --color: white;
  --background-color: #41dcbb;
  --border-radius: 30px;
  --position: absolute;
  --right: 0px;
  --box-shadow: none;
  --font-family: 'Inter', sans-serif;
  --margin: 0 auto;
  --display: block;
}

 .footer {
  background: linear-gradient(90deg, #2c3b93 57%, #33629c 81%, #0f908e 99.9%);
  height: 250px;
 }

 .copyright {
  color: white;
  font-family: 'Inter', sans-serif;
  text-align: right;
  font-size: 20px;
  line-height: 250px;
  position: absolute;
  right: 160px;
 }

 .bicara-ai-bot {
  color: white;
  font-family: 'Krona One', sans-serif;
  font-size: 40px;
  line-height: 250px;
  padding-left: 160px;
 }</style>