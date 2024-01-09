<script>
    export default {
        name: 'AppBonus',
        data(){
            return{
                options:[
                    {
                        optionString: 'DIGITAL COMICS',
                        optionImage:  new URL('../assets/img/buy-comics-digital-comics.png', import.meta.url).href,
                    },
                    {
                        optionString: 'DC MERCHANDISE',
                        optionImage:  new URL('../assets/img/buy-comics-merchandise.png', import.meta.url).href
                        
                    },
                    {
                        optionString: 'SUBSCRIPTION',
                        optionImage:  new URL('../assets/img/buy-comics-subscriptions.png', import.meta.url).href
                    },
                    {
                        optionString: 'COMIC SHOP LOCATOR',
                        optionImage:  new URL('../assets/img/buy-comics-shop-locator.png', import.meta.url).href
                    },
                    {
                        optionString: 'DC POWER VISA',
                        optionImage:  new URL('../assets/img/buy-dc-power-visa.svg', import.meta.url).href
                    },
                ]
            };
        }
    }
</script>

<template>
    <div>
        <div class="container">
            <div v-for="option, index in options" :key="index">
                <img :src="option.optionImage" :alt="option.optionString" class="optionImage">
                {{ option.optionString }}
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use './styles/generals.css';

div{
    background-color: cyan;
    .container{
        margin: 0 auto;
        max-width: 60%; 
        display: flex;
        justify-content: space-around;
        align-items: center;

        div{
            padding: 1rem 0;
            width: calc(100% / 5 - 20px);
            font-size: small;
        }
    }
}

.optionImage{
    width: 25%;
}
</style>
