<template>
    {{ videoContent }}
</template>

<script>
    export default {
        name: "CardVideo",
        props: {
            videoContent: Object, //nom de la props qui sera un objet
        },
    }
</script>