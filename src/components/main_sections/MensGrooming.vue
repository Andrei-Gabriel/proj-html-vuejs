<template>
    <section class="content">
        <div class="services">
            <span>mens grooming</span>
            <h2>Services</h2>
        </div>
        <div class="list-services">
            <Services v-for="(column, index) in columnData" :key="index" :column="columnData" :i="index"/>
        </div>
        <button>read about services</button>
    </section>
</template>

<script>
    import Services from './subsections/Services.vue'

    export default {
        name: 'MensGrooming',
        components: {
        Services,
        },
        data() {
            return {
                columnData: [
                    {
                        img: "avadabarbers-trimcut-icon-before.png",
                        title: "Trim & Cut"
                    },
                    {
                        img: "avadabarbers-washndry-icon.png",
                        title: "Wash & Dry"
                    },
                    {
                        img: "avadabarbers-beardtrim-icon.png",
                        title: "Beard Tidy"
                    },
                ]
            }
        },
    }
</script>

<style scoped lang="scss">
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-bottom: 55px;
        .services {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            h2 {
                font-family: 'Abril Fatface', cursive;
                font-size: 70px;
                color: #b0b0b0;
            }
            span {
                font-weight: bold;
            }
        }
        span, button {
            font-family: 'Lato', sans-serif;
            text-transform: uppercase;
            color: #ae8652;
            opacity: 0.8;
        }
        button {
            width: fit-content;
            margin: 0 0 25px;
            padding: 10px 35px;
            text-transform: uppercase;
            background-color: rgba(0, 0, 0, 0);
            border: none;
            border: 2px solid #ae8652;;
            cursor: pointer;
            opacity: 0.7;
        }
        button:hover {
            opacity: 0.5;
        }
        .list-services {
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 45px;
        }
    }
</style>