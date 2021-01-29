<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 2</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Page métiers</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-list>


        <ion-item lines="full"
                  button
                  v-for="metier in metiers"
                  :key="metier.id"
        >
          <ion-icon slot="start"
                    color="dark"
                    name="wifi"
          ></ion-icon>
          <ion-label>{{ metier.nom }}</ion-label>
        </ion-item>
      </ion-list>
    </ion-content>
  </ion-page>
</template>

<script>
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
/* Importation des données JSON */
import metiersJson from '@/data/metiers.json';

export default  {
  name: 'PageMetiers',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage },
  data() {
    return {
      metiers: metiersJson
    }
  }
}
</script>
