<script>
    export default {
        name: 'AppBonus',
        data(){
            return{
                dcComics: [
                    'Characters',
                    'Comics',
                    'Movies',
                    'TV',
                    'Games',
                    'Videos',
                    'News'
                ],
                shop: [
                    'Shop DC',
                    'Shop DC Collectibles'
                ],
                dcCompany: [
                    'Terms of Use',
                    'Privacy Policy (New)',
                    'Ad Choices',
                    'Advertising',
                    'Jobs',
                    'Subscriptions',
                    'Talent Workshops',
                    'CPCS Certificates',
                    'Ratings',
                    'Shop Help',
                    'Contact Us',
                ],
                sites: [
                    'DC',
                    'MAD Magazine',
                    'DC Kids',
                    'DC Universe',
                    'DC Power Visa'
                ]
            }
        }
    }
</script>

<template>
    <footer>
        <div class="dc-background">
            <div class="container">
                <div>
                    <h3 class="menu-title">DC COMICS</h3>
                    <ul>
                        <li v-for="option, index in dcComics" :key="index">
                            <span class="menu-option">
                                {{ option }}
                            </span>
                        </li>
                    </ul>
    
                    <h3 class="menu-title">SHOP</h3>
                    <ul>
                        <li v-for="option, index in shop" :key="index">
                            <span class="menu-option">
                                {{ option }}
                            </span>
                        </li>
                    </ul>
                </div>
    
                <div>
                    <h3 class="menu-title">DC</h3>
                    <ul>
                        <li v-for="option, index in dcCompany" :key="index">
                            <span class="menu-option">
                                {{ option }}
                            </span>
                        </li>
                    </ul>
                </div>
    
                <div>
                    <h3 class="menu-title">SITES</h3>
                    <ul>
                        <li v-for="option, index in sites" :key="index">
                            <span class="menu-option">
                                {{ option }}
                            </span>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="dc-logo-div">
                <img src=".././assets/img/dc-logo-bg.png" class="dc-logo-bg">
            </div>
        </div>

        <div class="container">
            <div class="sign-up-btn">
                SIGN UP NOW!
            </div>
            
            <div class="d-flex">
                <div class="follow-btn">
                    FOLLOW US
                </div>
                <div>
                    <img src=".././assets/img/footer-facebook.png">
                </div>
                <div>
                    <img src=".././assets/img/footer-twitter.png">
                </div>
                <div>
                    <img src=".././assets/img/footer-youtube.png">
                </div>
                <div>
                    <img src=".././assets/img/footer-pinterest.png">
                </div>
                <div>
                    <img src=".././assets/img/footer-periscope.png">
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '.././styles/generals.scss';
@use '.././styles/partials/variables' as *;

footer{
    background-color: rgb(59, 59, 59);

    .dc-background{
        background-image: url(".././assets/img/footer-bg.jpg");
        display: flex;

        .dc-logo-div{
            height: 400px;
            .dc-logo-bg{
                max-height: 100%;
                object-fit: contain;
            }
        }
    }

    .sign-up-btn{
        margin: 15px;
        padding: 10px;
        border: 3px solid $primary_color;
        color: white;
    }

    .follow-btn{
        font-style: bolder;
        font-size: 1.5rem;
        color: $primary_color;
    }

    img{
        margin: 5px;
    }
}
.container{
    display: flex;
    margin: 0 auto;
    max-width: 60%;
    justify-content: space-between;

    .menu-title{
        font-size: larger;
        color: white;
        margin: 10px 0px;
    }
    
    .menu-option{
        font-size: medium;
        color: gray;
    }
    
    ul{
        padding: 10px 0px;
        list-style-type: none;
    }
}
</style>
