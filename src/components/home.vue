<template>
  <div class="home">
    <h1>{{title}}</h1>
    
    <div class="row">
      <div class="col-md-4 col-lg4" v-for="(data,index) in products" :key="index">
         <img id="mouse" @click="goTodetail(data.productId)" :src="data.image" class="img-fluid">
         <h7 id="mouse" @click="goTodetail(data.productId)" >{{data.productTitle}}</h7>
         <h4>{{data.subtitle}} </h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      title: 'Super Miniaturas',
      products:[
      {
        productTitle:"Miniatura Fórmula 1, Ferrari SF16-H, do piloto Sebastian Vettel",
        subtitle: "R$: 50,00",
        image       : require('../assets/images/ferarri-1.png'),
        productId:1
      },
      {
        productTitle:"Miniatura de carro Chevrolet Camaro, 1967, da série Bigtime Muscle, na escala 1:24.",
        image       : require('../assets/images/camaro1.png'),
        subtitle: "R$: 30,00",
        productId:2
      },
      {
        productTitle:"Miniatura de Checker A11, New York Taxi Cab, táxi verificador, 1981, na escala 1:18.",
        image       : require('../assets/images/taxi1.png'),
        subtitle: "R$: 45,00",
        productId:3
      },
      {
        productTitle:"Miniatura de carro Volkswagen Beetle / Fusca, 1955, da série Gold Collezione na escala 1:18.",
        subtitle: "R$: 61,00",
        image       : require('../assets/images/fusca1.png'),
        productId:4
      },
      {
        productTitle:"Miniatura de carro Ford Maverick, 1974, na escala 1:24.",
        subtitle: "R$: 56,00",
        image       : require('../assets/images/maverick1.png'),
        productId:5
      },
      {
        productTitle:"Miniatura de carro Ford Mustang GT, 2015, da série Special Edition, na escala 1:24.",
        subtitle: "R$: 49,00",
        image       : require('../assets/images/mustang1.png'),
        productId:6
      }
      ]
    }
  },
  methods:{
  goTodetail(prodId) {
    let proId=prodId
    this.$router.push({name:'details',params:{Pid:proId}})
  }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.row img{
  max-height: 15em;
  width: 100%;

}

.carousel-inner > .item > img,
  .carousel-inner > .item > a > img {
    width: 70%;
    margin: auto;
  }

#mouse{
  cursor:pointer;
}
.row h3{
  cursor:pointer;
}
</style>
