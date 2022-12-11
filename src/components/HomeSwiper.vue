<template>
  <swiper
    :spaceBetween="30"
    :pagination="{
      clickable: true,
    }"
    :autoplay="{ delay: 5000 }"
    class="mySwiper"
  >
    <swiper-slide class="swiper-1 swiper-background-img">
      <img src="../assets/img/home-swiper/swiper-1-mobile.png" class="swiper-img-mobile"/>
        <div class="swiper-text">
            <h1>Pottery lovers</h1>
            <p>¡Te invitamos a desatar la creatividad en nuestras clases! Alocate y realizá piezas únicas de cerámica. Tazas, platos, bandejas y muchas más son las piezas que podes crear y llevarte a casa. ¿Qué estas esperando?</p>
            <a class="button" href="#">¡Quiero anotarme!</a>
        </div>
    </swiper-slide>
    <swiper-slide class="swiper-2 swiper-background-img">
      <img src="../assets/img/home-swiper/swiper-2-mobile.png" class="swiper-img-mobile"/>
        <div class="swiper-text">
            <h1>¡Arcilla, inspiración y acción!</h1>
            <p>No hay nada más lindo que realizar una pieza desde cero con tus propias manos. Pasate por nuestra galeria de fotos para ver los trabajos de nuestras/os alumnas/os.</p>
            <a class="button" href="#">Galería de fotos</a>
        </div>
    </swiper-slide>
    <swiper-slide class="swiper-3 swiper-background-img">
      <img src="../assets/img/home-swiper/swiper-3-mobile.png" class="swiper-img-mobile"/>
      <div class="swiper-text">
          <h1>¡Felices fiestas!</h1>
          <p>¿Estás buscando un regalo para alguien especial? Pasate por nuestro catálogo y encontrá ese obsequio único que estabas buscando. </p>
          <a class="button" href="#">Ir al catálogo</a>
      </div>  
    </swiper-slide>
  </swiper>
</template>

<script>
    // Import Swiper Vue.js components
    import { Swiper } from "swiper/vue/swiper";
    import { SwiperSlide } from "swiper/vue/swiper-slide";
    import SwiperCore, { Navigation, Autoplay, Pagination} from "swiper";
    
    // Import Swiper styles
    import "swiper/swiper.min.css";
    import "swiper/modules/navigation/navigation.min.css";
    import "swiper/modules/autoplay/autoplay.min.css";
    import "swiper/modules/pagination/pagination.min.css";
    SwiperCore.use([Navigation]);
    SwiperCore.use([Autoplay]);
    SwiperCore.use([Pagination]);

    export default {
        components: {
            Swiper,
            SwiperSlide,
        },
    };
</script>

<style scoped>
.swiper-slide {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.swiper-background-img{
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.swiper-img-mobile{
  width: 100%;
  height: auto;
}

.swiper-text-mobile{
  width: 56%;
  padding: 0 1.5rem 0 0;
} 

.swiper-text-mobile h1{
  font-size: 1rem;
}

.swiper-text{
  display: none;
}

@media screen and (min-width: 760px){
  .swiper-slide{
    align-items: normal;
    height: 350px;
  }

  .swiper-background-img{
    box-shadow: none;
  }

  .swiper-1{
    background-image: url('../assets/img/home-swiper/swiper-1-tablet.png');
  }

  .swiper-2{
    background-image: url('../assets/img/home-swiper/swiper-2-tablet.png');
  }

  .swiper-3{
    background-image: url('../assets/img/home-swiper/swiper-3-tablet.png');
  }

  .swiper-text{
    width: 56%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-around;
    padding: 2.8rem 0;
  }

  .swiper-text h1{
    font-size: 1.8rem;
    text-align: left;
  }

  .swiper-text p{
    margin-bottom: 0.5rem;
    margin-right: 2rem;
    text-align: left;
    font-size: 0.9rem;
    font-weight: 500;
    line-height : 1.9rem;
  }

   .swiper-img-mobile{
    display: none;
  }
}

@media screen and (min-width: 1000px){
  .swiper-slide{
    height: 400px;
  }

  .swiper-text{
    width: 50%;
    padding: 3.5rem 0;
  }

  .swiper-text p{
    margin-right: 3.5rem;
    line-height : 2rem;
    font-size: 1rem;
    font-weight: 500;
  }

  .swiper-1{
    background-image: url('../assets/img/home-swiper/swiper-1.png');
  }

  .swiper-2{
    background-image: url('../assets/img/home-swiper/swiper-2.png');
  }

  .swiper-3{
    background-image: url('../assets/img/home-swiper/swiper-3.png');
  }
}

@media screen and (min-width: 1400px){
  .swiper-text{
    padding: 6rem 0;
    row-gap: 2rem;
  }

  .swiper-text h1{
    font-size: 2.2rem;
  }

  .swiper-text p{
    margin-right: 4.5rem;
    line-height : 2.2rem;
    font-size: 1.1rem;
  }
}
</style>
