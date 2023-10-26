<template>
  <div>
    <Header />
    <section id="sct_1">
      <div class="container">
        <div class="row">
          <div class="col-md-8">
            <div class="title_banner">
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="sct_2">
      <div class="container">
        <div class="row">
          <div class="col-md-4" v-for="dino in state.dinos.carnivoros" :key="dino.id">
            <Card/>
          </div>
        </div>
      </div>

    </section>
    <!--<h1>Dinos</h1>
    {{ state.dinos.carnivoros }}
    <div v-for="dino in state.dinos.carnivoros" :key="dino.id">
      {{ dino.nome }}
      {{ dino.imagem }}
      <img :src="dino.imagem" />
    </div>-->
  </div>
</template>
<script>
import Header from './components/Header.vue'
import Card from './components/Card.vue'
import { reactive, onMounted } from 'vue'
export default {
  components: {
    Header,
    Card,
  },
  setup() {
    const state = reactive({
      dinos: [{ carnivoros: [] }],
    });
    onMounted(() => {
      getDinos();
    })
    async function getDinos() {
      const req = await fetch("http://localhost:3000/dinos ");
      const data = await req.json();
      console.log(data)
      state.dinos = data;
    }
    return {
      state,
    }
  },
}
</script>
<style scoped>
#sct_1 {
  background-image: url(./../../public/images/banner_1.jpg);
  height: 80vh;
  background-position: center;
  background-size: cover;
}
</style>