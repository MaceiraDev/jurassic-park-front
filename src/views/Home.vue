<template>
  <div>
    <h1>Dinos</h1>
    {{ state.dinos.carnivoros }}
    <div v-for="dino in state.dinos.carnivoros" :key="dino.id">
      {{ dino.nome }}
      <img :src="dino.imagem" />
    </div>
  </div>
</template>
<script>
import { reactive, onMounted } from 'vue'
export default {
  setup() {
    const state = reactive({
      nome: "Leonardo",
      dinos: [{ carnivoros: [] }],
    });
    onMounted(() => {
      getDinos();
    })
    async function getDinos() {
      const req = await fetch("http://localhost:3000/dinos ");
      const data = await req.json();
      state.dinos = data;
    }
    return {
      state,
    }
  },
}
</script>