<template>
  <ion-page>
   <ion-content>
    <p>This will go to tabs</p>
    <ion-button @click="() => router.replace('/tabs/')">Start</ion-button>
   </ion-content>
  </ion-page>
</template>

<script>
import { IonButton, IonPage, IonContent } from '@ionic/vue';
import { useRouter } from 'vue-router';
import { defineComponent } from 'vue';

export default defineComponent({
 name: "login",
 components: {
  IonButton,
  IonPage,
  IonContent
 },
 setup() {
   const router = useRouter();

  return {
   router: useRouter()
  }
 }
})
</script>

<style>

</style>