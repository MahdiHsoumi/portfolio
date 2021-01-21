<template>
  <q-page class="work">
    <div @click="egsyDialog = true" class="card-work glass">
      <div
        class="content arrow animate__animated animate__wobble  animate__slower"
      >
        <p class="project-name">EGSY</p>
      </div>
    </div>
    <q-dialog v-model="egsyDialog">
      <q-card class="glass" style="width:600px">
        <q-card-section>
          <a target="_blank" href="https://egsy.ai/">
            <div class="text-h6 text-uppercase text-primary">EGSY</div>
          </a>
        </q-card-section>

        <q-carousel
          v-model="egsyCarousel"
          swipeable
          animated
          thumbnails
          :fullscreen.sync="fullscreen"
          transition-prev="slide-right"
          transition-next="slide-left"
          infinite
        >
          <q-carousel-slide
            name="home"
            img-src="../assets/egsy/egsyHome.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Home Page
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="canvas"
            img-src="../assets/egsy/egsyCanvas.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="q-pa-md glass text-center text-primary"
            >
              Create your AI assistant with ease by creating and linking
              different nodes over the scenario. Drag and drop responses and
              actions to compose the best conversational experience
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="projects"
            img-src="../assets/egsy/egsyProjects.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Easly Create, Organise and Share your Stories and Skill between
              multiple projects, no need to duplicate the same story, just use
              the existent one from another project.
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="chat"
            img-src="../assets/egsy/egsyChat.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Integrate your assistant or chatbot with the Most Popular
              messaging platforms such as Facebook, Slack, Telegram, Twilio,
              Rocketchat, etc..., even with your Website.
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="telegram"
            img-src="../assets/egsy/egsyTelegram.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Telegram
            </div>
          </q-carousel-slide>

          <q-carousel-slide
            name="tech"
            img-src="../assets/egsy/egsyMyCode.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Main Techs: VueJS (Vuetify), NodeJs (Fastify), MongoDB
            </div>
          </q-carousel-slide>
          <template v-slot:control>
            <q-carousel-control position="top-right" :offset="[18, 18]">
              <q-btn
                push
                round
                dense
                color="white"
                text-color="secondary"
                :icon="fullscreen ? ionContractOutline : ionExpandOutline"
                @click="fullscreen = !fullscreen"
              />
            </q-carousel-control>
          </template>
        </q-carousel>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
    <div @click="theradiaDialog = true" class="card-work glass">
      <div
        class="content arrow animate__animated animate__wobble  animate__slower"
      >
        <p class="project-name">theradia</p>
      </div>
    </div>
    <q-dialog v-model="theradiaDialog">
      <q-card class="glass" style="width:600px">
        <q-card-section>
          <div class="text-h6 text-uppercase text-primary">Theradia</div>
        </q-card-section>

        <q-carousel
          v-model="theradiaCarousel"
          swipeable
          animated
          thumbnails
          :fullscreen.sync="fullscreen"
          transition-prev="slide-right"
          transition-next="slide-left"
          infinite
        >
          <q-carousel-slide
            name="home"
            img-src="../assets/theradia/theradiaHome.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="q-pa-md glass text-center text-primary"
            >
              Create your AI assistant with ease by creating and linking
              different nodes over the scenario. Drag and drop responses and
              actions to compose the best conversational experience
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="projects"
            img-src="../assets/theradia/theradiaProject.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="q-pa-md glass text-center text-primary"
            >
              Create projects import/export, Integrate your assistant or chatbot
              with the Most Popular messaging platforms such as Facebook, Slack,
              Telegram, even with your Website.
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="history"
            img-src="../assets/theradia/theradiaHistory.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="q-pa-md glass text-center text-primary"
            >
              Project Chat History/Errors and Test
            </div>
          </q-carousel-slide>

          <template v-slot:control>
            <q-carousel-control position="top-right" :offset="[18, 18]">
              <q-btn
                push
                round
                dense
                color="white"
                text-color="secondary"
                :icon="fullscreen ? ionContractOutline : ionExpandOutline"
                @click="fullscreen = !fullscreen"
              />
            </q-carousel-control>
          </template>
        </q-carousel>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
    <div @click="comeTripDialog = true" class="card-work glass">
      <div
        class="content arrow animate__animated animate__wobble  animate__slower"
      >
        <p class="project-name">ComeTrip</p>
      </div>
    </div>
    <q-dialog v-model="comeTripDialog">
      <q-card class="glass" style="width:600px">
        <q-card-section>
          <a target="_blank" href="https://cometrip.sn/">
            <div class="text-h6 text-uppercase text-primary">ComeTrip</div>
          </a>
        </q-card-section>

        <q-carousel
          v-model="comeTripCarousel"
          swipeable
          animated
          thumbnails
          :fullscreen.sync="fullscreen"
          transition-prev="slide-right"
          transition-next="slide-left"
          infinite
        >
          <q-carousel-slide
            name="home"
            img-src="../assets/cometrip/cometripHome.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md text-subtitle1 text-center text-primary"
            >
              A responsive web platform (Alternative de Airbnb) which offers
              short-term property rental services in Senegal. The objective of
              the platform is to facilitate the accessibility and speed of
              short-term rentals in real estate.
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="property"
            img-src="../assets/cometrip/cometripProperties.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-subtitle1 text-primary"
            >
              Property
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="cars"
            img-src="../assets/cometrip/cometripCars.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-subtitle1 text-primary"
            >
              Cars
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="events"
            img-src="../assets/cometrip/cometripEvents.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-subtitle1 text-primary"
            >
              Events
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="book"
            img-src="../assets/cometrip/cometripBook.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-subtitle1 text-primary"
            >
              Book
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="auth"
            img-src="../assets/cometrip/cometripAuth.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-subtitle1 text-primary"
            >
              Auth
            </div>
          </q-carousel-slide>
          <template v-slot:control>
            <q-carousel-control position="top-right" :offset="[18, 18]">
              <q-btn
                push
                round
                dense
                color="white"
                text-color="secondary"
                :icon="fullscreen ? ionContractOutline : ionExpandOutline"
                @click="fullscreen = !fullscreen"
              />
            </q-carousel-control>
          </template>
        </q-carousel>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
    <div @click="kleaDialog = true" class="card-work glass">
      <div
        class="content arrow animate__animated animate__wobble  animate__slower"
      >
        <p class="project-name">klea market</p>
      </div>
    </div>
    <q-dialog v-model="kleaDialog">
      <q-card class="glass" style="width:600px">
        <q-card-section>
          <div class="text-h6 text-uppercase text-primary">Klea market</div>
        </q-card-section>

        <q-carousel
          v-model="kleaCarousel"
          swipeable
          animated
          thumbnails
          :fullscreen.sync="fullscreen"
          transition-prev="slide-right"
          transition-next="slide-left"
          infinite
        >
          <q-carousel-slide
            name="home"
            img-src="../assets/klea/kleaHome.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Home Page, klea is an e-commerce site
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="Products"
            img-src="../assets/klea/kleaProduct.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Search Products
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="Basket"
            img-src="../assets/klea/kleaBasket.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Basket
            </div>
          </q-carousel-slide>
          <q-carousel-slide
            name="Auth"
            img-src="../assets/klea/kleaAuth.png"
            class="column no-wrap flex-center"
          >
            <div
              style="width:100%"
              class="glass q-pa-md  text-center text-primary"
            >
              Auth
            </div>
          </q-carousel-slide>
          <template v-slot:control>
            <q-carousel-control position="top-right" :offset="[18, 18]">
              <q-btn
                push
                round
                dense
                color="white"
                text-color="secondary"
                :icon="fullscreen ? ionContractOutline : ionExpandOutline"
                @click="fullscreen = !fullscreen"
              />
            </q-carousel-control>
          </template>
        </q-carousel>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </q-page>
</template>

<script>
import VanillaTilt from "vanilla-tilt";
import {
  ionExpandOutline,
  ionContractOutline
} from "@quasar/extras/ionicons-v5";
export default {
  name: "work",
  data() {
    return {
      egsyDialog: false,
      egsyCarousel: "home",
      theradiaDialog: false,
      theradiaCarousel: "home",
      comeTripDialog: false,
      comeTripCarousel: "home",
      kleaDialog: false,
      kleaCarousel: "home",
      fullscreen: false,
      ionExpandOutline,
      ionContractOutline
    };
  },
  mounted() {
    VanillaTilt.init(document.querySelectorAll(".card-work"), {
      max: 35,
      speed: 400,
      glare: true,
      "max-glare": 1
    });
  }
};
</script>
<style>
.glass {
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
  background: rgba(0, 0, 0, 0.1);
  border-top: 1px solid rgba(255, 255, 255, 0.5);
  border-left: 1px solid rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(5px);
}

.work {
  position: relative;
  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  z-index: 1;
}

.card-work {
  position: relative;
  margin: 30px;
  width: 280px;
  height: 200px;
  border-radius: 15px;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 2;
  cursor: pointer;
}

.project-name {
  position: relative;
  color: white;
  text-transform: uppercase;
  text-align: center;
  font-size: 32px;
  -webkit-text-stroke: 2px #000000;
}

.project-name::before {
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
