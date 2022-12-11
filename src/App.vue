<template>
  <NavBar />
  <HomeSwiper />
  <HomeLinkCards />
  <ProductsGrid />
  <HomeGallery />
  <Footer />
</template>

<script>
import NavBar from './components/NavBar.vue';
import HomeSwiper from './components/HomeSwiper.vue';
import HomeLinkCards from './components/HomeLinkCards.vue';
import ProductsGrid from './components/ProductsGrid.vue';
import Footer from './components/Footer.vue';
import HomeGallery from './components/HomeGallery.vue';
export default {
  name: 'App',
  components: {
    NavBar,
    HomeSwiper,
    HomeLinkCards,
    ProductsGrid,
    HomeGallery,
    Footer
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&family=Lora:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Quicksand:wght@300;400;500;600;700&display=swap');

:root{
  /* COLORS */
  --dark-blue: #303c4c;
  --blue: #2f496e;
  --beige-cream: #faf5f1;
  --beige-cream-darker: #faf5f1;
}

#app {
  font-family: 'Quicksand', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--dark-blue);
}

ul{
  list-style: none;
}

a{
  text-decoration: none;
  color: black;
}

*{
  margin: 0;
  padding: 0;
}

input{
  border: none;
  outline: none;
}

input::placeholder{
  font-family: 'Quicksand', sans-serif;
}

.swiper-pagination-bullet-active{
  background: white;
}

@media screen and (min-width: 760px){
  .swiper-pagination-bullet-active{
    background: #303c4cb5;
  }
}

::-webkit-scrollbar{
    width: 0.6rem;
    background: #f4eee9;
}

::-webkit-scrollbar-thumb{
    background: #d4cec7;
}


/*REUSABLES */
.display-none{
  display: none;
}

.display{
  display: inline;
}

.dancing-script{
  font-family: 'Dancing Script', cursive;
}

.lora{
  font-family: 'Lora', cursive;
}

.bold{
  font-weight: bold;
}

.bolder{
  font-weight: bolder;
}

.button{
  color: white;
  background-color: var(--dark-blue);
  padding: 0.5rem 3rem;
}

.button:hover,
.button:focus{
  background-color: var(--blue);
}

@media screen and (min-width: 1000px){
  .button{
    font-size: 1.1rem;
    padding: 0.5rem 3rem;
  }
}

</style>
