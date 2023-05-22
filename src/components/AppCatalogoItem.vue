<script>
    export default {
        props: {
            "thumb": String,
            "price": String,
            "series": String,
            "type": String,
        }
    }
</script>

<template>
    <div>
        <img :src="thumb" alt="" width="150" height="150">
        <p class="textCatalogo">{{series}}</p>
    </div>
</template>

<style>
.textCatalogo {
    color: white;
    font-size: 8px;
}
</style>