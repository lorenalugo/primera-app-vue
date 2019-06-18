<template>
  <div class="footer">
    <div class="col">{{ footeritem1 }}
      <Form />
    </div>
    <div class="col">{{ footeritem2 }}</div>
    <div class="col">{{ footeritem3 }}</div>
    <div class="texto">Este es un texto en el footer</div>
  </div>
</template>

<script>
import Form from './Form.vue';
export default {
  name: 'Footer',
  components: {
    Form
  },
  data: function () {
    return {
      footeritem1: 'Core Docs',
      footeritem2: 'Forum',
      footeritem3: 'Community'
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.footer {
  background-color: #42b983;
  color: #fff;
}
.col {
  box-sizing: border-box;
  width: 33.33%;
  float: left;
  height: 100px;
}
.texto {
  text-align: center;
}
</style>
