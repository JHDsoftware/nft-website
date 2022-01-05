<template>
  <div class="backgroundPic">
    <div class="backgroungPicture">
      <v-app-bar app dark>
        <v-container class="d-flex" style="width: 100%">
          <div>Crpto Naughty Mammal</div>
          <v-spacer></v-spacer>
          <div>
            <v-btn
                href="#home"
                text
            >
              <div style="color: white">Home</div>
            </v-btn>
            <v-btn
                href="#story"
                text
            >
              <div style="color: white">Story</div>
            </v-btn>
            <v-btn
                href="#community"
                text
            >
              <div style="color: white">Community</div>
            </v-btn>
            <v-btn
                href="#roadmap"
                text
            >
              <div style="color: white">Roadmap</div>
            </v-btn>
            <v-btn
                href="#team"
                text
            >
              <div style="color: white">Team</div>
            </v-btn>
          </div>
        </v-container>

      </v-app-bar>
      <v-main>
        <v-container>
          <v-row class="mt-16">
            <v-col class="pa-4" cols="6" id="home">
              <div class="d-flex align-center justify-center flex-wrap" style="height: 100%">
                <div>
                  <h1 style="color: white">The <span style="color: purple">Project</span> You Have <br>Been Waiting
                    For...
                  </h1>
                  <p style="color: white">6888 of CryptoNaughtyMammals are coming to the town of NFT and we are here to stay!</p>

                  <v-btn color="#FF00FF" style="margin-top: 30px"><span style="color: white">Connect Wallet</span>
                  </v-btn>
                </div>
              </div>
            </v-col>
            <v-col class="pa-4" cols="6">
              <div class=" d-flex justify-center">
                <v-img :src="require('../assets/1.png')"></v-img>
              </div>
            </v-col>
          </v-row>
          <v-row class="mt-16">
            <v-col class="pa-4" cols="6">
              <div class=" d-flex justify-center">
                <v-img :src="require('../../public/891.png')"></v-img>
              </div>
            </v-col>
            <v-col id="story" class="pa-4" cols="6">
              <div class="d-flex align-center justify-center flex-wrap" style="height: 100%">
                <div>
                  <h1 style="color: white">Story</h1>
                  <p style="color: white">We don't want to take it over or fly to the moon (We don't have wings or rockets). It feels good just to be a neighborhood-friendly CrptoNaughtyMammal.
                  </p>
                </div>
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col class="pa-4" cols="8" offset="2" id="community">
              <div class="third mt-16">
                <div class="thirdTitle d-flex justify-space-between"><h1 style="color: white">Community</h1>
                  <div>
                    <v-btn color="purple" icon outlined @click="model--">
                      <v-icon>mdi-arrow-left</v-icon>
                    </v-btn>
                    <v-btn class="ml-2" color="purple" icon outlined @click="model++">
                      <v-icon>mdi-arrow-right</v-icon>
                    </v-btn>
                  </div>
                </div>
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12">
              <div class="banner">
                <div class="bannerPic">
                  <v-sheet
                      class="mx-auto"
                      color="#100428"
                      elevation="8"
                      max-width="1200"
                  >
                    <v-slide-group
                        v-model="model"
                        center-active
                        class="pa-4"
                    >
                      <v-slide-item
                          v-for="(item,i) in items"
                          :key="i"
                          v-slot="{ active, toggle }"
                          :src="item.src"
                      >
                        <v-card
                            :color="active ? 'primary' : 'primary'"
                            class="ma-4"
                            height="250"
                            style="position: relative"
                            width="250"
                            @click="toggle"
                        >
                          <v-img
                              :src="item.src"
                              class="white--text align-end"
                              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                              height="250px"
                          >
                          </v-img>
                          <v-card class="d-flex justify-space-between align-center"
                                  dark
                                  style="width: 100%;position: absolute;bottom: 0;height: 36px;background: rgba(0,0,0,0.76)">
                            <div>Name</div>
                            <div>
                              <v-icon class="mr-2" small color="red">mdi-heart</v-icon>
                              37
                            </div>
                          </v-card>
                        </v-card>
                      </v-slide-item>
                    </v-slide-group>
                  </v-sheet>
                </div>
              </div>
            </v-col>
          </v-row>
          <v-row id="roadmap">
            <v-col cols="12">
              <div class="text-center">
                <h1 style="color: white">Roadmap</h1>
              </div>
            </v-col>
          </v-row>
          <v-row class="mt-16">
            <v-col cols="4" offset="1">
              <v-card class="d-flex justify-center" style="background-color: #80cd93;border-radius: 20px">
                <v-img :src="require('../assets/854.png')" class="flex-grow-0" width="250px"></v-img>
              </v-card>
            </v-col>
            <v-col class="pa-4" cols="6" offset="1">
              <div class="d-flex align-center justify-center flex-wrap" style="height: 100%">
                <div >
                  <v-card color="#100428"
                          style="padding-top: 15px;padding-bottom: 15px;border-radius: 20px;width: 50%;height: 100%;border-style:solid;border-color:purple;  ">
                    <h3 style="color: white;text-align: center">Round1</h3>
                    <ul>
                      <li style="color: #a74ae1;padding-left: 10px">
                        <div style="color: white;">
                          early-bird sale [2021/12/25 - 2021/12/31]
                        </div>
                      </li>
                    </ul>
                  </v-card>
                </div>
              </div>
            </v-col>
          </v-row>
          <v-row no-gutters>
            <v-col cols="6" offset="3">
              <div style="border-left-style: dotted;border-bottom-style: dotted;border-width: 2px;border-color: white;height: 20px">
              </div>
            </v-col>
          </v-row>
          <v-row no-gutters>
            <v-col cols="6" offset="3">
              <div style="border-right-style: dotted;border-width: 2px;border-color: white;height: 20px">
              </div>
            </v-col>
          </v-row>
          <v-row no-gutters>
            <v-col class="pa-4" cols="6" offset="1">
              <div class="d-flex align-center justify-center flex-wrap" style="height: 100%">
                <div>
                  <v-card color="#100428"
                          style="padding-top: 15px;padding-bottom: 15px;border-radius: 20px;width: 50%;height: 100%;border-style:solid;border-color:purple;">
                    <h3 style="color: white;text-align: center">Round2</h3>
                    <ul>
                      <li style="color: #a74ae1;padding-left: 10px">
                        <div style="color: white">
                          community sale [2022/01/01 - 2022/01/15]
                        </div>
                      </li>
                    </ul>
                  </v-card>
                </div>
              </div>
            </v-col>
            <v-col cols="4">
              <v-card class=" d-flex justify-center" style="background-color: #53739a;border-radius: 20px">
                <v-img :src="require('../assets/855.png')" class="flex-grow-0" width="250px"></v-img>
              </v-card>
            </v-col>
          </v-row>
          <v-row no-gutters>
            <v-col cols="6" offset="3">
              <div style="border-right-style: dotted;border-bottom-style: dotted;border-width: 2px;border-color: white;height: 20px">
              </div>
            </v-col>
          </v-row>
          <v-row no-gutters>
            <v-col cols="6" offset="3">
              <div style="border-left-style: dotted;border-width: 2px;border-color: white;height: 20px">
              </div>
            </v-col>
          </v-row>
          <v-row no-gutters>
            <v-col cols="4" offset="1">
              <v-card class=" d-flex justify-center" style="background-color: #918787;border-radius: 20px">
                <v-img :src="require('../assets/857.png')" class="flex-grow-0" width="250px"></v-img>
              </v-card>
            </v-col>
            <v-col class="pa-4" cols="6" offset="1">
              <div class="d-flex align-center justify-center flex-wrap" style="height: 100%">
                <div>
                  <v-card color="#100428"
                          style="padding-top: 15px;padding-bottom: 15px;border-radius: 20px;width: 50%;height: 100%;border-style:solid;border-color:purple;">
                    <h3 style="color: white;text-align: center">Open sale</h3>
                    <ul>
                      <li style="color: #a74ae1;padding-left: 10px">
                        <div style="color: white">
                          Open sale
                          [2022/01/16 to 2077/12/30]
                        </div>
                      </li>
                    </ul>
                  </v-card>
                </div>
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12" id="team">
              <div class="text-center">
                <h1 style="color: white">Our Team</h1>
              </div>
            </v-col>
          </v-row>
          <v-row class="mt-16">
            <v-col
                v-for="card in cards"
                :key="card.title"
                :cols="card.flex"
                class="d-flex justify-center"
            >
              <v-card max-width="360px" style="background-color: #a74ae1;border-radius: 20px">
                <v-card class="ml-2 mr-2 mt-2 mb-2" style="border-radius: 10px">
                  <v-img
                      :src="card.src"
                      class="white--text align-end"
                      gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                      height="250px"
                  >
                  </v-img>
                </v-card>
                <div class="pa-2">
                  <div style="text-align: center;width: 100%;font-size: 28px;color: white"> {{ card.title }}</div>
                  <div style="text-align: center;width: 100%;font-size: 20px;color: white"> {{ card.subtitle }}</div>
                </div>
                <div>
                  <v-card-actions class="justify-center flex-wrap">
                    <div>
                      <v-btn icon>
                        <v-icon color="white">mdi-facebook</v-icon>
                      </v-btn>
                      <v-btn icon>
                        <v-icon color="white">mdi-twitter</v-icon>
                      </v-btn>
                      <v-btn icon>
                        <v-icon color="white">mdi-linkedin</v-icon>
                      </v-btn>
                    </div>
                  </v-card-actions>
                </div>
              </v-card>
            </v-col>
          </v-row>
          <v-row class="mt-16">
            <v-col cols="8" offset="2">
              <v-card color="#100428" style="border-radius: 20px">
                <div style="border-style:solid;border-color:purple;">
                  <br>
                  <h2 style="text-align: center;color: white">Community giveaway</h2>
                  <br>
                  <p style="text-align: center;color: white" >
                    A sign of appreciations to the creator and publisher:
                    150pcs reserved for CNM`s mom, the creator of the graphics: Giopine
                    150pcs reserved for CNM's dad, the mysterious coder: is4yNo-
                    688 whitelist spots for our lovely CNM community! Stay tuned to our discord, Twitter, Facebook, and website for more details</p>
                  <div class="d-flex  justify-center mt-12" style="width: 100%">
                    <div>
                      <v-text-field dark label="Enter Your Email Address" outlined
                                    style="width: 100%;"
                      ></v-text-field>
                    </div>
                    <div>
                      <v-btn height="55px" style="background-color: purple; color: white">Join Our Discord</v-btn>
                    </div>
                  </div>
                </div>
              </v-card>
            </v-col>
          </v-row>
          <v-row class="mt-16">
            <v-col cols="12">
              <v-footer style="background-color: purple;color: white;text-align: center">
                <div style="width: 100%">Copyright © {{ new Date().getFullYear() }} All Right Reserved</div>
              </v-footer>
            </v-col>
          </v-row>
          <v-row>
            <div>

            </div>
          </v-row>
        </v-container>
      </v-main>
    </div>
  </div>

</template>

<script>
export default {
  data() {
    return {
      selection: 1,
      model: null,
      items: [
        {
          src: "/858.png",
        },
        {
          src: "/859.png",
        },
        {
          src: "/860.png",
        },
        {
          src: "/861.png",
        },
        {
          src: "/862.png",
        },
        {
          src: "/891.png",
        },
        {
          src: "/892.png",
        },
        {
          src: "/893.png",
        },
        {
          src: "/894.png",
        },
        {
          src: "/895.png",
        },
        {
          src: "/896.png",
        },
        {
          src: "/897.png",
        },
        {
          src: "/898.png",
        },
        {
          src: "/899.png",
        },

      ],
      cards: [
        {title: 'Oscar', subtitle: 'The Owner', src: "/864.png", flex: 4},
        {title: 'Jane Williams', subtitle: 'The Designer', src: '/865.png', flex: 4},
        {title: 'Jefferson Coles', subtitle: 'The Artist', src: '/863.png', flex: 4},
      ],
    }
  },
  watch: {
    model: function (val) {
      console.log(val)
    }
  },
  methods: {}
}
</script>

<style>
.backgroundPic {
  background-color: #100428;
}


.thirdTitle {
  width: 100%;
  text-align: center;
}

.bannerPic {
  width: 100%;
  height: 350px;
}

/*.backgroungPicture{*/
/*  background: url("../assets/backPic.png");*/
/*}*/
/*::-webkit-scrollbar {*/
/*  !*隐藏滚轮*!*/
/*  display: none;*/
/*}*/
</style>
