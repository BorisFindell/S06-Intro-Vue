<template>
  <div class="container d-flex justify-content-center w-100">
    <button type="button" class="button ant mt-5 btn-primary d-flex justify-content-center" @click="$emit('ant-sentence')">Anterior</button>
    <button type="button" class="button seg mt-5 btn-warning d-flex justify-content-center" @click="$emit('seg-sentence')">Siguiente</button>
  </div>
</template>

<script>

export default {
  name: 'botons',
  emits: ['ant-sentence', 'seg-sentence']
}

</script>

<style scoped>

.ant,
.seg {
  width: 30%;
  padding: 10px;
}


</style>