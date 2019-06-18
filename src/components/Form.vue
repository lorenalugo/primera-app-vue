<template>
  <div class="form">
    <p class="clear">
      Este es el subcomponente adentro del footer, falta agregar el {{ text }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'Form',
  data: function () {
    return {
      text: 'Formulario'
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
