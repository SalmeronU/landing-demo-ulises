<template>
  <div class="home">
    <video-bg
    :sources="[require('@/assets/videobg.mp4')]">
      <!-- Row centrado titulo -->
      <v-row justify="center">
        <v-col lg="8">
          <h1 class="tituloSlogan">
            El lugar favorito de tu hogar
          </h1>
        </v-col>
      </v-row>

      <!-- row centrado subtitulo -->
      <v-row justify="center">
        <v-col lg="8">
          <h3 class="subtituloSlogan">
            Seguimos trabajando para ti. Realiza tus compras en línea 24/7
          </h3>
        </v-col>
      </v-row>

      <!-- row centrado btn -->
      <v-row justify="center">
        <v-btn
        class="mt-5"
        elevation="3"
        color="black"
        :style="{color: 'white', borderRadius: '10px'}"
        >
          Comprar ahora
        </v-btn>
      </v-row>
    </video-bg>

   <first-banner
   :areaSections="areas">
   </first-banner> 
  </div>
</template>

<script>
import VideoBg from 'vue-videobg';
import FirstBanner from '../components/homeBanners/firstBanner.vue';
export default {

  components:{
    VideoBg,
    FirstBanner
    },
    data(){
      return{
        areas:[
          {name:'Dormitorios',img:'https://www.osgohome.com/website-images/homepage/2021/bedroom-homepage.png'},
          {name:'Comedores',img:'https://www.osgohome.com/website-images/homepage/2021/diningroom3.png'},
          {name:'Salas',img:'https://www.osgohome.com/website-images/homepage/2021/livingroom-homepage3.png'},
          {name:'Bar y Recreativo',img:'https://www.osgohome.com/website-images/homepage/2021/bar-homepage.png'},
          {name:'Decoración',img:'https://www.osgohome.com/website-images/homepage/2021/decor-homepage.png'},
          {name:'Niños y Jovenes',img:'https://www.osgohome.com/website-images/homepage/2021/kids-homepage.png'},
          {name:'Mascotas',img:'https://www.osgohome.com/website-images/homepage/2021/pets-homepage.png'}
          ]
      };
    }
}
</script>


<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

  .tituloSlogan{
    font-family: 'Montserrat', sans-serif;
    text-align: center;
    font-size: 4.5rem;
    font-weight: bolder;
    color: white;
    margin-top: 18%
  }

  .subtituloSlogan{
    color: white;
    font-family: 'Montserrat', sans-serif;
    font-weight: 400;
    font-size: 1.5rem;
    text-align: center;
  }
</style>