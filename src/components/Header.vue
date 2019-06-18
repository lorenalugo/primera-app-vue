<template>
  <div class="header">
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">{{ item1 }}</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">{{ item2 }}</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">{{ item3 }}</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">{{ item4 }}</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">{{ item5 }}</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data: function () {
    return {
      item1: 'Core Docs',
      item2: 'Forum',
      item3: 'Community',
      item4: 'Twitter',
      item5: 'News'
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
