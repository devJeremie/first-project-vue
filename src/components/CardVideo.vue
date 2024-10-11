<template>
    <div>
        <img :src="videoInfo.video.thumbnails[0].url" alt="">
        <h2>{{ videoInfo.video.title }}</h2>
    </div>
    {{ videoInfo }}
</template>

<script>
    export default {
        name: "CardVideo",
        props: {
            videoInfo: Object, //nom de la props qui sera un objet
        },
    }
</script>