<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <button slot="start" v-on:click="open_side()" id="menu">
          <span class="material-symbols-rounded menu"> menu </span>
        </button>
        <ion-title>Bicara.ai</ion-title>
        <ion-button id="open-modal-upload" slot="end">
          <span class="material-symbols-outlined"> video_call </span>
          <p class="upload-nav" style="margin-left: 10px">Upload Video</p>
        </ion-button>
        <ion-button slot="end">
          <span class="material-symbols-outlined"> search </span>
        </ion-button>
        <ion-avatar slot="end" style="width: 38px; height: 38px; margin-left: 10px">
          <img alt="Silhouette of a person's head" src="https://ionicframework.com/docs/img/demos/avatar.svg" />
        </ion-avatar>

        <ion-modal id="example-modal" ref="modal" trigger="open-modal-upload">
          <div class="wrapper" @dragover="dragover" @dragleave="dragleave" @drop="drop">
            <h1 style="color: black">Upload Your Video</h1>

            <input type="file" name="file" id="fileInput" class="hidden-input" v-on:change="onChange" ref="file" accept=".pdf,.jpg,.jpeg,.png" />

            <label class="uploaddrag file-label" for="fileInput">
              <ion-img class="uploadvid-img" src="assets/icon/uploadvid.svg"></ion-img>
              <p v-if="isDragging" class="textupload">Release to drop files here.</p>
              <p v-else class="textupload">Drag and drop file or <span style="cursor: pointer">browse local files</span></p>
              <p class="textupload2">max. file size 10MB</p>
            </label>

            <ion-button :disabled="true">Upload</ion-button>
          </div>
        </ion-modal>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <div class="dashboard">
        <!-- Sidebar History-->
        <div class="aside w3-animate-left" id="aside" style="position: fixed">
          <div class="firstsidebar">
            <div style="display: flex; justify-content: space-between; align-items: center">
              <h1 slot="start">Hi, Jake!</h1>
              <button slot="end" v-on:click="close_side()" id="close">
                <span class="material-symbols-rounded close"> close </span>
              </button>
            </div>
            <h4>What would you like to do today?</h4>
            <a href="/dashboard">
              <span class="material-symbols-outlined">home</span>
              <p>Home</p>
            </a>
            <a href="#">
              <span class="material-symbols-outlined"> video_library </span>
              <p>History</p>
            </a>
            <a href="#">
              <span class="material-symbols-outlined"> help_center </span>
              <p>FAQ</p>
            </a>
          </div>
          <div class="lastsidebar">
            <a href="#">
              <span class="material-symbols-outlined"> group </span>
              <p>Contact Support</p>
            </a>
            <a href="#">
              <span class="material-symbols-outlined"> logout </span>
              <p>Sign Out</p>
            </a>
          </div>
        </div>

        <!-- Content History -->
        <div class="content">
          <ion-card class="history-video">
            <ion-grid>
              <ion-row >
                <ion-col>
                  <h4>Video</h4>
                </ion-col>
                <ion-col>
                  <h4>Upload</h4>
                </ion-col>
                <ion-col>
                  <h4>Duration</h4>
                </ion-col>
                <ion-col>
                  <h4>Pacing (word/min)</h4>
                </ion-col>
                <ion-col>
                  <h4>Filler Word</h4>
                </ion-col>
              </ion-row>
              <ion-row class="table-history">
                <ion-col>
                  <a href=""></a>
                </ion-col>
                <ion-col>
                  <p class="tablecontent">11 Aug 2022</p>
                </ion-col>
                <ion-col>
                  <p class="tablecontent">11:11</p>
                </ion-col>
                <ion-col>
                  <p class="tablecontent">205</p>
                </ion-col>
                <ion-col>
                  <p class="tablecontent">4 Filler</p>
                </ion-col>
              </ion-row>

            </ion-grid>
          </ion-card>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonButton, IonContent, IonPage, IonHeader, IonTitle, IonToolbar, IonModal } from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "HistoryPage",
  components: {
    IonButton,
    IonContent,
    IonPage,
    IonHeader,
    IonTitle,
    IonToolbar,
    IonModal,
  },
  data() {
    return {
      isDragging: false,
      // files: [],
    };
  },
  methods: {
    close_side() {
      (document.getElementById("aside") as HTMLInputElement).style.display = "none";
      (document.getElementById("close") as HTMLInputElement).style.display = "none";
      (document.getElementById("menu") as HTMLInputElement).style.display = "inline-block";
    },
    open_side() {
      (document.getElementById("menu") as HTMLInputElement).style.display = "none";
      (document.getElementById("aside") as HTMLInputElement).style.display = "block";
      (document.getElementById("close") as HTMLInputElement).style.display = "inline-block";
    },
    // onChange() {
    //   console.log(this.$refs.file)
    // },
    dragover(event: { preventDefault: () => void; currentTarget: { classList: { contains: (arg0: string) => any; remove: (arg0: string) => void; add: (arg0: string) => void } } }) {
      event.preventDefault();
      this.isDragging = true;
    },
    dragleave() {
      this.isDragging = false;
    },
    drop(event: { preventDefault: () => void; dataTransfer: { files: any }; currentTarget: { classList: { add: (arg0: string) => void; remove: (arg0: string) => void } } }) {
      event.preventDefault();
      this.isDragging = false;
    },
  },
});
</script>

<style scoped>
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

ion-page {
  --ion-background-color: #ffffff;
}

/* CSS HEADER/NAVBAR */

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
  --background: #3e54d3;
  --padding-start: 10px;
  --padding-end: 20px;
  --padding-top: 15px;
  --padding-bottom: 15px;
  --color: white;
}

ion-header ion-toolbar ion-button,
.upload-vid {
  --background: #ffffff;
  --background-hover: #3e54d3;
  --background-activated: #dcdcdc;
  --background-focused: #dddddd;
  --color: rgb(0, 0, 0);
  --border-radius: 10px;
  --box-shadow: 0 2px 6px 0 rgb(0, 0, 0, 0.25);
  --ripple-color: #4f80e2;
  --padding-top: 0px;
  --padding-bottom: 0px;
  font-family: "Segoe UI", Arial, sans-serif;
  margin-right: 10px;
  text-transform: capitalize;
  font-style: normal;
  font-weight: 600;
  /* line-height: 24px; */
  letter-spacing: -1px;
  font-size: 18px;
}

ion-header ion-toolbar button .menu {
  font-size: 30px;
  margin-left: 15px;
}
ion-header ion-toolbar button .close {
  font-size: 30px;
  margin-left: 15px;
  display: none;
}

ion-button i {
  width: 10px;
  margin-right: 15px;
}

ion-modal#example-modal {
  --width: 680px;
  /* --min-width: 250px; */
  --height: 450px;
  --border-radius: 6px;
  --box-shadow: 0 28px 48px rgba(0, 0, 0, 0.4);
  padding-left: 20px;
  padding-right: 20px;
}

.file-label {
  /* font-size: 20px; */
  display: block;
}
.hidden-input {
  opacity: 0;
  overflow: hidden;
  position: absolute;
  width: 1px;
  height: 1px;
}

.wrapper {
  margin: 30px;
  /* height: 100%; */
}

.wrapper > h1 {
  margin: 18px 0px;
  font-size: 24px;
}

.uploaddrag {
  border: 7px dashed #15cdcb4f;
  width: 100%;
  height: 285px;
  padding-top: 30px;
}

.uploadvid-img {
  width: 140px;
  margin: 20px auto;
}

.uploaddrag > p {
  font-family: "Segoe UI", Arial, sans-serif;
  font-style: normal;
  font-weight: 600;
  color: rgba(0, 0, 0, 0.45);
  margin: 0px;
  text-align: center;
}

.textupload {
  font-size: 20px;
}
.textupload2 {
  font-size: 18px;
  margin-top: 5px !important;
}

.textupload > span {
  color: #3e54d3;
  text-decoration: underline;
}

.wrapper > ion-button {
  --background: #3e54d3;
  --border-radius: 8px;
  width: 100%;
  margin: 20px 0px;
  font-family: "Segoe UI", Arial, sans-serif;
  font-style: normal;
  font-weight: 600;
  text-transform: capitalize;
  font-size: 18px;
}

#menu {
  background-color: #3f54d1;
}

#close {
  background-color: #ffffff;
  color: black;
}

/* CSS SIDEBAR */

.dashboard {
  display: flex;
}

.intro-mobile,
.intro-mobile-2 {
  display: none;
}

.aside {
  background-color: rgb(255, 255, 255);
  border-right: 1px solid #8c8c8c;
  width: 300px;
  height: 100%;
  display: none;
  z-index: 200;
}

.w3-animate-left {
  position: relative;
  animation: animateleft 0.4s;
}
@keyframes animateleft {
  from {
    left: -200px;
    opacity: 0;
  }
  to {
    left: 0;
    opacity: 1;
  }
}

.aside ion-button {
  --background: #ffffff;
  --background-hover: #3e54d3;
  --background-activated: #dcdcdc;
  --background-focused: #dddddd;
  --color: rgb(0, 0, 0);
  --border-radius: 20px;
  --box-shadow: 0;
  --ripple-color: #4f80e2;
  text-transform: capitalize;
  font-family: "Segoe UI", Arial, sans-serif;
  letter-spacing: 0px;
  width: 230px;
}

.aside h4 {
  position: relative;
}
.aside h1 {
  margin: 9px 0;
}

.aside ion-button span {
  margin-right: 10px;
}

.aside a:nth-child(4) {
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
  background-color: #3f54d1;
  font-size: 18px;
  gap: 8px;
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

.aside .firstsidebar {
  margin: 0px 25px;
  margin-top: 20px;
}
.aside .lastsidebar {
  position: absolute;
  bottom: 80px;
  border-top: 1px solid #8c8c8c;
  padding: 10px 25px;
  width: 100%;
}

.aside a span {
  margin-top: 4px;
}

.aside a:hover {
  background-color: rgb(226, 232, 238);
  color: black;
}

.aside a:nth-child(4):hover {
  background-color: #3f54d1;
  color: #ffffff;
}

.aside a p {
  margin: 3px 0 0 5px;
  padding: 0;
}

/* CSS Content Dashboard */

.content {
  width: 1000px;
  margin: 0 auto;
  padding-top: 10px;
  transition: all 0.2 s;
}

.content h1 {
  font-size: 30px;
  margin-left: 8px;

}

ion-card {
  --background: #e4eaeffe;
  --color: black;
  border-radius: 10px;
  box-shadow: none;
  margin: 0;
  padding: 0 !important;
}

h4, .tablecontent{
  text-align: center;
  font-family: "Segoe UI", Arial, sans-serif;
}

.tablecontent{
  font-size: 18px;
  font-weight: 450;
}

ion-grid{
  padding: 0;
}
.table-history{
  border-top: 1px solid #8c8c8c;
  height: 120px;
}


@media (max-width: 576px) {
  .lastsidebar {
    bottom: 3px !important;
  }

  .dashboard {
    z-index: 0;
  }
  ion-header {
    display: none;
  }
  .detail-rating,
  ion-header ion-toolbar ion-button,
  ion-header ion-toolbar ion-avatar,
  #asidee {
    display: none;
  }

  .content {
    width: 97vw;
  }

  .content h1 {
    font-size: 25px;
  }

  .content .title-rat {
    margin-top: 0px;
    color: #ffffff;
  }
}
</style>
