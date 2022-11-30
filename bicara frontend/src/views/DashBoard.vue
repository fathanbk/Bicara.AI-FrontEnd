<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Bicara.ai</ion-title>
        <ion-button slot="end">
          <span class="material-symbols-outlined" style="margin-right: 10px"> video_call </span>
          Upload Video
        </ion-button>
        <ion-button slot="end">
          <span class="material-symbols-outlined"> search </span>
        </ion-button>
        <ion-avatar slot="end" style="width: 38px; height: 38px; margin-left: 10px">
          <a href="">
          <img alt="Silhouette of a person's head" src="https://ionicframework.com/docs/img/demos/avatar.svg" style="border-radius:50%;"/>
          </a>
        </ion-avatar>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <div class="dashboard">
        <div class="aside"></div>
        <div class="aside" style="position: fixed">
          <h1>Hi, Jake!</h1>
          <h4>What would you like to do today?</h4>
          <a href="#">
            <span class="material-symbols-outlined">home</span>
            <p style="margin: 3px 0 0 5px; padding: 0">Home</p>
          </a>
          <a href="#">
            <span class="material-symbols-outlined"> video_library </span>
            <p style="margin: 3px 0 0 5px; padding: 0">Library</p>
          </a>
          <a href="#">
            <span class="material-symbols-outlined"> summarize </span>
            <p style="margin: 3px 0 0 5px; padding: 0">Report</p>
          </a>
          <a href="#">
            <span class="material-symbols-outlined"> group </span>
            <p style="margin: 3px 0 0 5px; padding: 0">Contact Support</p>
          </a>
          <a href="#">
            <span class="material-symbols-outlined"> settings </span>
            <p style="margin: 3px 0 0 5px; padding: 0">Settings</p>
          </a>
          <a href="#">
            <span class="material-symbols-outlined"> help_center </span>
            <p style="margin: 3px 0 0 5px; padding: 0">Help</p>
          </a>
          <a href="#">
            <span class="material-symbols-outlined"> logout </span>
            <p style="margin: 3px 0 0 5px; padding: 0">Sign Out</p>
          </a>
        </div>
        <div class="content" style="">
          <h1>Rating Result</h1>
          <ion-grid>
            <ion-row class="ion-justify-content-end">
              <ion-col size="4">
                <div class="card">
                  <p>Uploaded 11 November 2022</p>
                </div>
              </ion-col>
            </ion-row>
            <!-- score, filler, pacing -->
            <ion-row>
              <ion-col size="6">
                <div class="card">
                  <p style="margin-top: 2px; margin-right: 10px; font-size: 24px">Score</p>
                  <p>
                    <span class="material-symbols-rounded"> star </span>
                    <span class="material-symbols-rounded"> star </span>
                    <span class="material-symbols-rounded"> star </span>
                    <span class="material-symbols-rounded"> star </span>
                    <span class="material-symbols-rounded"> star </span>
                  </p>
                </div>
              </ion-col>
              <ion-col size="3">
                <ion-card>
                  <ion-row class="ion-justify-content-between">
                    <ion-col size="7">
                      <ion-card-content>Filler Word</ion-card-content>
                    </ion-col>
                    <ion-col size="4">
                      <ion-card-content>40%</ion-card-content>
                    </ion-col>
                  </ion-row>
                </ion-card>
              </ion-col>
              <ion-col size="3">
                <ion-card>
                  <ion-row class="ion-justify-content-between">
                    <ion-col size="5">
                      <ion-card-content>Pacing</ion-card-content>
                    </ion-col>
                    <ion-col size="4">
                      <ion-card-content>250</ion-card-content>
                    </ion-col>
                  </ion-row>
                </ion-card>
              </ion-col>
            </ion-row>
            <!-- detail -->
            <ion-row>
              <ion-col>
                <ion-card>
                  <ion-row>
                    <ion-col class="detailborder">
                      <div class="detail">
                        <p><span class="dot inton"></span></p>
                        <p>Intonation</p>
                      </div>
                      <p class="val">75%</p>
                      <div class="progessline">
                        <div class="progessvalue IntonLine"></div>
                      </div>
                    </ion-col>
                    <ion-col class="detailborder">
                      <div class="detail">
                        <p><span class="dot pronun"></span></p>
                        <p>Pronunciation</p>
                      </div>
                      <p class="val">65.7%</p>
                      <div class="progessline">
                        <div class="progessvalue PronunLine"></div>
                      </div>
                    </ion-col>
                    <ion-col class="detailborder">
                      <div class="detail">
                        <p><span class="dot grammar"></span></p>
                        <p>Grammar</p>
                      </div>
                      <p class="val">80%</p>
                      <div class="progessline">
                        <div class="progessvalue GrammarLine"></div>
                      </div>
                    </ion-col>
                    <ion-col class="">
                      <div class="detail">
                        <p><span class="dot eyecontact"></span></p>
                        <p>Eye Contact</p>
                      </div>
                      <p class="val">50%</p>
                      <div class="progessline">
                        <div class="progessvalue EyeconLine"></div>
                      </div>
                    </ion-col>
                  </ion-row>
                </ion-card>
              </ion-col>
            </ion-row>
          </ion-grid>
          <h1>Progress Report</h1>
          <ion-grid>
            <ion-row class="ion-justify-content-end">
              <ion-col size="4">
                <div class="card progressreport" style="padding-bottom: 0px; display: flex; justify-content: space-between">
                  <p>
                    <span class="material-symbols-outlined" style="margin: 0px 10px 0px 0px"> chevron_left </span>
                  </p>
                  <p style="margin-top: 3px">November 2022</p>
                  <p>
                    <span class="material-symbols-outlined" style="margin: 0px 0px 0px 10px"> chevron_right </span>
                  </p>
                </div>
              </ion-col>
            </ion-row>
            <ion-row>
              <ion-col>
                <div class="chart">
                  <div class="grafik">
                    <div class="starline">
                      <p>5 star</p>
                    </div>
                    <div class="starline">
                      <p>4 star</p>
                    </div>
                    <div class="starline">
                      <p>3 star</p>
                    </div>
                    <div class="starline">
                      <p>2 star</p>
                    </div>
                    <div class="starline s1">
                      <p>1 star</p>
                    </div>
                  </div>
                  <div class="grafiky">
                    <div class="fillline" style="margin-top: 30%">
                      <p>12/11</p>
                    </div>
                    <div class="fillline" style="margin-top: 20%">
                      <p>13/11</p>
                    </div>
                    <div class="fillline" style="margin-top: 10%">
                      <p>16/11</p>
                    </div>
                    <div class="fillline" style="margin-top: 20%">
                      <p>17/11</p>
                    </div>
                    <div class="fillline" style="margin-top: 0%">
                      <p>19/11</p>
                    </div>
                    <div class="fillline" style="margin-top: 10%">
                      <p>21/11</p>
                    </div>
                  </div>
                </div>
              </ion-col>
              <ion-col size="4">
                <ion-row>
                  <ion-card class="progress-count">
                    <ion-card-content class="progress-title">Filler Word Count</ion-card-content>
                    <ion-grid>
                      <ion-row class="progress-table progress-title2 ion-justify-content-between">
                        <ion-col size="5">Date</ion-col>
                        <ion-col size="5">%Count</ion-col>
                      </ion-row>
                      <ion-row class="progress-table ion-justify-content-between">
                        <ion-col size="5">11:11 / 12 Nov</ion-col>
                        <ion-col size="5">'uh', 'hm' - 40%</ion-col>
                      </ion-row>
                      <ion-row class="progress-table ion-justify-content-between">
                        <ion-col size="5">11:11 / 12 Nov</ion-col>
                        <ion-col size="5">'uh', 'hm' - 40%</ion-col>
                      </ion-row>
                      <ion-row class="progress-table ion-justify-content-between">
                        <ion-col size="5">11:11 / 12 Nov</ion-col>
                        <ion-col size="5">'uh', 'hm' - 40%</ion-col>
                      </ion-row>
                    </ion-grid>
                  </ion-card>
                </ion-row>
                <ion-row>
                  <ion-card class="progress-count pacing-count">
                    <ion-card-content class="progress-title">Pacing Count</ion-card-content>
                    <ion-grid>
                      <ion-row class="progress-table progress-title2 ion-justify-content-between">
                        <ion-col size="5">Date</ion-col>
                        <ion-col size="6">Pacing (word/min)</ion-col>
                      </ion-row>
                      <ion-row class="progress-table ion-justify-content-between">
                        <ion-col size="5">11:11 / 12 Nov</ion-col>
                        <ion-col size="6">205</ion-col>
                      </ion-row>
                      <ion-row class="progress-table ion-justify-content-between">
                        <ion-col size="5">11:11 / 12 Nov</ion-col>
                        <ion-col size="6">205</ion-col>
                      </ion-row>
                      <ion-row class="progress-table ion-justify-content-between">
                        <ion-col size="5">11:11 / 12 Nov</ion-col>
                        <ion-col size="6">205</ion-col>
                      </ion-row>
                    </ion-grid>
                  </ion-card>
                </ion-row>
              </ion-col>
            </ion-row>
          </ion-grid>
          <h1>Sample Speech</h1>
          <div class="samplespeech">
            <ion-card>
              <img alt="Silhouette of mountains" src="https://d2v9ipibika81v.cloudfront.net/uploads/sites/72/BDS-0690.jpg" />
              <ion-card-content> Ambassador Kim's Remarks on Women in Fintech </ion-card-content>
            </ion-card>
            <ion-card>
              <img alt="Silhouette of mountains" src="https://d2v9ipibika81v.cloudfront.net/uploads/sites/72/BDS-0690.jpg" />
              <ion-card-content> Ambassador Kim's Remarks on Women in Fintech </ion-card-content>
            </ion-card>
            <ion-card>
              <img alt="Silhouette of mountains" src="https://d2v9ipibika81v.cloudfront.net/uploads/sites/72/BDS-0690.jpg" />
              <ion-card-content> Ambassador Kim's Remarks on Women in Fintech </ion-card-content>
            </ion-card>
          </div>
          <ion-footer class="ion-no-border">
            <ion-toolbar>
              <ion-title>© 2022 Bicara.ai | Policy</ion-title>
            </ion-toolbar>
          </ion-footer>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonButton, IonContent, IonPage, IonHeader, IonTitle, IonToolbar } from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "DashBoard",
  components: {
    IonButton,
    IonContent,
    IonPage,
    IonHeader,
    IonTitle,
    IonToolbar,
  },
});
</script>

<style scoped>
@media (max-width: 480px) {
}

#container {
  text-align: center;

  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;

  color: #8c8c8c;

  margin: 0;
}

#container a {
  text-decoration: none;
}

.ion-content {
  background-color: rgb(122, 104, 104);
}

ion-page {
  --ion-background-color: #ffffff;
}

ion-header ion-toolbar ion-title {
  font-family: "Krona One", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 30px;
  line-height: 45px;
  display: flex;
  align-items: center;
  letter-spacing: 0.03em;
}

ion-header ion-toolbar {
  --background: var(--ion-color-template1);
  --padding-start: 10px;
  --padding-end: 20px;
  --padding-top: 15px;
  --padding-bottom: 15px;
  --color: white;
}

ion-header ion-toolbar ion-button {
  --background: #ffffff;
  --background-hover: var(--ion-color-template1);
  --background-activated: #dcdcdc;
  --background-focused: #dddddd;
  --color: rgb(0, 0, 0);
  --border-radius: 10px;
  /*
  --border-color: #000;
  --border-style: solid;
  --border-width: 1px; 
  */
  --box-shadow: 0 2px 6px 0 rgb(0, 0, 0, 0.25);
  --ripple-color: var(--ion-color-template2);
  --padding-top: 0px;
  --padding-bottom: 0px;
  font-family: "Segoe UI", Arial, sans-serif;
  margin-right: 10px;
  text-transform: capitalize;
  font-style: normal;
  font-weight: 600;
  line-height: 24px;
  letter-spacing: -1px;
  font-size: 18px;
}

ion-button i {
  width: 10px;
  margin-right: 15px;
}

.dashboard {
  display: grid;
  grid-template-columns: 320px auto;
}

.aside {
  background-color: rgb(255, 255, 255);
  border-right: 1px solid #8c8c8c;
  padding-left: 25px;
  padding-right: 25px;
  width: 310px;
  height: 870px;
}

.aside ion-button {
  --background: #ffffff;
  --background-hover: var(--ion-color-template1);
  --background-activated: #dcdcdc;
  --background-focused: #dddddd;
  --color: rgb(0, 0, 0);
  --border-radius: 20px;
  --box-shadow: 0;
  --ripple-color: var(--ion-color-template2);
  text-transform: capitalize;
  font-family: "Segoe UI", Arial, sans-serif;
  letter-spacing: 0px;
  width: 230px;
}

.aside h4 {
  position: relative;
}

.aside ion-button span {
  margin-right: 10px;
}

.aside a:nth-child(3) {
  outline: 0;
  appearance: none;
  text-decoration: none;
  list-style: none;
  display: flex;
  color: rgb(255, 255, 255);
  position: relative;
  width: 220px;
  border-radius: 20px;
  padding-left: 15px;
  padding-top: 8px;
  padding-bottom: 8px;
  background-color: var(--ion-color-template1);
  font-size: 18px;
  gap: 8px;
  margin-top: 20px;
  font-weight: 600;
  font-family: "Segoe UI", Arial, sans-serif;
}
.aside a {
  outline: 0;
  appearance: none;
  text-decoration: none;
  list-style: none;
  display: flex;
  color: rgb(0, 0, 0);
  position: relative;
  width: 220px;
  border-radius: 20px;
  padding-left: 15px;
  padding-top: 8px;
  padding-bottom: 8px;
  font-size: 18px;
  gap: 8px;
  margin-top: 6px;
  font-weight: 510;
  font-family: "Segoe UI", Arial, sans-serif;
  transition: background-color 0.6s;
}

.aside a:last-child {
  position: absolute;
  bottom: 40px;
}

.aside a span {
  margin-top: 4px;
}

.aside a:hover {
  background-color: rgb(226, 232, 238);
  color: black;
}

.content {
  /* padding-left: 50px;
  padding-right: 50px; */
  width: 1000px;
  margin: 0 auto;
  padding-top: 10px;
}

.content h1 {
  font-size: 30px;
  margin-left: 8px;
}

.card {
  font-family: "Segoe UI";
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  background-color: #e4eaeffe;
  color: black;
  border-radius: 10px;
  text-align: center;
  margin: 0;
  display: flex;
  justify-content: center;
}

.card p {
  padding-top: 5px;
  padding-bottom: 5px;
  margin: 0;
}

.card p span:first-child {
  color: #3f54d1;
}
.card p span:nth-child(2) {
  color: #3f54d1;
}
.card p span {
  color: #a8b9be;
  font-size: 37px !important;
  margin-left: 20px;
}

/* .isicontent */

ion-card {
  --background: #e4eaeffe;
  --color: black;
  border-radius: 10px;
  box-shadow: none;
  margin: 0;
}

ion-card-content {
  font-family: "Segoe UI";
  font-style: normal;
  font-weight: 600;
  font-size: 21px;
  line-height: 27px;
}

ion-card ion-row ion-col,
ion-card ion-row {
  margin: 0;
  padding: 0;
}

ion-card ion-row ion-col ion-card-content {
  text-align: center;
}

ion-col p {
  font-family: "Segoe UI";
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  text-align: center;
}

/* Detail Intonasi */
.dot {
  height: 20px;
  width: 20px;
  border-radius: 50%;
  display: inline-block;
  margin-top: 10px;
  margin-right: 13px;
}

.detail {
  display: flex;
  justify-content: left;
  margin-left: 33px;
}
.detail p {
  margin: 15px 0 3px;
  font-size: 24px;
}

.val {
  margin: 3px 0 8px;
  font-size: 24px;
}

.detailborder {
  border-right: 1px solid rgb(191, 187, 187);
}

.progessline {
  margin: 20px auto;
  width: 180px;
  height: 16px;
  background-color: #ababab;
  border-radius: 10px;
}
.progessvalue {
  height: 16px;
  border-radius: 10px;
}

.IntonLine {
  width: 75%;
  background-color: #3f54d1;
}

.inton {
  background-color: #3f54d1;
}
.PronunLine {
  width: 65.7%;
  background-color: #5280e2;
}

.pronun {
  background-color: #5280e2;
}

.GrammarLine {
  width: 80%;
  background-color: #15cdcb;
}
.grammar {
  background-color: #15cdcb;
}

.EyeconLine {
  width: 50%;
  background-color: #4fe0b5;
}
.eyecontact {
  background-color: #4fe0b5;
}

.chart {
  font-family: "Segoe UI";
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  background-color: #e4eaeffe;
  color: black;
  border-radius: 10px;
  text-align: center;
  margin: 0;
  display: flex;
  justify-content: center;
  width: 100%;
  height: 400px;
  position: relative;
}

.grafik {
  margin: auto;
  margin-left: 50px;
  z-index: 0;
}
.starline {
  border-top: 2px solid rgb(182, 182, 182);
  width: 500px;
  height: 50px;
}

.s1 {
  border-bottom: 2px solid rgb(182, 182, 182);
}
.starline p {
  right: 5px;
  margin: 0px;
  margin-right: -580px;
  margin-top: -18px;
}

.grafiky {
  position: absolute;
  margin: 77px auto;
  /* margin-left: 50px; */
  width: 500px;
  height: 250px;
  z-index: 100;
  display: flex;
  gap: 68px;
}

.fillline {
  width: 17px;
  border-radius: 10px;
  bottom: 5;
}

.fillline:nth-child(odd) {
  background-color: #3f54d1;
}
.fillline:nth-child(even) {
  background-color: #4fe0b5;
}

.fillline p {
  position: absolute;
  bottom: -58px;
  margin-left: -13px;
}

/* ion-list {
  --background: #e4eaeffe;
  --color: black;
  border-radius: 10px;
  box-shadow: none;
  margin: 0;
  padding: 0;
  border: none;
}

ion-list ion-item {
  --background: #e4eaeffe;
  --color: black;
  height: 30px;
}

ion-list ion-item ion-label {
  --background: #e4eaeffe;
  --color: black;
  margin: 3px 0px;
  padding: 0px;
} 
*/

.progress-count {
  --background: #e4eaeffe;
  --color: black;
  padding: 10px 15px;
  width: 100%;
  height: 195px;
}

.progress-table {
  border-bottom: 0.5px solid grey;
  padding-top: 4px;
  font-family: "Segoe UI", Arial, sans-serif;
  font-size: 15px;
  font-weight: 500;
}

.progress-title {
  text-align: center;
  font-family: "Segoe UI", Arial, sans-serif;
}

.progress-title2 {
  color: #ababab;
}

.pacing-count {
  margin-top: 10px;
}

.samplespeech{
  margin: 30px auto;
  display: flex;
}

.samplespeech ion-card{
  width: 360px;
  height: 310px;
  margin: auto 10px;
}

ion-footer ion-toolbar{
  --background: white;
  margin: 20px;
}
ion-footer ion-toolbar ion-title{
  font-size: 15px;
  text-align: center;
}

.samplespeech ion-card ion-card-content{
  text-align: center;
}
</style>
