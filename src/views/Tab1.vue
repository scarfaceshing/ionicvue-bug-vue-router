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
     <ion-button @click="() => router.replace('/login')">Logout</ion-button>
      <ExploreContainer name="Tab 1 page" />
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonButton } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
import { useRouter } from 'vue-router';
import { defineComponent } from 'vue';

const title = "Tab1";

const debugCall: any = {
    ionViewDidEnter: () => {
      console.log(`${title} ionViewDidEnter`)
    },
    ionViewDidLeave: () => {
      console.log(`${title} ionViewDidLeave`)
    },
    ionViewWillEnter: () => {
      console.log(`${title} ionViewWillEnter`)
    },
    ionViewWillLeave: () => {
       console.log(`${title} ionViewWillLeave`)
    }
}

export default defineComponent({
  name: 'Tab1',
  components: { ExploreContainer, IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonButton },
  methods: debugCall,
  setup() {
   const router = useRouter();

   return {
    router
   }
  }
})
</script>