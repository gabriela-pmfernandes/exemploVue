<template>
  <h1>Food</h1>
  <!-- <p>Minha comida favorita tem uma imagem de diploma anexada.</p> -->
  <p>
    A descrição do alimento para o componente arroz não é fornecida, então o
    valor padrão é usado.
  </p>
  <div id="wrapper">
    <food-item
      food-name="Apples"
      food-desc="Maças sao um tipo de fruta que cresce em arvores."
      v-bind:is-favorite="true"
    />
    <food-item
      food-name="Pizza"
      food-desc="Pizza tem base de pao com molho de tomate, queijo e cobertura por cima."
      v-bind:is-favorite="false"
    />
    <food-item food-name="Rice" v-bind:is-favorite="false" />
  </div>
</template>

<style>
#wrapper {
  display: flex;
  flex-wrap: wrap;
}
#wrapper > div {
  border: dashed black 1px;
  flex-basis: 120px; /**ajusta o texto em baixo da imagem*/
  margin: 10px;
  padding: 10px;
  background-color: lightgreen;
}
</style>
