<template>
    <header>
        <div class="header-content">
            <div class="header-top">
                <img src="../assets/img/avadabarbers-logo-x1.png" alt="Logo Avada Baebers">
                <div class="header-icons">
                    <i class="fas fa-shopping-cart"></i>
                    <i class="fas fa-bars"></i>
                </div>
            </div>
        </div>
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
        .header-content {
            max-width: 1100px;
            margin: 0 auto;
            .header-top {
                height: 100px;
                display: flex;
                justify-content: space-between;
                align-items: center;
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