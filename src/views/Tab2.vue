<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Photo Gallery App</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
       <ion-fab vertical="bottom" horizontal="center" slot="fixed">
    <ion-fab-button @click="takePhoto()">
      <ion-icon :icon="camera"></ion-icon>
    </ion-fab-button>
  </ion-fab>
      
      
     
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { camera, trash, close } from 'ionicons/icons';
import { IonPage, IonHeader, IonFab, IonFabButton, IonIcon, 
         IonToolbar, IonTitle, IonContent,  } from '@ionic/vue';
import { usePhotoGallery} from '@/composables/usePhotoGallery';


export default  {
  name: 'Tab2',
  components: { IonPage, IonHeader, IonFab, IonFabButton, IonIcon, 
         IonToolbar, IonTitle, IonContent,  },
  setup() {
     const { takePhoto } = usePhotoGallery();

    return {
      camera, trash, close,takePhoto
    }
  }
}
</script>