<template>
	<div class="contact">
		<h1>{{title}}</h1>
		
		 <div class="contact">
		 	<form id="formulario">
		 		<div class="form-group">
		 			<div class="input-group-prepend">
		 				
		 				<input id="nome" type="text" class="form-control" name="" placeholder="Nome">
		 			</div>
		 			<div class="input-group-prepend">
		 				
		 				<input type="text" class="form-control" name="" placeholder="E-mail">
		 			</div>
		 			<div class="input-group-prepend">
		 			
		 				<textarea class="form-control" placeholder="Mensagem">
		 					
		 				</textarea>
		 			</div>
		 			<button v-on:click="sucesso()" class="btn btn-primary btn-block">Submit</button>
		 		</div>
		 	</form>
		 </div>
	</div>
</template>
<script>
	export default{
		name:'blog',
		data (){
			return{
				title:'Contato',
				mostrar: 'Mensagem enviada com Sucesso'
			}
		},
	methods: {
		sucesso(){
			alert(this.mostrar);
			
		}
	}
	}
</script>


<style scoped>
.contact form{
	max-width: 40em;
	margin: 2em auto;
}
.contact form .form-control{
	margin-bottom: 1em;
}
.contact form textarea{
	min-height: 20em;
}	
</style>