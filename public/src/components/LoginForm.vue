<template>
  <v-flex
    d-flex
    flex-column
    align-center
  >
    <v-flex
      d-flex
      flex-column
      class="form-inputs"
    >
      <label>ИМЯ ПОЛЬЗОВАТЕЛЯ</label>
      <input
        placeholder="Введите ваше имя пользователя"
        v-model="name"
      />
    </v-flex>
    <v-flex
      d-flex
      flex-column
      class="form-inputs"
    >
      <label>ПАРОЛЬ</label>
      <input
        label="ПАРОЛЬ"
        placeholder="Введите ваш пароль"
        type="password"
        v-model="password"
      />
    </v-flex>
    <div class="danger-alert" v-html="error" />
    <button
      class="log-in"
    >
      Войти
    </button>
  </v-flex>
</template>

<script>
export default {  
  data() {
    return {
      name: '',
      password: '',
      error: null
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.form-inputs {
  font-family: Montserrat;
  font-size: 20px;
  width: 100%;
  margin: 20px 0;
}

.form-inputs > label {
  font-style: normal;
  font-weight: 800;
  letter-spacing: -0.03em;
  color: #394656;
  margin-bottom: 10px;
}

.form-inputs > input {
  border: 2px solid rgba(57, 70, 86, 0.3);
  box-sizing: border-box;
  border-radius: 5px;
  padding: 0 23px;
  font-style: normal;
  height: 69px;
  font-weight: 500;
}

.log-in {
  background: linear-gradient(90deg, #00B3F4 26.42%, #007AD7 99.99%, rgba(196, 196, 196, 0) 100%);
  box-shadow: 0px 4px 15px rgba(0, 122, 215, 0.3);
  border-radius: 10px;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
  font-size: 40px;
  letter-spacing: -0.03em;
  color: #FFFFFF;
  width: 70%;
  height: 74px;
  margin-top: 30px;
}
</style>
