<template>
    <header>
        <div class="header-top">
            <div class="header-top-content">
                <img src="../assets/img/avadabarbers-logo-x1.png" alt="Logo Avada Baebers">
                <div class="header-icons">
                    <i class="fas fa-shopping-cart"></i>
                    <i class="fas fa-bars"></i>
                </div>
            </div>
        </div>
        lorem*100
    </header>
</template>

<script>
    export default {
        name: 'Header',
    }
</script>

<style scoped lang="scss">
    header {
        background-image: url("../assets/img/avadabarbers-homepage-hero-bg.jpg");
        height: 500px;
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
                display: flex;
                justify-content: space-between;
                align-items: center;
                max-width: 1100px;
                margin: 0 auto;
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
    }
</style>