<template>
  <div>
    <ul>
      <li v-for="(frase, index) in frases" :key="index">
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
