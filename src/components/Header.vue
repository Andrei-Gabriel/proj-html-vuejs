<template>
    <header>
        <div class="header-top">
            <div class="header-top-content content">
                <img :src="require(`../assets/img/${smLogo}`)">
                <div class="header-icons">
                    <i class="fas fa-shopping-cart"></i>
                    <i class="fas fa-bars"></i>
                </div>
            </div>
        </div>
        <div class="header-main">
            <div class="header-main-content content">
                <div class="header-main-info">
                    <h1>{{headerData.headingOne}}</h1>
                    <hr>
                    <span>{{headerData.sloganHeader}}</span>
                    <button class="header-main-btn">{{headerData.headerTextBtn}}</button>
                </div>
                <img class="header-main-img" :src="require(`../assets/img/${headerData.headerImg}`)" alt="Barber">
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'Header',
        props: {
          smLogo: String,
          headerData: Object,
        },
        // created () {
        //     window.addEventListener('scroll', this.handleScroll);
        // },
        // destroyed () {
        //     window.removeEventListener('scroll', this.handleScroll);
        // },
        // methods: {
        //     handleScroll (event) {
            
        //     }
        // }
    }
</script>

<style scoped lang="scss">
    header {
        background-image: url("../assets/img/avadabarbers-homepage-hero-bg.jpg");
        // Quando scorre height: 100px, fixed, top, left: 0, width: 100%. Non serve margin-top
        .header-top {
            // background-color: #000;
            // // Non ho messo "sticky perché non scorreva oltre l'heaeder"
            // position: fixed;
            // width: 100%;
            // top: 0;
            // left: 0;
            // z-index: 1;
            .header-top-content {
                height: 120px;
                justify-content: space-between;
                align-items: center;
                display: flex;
                .header-icons {
                    width: 70px;
                    display: flex;
                    justify-content: space-between;
                    i {
                        font-size: 24px;
                        color: #fff;
                        cursor: pointer;
                    }
                    .fa-shopping-cart {
                        transition: color 0.5s;
                    }
                    .fa-shopping-cart:hover {
                        color: #ae8d67;
                    }
                }
            }
        }
        .header-main {
            padding-bottom: 150px;
            .header-main-content {
                display: flex;
                align-items: center;
                justify-content: space-between;
                .header-main-info {
                    width: 50%;
                    display: flex;
                    flex-direction: column;
                    h1 {
                        font-size: 80px;
                        font-family: 'Abril Fatface', cursive;
                        color: #fff;
                    }
                    hr {
                        color: #ffcf6a;
                        width: 40%;
                        height: 3px;
                        background-color: #ffcf6a;
                        margin: 20px 0;
                    }
                    span {
                        color: #505050;
                        font-size: 18px;
                        font-family: 'Lato', sans-serif;
                        margin: 10px 0 30px;
                        display: inline-block;
                    }
                    .header-main-btn {
                        width: fit-content;
                        padding: 10px 35px;
                        text-transform: uppercase;
                        color: #ffcf6a;
                        background-color: rgba(0, 0, 0, 0);
                        border: none;
                        border: 2px solid #ffcf6a;
                        cursor: pointer;
                        opacity: 0.7;
                    }
                    .header-main-btn:hover {
                        opacity: 0.5;
                    }
                }
                .header-main-img {
                    width: 50%;
                }
            }
        }
    }
</style>
