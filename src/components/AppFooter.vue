<script>
export default{
    name: "AppFooter",
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
            ],
            socialLinks: [
                {
                    name: "facebook",
                    href: "/facebook",
                    imgUrl: "../assets/img/footer-facebook.png",
                },
                {
                    name: "twitter",
                    href: "/twitter",
                    imgUrl: "../assets/img/footer-twitter.png",
                },                
                {
                    name: "youtube",
                    href: "/youtube",
                    imgUrl: "../assets/img/footer-youtube.png",
                },                
                {
                    name: "pinterest",
                    href: "/pinterest",
                    imgUrl: "../assets/img/footer-pinterest.png",
                },
                {
                    name: "periscope",
                    href: "/periscope",
                    imgUrl: "../assets/img/footer-periscope.png",
                }
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
    <footer>
        <div class="footer-top">
            <div class="container">
                <div class="navigation-links">
                    <ul v-for="category in navigationLinks">
                        <h3>{{ category.name.toUpperCase() }}</h3>
                        <li v-for="link in category.links"><a :href="link.href">{{ link.name }}</a></li>
                    </ul>
                </div>
                <div class="logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
    
        <div class="footer-bottom">
            <div class="container">
                <div class="button">
                    <button>SIGN-UP NOW!</button>
                </div>
                <div class="social-links">
                    <h3>FOLLOW US</h3>
                    <ul>
                        <li v-for="social in socialLinks">
                            <a :href="social.href">
                                <img :src="getImagePath(social.imgUrl)" :alt="social.name">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.footer-top{
    background-image: url("../assets/img/footer-bg.jpg");
    background-repeat: no-repeat;

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
                // width: calc(100% / 4 - 1em);
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

.footer-bottom{
    background-color: $third-color;
    .container{
        @include flex-center("vertical");
        justify-content: space-between;
        padding: 2em 0;

        .button{
            button{
                padding: 1em;
                color: #fff;
                border: 3px solid $primary-color;
                background-color: $third-color;
            }
        }

        .social-links{
            @include flex-center("vertical");

            h3{
                color: $primary-color;
            }

            ul{
                @include flex-center("vertical");
                margin: 0 1em;

                li{
                    margin: 0 .5em;
                }
            }
        }
    }
}

</style>