<template>
    <div>
        <div class="img-cont">
            <img :src="images.cat" class="img-main"/>
        </div>

    </div>
</template>

<script>
export default {
    data() {
       return {
           images: {
               cat: require("../assets/img/cats.jpg")
           }
        }
    }
}
</script>

<style>
.img-main {
    width: 100%;
    height: auto;
}
</style>