<template>
    <div>
        <img :src="require(`../../../assets/img/${column[i].img}`)" :alt="`${column[i].title}`">
        <h3>{{column[i].title}}</h3>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Mollitia eaque facere fugit debitis vero voluptatibus voluptatem, ratione reiciendis officia. </p>
    </div>
</template>

<script>
    export default {
        name: 'Services',
        props: {
            column: Array,
            i: Number,
        },
    }
</script>

<style scoped lang="scss">
    div {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 25%;
        img {
            width: 15%;
        }
        h3 {
            color: #ae8652;
            font-size: 22px;
            margin: 20px 0;
        }
        p {
            color: #b0b0b0;
            text-align: center;
            width: 90%;
        }
    }
</style>