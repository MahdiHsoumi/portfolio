<template>
  <q-page class="home ">
    <div class="row justify-center align-center">
      <transition-group
        class="column justify-center items-center q-pa-sm"
        appear
        enter-active-class="animated backInRight"
      >
        <div key="container3D" class="container3D">
          <span style="--i:1;"></span>
          <span style="--i:2;"></span>
          <span style="--i:3;"></span>
          <span style="--i:4;"></span>
          <span style="--i:5;"></span>
          <span style="--i:6;"></span>
        </div>
        <h2
          key="title"
          class="title"
          data-text="Hello, my name is Mahdi HSOUMI."
        >
          Hello, my name is Mahdi HSOUMI.
        </h2>
        <p
          key="subtitle"
          class="subtitle"
          data-text=" I'm a full-stack Javascript developer."
        >
          I'm a full-stack Javascript developer.
        </p>
        <a
          key="button"
          href="https://drive.google.com/uc?export=download&id=12NqVbok3GgnUYNmB-QMTAQbELc4Mtqpq"
          download="Mahdi's Resume.pdf"
          style="text-decoration:none"
        >
          <q-btn
            class="glass text-primary"
            size="lg"
            :icon-right="ionDownloadOutline"
            label="my resume"
          />
        </a>
      </transition-group>
    </div>
  </q-page>
</template>

<script>
import { ionDownloadOutline } from "@quasar/extras/ionicons-v5";
export default {
  name: "home",
  data() {
    return { ionDownloadOutline };
  },

  methods: {}
};
</script>
<style scoped>
.container3D {
  position: relative;
  width: 150px;
  height: 150px;
  display: flex;
  justify-content: center;
  align-items: center;
  transform-style: preserve-3d;
  transform: perspective(500px) rotateX(135deg);
  margin-bottom: 50px;
  z-index: 1;
}
.container3D span {
  position: absolute;
  display: block;
  border: 15px solid white;
  border-radius: 50%;
  animation: animate 6s ease-in-out infinite;
  box-shadow: 0 10px 0 #efebeb, inset 0 10px 0 #ececec;
  animation-delay: calc(-1s * var(--i));
}
@keyframes animate {
  0% {
    transform: translateZ(-100px);
    width: 100%;
    height: 100%;
  }
  25% {
    transform: translateZ(100px);
    width: 100%;
    height: 100%;
  }
  50% {
    transform: translateZ(100px);
    width: 15%;
    height: 15%;
  }
  75% {
    transform: translateZ(-100px);
    width: 15%;
    height: 15%;
  }
  100% {
    transform: translateZ(-100px);
    width: 100%;
    height: 100%;
  }
}

.home {
  display: flex;
  justify-content: center;
  align-items: center;
  /* background-image: url("../assets/bg.gif"); */
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}
.title,
.subtitle {
  position: relative;

  color: white;
}
.title {
  font-size: 32px;
  text-align: center;
  text-transform: uppercase;
  -webkit-text-stroke: 2px #000000;
}

.subtitle {
  font-size: 20px;
  text-align: center;
  -webkit-text-stroke: 1px #000000;
}

@media screen and (min-width: 480px) {
  .title {
    font-size: 50px;
    -webkit-text-stroke: 3px #000000;
  }
  .subtitle {
    font-size: 32px;
    -webkit-text-stroke: 2px #000000;
  }
}
.title::before,
.subtitle::before {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  color: #00ddef;
  -webkit-text-stroke: 0vw #000000;

  overflow: hidden;
}
</style>
