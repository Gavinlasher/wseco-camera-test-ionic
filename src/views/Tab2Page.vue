<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Vue Camera App</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
     <ion-fab vertical="bottom" horizontal="center" slot="fixed" >   
<ion-fab-button @click="takePhoto()">
<ion-icon :icon="camera"> 

</ion-icon>
</ion-fab-button>
     </ion-fab>
      
     
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {camera,trash, close} from "ionicons/icons"
import { defineComponent } from 'vue';
import {
  IonPage,
  IonHeader,
  IonFab,
  IonFabButton,
  IonIcon,
  IonToolbar,
  IonTitle,
  IonContent,
  IonGrid,
  IonRow,
  IonCol,
  IonImg,
} from '@ionic/vue';
import { setupConfig } from "@ionic/core";
import  {usePhotoGallery} from "@/composables/usePhotoGallery"


export default {
  name: 'Tab2Page',
components: {
    IonPage,
    IonHeader,
    IonFab,
    IonFabButton,
    IonIcon,
    IonToolbar,
    IonTitle,
    IonContent,
    IonGrid,
    IonRow,
    IonCol,
    IonImg,
  },

setup(){
  const {takePhoto} = usePhotoGallery();
  return{
camera, trash,close, takePhoto
  }
}


}


</script>
