<template>
  <div>

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
            <select class="select-custom" v-model="currentLocale">
                <option v-for="locale in locales" v-bind:value="locale.id">{{locale.name}}</option>
            </select>
        </div>

            <b-button href="https://app.empirebcluster.com/#/register" target="_self" class="menu-singup-button">{{ signupBtn[currentLocale] }}</b-button>            
            <b-button href="https://app.empirebcluster.com/" target="_self" class="menu-singup-button">{{ loginBtn[currentLocale] }}</b-button>
          </div>
      </div>
    </nav>
  </div>



    <!-- <Header/> -->
			<div id="carouselExampleIndicators" class="carousel slide custom-slide" data-ride="carousel">
				
				<div class="carousel-inner">
						<div class="carousel-item active slide1"></div>
						<div class="carousel-item slide2"></div>
						<div class="carousel-item slide3"></div>
						<div class="carousel-item slide4"></div>
				</div>

				<a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
						<span class="carousel-control-prev-icon" aria-hidden="true"></span>
						<span class="sr-only">Previous</span>
				</a>
					
				<a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
					<span class="carousel-control-next-icon" aria-hidden="true"></span>
					<span class="sr-only">Next</span>
				</a>
    </div>

		<div class="hero-text-container">
					<h1 class="hero-text-title">{{heroText[currentLocale]}}</h1>
					<a href="https://app.empirebcluster.com/#/register">
                        <b-button class="menu-singup-button herobtn"> {{ctaBtn[currentLocale]}}</b-button>
                    </a>

					<div class="tickers">
						<div class="coinmarketcap-currency-widget" data-currencyid="1" data-base="USD" data-secondary="" data-ticker="true" data-rank="false" data-marketcap="false" data-volume="false" data-stats="USD" data-statsticker="false"></div>
						<div class="coinmarketcap-currency-widget" data-currencyid="2" data-base="USD" data-secondary="" data-ticker="true" data-rank="false" data-marketcap="false" data-volume="false" data-stats="USD" data-statsticker="false"></div>
						<div class="coinmarketcap-currency-widget" data-currencyid="74" data-base="USD" data-secondary="" data-ticker="true" data-rank="false" data-marketcap="false" data-volume="false" data-stats="USD" data-statsticker="false"></div>
					</div>

				</div>

    <section class="about">
      <div class="about_text container">
        <h1>{{ aboutLabel[currentLocale]}}</h1>
        <p>{{aboutText1[currentLocale]}}</p>
        <p>{{aboutText2[currentLocale]}}</p>
        <p>{{aboutText3[currentLocale]}}</p>
        <p>{{aboutText4[currentLocale]}}</p>

        <!-- <button class="about_button">Read More</button> -->
      </div>
    </section>

    <section class="inversion-packets">
      <h1>{{investmentLabel[currentLocale]}}</h1>
    </section>

    
    <section class="features container">
      <h1>{{packetsLabel[currentLocale]}}</h1>
      <p>{{packetsSubText[currentLocale]}}</p>
      <div>
        <b-card-group deck >
            <b-card class="features-card">
                <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                <h2>FOUNDER</h2>
                <h3 class="features-card_price">$200 USD</h3>
                <p class="features-card_text">
                    {{packetsText1[currentLocale]}} 
                </p>
                <p>{{packetsText1[currentLocale]}}</p>
                <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
            </b-card>
           <b-card class="features-card">
                <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                <h2>BASIC</h2>
                <h3 class="features-card_price">$100 USD</h3>
               <p class="features-card_text">
                    {{packetsText1[currentLocale]}}
                </p>
                <p>{{packetsText1[currentLocale]}}</p>
                <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
            </b-card>
            <b-card class="features-card">
                <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                <h2>MEDIUM</h2>
                <h3 class="features-card_price">$300 USD</h3>
                <p class="features-card_text">
                    {{packetsText1[currentLocale]}}
                </p>
                <p>{{packetsText1[currentLocale]}}</p>
                <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
            </b-card>
        </b-card-group>
        <b-card-group deck >
            <b-card class="features-card">
                <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                <h2>PRO</h2>
                <h3 class="features-card_price">$600 USD</h3>
               <p class="features-card_text">
                    {{packetsText1[currentLocale]}}
                </p>
                <p>{{packetsText1[currentLocale]}}</p>
                <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
            </b-card>
           <b-card class="features-card">
                <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                <h2>GOLD</h2>
                <h3 class="features-card_price">$900 USD</h3>
                <p class="features-card_text">
                    {{packetsText1[currentLocale]}}
                </p>
                <p>{{packetsText3[currentLocale]}}</p>
                <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
            </b-card>
            <b-card class="features-card">
                <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                <h2>PLATINUM</h2>
                <h3 class="features-card_price">$1,800 USD</h3>
                <p class="features-card_text">
                    {{packetsText1[currentLocale]}}
                </p>
                <p>{{packetsText3[currentLocale]}}</p>
                <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
            </b-card>
        </b-card-group>
      </div>
    </section>

    <!-- <section class="our-plans">
      <div class="container">
        <div class="our-plans_titletext">
          <h1>OUR PLANS</h1>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore sint, reprehenderit ipsum non, obcaecati asperiores vel, rerum minus deleniti aut molestiae unde laborum numquam illo! Nesciunt mollitia quos molestiae nam.</p>
        </div>
        <div>
          <b-card-group deck >
              <b-card class="features-card">
                  <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                  <h2>BRONCE</h2>
                  <h3 class="features-card_price">$2,000</h3>
                  <p class="features-card_text">
                      This is a wider card with supporting text below as a
                      natural lead-in
                  </p>
                  <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
              </b-card>
            <b-card class="features-card">
                  <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                  <h2>BRONCE</h2>
                  <h3 class="features-card_price">$2,000</h3>
                  <p class="features-card_text">
                      This is a wider card with supporting text below as a
                      natural lead-in
                  </p>
                  <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
              </b-card>
              <b-card class="features-card">
                  <img src="@/assets/img/bronce.png" alt="" class="features-card_img">
                  <h2>BRONCE</h2>
                  <h3 class="features-card_price">$2,000</h3>
                  <p class="features-card_text">
                      This is a wider card with supporting text below as a
                      natural lead-in
                  </p>
                  <img src="@/assets/img/bronce_icon.png" alt="" class="features-card_icon">
              </b-card>
          </b-card-group>
        </div>
      </div>
    </section> -->

    <!-- <div class="newsletter">
      <div class="container">
        <h1 class="newsletter-title">Subscribe for Our Newsletter</h1>
        <p class="newsletter-subtext">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque soluta ducimus porro vel aperiam quos dicta hic excepturi alias. Omnis similique beatae nam unde. Recusandae asperiores porro minus sapiente et?</p>
        <input class="newsletter-input" type="text" placeholder="your email here">
        <b-btn class="newsletter-btn">
          <span class="newsletter-text"> Subscribe</span>
        </b-btn>
      </div>
    </div> -->



        <section class="contact__container">
        <div class="contact_form"> 
            <div class="container text-center">
                <h1 class="col-12 text-center mb-5">{{contactLabel[currentLocale]}}</h1>
                <p>{{contactText[currentLocale]}}</p>
                </br>
                <h2> info@empirebcluster.com</h2>

                <!-- <b-form-group inline class="contact_form-group"  label-for="elementsAppend" >
                    <b-input-group>
                    <b-form-input v-model="form.email"placeholder="EMAIL" type="text">
                    </b-form-input>
                    </b-input-group>
                </b-form-group>
                <b-form-group v-model="form.name"class="contact_form-group" label-for="elementsAppend" >
                    <b-input-group>
                    <b-form-input placeholder="NAME"  type="text" ></b-form-input>
                    </b-input-group>
                </b-form-group>
                <b-form-group class="contact_form-group"  label-for="elementsAppend" >
                    <div data-aos="fade-up" class="form-right">
                        <label>MESSAGE</label>
                        <textarea rows="8" cols="40" v-model="form.message"></textarea>
                    </div>
                </b-form-group>
                <div class="col-6 contact_form-group contact_form-submit" label-for="elementsAppend" >
                    <button class="contact_form-button">
                    <span class="contact_form-button-text">Enviar </span>
                    </button>
                </div> -->
            </div>
        </div>
    </section>


    <!-- <Contact/> -->
    <Footer/>
  </div>
</template>

<script>
import axios from 'axios'

import Header from '@/components/Header'
import Footer from '@/components/Footer'
import Contact from '@/views/Contact/Contact'
import config from '@/config/settings'
import { serverBus } from '@/main'


export default {
  name: 'Home',
  components: {
    Footer,
    Header,
    Contact
  },

  data(){
      return{
          form: {
            email: '',
            name: '',
            message: null
            },
            show: true,
            api: 'https://api.tzuru.com/api/v1/store/91f6eb0d-fc05-4c99-a744-336f29ecbe40/client/forms?type=contact',
    
        
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
        },
        ctaBtn: {
            eng: 'Register Today!',
            esp: 'Registrate Hoy!'
        },
        aboutLabel: {
            eng: 'ABOUT US',
            esp: 'SOBRE NOSOTROS'
        },
        ctaBtn: {
            eng: 'Register Today!',
            esp: 'Registrate Hoy!'
        },
        aboutLabel: {
            eng: 'ABOUT US',
            esp: 'SOBRE NOSOTROS'
        },
         aboutText1: {
          eng: 'Empire Business Cluster, is a global and independent investment company, formed by an expert team in both virtual and physical stock markets and specialized in the cryptocurrency market, focused on BitCoin (BTC), LiteCoin (LTC) and DogeCoin ( DOGE).',
          esp: 'Empire Business Cluster, es una compañía de inversiones global e independiente, formada por un equipo de trabajo experto en mercados bursátiles tanto virtuales como físicos y especializados en el mercado de las criptomonedas, enfocados en BitCoin (BTC), LiteCoin (LTC) y DogeCoin (DOGE).'
        },
        aboutText2: {
          eng: 'We offer each investor the opportunity to generate stable profits, without taking risks due to lack of knowledge and training.',
          esp: 'Ofrecemos a cada inversionista la oportunidad de generar ganancias estables, sin asumir riesgo por falta de conocimiento y capacitación.'
        },
        aboutText3: {
          eng: 'Empire Business Cluster not only operates in the cryptocurrency trade, but also works with one of the most traded jokers in the world such as coffee, mixing a variety of investments in: Caffe Bars (Coffee Shop), restaurants and an Ecommerce. The perfect combination of the economy of the future and the traditional one.',
          esp: 'Empire Business Cluster no solo opera en el comercio de criptomonedas, sino que a su vez trabaja con uno de los comodines más transados en el mundo como lo es el café, mezclando una variedad de inversiones en: Barras de Caffe (Coffee Shop), restaurantes y un Ecommerce. La combinación perfecta de la economía del futuro y la tradicional.'
        },
        aboutText4: {
          eng: 'We want to help you maintain and increase your capital in a safe manner, minimizing the risks.',
          esp: 'Queremos ayudarte a mantener y aumentar tu capital de manera segura, minimizando los riesgos.'
        },
        investmentLabel:{
            eng: 'INVESTMENT PLANS',
            esp: 'PLANES DE INVERSION'
        },
        packetsLabel: {
            eng: 'Packs',
            esp: 'Paquetes'
        },
        packetsSubText: {
            eng: 'Register now and start earning profits with cryptocurrencies',
            esp: 'Regístrese ahora y comience a obtener ganancias con criptomonedas.'
        },
        packetsText1: {
            eng: 'Monday to Friday payouts',
            esp: 'Pagos de lunes a viernes'
        },
        packetsText2: {
            eng: 'Gain 150% of your investment',
            esp: 'Gana el 150% de tu inversión.'
        },
        packetsText3: {
            eng: 'Gain 160% of your investment',
            esp: 'Gana el 160% de tu inversión.'
        },
        contactLabel: {
            eng: 'CONTACT US',
            esp: 'CONTACTO'
        },
         contactText: {
            eng: 'Any questions please email us at: ',
            esp: 'Cualquier pregunta favor enviarnos un correo: '
        },
      }
  },

  methods:{
       openNav() {
      document.getElementById("myNav").style.width = "450px"
    },

    closeNav() {
      document.getElementById("myNav").style.width = "0"
    },

    onSubmit (evt) {
      evt.preventDefault();
      this.loading = true
      axios.post(this.api, this.form)
      .then(response => {
        this.$toasted.show('Contact form sent', { 
          position:'top-right',
          duration: 5000,
          type: 'success'
        })
        this.onReset(evt)
        this.loading = false
      })
      .catch((error) => {
        this.$toasted.show(error.response.data.m, {
          position:'top-right', 
          duration: 5000,
          type: 'error'
        })
        this.loading = false
      })
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