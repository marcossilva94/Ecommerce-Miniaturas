<template>
  <div class="details">
    <div class="container">
      <div class="row">
        <div class="col-md-12" v-for="(product,index) in products" :key="index">
          <div v-if="proId == product.productId">
            <h1>{{product.productTitle}}</h1>
            <div>
              <div style="float: left; width: 45%">
                <img :src="product.image" class="img-fluid">
              </div>
              <div style="float: right; width: 45%; margin-top: 50px">
                <h4>{{product.description}}</h4>
                <p style="text-align: justify">{{product.details}}</p>
              </div>
              <div style="float: right; width: 45%; margin-top: 50px">
                <br>
                <h5 style="text-align: justify">
                  {{product.valor}}
                  <button
                    v-on:click="AddCarrinho"
                    class="fas fa-shopping-cart btn btn-primary"
                  >Adicionr ao Carrinho</button>
					<i class="fas fa-shopping-cart"> {{car}}</i>
                </h5>
				
			
              </div>
            </div>
            <div style="clear: both">
              <div style="float: left; width: 25%">
                <img style="width: 150px; height: 150px;" class="img-fluid" :src="product.image2">
              </div>
              <div style="float: left; width: 25%">
                <img style="width: 150px; height: 150px;" class="img-fluid" :src="product.image3">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
	export default{
		name:'details',
		data(){
			return{
				proId:this.$route.params.Pid,
				title:"details",
				car: 0,
				products:[
				{
				productTitle:"Ferrari",
				image       : require('../assets/images/ferarri-1.png'),
				image2      : require('../assets/images/ferarri-2.png'),
				image3      : require('../assets/images/ferarri-3.png'),
				productId:1,
				description: "Descrição",
				details: "Miniatura Fórmula 1, Ferrari SF16-H, do piloto Sebastian Vettel, Nº 5, na escala 1:43" + 
						"Produzida em metal com detalhes em plástico, apresenta alto grau de detalhamento, pneus emborrachados, e pintura na cor vermelha." + 
						"Comprimento aproximado: 11 cm.",
				
				},

				{
				productTitle:"Camaro",
				image       : require('../assets/images/camaro1.png'),
				image2      : require('../assets/images/camaro2.png'),
				image3      : require('../assets/images/camaro3.png'),
				productId:2,
				description: "Descrição",
				details: "Miniatura de carro Chevrolet Camaro, 1967, da série Bigtime Muscle, na escala 1:24." + 
				"Produzida em metal com detalhes em plástico, apresenta pneus emborrachados, abertura das portas, do capô e pintura na cor vermelha. Comprimento aproximado: 20 cm."
				},
				{
				productTitle:"Taxi",
				image       : require('../assets/images/taxi1.png'),
				image2      : require('../assets/images/taxi2.png'),
				image3      : require('../assets/images/taxi3.png'),
				productId:3,
				description: "Descrição",
				details: "Miniatura de Checker A11, New York Taxi Cab, táxi verificador, 1981, na escala 1:18." +
				"Produzida em metal com detalhes em plástico, apresenta alto grau de detalhamento, abertura das portas, do porta-malas e do capô, pneus emborrachados e pintura na cor amarela."
				},
				{
				productTitle:"Fusca",
				image       : require('../assets/images/fusca1.png'),
				image2      : require('../assets/images/fusca2.png'),
				image3      : require('../assets/images/fusca3.png'),
				productId:4,
				description: "Descrição",
				details: "Miniatura de carro Volkswagen Beetle / Fusca, 1955, da série Gold Collezione na escala 1:18." + 
				"Produzida em metal com detalhes em plástico, apresenta abertura das portas, capô e do porta-malas, pneus emborrachados e pintura na cor azul" +
				"Rodas esterçam (Volante acompanha movimento)"
				},
				{
				productTitle:"Maverick",
				image       : require('../assets/images/maverick1.png'),
				image2      : require('../assets/images/maverick2.png'),
				image3      : require('../assets/images/maverick3.png'),
				productId:5,
				description: "Descrição",
				details: "Miniatura de carro Ford Maverick, 1974, na escala 1:24." + 
				"Produzida em metal com detalhes em plástico, apresenta pneus emborrachados, abertura das portas e capô, pintura na cor preta, volante acompanha movimento das rodas e acompanha base de plástico."
				},
				{
				productTitle:"Mustang",
				image       : require('../assets/images/mustang1.png'),
				image2      : require('../assets/images/mustang2.png'),
				image3      : require('../assets/images/mustang3.png'),
				productId:6,
				description: "Descrição",
				details: "Miniatura de carro Ford Mustang GT, 2015, da série Special Edition, na escala 1:24. " + 
				"Produzida em metal com detalhes em plástico, apresenta pneus emborrachados, abertura das portas e do capô, e pintura na cor azul. "
				}
				]
				 
			}
		},
		methods: {
			AddCarrinho(){
				
				this.car += 1;
			}
			 
		}
		
	}
</script>