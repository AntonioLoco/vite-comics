<script>
export default{
    name: "AppHeader",
    data(){
        return {
            navigations: [
                {
                    name: "characters",
                    href: "/characters",
                    active: false,
                },
                {
                    name: "comics",
                    href: "/comics",
                    active: true,
                },                
                {
                    name: "movies",
                    href: "/movies",
                    active: false,
                },
                {
                    name: "tv",
                    href: "/tv",
                    active: false,
                },
                {
                    name: "games",
                    href: "/games",
                    active: false,
                },
                {
                    name: "collectibles",
                    href: "/collectibles",
                    active: false,
                },
                {
                    name: "videos",
                    href: "/videos",
                    active: false,
                },
                {
                    name: "fans",
                    href: "/fans",
                    active: false,
                },
                {
                    name: "news",
                    href: "/news",
                    active: false,
                },
                {
                    name: "shop",
                    href: "/shop",
                    active: false,
                }
            ]
        }
    }
}
</script>

<template>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="Logo DC Comics">
            </div>
            <nav class="navigation">
                <ul>
                    <li v-for="link in navigations" :class="{'active' : link.active}">
                        <a :href="link.href">{{ link.name.toUpperCase() }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
    <!-- /Header -->

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

header {

    .container{
        @include flex-center("horizontal");
    }
    .logo{
        width: 30%;
        padding: .5em 0;
        @include flex-center("vertical");
    }

    .navigation{
        width: 70%;

        ul{
            height: 100%;
            @include flex-center("horizontal");

            li {
                height: 100%;
                @include flex-center("vertical");
                margin: 0 .5em;
                border-bottom: 5px solid #fff;

                a{
                    color: #000;
                    font-weight: bold;
                    font-size: .8rem;
                }

                &.active{
                    border-bottom: 5px solid $primary-color;
                }
            }
        }
    }
}
</style>