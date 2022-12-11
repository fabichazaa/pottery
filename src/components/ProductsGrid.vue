<template>
    <!-- TODO: in mobile show only 6 -->
    <!-- TODO: add button to go directly to catalog -->
    <div class="product-grid">
        <div class="products">
            <div v-for="product in products" :key="product.id" class="product">
                <img :src="require('../assets/img/products-square/' + product.src[0])" alt="" class="prodcut-img"/>
                <div class="product-data">
                    <div class="product-name">
                        <h3>{{product.name}}</h3>
                        <h4>{{product.type}}</h4>
                    </div>
                    <h3 class="product-price">${{product.price}}</h3>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    data() {
        return {
            products: [
            {
                id: 1,
                name: 'Zebra Print',
                type: 'Vajilla',
                keywords: ['cuenco', 'vajilla', 'zebra', 'negro'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['1-1.png', '1-2.png']
            },
            {
                id: 2,
                name: 'Nubecitas',
                type: 'Vajilla',
                keywords: ['cuenco', 'vajilla', 'nube', 'negro', 'celeste', 'acuarela'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['2-1.png', '2-2.png']
            },
            {
                id: 3,
                name: 'Baile de Plumas',
                type: 'Vajilla',
                keywords: ['cuenco', 'vajilla', 'plumas', 'negro'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['3-1.png', '3-2.png']
            },
            {
                id: 4,
                name: 'Sandía Mug',
                type: 'Taza',
                keywords: ['taza', 'rojo', 'roja', 'verde', 'sandia', 'verano'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['4-1.png', '4-2.png']
            },
            {
                id: 5,
                name: 'Chanchi',
                type: 'Taza',
                keywords: ['taza', 'rosa', 'animal', 'kids', 'chicos', 'rosado', 'chancho', 'chanchito'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['5-1.png']
            },
            {
                id: 6,
                name: 'Patitas de Liebre ',
                type: 'Taza',
                keywords: ['taza', 'kids', 'naranja'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['6-1.png', '6-2.png']
            },
            {
                id: 7,
                name: 'Color Pop',
                type: 'Taza',
                keywords: ['taza', 'arco-iris', 'colorido', 'flores'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['7-1.png', '7-2.png']
            },
            {
                id: 8,
                name: 'Ramitas Navideñas',
                type: 'Plato',
                keywords: ['plato', 'navidad', 'árbol', 'arbol', 'verde'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['8-1.png', '8-2.png']
            },
            {
                id: 9,
                name: 'Ojo de gato',
                type: 'Tazón',
                keywords: ['tazón', 'tazón', 'gato', 'de-lujo'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['9-1.png']
            },
            {
                id: 10,
                name: 'Hello Kitty',
                type: 'Tazón',
                keywords: ['tazón', 'tazon',  'kids', 'rosa', 'blanco'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['10-1.png']
            },
            {
                id: 11,
                name: 'Garritas amarillas',
                type: 'Taza',
                keywords: ['taza', 'amarilla', 'amarillo', 'kids'],
                microwave: 1,
                measures: '2X2',
                price: 123,
                src: ['11-1.png']
            }
        ]
        }
        
    }
    //recieves as prop the filter and the quantity showed
    //default shows x quantity, and loads more when clicking the button
}
</script>

<style scoped>
.product-grid-title{
    font-size: 1.6rem;
    margin-bottom: 1rem;
}

.products{
    display: grid;
    grid-template-columns: repeat(1, 1fr);
}

.product{
    margin: 0.5rem 3rem 0.8rem 3rem;
}

.product-data{
    margin: 0.6rem 0;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    row-gap: 0.8rem;
}

.product-name{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    row-gap: 0.2rem;
}

.product-name h3{
    font-family: 'Lora', serif;
    font-size: 1rem;
    font-weight: 500;
}

.product-name h4{
    font-weight: 500;
    font-size: 0.9rem;
}

.product-price{
    font-family: 'Lora', serif;
    font-size: 1.5rem;
    font-weight: 600;
}

.prodcut-img{
    width: 100%;
    height: auto;
}

@media screen and (min-width: 760px){
    .product-grid-title{
        font-size: 1.6rem;
        margin-top: 3rem;
        margin-bottom: 1.2rem;
    }

    .products{
        grid-template-columns: repeat(3, 1fr);
        margin: 1.6rem 2rem;
    }

    .product{
        margin: 0.5rem 1.5rem 0.8rem 1.5rem;
    }
}

@media screen and (min-width: 1000px){
    .product-grid-title{
        font-size: 2.2rem;
        font-weight: 600;
        margin-top: 4rem;
        margin-bottom: 1.5rem;
    }

    .products{
        column-gap: 0.5rem;
        margin: 1.5rem 6rem;
    }

    .product{
        margin: 0.5rem 1.5rem 0.8rem 1.5rem;
    }
}

@media screen and (min-width: 1400px){
    .product-grid-title{
        font-size: 2.2rem;
        margin-top: 3rem;
        margin-bottom: 1.5rem;
        font-weight: 500;
    }

    .products{
        grid-template-columns: repeat(4, 1fr);
        column-gap: 0.5rem;
        margin: 1.5rem 12rem;
    }

    .product{
        margin: 0.5rem 1.5rem 0.8rem 1.5rem;
    }
}
</style>

