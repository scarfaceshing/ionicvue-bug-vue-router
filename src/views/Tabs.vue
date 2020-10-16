<template>
  <ion-page>
    <ion-tabs>
      <ion-tab-bar slot="bottom">
        <ion-tab-button tab="tab1" href="/tabs/tab1">
          <ion-icon :icon="triangle" />
          <ion-label>Tab 1</ion-label>
        </ion-tab-button>
          
        <ion-tab-button tab="tab2" href="/tabs/tab2">
          <ion-icon :icon="ellipse" />
          <ion-label>Tab 2</ion-label>
        </ion-tab-button>
        
        <ion-tab-button tab="tab3" href="/tabs/tab3">
          <ion-icon :icon="square" />
          <ion-label>Tab 3</ion-label>
        </ion-tab-button>

      </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script lang="ts">
import { IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonPage } from '@ionic/vue';
import { ellipse, square, triangle } from 'ionicons/icons';
import { defineComponent } from 'vue';

const title = "Tab3";

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
  name: 'Tabs',
  components: { IonLabel, IonTabs, IonTabBar, IonTabButton, IonIcon, IonPage },
  methods: debugCall,
  setup() {
    return {
      ellipse, 
      square, 
      triangle,
    }
  }
})
</script>