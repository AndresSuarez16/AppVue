<script>

export default {
  data() {
    return {
      num1: 5,
      num2: 6,
      resultado: "",
    };
  },
  methods: {
    sumar() {
      this.resultado = num1 + num2;
    },
    restar() {
      this.resultado = num1 - num2;
    },
  },
};
</script>

<template>
  <div>
    <button @click="sumar">sumar</button>
    <p>La Suma de los dos numeros es: {{ resultado }}</p>

    <button id="resta" @click="restar">restar</button>
    <p id="resta">La Resta de los dos numeros es: {{ resultado }}</p>
  </div>
</template>

<style>
@import "./assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
