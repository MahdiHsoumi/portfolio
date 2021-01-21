<template>
  <q-page class="contact-container q-pa-sm">
    <div class="card-contact">
      <div class="face front">
        <h3 class="name">Mahdi Hsoumi</h3>
        <p class="description text-subtitle1 q-mt-xl">
          Currently looking for a good place to work where I can work and have
          fun at the same time, I would choose a low salary rather than a bad
          working environment.
        </p>
      </div>
      <div class="face back">
        <h3 class="name">Contact Information</h3>
        <p class="description text-subtitle1 q-mt-xl">
          <q-icon class="q-mr-sm" :name="ionCallOutline" />+90 05394982764
        </p>
        <p class="description text-subtitle1 q-mt-xl">
          <q-icon class="q-mr-sm" :name="ionMailOutline" />
          mahdihsoumi@gmail.com
        </p>
        <p class="description text-subtitle1 q-mt-xl">
          <q-icon class="q-mr-sm" :name="ionHomeOutline" />
          Istanbul, Turkey
        </p>
      </div>
    </div>
  </q-page>
</template>
<script>
import {
  ionCallOutline,
  ionMailOutline,
  ionHomeOutline
} from "@quasar/extras/ionicons-v5";
export default {
  data() {
    return {
      ionCallOutline,
      ionMailOutline,
      ionHomeOutline
    };
  },

  name: "contact"
};
</script>
<style>
.contact-container {
  display: flex;
  justify-content: center;
  align-items: center;
}
.card-contact {
  position: relative;
  width: 600px;
  height: 400px;
  transform-style: preserve-3d;
  perspective: 500px;
}
.card-contact .face {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
  border-radius: 15px;
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  transform-style: preserve-3d;
  transition: 1s;
  padding: 30px;
}
.card-contact .face.front::before {
  content: "";
  position: absolute;
  bottom: 40px;
  right: 40px;
  width: 60px;
  height: 60px;
  background: #fff;
  border-radius: 50%;
  opacity: 0.5;
}
.description,
.name {
  color: #fff;
}
.card-contact:hover .face.front {
  transform: rotateY(180deg);
}
.card-contact .face.back {
  transform: rotateY(180deg);
}
.card-contact:hover .face.back {
  transform: rotateY(360deg);
  z-index: 2;
}
</style>
