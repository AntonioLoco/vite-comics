<script>
export default{
    name: "FooterLinks",
    data(){
        return {
            navigationLinks: [
                {
                    name: "dc comics",
                    links: [
                        {
                            name: "Characters",
                            href: "/characters"
                        },
                        {
                            name: "comics",
                            href: "/comics"
                        },
                        {
                            name: "tv",
                            href: "/tv"
                        },
                        {
                            name: "games",
                            href: "/games"
                        },
                        {
                            name: "videos",
                            href: "/videos"
                        },
                        {
                            name: "news",
                            href: "/news"
                        },
                    ]
                },
                {
                    name: "Shop",
                    links: [
                        {
                            name: "shop Dc",
                            href: "/shopDc"
                        },
                        {
                            name: "shop Dc Collectibles",
                            href: "/shopDcCollectibles"
                        },
                        {
                            name: "shop Dc",
                            href: "/shopDc"
                        },
                        {
                            name: "shop Dc Collectibles",
                            href: "/shopDcCollectibles"
                        },
                        {
                            name: "shop Dc",
                            href: "/shopDc"
                        },
                        {
                            name: "shop Dc Collectibles",
                            href: "/shopDcCollectibles"
                        },
                        {
                            name: "shop Dc",
                            href: "/shopDc"
                        },
                        {
                            name: "shop Dc Collectibles",
                            href: "/shopDcCollectibles"
                        }
                    ]
                },
                {
                    name: "dc",
                    links: [
                        {
                            name: "Characters",
                            href: "/characters"
                        },
                        {
                            name: "comics",
                            href: "/comics"
                        },
                        {
                            name: "tv",
                            href: "/tv"
                        },
                        {
                            name: "games",
                            href: "/games"
                        },
                        {
                            name: "videos",
                            href: "/videos"
                        },
                        {
                            name: "news",
                            href: "/news"
                        },
                    ]
                },
                {
                    name: "sites",
                    links: [
                        {
                            name: "Characters",
                            href: "/characters"
                        },
                        {
                            name: "comics",
                            href: "/comics"
                        },
                        {
                            name: "tv",
                            href: "/tv"
                        },
                        {
                            name: "games",
                            href: "/games"
                        }
                    ]
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
    <div class="footer-links">
        <div class="container">
            <div class="navigation-links">
                <ul v-for="(category,index) in navigationLinks" :key="index">
                    <h3>{{ category.name.toUpperCase() }}</h3>
                    <li v-for="(link, secondaryIndex) in category.links" :key="secondaryIndex"><a :href="link.href">{{ link.name }}</a></li>
                </ul>
            </div>
            <div class="logo">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.footer-links{
    background-image: url("../assets/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;

    .container {
        display: flex;
        position: relative;
        overflow: hidden;

        .navigation-links{
            width: 40%;
            display: flex;
            flex-wrap: wrap;
            padding: 2em 0;    

            ul{
                width: calc(100% / 4 - 1em);
                margin: 0 1em;

                h3{
                    font-size: 1rem;
                    color: #fff;
                }

                li{
                        margin: .5em 0;

                        a{
                            font-size: .8rem;
                            color: #999999;
                        }
                }
            }
        }

        .logo{
            width: 60%;
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
            display: flex;
            justify-content: flex-end;
        }

    }

}
</style>