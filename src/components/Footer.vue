<template>
    <div class="footer">
        <div class="footer-grid">
            <div class="footer-column">
                <h4>Gladys Alicia</h4>
                <h5>¡Gracias por visitar nuestra página!</h5>
                <div class="social-media">
                    <a href="#" class="sm-icon"><i class='bx bxl-instagram'></i></a>
                    <a href="#" class="sm-icon"><i class='bx bxl-facebook' ></i></a>
                    <a href="#" class="sm-icon"><i class="bx bxl-whatsapp"></i></a>
                </div>
                <!-- <img src="#" alt="ice-cream-w-spoon" class="footer-img-1"/> -->
            </div>
            <div class="footer-column">
                <h4>Nosotros</h4>
                <h5>Ubicación</h5>
                <h5>FAQ</h5>
            </div>
            <div class="footer-column">
                <h4>Catálogo</h4>
                <h5>Tazones</h5>
                <h5>Tazas</h5>
                <h5>Navidad</h5>
            </div>
            <div class="footer-column">
                <h4>Contacto</h4>
                <h5>gladysaliciapottery@gmail.com</h5>
                <h5>+54 0 11 3453535</h5>
                <!-- <img src="#" alt="ice-cream-w-spoon" class="footer-img-2"/> -->
            </div>
        </div>
        <p class="footer-copyright">© Gladys Alicia Pottery</p>
    </div>
</template>

<style scoped>
.footer{
    position: relative;
    overflow: hidden;
    background-color: var(--beige-cream);
    margin-top: 1rem;
}

.footer-grid{
    margin: 1rem 0 2.2rem 0;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    font-size: 1.2rem;
    padding: 1rem 1.5rem;
    row-gap: 2.2rem;
}

.footer-column{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    row-gap: 0.6rem;
    overflow: hidden;
}

.footer-column h4{
    margin-bottom: 0.2rem;
}

.footer-column h5{
    font-weight: 400;
}

.footer-copyright{
    text-align: center;
    margin-bottom: 1.5rem;
    font-weight: 500;
}

.footer-img-1{
    position: absolute;
    width: 250px;
    right: -33%;
}

.footer-img-2{
    position: absolute;
    width: 160px;
    right: 0%;
}

.social-media{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    column-gap: 1rem;
    margin-top: 0.5rem;
}

.sm-icon{
    color: white;
    background-color: var(--blue);
    padding: 0.3rem 0.4rem;
    border-radius: 4px;
}

@media screen and (min-width: 760px){
    .footer-grid{
        flex-direction: row;
        justify-content: space-around;
        margin: 2rem 3rem 2rem 3rem;
        font-size: 1rem;
    }

    .footer-img-1{
        width: 150px;
        left: -8%;
    }
    
    .footer-img-2{
        width: 150px;
        right: -9%;
    }
}

@media screen and (min-width: 1000px){
    .footer-grid{
        font-size: 1.2rem;
    }
}

</style>
