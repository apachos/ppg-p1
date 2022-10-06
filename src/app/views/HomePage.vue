<template>
  <ion-page>
    <img class="canvas__photo" src="assets/india-gate.svg" />
    <div class="canvas__overlay"></div>

    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title slot="start">Travel</ion-title>
        <ion-buttons slot="end">
          <ion-button fill="clear">Home</ion-button>
          <ion-button fill="clear">About</ion-button>
          <ion-button fill="clear">Contact</ion-button>
          <div class="hamburger"></div>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>

    <!-- TODO Vue component for home header -->
    <!-- TODO Vue component for exploring -->
  </ion-page>
</template>

<script lang="ts">
import { IonButton, IonButtons, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomePage',
  components: { IonButton, IonButtons, IonHeader, IonPage, IonTitle, IonToolbar }
});
</script>

<style scoped>
.ion-page {
  height: 900px;
  margin: auto;
}

.canvas__photo {
  object-fit: cover;
  box-shadow: 0 4px 14px 4px rgba(0, 0, 0, 0.25);
  width: 100%;
  height: 100%;
  border-radius: 24px;
}

.canvas__overlay {
  position: absolute;
  top: 0;
  right: 0;

  width: 50%;
  height: 100%;
  border-radius: 0 24px 24px 0;

  background: rgba(0, 0, 0, 0.5);
}

ion-header {
  position: absolute;
  top: 55px;

  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 75px;
  padding-left: 33px;
  padding-right: 58px;
}

ion-toolbar {
  --background: transparent;
}

ion-title {
  font-family: 'Quicksand', sans-serif;
  font-size: 60px;
  font-weight: bold;
  letter-spacing: 0;
}

ion-buttons {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 534px;
  max-width: 534px;
  padding: 0 0 0 40px;
}

ion-button {
  margin-left: 0;
  margin-right: 0;

  color: white;

  font-family: 'Mulish', sans-serif;
  font-size: 24px;
  font-weight: bold;
  text-transform: capitalize;
  letter-spacing: 0;
}

ion-button:hover {
  transform: scale(1.1);

  color: aqua;
}

ion-button::part(native) {
  padding-left: 0;
  padding-right: 0;
}

ion-button::part(native):hover {
  text-shadow: 3px 3px 3px rgba(0, 0, 0, 0.5);
}

ion-button.button-clear {
  --background-hover-opacity: 0;
}

.hamburger {
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  align-items: flex-end;
  gap: 10px;
  min-width: 50px;
  height: 50px;

  cursor: pointer;
}

.hamburger::before,
.hamburger::after {
  height: 5px;
  border-radius: 10px;

  background-color: white;

  content: '';
}

.hamburger::before {
  width: 50px;
}

.hamburger::after {
  width: 35px;
}

.hamburger:hover::before,
.hamburger:hover::after {
  box-shadow: 3px 3px 3px 0 rgba(0, 0, 0, 0.5);
  transform: scale(1.1);

  background-color: aqua;
}
</style>
