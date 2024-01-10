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
            <div v-for="option, index in options" :key="index" class="container">
                <div class="w-50">
                    <img :src="option.optionImage" :alt="option.optionString">
                </div>
                <div class="w-50">
                    {{ option.optionString }}
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '.././styles/generals.scss';
@use '.././styles/partials/variables' as *;

div{
    background-color: $primary_color;
    .container{
        margin: 0 auto;
        max-width: 60%; 
        display: flex;
        justify-content: space-around;
        align-items: center;

        img{
            max-width: 75px;
            max-height: 75px;
            margin: 10px 0;
        }
    }
}
</style>
