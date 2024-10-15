<template>
    <div class="sm:px-32 flex flex-wrap justify-center">
        <CardVideo v-for="video in videos" :key='video.id' :videoInfo="video"/>
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
                videos: []
            }
        },
        mounted() {
            const url = 'https://youtube138.p.rapidapi.com/channel/videos/?id=UCh5zlvB1pZyU3KYjEPC38KQ&filter=videos_latest&hl=en&gl=US';
            const options = {
                method: 'GET',
                headers: {
                    'x-rapidapi-key': 'fd1c64b4eemshcf10048304ebaf3p16153ajsn40cbce628990',
                    'x-rapidapi-host': 'youtube138.p.rapidapi.com'
                }
            };

            fetch(url, options)
            .then((response) => response.json())
            .then((data) => (this.videos = data.contents))
            .catch((error) => console.error("Probleme with the fetch", error));
        },
    };
</script>
