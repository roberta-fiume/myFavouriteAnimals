<template>
    <div>
        <div class="img-cont">
            <img :src="images.cat"/>
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