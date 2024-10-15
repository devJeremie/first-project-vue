<template>
    <RouterLink :to="`video/${videoInfo.video.videoId}`">
        <div class="w-40 h-44 m-2 p-2 rounded-xl bg-white shadow-lg"
            @mouseover="isHovering = true"
            @mouseleave="isHovering = false"
        >
            <img 
                :src="
                    isHovering && 
                    videoInfo.video.movingThumbnails && 
                    videoInfo.video.movingThumbnails.length > 0
                    ? videoInfo.video.movingThumbnails[0].url
                    : videoInfo.video.thumbnails[0].url
                " 
                alt="Vidéo"
                class="rounded-xl"
            />
            <h3 class="titleCard my-2 text-xxs" >{{ videoInfo.video.title }}</h3>
            <h4 class="text-xxs">Kfir Ochaion</h4>
            <p class="text-xxs">
                {{ videoInfo.video.stats.views }} vues
                {{ videoInfo.video.publishedTimeText }}
            </p>
        </div>
    <!-- {{ videoInfo }} -->
    </RouterLink>     
</template>

<script>
    export default {
        name: "CardVideo",
        props: {
            videoInfo: Object, //nom de la props qui sera un objet
        },
        data(){
            return {
                isHovering: false,
            }
        },
    }
</script>
<style>
.titleCard{
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
    text-overflow: ellipsis;
    line-height: 1.5em;
    font-weight: bolder;
}
</style>