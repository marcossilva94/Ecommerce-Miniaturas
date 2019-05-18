<template>
	<div class="semelhante">
		<h1>{{title}}</h1>
		<div class="row">
			<div class="col-md-4">
				<div class="card">
					<div class="card-header"  v-for="(data,index) in logos" :key="index">
						<img  :src="data.image1" alt="minimundi">
					</div>
					<div class="card-body">
						
						Minimundi – O minimundi.com.br já está a mais de 10 anos no mercado, sendo assim possui um estoque muito vasto de objetos, desta forma apresenta uma boa experiencia para os clientes que buscam adquirir suas novas miniaturas para que possam ampliar sua coleção
					</div>
					<a v-bind:href ="url" target="_blank">MiniMundi</a>
				</div>
			</div>
			<div class="col-md-4">
				<div class="card">
					<div class="card-header"  v-for="(data,index) in logos" :key="index">
						<img :src="data.image2" alt="orangebox">
					</div>
					<div class="card-body">
						
						A Orange box miniaturas esta no mercado desde de 2006, possui mais de 3500 itens na
						coleção disponível para os clientesAtendimento personalizado na venda e pós venda
						Comprometimento com a qualidade Logística impecável
						Novidades, variedades de produtos.
					</div>
					<a v-bind:href ="url2" target="_blank">OrangeBox</a>
				</div>
			</div>
			<div class="col-md-4">
				<div class="card" v-for="(data,index) in logos" :key="index">
					<div class="card-header">
						<img class="img-fluid" :src="data.image3" alt="automobilli">
					</div>
					<div class="card-body">
						
						A autimobilli traz produtos com alta qualidade e exclusividade para seus clientes, com
						muitas variedades como AutoArt, Greenlight, Jada Toys,
						Norev, Schuco. entre outras marcas conceituadas no mercado mundial estão presentes em
						nosso mix de produtos, assim como inúmeros modelos de carros. 
						
						
					</div>
						<a v-bind:href ="url3" target="_blank">Automobilli</a>
						
				</div>
				
			</div>
		</div>
	</div>
</template>
<script>
	
	export default{
		
		name:'semelhante',
		data () {
			
			return{
				
				title:'Sites Semelhantes',
				url: 'https://www.minimundi.com.br/',
				url2: 'https://www.orangeboxminiaturas.com.br/',
				url3: 'https://www.automobilli.com.br/',
			
				logos:[
					{
					logotitle	: "imagens",
					image1      : require('../assets/images/logominimundi.png'),
					image2       : require('../assets/images/logoorangebox.png'),
					image3      : require('../assets/images/logoautomobilli.png'),
					logoId:1

					},
				]
			}
		}
	}
</script>

<style scoped>
	
</style>