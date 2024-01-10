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
                <li v-for="item, index in menu" :key="index" :class="index == 1 ? 'active' : ''">
                    <div>
                        {{ item }}
                    </div>
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '.././styles/generals.scss';

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
                div{
                    padding: 50px 0;
                    margin: 0 5px;
                    height: 100%;
                }

                &.active{
                    border-bottom: 3px solid blue;
                }
            }

            li:hover{
                border-bottom: 3px solid blue;
            }
        }
    }
}
</style>
