<template>
    <div class="home-gallery">
        <h2>El taller</h2>
        <div class="gallery">
            <img src="../assets/img/home-swiper/swiper-2-tablet.png" class="item-1"/>
            <img src="../assets/img/home-swiper/swiper-2-tablet.png" class="item-2"/>
            <img src="../assets/img/home-swiper/swiper-2-tablet.png" class="item-3"/>
        </div>
        

    </div>
</template>

<style scoped>
.gallery{
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-auto-rows: 0.5fr;
    margin: 1.5rem 10rem;
    column-gap: 0.5rem;
    row-gap: 0.5rem;
}

.gallery img{
    width: 100%;
    height: auto;
    border-radius: 5px;
}

.item-1 {
  grid-column-start: 1;
  grid-column-end: 4;
  grid-row-start: 1;
  grid-row-end: 3;
}
</style>