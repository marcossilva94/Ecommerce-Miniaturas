<template>
  <div id="app">
      <!-- navbar -->
      <div class="navbar navbar-expand-lg  fixed-top navbar-light ">
        <div class="container">
        <router-link to="/" class="navbar-brand">Inicio</router-link>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="navbar-nav">
      
            <li class="nav-item">
             <router-link class="nav-link" to="/semelhante">Semelhantes</router-link>
            </li>
            <li class="nav-item">
            <router-link class="nav-link" to="/services">Sobre</router-link>
            </li>
            <li class="nav-item">
             <router-link class="nav-link" to="/contact">Contato</router-link>
            </li>
            <li class="nav-item">
             
             <a class="nav-link" href="https://drive.google.com/open?id=14xcPYb3p8OCdxx2sEdOcb-vkWXYtS20I" target="_blank">Atividade PDF</a>
            </li>


          </ul>
        </div>
        </div>
      </div>
      <div class="container">
       <transition name="moveInUp">
         <router-view/>
       </transition>
        
      </div>
    <div id="rodape">
       <p> 2019 © Todos os Direitos Reservados - Antonio Marcos da Silva  - Faculdade Guairacá</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
.navbar{
  background-color: #00BFFF;
  
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
.moveInUp-enter-active{
  animation: fadeIn 2s ease-in;
}
@keyframes fadeIn{
  0%{
    opacity: 0;
  }
  50%{
    opacity: 0.5;
  }
  100%{
    opacity: 1;
  }
  
}

#rodape{
  border-top-style: solid;
  border-width: 1px;
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: #F0F8FF;
  
}

.moveInUp-leave-active{
  animation: moveInUp .3s ease-in;
}
@keyframes moveInUp{
 0%{
  transform: translateY(0);
 }
  100%{
  transform: translateY(-400px);
 }
}
</style>
