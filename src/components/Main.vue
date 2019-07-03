<template>
  <div class="main">
    <h1>MOBILE SLIDER</h1>
    <div class="content display-container">
  <img class="mySlides" src="https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Fcolorinnature.files.wordpress.com%2F2011%2F04%2Funa-noche-en-santander.jpg&f=1">
  <img class="mySlides" src="https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Fgaleriasdeimagenes1b311.files.wordpress.com%2F2013%2F03%2Ffoto_de_flor_orquidea_17.jpg&f=1">
  <img class="mySlides" src="https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Ftse2.mm.bing.net%2Fth%3Fid%3DOIP.SOaVafEkI9Qh-ZnNexzCcwHaFj%26pid%3DApi&f=1">
  <img class="mySlides" src="https://proxy.duckduckgo.com/iu/?u=http%3A%2F%2F2.bp.blogspot.com%2F_NHn6x9daBKk%2FS91yQMj2kyI%2FAAAAAAAAABI%2FwKXz4Z2WQEg%2Fs1600%2F011024ry2.jpg&f=1">

  <button class="button black display-left" v-on:click="plusDivs(-1)">&#10094;</button>
  <button class="button black display-right" v-on:click="plusDivs(1)">&#10095;</button>
</div>

  </div>
</template>

<script>

export default {
  name: 'Main',
  data () {
  return {
    slideIndex: 1
  }
},
  
  methods: {
   plusDivs(n) {
    this.showDivs(this.slideIndex += n);
  },
    showDivs(n) {
      const x = document.querySelectorAll(".mySlides");
        if (n > x.length) {this.slideIndex = 1}
        if (n < 1) {this.slideIndex = x.length}
        for (let i = 0; i < x.length; i++) {
          x[i].classList.add("none");  
        }
        x[this.slideIndex-1].classList.remove("none");  
    }
  },
  mounted: function() {
      const x = document.querySelectorAll(".mySlides");
        for (let i = 0; i < x.length; i++) {
          x[i].classList.add("none");  
        }
        x[0].classList.remove("none");  
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
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

.mySlides{width:100%;}
*{box-sizing:border-box;}
.button {border:none;display:inline-block;padding:8px 16px;vertical-align:middle;overflow:hidden;text-decoration:none;color:inherit;background-color:inherit;text-align:center;cursor:pointer;white-space:nowrap;-webkit-touch-callout:none;-webkit-user-select:none;-khtml-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none}

.button:hover{color:#000!important;background-color:#ccc!important}

.display-left{position:absolute;top:50%;left:0%;transform:translate(0%,-50%);-ms-transform:translate(-0%,-50%)}
.display-right{position:absolute;top:50%;right:0%;transform:translate(0%,-50%);-ms-transform:translate(0%,-50%)}

.black {color:#fff!important;background-color:#000!important}

.content {
    max-width: 980px;
  margin-left: auto;
margin-right: auto;
}

.display-container {
    position: relative;
}
  .none{
    display:none;
  }
@media (min-width:740px) {
.button{display:none}
.mySlides{display: inline-block; width: 20%; margin: 0px 2%;}
}
</style>
