<script>
export default{
    name: "AppIcons",
    data(){
        return {
            navigationLinks: [
                {
                    name: "digital comics",
                    href: "/digital-comics",
                    urlImage: "../assets/img/buy-comics-digital-comics.png"
                },
                {
                    name: "dc merchandise",
                    href: "/dc-merchandise",
                    urlImage: "../assets/img/buy-comics-merchandise.png"
                },
                {
                    name: "subscription",
                    href: "/subscription",
                    urlImage: "../assets/img/buy-comics-subscriptions.png"
                },
                {
                    name: "comic shop locator",
                    href: "/comic-shop-locator",
                    urlImage: "../assets/img/buy-comics-shop-locator.png"
                },
                {
                    name: "dc power visa",
                    href: "/dc-power-visa",
                    urlImage: "../assets/img/buy-dc-power-visa.svg"
                },
            ]
        }
    },
    methods: {
        getImagePath(imgPath){
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="icons-banner">
        <div class="container">
            <ul>
                <li v-for="(link,index) in navigationLinks" :key="index">
                    <img :src="getImagePath(link.urlImage)" :alt="link.name">
                    <a href="">{{link.name.toUpperCase()}}</a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.icons-banner{
    background-color: $primary-color;
    color: #fff;
    .container{
        padding: 2em 0;

        ul{
            display: flex;
            justify-content: space-between;

            li{
                @include flex-center;
                img{
                    width: 50px;
                }

                a{
                    font-size: .8rem;
                    color: #fff;
                    padding: 0 .5em;
                }
            }
        }
    }
}
</style>