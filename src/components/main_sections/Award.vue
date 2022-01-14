<template>
    <section>
    <div class="award">
        <span>award winnig</span>
        <h2>Pro Barbers</h2>
        <button class="meet-barber">meet your barber</button>
    </div>
    <svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="100%" height="100" viewBox="0 0 100 100" preserveAspectRatio="none" style="padding:0;" fill="rgba(255,255,255,1)"><path d="M0 100 L50 2 L100 100 Z"></path></svg>
    </section>
</template>

<script>
    export default {
        name: "Award",
    }
</script>

<style scoped lang="scss">
    section {
        background-image: url("../../assets/img/avadabarbers-about-introbackground.jpg");
        background-size: cover;
        padding: 100px 0 0;
        .award {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-bottom: 60px;
            h2 {
                font-family: 'Abril Fatface', cursive;
                font-size: 70px;
                color: #b0b0b0;
            }
            span, button {
                font-family: 'Lato', sans-serif;
                color: #ffcf6a;
                text-transform: uppercase;
                opacity: 0.8;
            }
            button {
                width: fit-content;
                margin: 25px;
                padding: 10px 35px;
                text-transform: uppercase;
                background-color: rgba(0, 0, 0, 0);
                border: none;
                border: 2px solid #ffcf6a;
                cursor: pointer;
                opacity: 0.7;
            }
            button:hover {
                opacity: 0.5;
            }
        }
        svg {
            position: relative;
            bottom: -4px;
        }
    }
</style>