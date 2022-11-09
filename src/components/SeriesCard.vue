<script>
export default{
    name: "SeriesCard",
    props: {
        imgUrl: String,
        series: String
    }
}
</script>

<template>
    <div class="card">
        <img :src="imgUrl" alt="">
        <h4>{{series}}</h4>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.card{
    width: calc(100% / 6 - 2em);
    margin: 1em;

    img{
        width: 100%;
        height: 80%;
        object-fit: cover;
        object-position: top;
    }

    h4{
        height: 20%;
        padding: 10px 0;
    }
}
</style>