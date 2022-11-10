<script>
export default{
    name: "AppJumbotron",
    props: {
        imgUrl: String,
        nameSection: String
    }
}
</script>

<template>
    <div class="jumbotron">
        <img :src="imgUrl" alt="jumbo photo">
        <div class="container">
            <div class="name-plate">
                <h4>{{nameSection.toUpperCase()}}</h4>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.jumbotron{
    width: 100%;
    height: 250px;

    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }

    .container{
    position: relative;        
        .name-plate{
            padding: .5em 1em;
            background-color: $primary-color;
            color: #fff;
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
        }
    }
}
</style>