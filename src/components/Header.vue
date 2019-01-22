<template>
  <div>
    <nav class="navbar__custom">
      <div id="myNav" class="overlay">
          <a href="javascript:void(0)" class="closebtn" @click="closeNav()">&times;</a>
        <div class="overlay-content">
          <router-link to="#about">About</router-link>
          <router-link to="#footer">Contact</router-link>
        </div>
      </div>
      
      <div class="menu">
        
          <a class="navbar-brand" href="/"><img class="header__logo" alt="Vue logo" src="@/assets/img/empire_logo_wht-h.png"></a>

          <div class="menu-right">
            <!-- <a class="menu__buttons" @click="openNav()"> 
              <span class>MENU</span>
              <img class="menu_ham" src="../assets/img/menu-button.svg" alt="">
            </a> -->

           <div>
            <select v-model="currentLocale">
              <option v-for="locale in locales" v-bind:value="locale.id">{{locale.name}}</option>
            </select>
          </div>

            <b-button href="https://app.empirebcluster.com/#/register" target="_self" class="menu-singup-button">{{ signupBtn[currentLocale] }}</b-button>            
            <b-button href="https://app.empirebcluster.com/" target="_self" class="menu-singup-button">{{ loginBtn[currentLocale]}}</b-button>
          </div>
      </div>
    </nav>
  </div>
</template>

<script>
import config from '@/config/settings'
import { serverBus } from '@/main'

export default {
  name: 'Header',


  data(){
    return {

    currentLocale:'eng',
      locales: [ 
        {id: 'eng', name: 'English'}, 
        {id: 'esp', name: 'Spanish'}
        ],

        heading: {
          eng: 'Hello you, Vue.js!',
          esp: "Hola tu, con Vue.js"
        },
        signupBtn: {
          eng: 'Sign Up',
          esp: 'Registrate'
        },
        loginBtn: {
          eng: 'Login',
          esp: 'Iniciar'
        },
        heroText: {
          eng: 'THE MOST INNOVATIVE WAY TO CAPITALIZE IN CRYPTOCURRENCY',
          esp: 'LA FORMA MAS INNOVADORA DE CAPITALIZAR CRIPTOMONEDA'
        }
    }
  },

  

  created(){ 
  
    
  },

  methods:{
    
    openNav() {
      document.getElementById("myNav").style.width = "450px"
    },

    closeNav() {
      document.getElementById("myNav").style.width = "0"
    },

    scroll(id){
      let data = async() => {
        await helper.goToByScroll(id)
        await this.closeNav()
      }
      data()
    }
  }
  
}

</script>

<style>

	.overlay {
    height: 100%;
    width: 0%;
    position: fixed;
    z-index: 999;
    top: 0;
    right: 0;
    background-color: rgb(0,0,0);
    background-color: rgba(0,0,0, 0.85);
    -webkit-clip-path: polygon(34% 0, 100% 0%, 100% 100%, 0% 100%);
    clip-path: polygon(34% 0, 100% 0%, 100% 100%, 0% 100%);
    overflow-x: hidden;
    transition: 0.5s;
}

	.-content {
    position: relative;
    top: 25%;
    width: 100%;
    text-align: center;
    margin-top: 30px;
}

.overlay a {
    padding: 1rem 5rem;;
    text-decoration: none;
    font-size: 36px;
    color: #fff;
    display: block;
    transition: 0.3s;
    text-align: right;
    
}

.overlay a:hover, .overlay a:focus {
    color: #666;
}

.overlay .closebtn {
    position: absolute;
    top: 20px;
    right: 45px;
    font-size: 60px;
}

  .menu {
    display: flex;
    justify-content: space-between;
}

 .menu__button {
    padding-left: 2rem;
}

  .menu__button img {
    width: 1.5rem;
    margin: 0 !important;
}
</style>
