<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <router-link to="/siswa">Data Siswa</router-link>
    <router-link to="/kelas">Data Kelas</router-link>
    <router-view/> --> <!-- update data yg di klik -->
    <h1>{{ nama }}</h1>
    <h2>Nama: <input v-model="nama"><br></h2>
    <h2>Nilai Anda:&nbsp{{ nilai }}</h2>
    <button @click="totalnilai">Click Me</button>  
    <h2>1. Salah satu nama kota di pulau Jawa?</h2>
    <input type="radio" v-model="soal1" value="Bandung">Bandung &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Sabang">Sabang &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Denpasar">Denpasar &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Jambi">Jambi &nbsp&nbsp<br>
    <h2>2. Aplikasi untuk Coding Web?</h2>
    <input type="radio" v-model="soal2" value="Mozilla Firefox">Mozilla Firefox &nbsp&nbsp
    <input type="radio" v-model="soal2" value="PUBG">PUBG &nbsp&nbsp
    <input type="radio" v-model="soal2" value="Sublime">Sublime &nbsp&nbsp
    <input type="radio" v-model="soal2" value="Steam">Steam &nbsp&nbsp<br>
    <h2>3. Berapakah 9 X 9?</h2>
    <input type="radio" v-model="soal3" value="81">81 &nbsp&nbsp
    <input type="radio" v-model="soal3" value="18">18 &nbsp&nbsp
    <input type="radio" v-model="soal3" value="999999999">999999999 &nbsp&nbsp
    <input type="radio" v-model="soal3" value="99">99 &nbsp&nbsp<br>
  </div>
</template>

<script>
/*import HelloWorld from './components/HelloWorld.vue'*/

export default {
  name: 'app',
  data() {
    return{
      nama: '',
      nilai: 0,
      soal1: '',
      soal2: '',
      soal3: ''
      /*components: {
        HelloWorld
      }*/
    }
  },
methods: {
  totalnilai(){
    if (this.soal1 == 'Bandung' && this.soal2 == 'Sublime' && this.soal3 == '81') {
      this.nilai=+3    
    }
    else if (this.soal1 == 'Bandung' && this.soal2 == 'Sublime') {
      this.nilai=+2 
    }
    else if (this.soal1 == 'Bandung' && this.soal3 == '81') {
      this.nilai=+2 
    }
    else if (this.soal2 == 'Sublime' && this.soal3 == '81') {
      this.nilai=+2 
    }
    else if (this.soal1 == 'Bandung') {
      this.nilai=+1 
    }
    else if (this.soal2 == 'Sublime') {
      this.nilai=+1 
    }
    else if (this.soal3 == '81') {
      this.nilai=+1 
    }
    else {
      this.nilai = 0 
    }
  }
}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
