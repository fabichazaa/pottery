<template>
    <nav class="nav">
        <div id="nav-title" class="nav-title dancing-script bolder">
            Gladys Alicia
        </div>
        <div class="nav-menu-background" id="nav-menu-background" v-on:click="closeMenu">
        </div>
        <div class="nav-menu" id="nav-menu">
            <i id="nav-menu-close" class='bx bx-x nav-menu-close' v-on:click="closeMenu"></i>
            <div class="nav-menu-title dancing-script bold">
                Gladys Alicia
            </div>
            <div class="nav-search-mobile">
                <input type="text" placeholder="Buscar..."/>
                <i class='bx bx-search' ></i>
            </div>
            <ul class="nav-links">
                <li>
                    <a href="#" class="nav-item nav-selected"><i class='bx bx-home nav-icon'></i>Inicio</a>
                </li>
                <li>
                    <a href="#" class="nav-item"><i class='bx bxs-book nav-icon'></i>Catálogo</a>
                </li>
                <li>
                    <a href="#" class="nav-item"><i class='bx bx-paint nav-icon'></i>Talleres</a>
                </li>
                <li>
                    <a href="#" class="nav-item"><i class='bx bxs-map nav-icon'></i>Ubicación</a>
                </li>
                <li>
                    <a href="#" class="nav-item"><i class='bx bx-envelope nav-icon' ></i>Contacto</a>
                </li>
            </ul>
            <ul class="nav-social-media">
                <li><a href="#"><i class='bx bxl-instagram nav-social-media-icon'></i></a></li>
                <li><a href="#"><i class='bx bxl-facebook-square nav-social-media-icon' ></i></a></li>
                <li><a href="#"><i class='bx bxl-whatsapp nav-social-media-icon' ></i></a></li>
            </ul>
        </div>
        <i id="nav-toggle" class='bx bx-menu nav-toggle' v-on:click="openMenu"></i>
    </nav>
</template>

<script>

export default ({
    methods: {
        openMenu(){
            document.getElementById('nav-menu').classList.add('show-nav-menu');
            document.getElementById('nav-menu-background').classList.add('display');
        },
        closeMenu(){
            document.getElementById('nav-menu').classList.remove('show-nav-menu');
            document.getElementById('nav-menu-background').classList.remove('display');
        }
    }
})
</script>

<style scoped>
.nav{
    display: flex;
    flex-direction: row-reverse;
    justify-content: space-between;
    align-items: center;
    column-gap: 0.6rem;
    padding: 1.2rem 1.5rem;
    background-color: white;
    font-size: 0.9rem;
    font-weight: 500;
}

@media screen and (max-width: 760px){
    .nav-menu{
        position: fixed;
        display: flex;
        flex-direction: column;
        row-gap: 2.5rem;
        background-color: #e2dfda;
        height: 100%;
        border-radius: 0 0 0.3rem 0.3rem;
        padding: 3rem 1.5rem 2rem 1.5rem;
        transition: .3s;
        top: 0;
        left: -150%;
        box-shadow: 10px 0px 15px -10px rgba(0,0,0,0.1);
        z-index: 100;
    }
}

.show-nav-menu{
    left: 0;
}

.nav-menu-background{
    position: fixed;
    height: 100%;
    width: 100%;
    top: 0; 
    left:0;
    display: none;
    z-index: 99;
}

.nav-toggle{
    font-size: 1.25rem;
    transition: .3s;
}

.nav-menu-close{
    position: absolute;
    right: 0;
    top: 0;
    margin: 1rem;
    font-size: 1.5rem;
}

.nav-title{
    font-size: 1.2rem;
    transition: .3s;
}

.nav-title-hide{
    color: transparent;
}

.nav-menu-title{
    font-size: 1.5rem;
}

.nav-search-mobile{
    display: flex;
    align-items: center;
    column-gap: 0.6rem;
}

.nav-search-mobile input{
    font-size: 0.9rem;
    background: none;
    border-bottom: 0.05rem solid var(--dark-blue);
    padding: 0.5rem 0;
}

.nav-item,
.nav-search-mobile input::placeholder,
.nav-social-media-icon{
  color: var(--dark-blue);
}

.nav-links{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    row-gap: 1.4rem;
    font-weight: 500;
    font-size: 1rem;
}

.nav-item{
    display: flex;
    align-items: center;
    column-gap: 0.8rem;
}

.nav-icon{
    font-size: 1rem;
}

.nav-social-media{
    margin-top: 1rem;
    display: flex;
    column-gap: 2rem;
    align-self: center;
    color: var(--dark-blue);
}

.nav-social-media i{
    font-size: 1.4rem;
}
.nav-search{
    display: none;
}

.display{
    display: inline;
}

.display-none{
    display: none;
}

@media screen and (min-width: 760px){
    .nav-toggle,
    .nav-menu-title,
    .nav-search-mobile,
    .nav-social-media,
    .nav-menu-close, 
    .nav-icon{
        display: none;
    }

    .nav-search{
        display: inherit;
    }

    .nav{
        flex-direction: column;
        align-items: normal;
        row-gap: 1.5rem;
        padding: 1.5rem 3rem 1rem 3rem;
    }

    .nav-title{
        font-size: 1.6rem;
    }

    .nav-menu{
        display: flex;
        flex-direction: row;
        justify-content: space-around;
    }

    .nav-links{
        font-weight: bold;
        display: flex;
        flex-direction: row;
        column-gap: 1.6rem;
    }

    .nav-item{
        padding-bottom: 0.1rem;
    }

    .nav-selected{
        border-bottom: 0.1rem solid var(--dark-blue);
    }
    
    .nav-search input:focus{
        border-bottom: 0.05rem solid black;
        transition: .3s;
    }
}

@media screen and (min-width: 1000px){
    .nav-title{
        font-size: 1.8rem;
    }
}
</style>