<template>
    <div>
        <CardVideo :videoContent="video"/>
    </div>
</template>

<script>
    import CardVideo from '../components/CardVideo.vue';

    export default {
        name: "HomeFeed",
        components: {
            CardVideo,
        }, 
        data() {
            return {
                video: "Voici la vidéo"
            }
        }
    };
</script>
