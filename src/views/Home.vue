<template>
  <div>
    <v-app-bar app>
      <v-container>
        <div class="titlePara">Crpto Naughty Mammal</div>
        <div class="button">
          <v-btn
              text
          >
            <div style="color: white">Home</div>
          </v-btn>
          <v-btn
              text
              href="#story"
          >
            <div style="color: white">Story</div>
          </v-btn>
          <v-btn
              text
          >
            <div style="color: white">Specs</div>
          </v-btn>
          <v-btn
              text
          >
            <div style="color: white">Community</div>
          </v-btn>
          <v-btn
              text
          >
            <div style="color: white">Roadmap</div>
          </v-btn>
          <v-btn
              text
          >
            <div style="color: white">Team</div>
          </v-btn>
        </div>
      </v-container>
    </v-app-bar>
    <v-main>
      <v-container>

        <v-row>
          <v-col cols="6"></v-col>
          <v-col cols="6"></v-col>
        </v-row>
        <v-row>
          <div class="backgroundPic">
            <div class="first">
              <div class="firstPara">
                <h1 style="color: white">The <span style="color: purple">Project</span> You Have <br>Been Waiting For...</h1>
                <p style="color: white">Lorem Ipsum is simply dummy text of the printing and
                  <br>typesetting industry Lorem Ipsum has been the industry's
                  <br>standard dummy text ever since the 1500s.</p>
                <v-btn color="#FF00FF" style="margin-top: 30px"><span style="color: white">Connect Wallet</span></v-btn>
              </div>
              <div class="firstPic">
                <v-img :src="require('../assets/1.png')" width="350px"></v-img>
              </div>
            </div>
            <div class="second">
              <div class="secondPic">
                <v-img :src="require('../../public/891.png')" width="350px"></v-img>
              </div>
              <div id="story" class="secondPara">
                <h1 style="color: white">Story</h1>
                <p style="color: white">Proin gravida nibh vel velit auctor aliquet.Aenean sollicitudin, lorem
                  <br>quis bibendum auctor, nisi elit consequat ipsum, nec sagittis sem
                  <br>nibh id elit. Duis sed odio sit amet nibh vulputate cursus a sit amet
                  <br>mauris. Morbi accumsan ipsum velit. Nam nec tellus a odio tincidunt
                  <br>auctor a ornare odio. Sed non mauris vitae erat consequat auctor eu
                  <br>in elit. Class aptent taciti sociosqu ad litora torquent per conubia
                  <br>nostra, per inceptos himenaeos. Mauris in eratjusto. Nullam ac urna
                  <br>eu felis dapibus condimentum sit amet a augue.
                </p>
              </div>
            </div>
            <div class="third">
              <div class="thirdTitle"><h1 style="color: white">Community</h1></div>
              <div class="banner">
                <div class="bannerPic">
                  <v-sheet
                      class="mx-auto"
                      elevation="8"
                      max-width="1200"
                      color="#100428"
                  >
                    <v-slide-group
                        v-model="model"
                        class="pa-4"
                        center-active
                        show-arrows
                    >
                      <template v-slot:prev="{ on, attrs }">
                        <v-icon
                            style="color: white"
                            v-bind="attrs"
                            v-on="on"
                        >mdi-chevron-left</v-icon>
                      </template>
                      <template v-slot:next="{ on, attrs }">
                        <v-icon
                            style="color: white"
                            v-bind="attrs"
                            v-on="on"
                        >mdi-chevron-right</v-icon>
                      </template>
                      <v-slide-item
                          v-for="(item,i) in items"
                          :src="item.src"
                          :key="i"
                          v-slot="{ active, toggle }"
                      >
                        <v-card
                            :color="active ? 'primary' : 'grey lighten-1'"
                            class="ma-4"
                            height="250"
                            width="250"
                            @click="toggle"
                            style="margin-left: 50px"
                        >
                          <v-img
                              :src="item.src"
                              class="white--text align-end"
                              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                              height="250px"
                          >
                          </v-img>
                        </v-card>
                      </v-slide-item>
                    </v-slide-group>
                  </v-sheet>
                </div>
              </div>
            </div>
            <div class="fourth">
              <div class="fourthTitle"><h1 style="color: white">Roadmap</h1></div>
              <div class="fourthOne">
                <div class="fourthPic">
                  <v-img :src="require('../assets/854.png')" width="250px"></v-img>
                </div>
                <div class="fourthPara">
                  <v-card width="400px" height="150px" color="#660066" rounded style="border-radius: 25px; padding-top: 15px">
                    <h3 style="color: white;text-align: center">Will Come a Next Season</h3>
                    <br>
                    <p style="color: white">&emsp;Proin gravida nibh vel velit auctor aliquet. Aenean
                      <br>&emsp;sollicitudin, lorem quis bibendum auctor, nisi elit
                      <br>&emsp;consequat ipsum, nec sagittis sem nibh id elit.
                    </p>
                  </v-card>
                </div>
              </div>
            </div>
            <div class="fifth">
              <div class="fifthPara">
                <v-card width="400px" height="150px" color="#660066" rounded style="border-radius: 25px;padding-top: 15px">
                  <h3 style="color: white;text-align: center">Will Come a Next Season</h3>
                  <br>
                  <p style="color: white">&emsp;Proin gravida nibh vel velit auctor aliquet. Aenean
                    <br>&emsp;sollicitudin, lorem quis bibendum auctor, nisi elit
                    <br>&emsp;consequat ipsum, nec sagittis sem nibh id elit.
                  </p>
                </v-card>
              </div>
              <div class="fifPic">
                <v-img :src="require('../assets/856.png')" width="250px"></v-img>
              </div>
            </div>
            <div class="sixth">
              <div class="sixthPic">
                <v-img :src="require('../assets/857.png')" width="250px"></v-img>
              </div>
              <div class="sixthPara">
                <v-card width="400px" height="150px" color="#660066" rounded style="border-radius: 25px;padding-top: 15px">
                  <h3 style="color: white;text-align: center">Will Come a Next Season</h3>
                  <br>
                  <p style="color: white">&emsp;Proin gravida nibh vel velit auctor aliquet. Aenean
                    <br>&emsp;sollicitudin, lorem quis bibendum auctor, nisi elit
                    <br>&emsp;consequat ipsum, nec sagittis sem nibh id elit.
                  </p>
                </v-card>
              </div>
            </div>
            <div class="seventh">
              <div class="seventhTitle"><h1 style="color: white">Our Team</h1></div>
              <div class="seventhCard">
                <v-container fluid>
                  <v-row>
                    <v-col
                        v-for="card in cards"
                        :key="card.title"
                        :cols="card.flex"
                    >
                      <v-card width="250px">
                        <v-img
                            :src="card.src"
                            class="white--text align-end"
                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                            height="250px"
                        >
                        </v-img>
                        <div>
                          <v-card-title>
                            <div style="text-align: center;width: 100%;font-size: 28px"> {{card.title}} </div>
                          </v-card-title>
                        </div>
                        <div>
                          <v-card-subtitle>
                            <div style="text-align: center;width: 100%;font-size: 20px"> {{card.subtitle}} </div>
                          </v-card-subtitle>
                        </div>
                        <v-card-actions>
                          <v-spacer></v-spacer>
                          <v-btn icon>
                            <v-icon>mdi-facebook</v-icon>
                          </v-btn>
                          <v-btn icon>
                            <v-icon>mdi-twitter</v-icon>
                          </v-btn>
                          <v-btn icon>
                            <v-icon>mdi-linkedin</v-icon>
                          </v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-col>
                  </v-row>
                </v-container>
              </div>
            </div>
            <div class="eighth">
              <v-card color="#100428" light width="800px" height="250px">
                <br><h2 style="text-align: center;color: white">Are You A Crpto Naughty Mammal. Collector?</h2>
                <br><p style="text-align: center;color: white">Aenean sollicitudin, lorem quis bibendum auctor, nisi elit consequatipsum, nec sagittis sem nibh id elit. Duis sed odio sit amet nibh vulputate cursus asit amet mauris</p><br><br>
                <div class="eighthGroup">
                  <div class="eighthText">
                    <v-text-field label="Enter Your Email Address" color="" dark outlined style="width: 500px;margin-left: 60px"></v-text-field>
                  </div>
                  <div>
                    <v-btn style="background-color: purple; color: white" height="55px">Join Our Discord</v-btn>
                  </div>
                </div>
              </v-card>
            </div>
            <div class="footer">
              <v-footer style="background-color: purple">
                <v-col
                    style="text-align: center; color: white"
                    cols="12"
                >
                  Copyright © {{ new Date().getFullYear() }} All Right Reserved
                </v-col>
              </v-footer>
            </div>
          </div>
        </v-row>
      </v-container>
    </v-main>

  </div>

</template>

<script>
  export default {
    data(){
      return{
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
          { title: 'Oscar',subtitle: 'The Owner', src: "/864.png", flex: 3 },
          { title: 'Jane Williams', subtitle: 'The Designer', src: '/865.png', flex: 3 },
          { title: 'Jefferson Coles', subtitle:  'The Artist', src: '/863.png', flex: 3 },
        ],
      }
    },
    methods:{
    }
  }
</script>

<style>
.backgroundPic{
  background: url("../assets/background.png");
  width: 100%;
  height: 100%;
}
.Title{
  display: flex;
  width: 100%;
  align-items: center;
}
.titlePara{
  width: 30%;
  text-align: center;
  color: #ffffff;
}
.button{
  width: 70%;
  text-align: center;
}
.first {
  display: flex;
  width: 100%;
  align-items: center;
}
.firstPara {
  margin-left: 20%;
  width: 40%;
  align-items: center;
}
.firstPic {
  margin-top: 125px;
  align-items: center;
}
.second{
  display: flex;
}
.secondPic{
  margin-top: 150px;
  margin-left: 20%;
  width: 40%;
  align-items: center;
}
.secondPara{
  margin-top: 200px;
  width: 60%;
}
.third{
}
.thirdTitle{
  width: 100%;
  margin-top: 200px;
  text-align: center;
}
.bannerPic{
  margin-top: 100px;
  width: 1200px;
  height: 350px;
  margin-left: 20%;
}
.fourth{
}
.fourthTitle{
  text-align: center;
  margin-top: 200px;
}
.fourthOne{
  display: flex;
}
.fourthPic{
  margin-top: 150px;
  margin-left: 30%;
  width: 40%;
  align-items: center;
}
.fourthPara{
  margin-top: 200px;
  width: 60%;
}
.fifth{
  display: flex;
}
.fifthPara{
  margin-top: 200px;
  margin-left: 22%;
  width: 47%;
  align-items: center;
}
.fifPic{
  margin-top: 150px;
  width: 53%;
}
.sixth{
  display: flex;
}
.sixthPic{
  margin-top: 150px;
  margin-left: 30%;
  width: 40%;
  align-items: center;
}
.sixthPara{
  margin-top: 200px;
  width: 60%;
}
.seventhTitle{
  text-align: center;
  margin-top: 200px;
}
.seventhCard{
  margin-top: 100px;
  margin-left: 23%;
}
.eighth{
  margin-bottom: 50px;
  margin-top: 200px;
  margin-left: 30%;
}
.eighthGroup{
  display: flex;
}
/*::-webkit-scrollbar {*/
/*  !*隐藏滚轮*!*/
/*  display: none;*/
/*}*/
</style>
