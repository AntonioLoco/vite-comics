<script>
export default{
    name: "FooterSocial",
    data(){
        return {
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
    <div class="footer-social">
        <div class="container">
            <div class="button">
                <button>SIGN-UP NOW!</button>
            </div>
            <div class="social-links">
                <h3>FOLLOW US</h3>
                <ul>
                    <li v-for="(social,index) in socialLinks" :key="index">
                        <a :href="social.href">
                            <img :src="getImagePath(social.imgUrl)" :alt="social.name">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.footer-social{
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