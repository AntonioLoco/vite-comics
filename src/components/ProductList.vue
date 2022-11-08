<script>
export default{
    name: "ProductList",
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
    <main>
        <section class="product">
            <div class="container">
                <div class="product-list">
                    <h2>--> Content goes here &lt;-- </h2>
                </div>
            </div>
        </section>

        <section class="icons-banner">
            <div class="container">
                <ul>
                    <li v-for="link in navigationLinks">
                        <img :src="getImagePath(link.urlImage)" :alt="link.name">
                        <a href="">{{link.name.toUpperCase()}}</a>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

main{
    color: #fff;
    .product{
        background-color: $secondary-color;
        .product-list{
            padding: 2em 0;
        }
    }

    .icons-banner{
        background-color: $primary-color;

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

}

</style>