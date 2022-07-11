<template>
    <v-carousel
        cycle
        height="400"
        hide-delimiter-background
        show-arrows="hover"
    >
        <v-carousel-item v-for="(slide, i) in slides" :key="i">
            <v-sheet :color="colors[i]" height="100%">
                <div class="d-flex fill-height justify-center align-center">
                    <div class="text-h2">{{ slide }} Slide</div>
                </div>
            </v-sheet>
        </v-carousel-item>
    </v-carousel>
</template>
<script>
export default {
    data() {
        return {
            items: [
                {
                    src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
                },
                {
                    src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
                },
                {
                    src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
                },
                {
                    src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
                },
            ],
        };
    },
};
</script>
