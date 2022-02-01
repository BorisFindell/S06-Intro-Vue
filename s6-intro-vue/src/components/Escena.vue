<template>
  <div class="container d-flex justify-content-center">
    <ul class="lista">
      <li :class="{btnActive: index == activeSentence}" v-for="(frase, index) in frases" :key="index">
          {{frase.txt}}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'escena',
  props: {
    frases:Array,
    activeSentence:Number}
}
</script>

<style scoped>

  .lista {
    padding: 0px;
    text-align: center;
    margin-top: 20px;
  }

  li {
    list-style: none;
    border: 1px solid black;
    margin-bottom: 10px;
    padding: 10px;
    border-radius: 50px;
    background-color: rgba(255, 255, 255, 0.9);
  }

.btnActive {
  background-color: burlywood;
}

</style>