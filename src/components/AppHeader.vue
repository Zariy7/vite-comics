<script>
    export default {
        name: 'AppHeader',
        data(){
            return{
                menu:[
                    'CHARACTERS',
                    'COMICS',
                    'MOVIES',
                    'TV',
                    'GAMES',
                    'COLLECTIBLES',
                    'VIDEOS',
                    'FANS',
                    'NEWS',
                    'SHOP'
                ]
            };
        }
    }
</script>

<template>
    <header>
        <div>
            <img src=".././assets/img/dc-logo.png">
            <ul>
                <li v-for="item, index in menu" :key="index">
                    {{ item }}
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header{
    div{
        margin: 0 auto;
        max-width: 60%;
        display: flex;
        justify-content: space-between;

        img{
            width: 100px;
            height: 100px;
            margin: 1rem;
        }
        
        ul{
            display: flex;
            list-style-type: none;
            
            li{
                margin: 50px 5px;
            }

            li:hover{
                border-bottom: 3px solid blue;
            }
        }
    }
}
</style>
