<template>
    <div class="home-link-cards">
        <div class="home-link-card card-1">
            <div class="home-link-card-text">
                <h2>Vajillas</h2>
                <p>Armá tu conjunto</p>
            </div>
        </div>
        <div class="home-link-card card-2">
            <div class="home-link-card-text">
                <h2>Portavelas</h2>
                <p>Deco iluminadora</p>
            </div>
        </div>
        <div class="home-link-card card-3">
            <div class="home-link-card-text">
                <h2>KIDS</h2>
                <p>Para los más peques</p>
            </div>
        </div>
    </div>
</template>

<script>

</script>

<style scoped>
.home-link-cards{
    display: flex;
    flex-direction: column;
    row-gap: 1rem;
    margin: 2rem 2rem 3rem 2rem;
}

.home-link-card{
    background-color: red;
    height: 8rem;
    border-radius: 0.5rem;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
}

.home-link-card-text{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    row-gap: 0.8rem;
    margin: 1.2rem 1.5rem 0 1.5rem;
}

.home-link-card-text p{
    border-bottom: 0.05rem solid var(--dark-blue);
}

.card-1{
    background-image: url('../assets/img/home-link-cards/home-link-card-1.webp');
}

.card-2{
    background-image: url('../assets/img/home-link-cards/home-link-card-2.webp');
}

.card-3{
    background-image: url('../assets/img/home-link-cards/home-link-card-3.webp');
}

@media screen and (min-width: 380px){
    .home-link-card{
        height: 9rem;
    }
}

@media screen and (min-width: 450px){
    .home-link-card{
        height: 11rem;
    }
}

@media screen and (min-width: 450px){
    .home-link-card{
        height: 14rem;
    }
}


@media screen and (min-width: 760px){
    .home-link-cards{
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        column-gap: 1rem;
        margin: 2rem 2rem;
    }

    .home-link-card{
        height: 8rem;
        width: 100%;
    }

    .home-link-card-text{
        row-gap: 0.6rem;
        margin: 1rem 1.2rem 0 1.2rem;
    }
    
    .home-link-card-text h2{
        font-size: 1.2rem;
    }
    
    .home-link-card-text p{
        font-size: 0.8rem;
    }
}

@media screen and (min-width: 1000px){
    .home-link-cards{
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        column-gap: 1rem;
        margin: 2rem 6rem;
    }

    .home-link-card{
        height: 10rem;
    }
}

@media screen and (min-width: 1400px){
    .home-link-cards{
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        column-gap: 1rem;
        margin: 3rem 13rem;
    }

    .home-link-card{
        height: 12rem;
    }

    .home-link-card-text h2{
        font-size: 1.5rem;
    }
    
    .home-link-card-text p{
        font-size: 1.1rem;
    }
}

</style>