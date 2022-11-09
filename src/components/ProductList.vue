<script>
export default{
    name: "ProductList"
}
</script>

<template>
    <section class="product">
        <div class="container">
            <div class="product-list">
                <h2>--> Content goes here &lt;-- </h2>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.product{
    background-color: $secondary-color;

    .container{
        color: #fff;
        .product-list{
            padding: 2em 0;
        }
    }
}
</style>