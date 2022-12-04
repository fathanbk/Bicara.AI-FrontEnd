<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content :fullscreen="true">
      
        <ion-header collapse="condense">
          <ion-toolbar>
            <ion-title size="large">Tab 1</ion-title>
          </ion-toolbar>
        </ion-header>
        <v-form v-slot="{values, errors}" @submit="onSubmit">
        <ion-item>
          <ion-label >Email </ion-label>
          <v-field name="email" v-slot="{field}" :rules="isRequired" >
            <ion-input v-bind="field" name="email" ></ion-input>
          </v-field>
        </ion-item>
        <v-error-message name="email" class="error" />
        <ion-item>
          <ion-label >First Name</ion-label>
          <v-field name="Firstname" v-slot="{field}" :rules="isRequired">
            <ion-input v-bind="field" name="Firstname" ></ion-input>
          </v-field>
        </ion-item>
        <v-error-message name="Firstname" class="error" />
  
        <ion-item>
          <ion-label >Last Name</ion-label>
          <v-field name="Lastname" v-slot="{field}" :rules="isRequired">
            <ion-input v-bind="field" name="Lastname" ></ion-input>
          </v-field>
        </ion-item>
        <v-error-message name="Lastname" class="error" />
        
        <p>
          <ion-button type="submit">Save</ion-button>
        </p>
        <pre>
          {{ values }}
          {{ errors }}
        </pre>
      </v-form>
      
      </ion-content>
  
    </ion-page>
  </template>
  
  <script lang="ts">
  import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonInput,IonButton,IonLabel,IonItem } from '@ionic/vue';
  import { defineComponent } from "vue";
  import * as V from "vee-validate/dist/vee-validate";
  import { defineRule } from "vee-validate/dist/vee-validate";
  import { email } from "@vee-validate/rules"
  
  
  
  export default  defineComponent({
    name: 'Tab1Page',
    components: {  IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonInput,IonButton,IonLabel, IonItem
    , VField: V.Field,
      VForm: V.Form, 
      VErrorMessage: V.ErrorMessage,},
    setup() {
      const onSubmit = (data:any) => {
  
        
        return alert("ON SUBMIT" + JSON.stringify(data, null, 2));
    
      };
     
      defineRule("email", email)  
  
      const isRequired = (value: any) => {
        if (!value) {
          return "This field is required";
        }
        return true;
      };
      
  
  
  
      return {
        onSubmit,
        isRequired,
        email
      };
    }
   
  
    });
  </script>
  <style scoped>
  .error{
    color: red;
    font-style: italic;
  }
  </style>
  
  