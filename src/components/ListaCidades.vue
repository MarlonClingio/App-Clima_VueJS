<template>
  <h2>{{ cidadeselecionada }}</h2>
  <br>
  <div class="lista">
    <CardCidade v-for="cidade in cidades" :key="cidade.id" :cidade="cidade" v-on:cidadeclicada="mudarcidadeselecionada" />
  </div>
</template>

<script>
import CardCidade from "./CardCidade.vue";
export default {
  components: { CardCidade },
  methods: {
    mudarcidadeselecionada(cidade) {
      alert(cidade.name)
    }
  },
  data() {
    return {
      cidadeselecionada: "",
      cidades: [
        {
          id: 8429,
          name: "Rio de Janeiro",
          description: "Nublado",
          icon: "01d",
          temp: "25",
        },
        {
          id: 8412,
          name: "Manaus",
          description: "Chuvas Fortes",
          icon: "09d",
          temp: "21",
        },
        {
          id: 8454,
          name: "Brasília",
          description: "Ensolarado",
          icon: "e81a",
          temp: "27.4",
        },
      ],
    };
  },
};
</script>

<style></style>