<script>
    export default {
        props:{
            comic: Object,
        }
    }
</script>

<template>
    <div class="comic-col">
        <img :src="`${comic.thumb}`" class="comic-img">
        <div class="comic-title">
            {{ comic.series }}
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '.././styles/generals.scss';
@use '.././styles/partials/variables' as *;

.comic-col{
    width: calc(100% / 6 - 20px);
}
.comic-img{
    width: 150px;
    height: 150px;
    object-fit: cover;
}

.comic-title{
    text-transform: uppercase;
    font-style: bold;
    color: white;
}
</style>
