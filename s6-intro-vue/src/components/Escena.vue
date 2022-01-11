<template>
  <div class="container d-flex justify-content-center">
    <ul class="lista">
      <li class="elem" v-for="(frase, index) in frases" :key="index">
          {{frase}}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'escena',
  props: ['frases']
}
</script>

<style scoped>
  .lista {
    padding: 0px;
    text-align: center;
    margin-top: 20px;
  }

  .elem {
    list-style: none;
    border: 1px solid black;
    margin-bottom: 10px;
    padding: 10px;
    border-radius: 50px;
  }


</style>