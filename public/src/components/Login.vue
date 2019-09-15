<template>
    <v-layout>
      <v-flex
        xs7
        class="picture"
      >
        <v-flex
          class="absolute-cover-bg"
          d-flex
          justify-start
          align-center
        >
          <v-flex
            offset-xs2
            class="login-content"
          >
            <h1 class="login-title">Вход в платформу</h1>
            <hr>
            <h3>Терапевт - лучший учет клиентов для вашей клиники</h3>
          </v-flex>
        </v-flex>
      </v-flex>
      <v-flex
        xs5
        class="workplace"
        d-flex
      >
        <v-flex
          xs8
          offset-xs2
          d-flex
          flex-column
          align-space-around
          align-self-stretch
          class="container-workplace"
        >
          <v-flex
            d-flex
            align-center
            justify-center
          >
            <img src="../assets/img/full_logo.png" alt="full logo">
          </v-flex>
          <v-flex
            d-flex
            align-center
            justify-center
            class="custom"
          >
            <v-flex
              d-flex
              align-center
              justify-center
              class="parallelogram"
            >
              <div class="custom-parallelogram"></div>
              <v-tabs
                v-model="tabs"
                background-color="transparent"
                color="#ffffff"
                class="blue-parallelogram"
                height="119"
                grow
                hide-slider
                active-class="active-custom"
              >
                <v-tab
                  href="#tab-1"
                  :ripple="false"
                  style="width:50%"
                >
                  <span class="direct-text">
                    Персонал
                  </span>
                </v-tab>

                <v-tab 
                  href="#tab-2"
                  :ripple="false"
                  style="width:50%"
                >
                  <span class="direct-text">
                    Доктор
                  </span>
                </v-tab>
              </v-tabs>
            </v-flex>
          </v-flex>
          <v-flex class="form">
            <v-tabs-items v-model="tabs">
              <v-tab-item
                value="tab-1"
              >
                <login-form />
              </v-tab-item>
              <v-tab-item
                value="tab-2"
              >
                <login-form />
              </v-tab-item>
            </v-tabs-items>
          </v-flex>
        </v-flex>
      </v-flex>
    </v-layout>
</template>

<script>
import LoginForm from './LoginForm'
export default {  
  data() {
    return {
      tabs: null
    }
  },

  components: {
    LoginForm
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.picture {
  background-image: url(../assets/img/computer-3343887.png);
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
}

.absolute-cover-bg {
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.5);
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.65);
}

.login-content > hr {
  width: 133px;
  height: 6px;
  background: #007AD7;
  border: 0;
  border-radius: 1px;
  margin: 40px 0;
}

.login-title {
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 65px;
  color: #FFFFFF;
}

.login-content > h3 {
  width: 60%;
  font-family: Montserrat;
  font-style: normal;
  font-weight: normal;
  font-size: 40px;
  color: #FFFFFF;
  padding-top: 40px;
}

.workplace {
  background-color: #FFFFFF;
}

.container-workplace {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.custom {
  width: 80%;
  position: relative;
}

.parallelogram {
  position: relative;
  height: 119px;
  width: 80%;
  background-color: transparent;
}

.custom-parallelogram {
  position: absolute;
  height: 92px;
  width: 100%;
  border: 3px solid #C4C7CC;
  transform: skew(145deg);
}

.blue-parallelogram {
  transform: skew(145deg);
}

.direct-text {
  transform: skew(35deg);
  font-family: Roboto;
  font-style: normal;
  font-weight: 500;
  font-size: 35px;
  text-transform: none;
}

.v-item-group {
  line-height: 35px;
}


.active-custom {
  background: linear-gradient(90deg, #00B3F4 32.17%, #007AD7 80.23%);
  box-shadow: 0px 4px 15px rgba(0, 122, 215, 0.3);
} 

.v-tab:before {
  display: none;
}

.form {
  width: 100%;
}

</style>
