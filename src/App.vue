<template>
  <q-layout>
  <div class="q-pa-md">

      <q-header elevated style="position: fixed; width: 100%; z-index: 1000;" class="header">
        <q-toolbar>
          <q-btn flat round dense icon="menu" class="q-mr-sm" />
          <q-avatar>
            <img src="https://media.discordapp.net/attachments/1112397346773417994/1242389796815503390/rsz_1aeon_store_stellaron_hunter_1.png?ex=664da92a&is=664c57aa&hm=a57922308f27fab7ab4189cf1c2304212b2c291d44d22dd1cf5f87d7297f46c9&=&format=webp&quality=lossless&width=207&height=365">
          </q-avatar>

          <q-toolbar-title>AEONS STORE x K2HOWU</q-toolbar-title>

          <q-btn flat round dense icon="whatshot" />
        </q-toolbar>

        <q-tabs v-model="tab">
          <q-tab name="images" label="HOME" />
          <q-tab name="videos" label="PROMO" />
          <q-tab name="articles" label="HISTORY" />
        </q-tabs>
      </q-header>
      


      <q-page-container>
        <q-page class="q-pa-md">
          <!--awal dari carousel-->
          <div class="q-pa-md">
            <div class="q-gutter-md">
            <q-carousel class="banner"
              animated
              v-model="slide"
              arrows
              navigation
              infinite
              >
              <q-carousel-slide name="style" class="column no-wrap flex-center">
                <q-img 
                  src="https://media.discordapp.net/attachments/1106545264774365274/1242348025507090492/Untitled_image_4.jpeg?ex=664d8242&is=664c30c2&hm=62ca705d90ed13e9c1bdb6fbe2815c71ceaec4c0adc6096a8dac85321872a496&=&format=webp&width=1176&height=662" 
                  class="banner"
                />
                <div class="q-mt-md text-center">
                  {{ lorem }}
                </div>
              </q-carousel-slide>
              <q-carousel-slide name="tv" class="column no-wrap flex-center">
                <q-img class="banner"
                  src="https://media.discordapp.net/attachments/1106545264774365274/1242377208119427152/image.png?ex=664d9d70&is=664c4bf0&hm=faebf73928c6de1518421ea60305d511f02f8f4e86272701569c0afd02ba7a27&=&format=webp&quality=lossless&width=687&height=233" 
                />
                <div class="q-mt-md text-center">
                  {{ lorem }}
                </div>
              </q-carousel-slide>
              <q-carousel-slide name="layers" class="column no-wrap flex-center">
                <q-img class="banner"
                  src="https://media.discordapp.net/attachments/1112397346773417994/1242378923216732271/image.png?ex=664d9f09&is=664c4d89&hm=06af2cddf628e7b1cb6d1bd10965d7475cc30f55c27d1b6fa41fefe7d46fb0f1&=&format=webp&quality=lossless&width=1357&height=661" 
                />
                <div class="q-mt-md text-center">
                  {{ lorem }}
                </div>
              </q-carousel-slide>
            </q-carousel>

          </div>
          <!--akhir dari carousel-->

          <!--awal dari card-->
          <div class="q-pa-md row items-start q-gutter-md">

            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">Mobile Legends</div>
                <div class="image-container">
                  <q-img class="image" src="https://play-lh.googleusercontent.com/B2aIz3JtIQ57hLCFo-mw9iymuFEe7A2wUvJYAjr1cuV28T2bzkWmAH0EU4JCw3T8hg"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>
            
            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">Free Fire</div>
                <div class="image-container">
                  <q-img class="image" src="https://i.pinimg.com/564x/bd/dc/ef/bddcef95802b5204fa2165729ab39971.jpg"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>

            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">Valorant</div>
                <div class="image-container">
                  <q-img class="image" src="https://seeklogo.com/images/V/valorant-logo-FAB2CA0E55-seeklogo.com.png"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>

            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">Apex Legend</div>
                <div class="image-container">
                  <q-img class="image" src="data:image/jpeg;base64,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"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>

            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">PUBG Mobile</div>
                <div class="image-container">
                  <q-img class="image" src="https://i.pinimg.com/564x/63/48/2f/63482fb173cb7b7cc6e2673960e9eb29.jpg"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>

            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">Solo Leveling</div>
                <div class="image-container">
                  <q-img class="image" src="https://cdn.mmoculture.com/mmo-images/2023/03/Solo-Leveling-ARISE.png"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>

            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">Genshin Impact</div>
                <div class="image-container">
                  <q-img class="image" src="https://upload-os-bbs.hoyolab.com/upload/2022/08/17/241468695/0f75d7bd2c7b9eba8063b5e2d618211d_4169469279575604257.jpg?x-oss-process=image%2Fresize%2Cs_1000%2Fauto-orient%2C0%2Finterlace%2C1%2Fformat%2Cwebp%2Fquality%2Cq_80"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>

            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">Honkai Star Rail</div>
                <div class="image-container">
                  <q-img class="image" src="https://upload-os-bbs.hoyolab.com/upload/2023/12/13/179113813/4bea3220f991a7e80e0a6d478cca7bd3_7981229778134100053.png?x-oss-process=image%2Fresize%2Cs_1000%2Fauto-orient%2C0%2Finterlace%2C1%2Fformat%2Cwebp%2Fquality%2Cq_80"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>

            <q-card class="store2">
              <q-card-section>
                <div class="text-h6">Roblox</div>
                <div class="image-container">
                  <q-img class="image" src="https://play-lh.googleusercontent.com/WNWZaxi9RdJKe2GQM3vqXIAkk69mnIl4Cc8EyZcir2SKlVOxeUv9tZGfNTmNaLC717Ht=w240-h480-rw"/>   
                </div>
              </q-card-section>

              <q-card-section>
                {{ lorem }}
              </q-card-section>

              <q-separator dark />

              <q-card-actions class="centered">
                <q-btn flat>TOP UP</q-btn>
                <q-btn flat>JOKI</q-btn>
              </q-card-actions>
            </q-card>
            
          </div>
          </div>
          <!--akhir dari card-->
        </q-page>
      </q-page-container>
 
  </div>
  <q-footer reveal elevated>
        <q-toolbar class="footer">
          <q-toolbar-title>Naufal Rizqullah | 223510805</q-toolbar-title>
        </q-toolbar>
      </q-footer>

</q-layout>
  <q-footer elevated>
    <q-toolbar class="glossy">
      <q-toolbar-title>Footer</q-toolbar-title>
    </q-toolbar>
  </q-footer>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      tab: ref("images"),
      time: ref("10:56"),
      timeWithSeconds: ref("09:24:10"),
      slide: ref("style"),
      lorem: "",
    };
  },
};
</script>

<style>
.header {
  background-image: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);
}

.store1 {
  width: 200px;
  height: 250px;
  background-image: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);
  border-radius: 16px;
  box-shadow: 0px 10px 15px -3px rgba(0, 0, 0, 0.1);
  transition: all 0.5s ease-in-out;
  display: flex;
  justify-content: center; 
  align-items: center;
}

.store1:hover {
  transform: scale(1.1);
}

.store2 {
  width: 200px;
  height: 250px;
  background-image: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);
  border-radius: 16px;
  box-shadow: 0px 10px 15px -3px rgba(0, 0, 0, 0.1);
  transition: all 0.5s ease-in-out;
  
}

.store2:hover {
  transform: scale(1.1);
}

.store0 {
  width: 200px;
  height: 250px;
  background-image: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);
  border-radius: 16px;
  box-shadow: 0px 10px 15px -3px rgba(0, 0, 0, 0.1);
  transition: all 0.5s ease-in-out;
}

.store0:hover {
  transform: scale(1.1);
}

.image-container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 50px;
  height: 100px; 
  width: 100%; 
}

.image {
  width: 120px;
  height: 120px;
  border-radius: 15px;
}

.centered {
  display: flex;
  flex-direction: column;
  align-self: center;
  justify-content: space-between;
  height: 0%;
}


.banner {
  border-radius: 16px;
  content: center;
  align-self: center;
}

.footer {
  background-image: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);
  text-align: center;
}
</style>
