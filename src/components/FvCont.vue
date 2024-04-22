<script>

// Import Swiper Vue.js components
import { ref } from 'vue';
import { Autoplay, EffectFade, Parallax } from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';

//画像のパス
import mainVisual1 from "@/assets/images/main-visual1.jpg";
import mainVisual2 from "@/assets/images/main-visual2.jpg";
import mainVisual3 from "@/assets/images/main-visual3.jpg";

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/autoplay';
import 'swiper/css/effect-fade';
import 'swiper/css/parallax';

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        const images = ref([
            mainVisual1,
            mainVisual2,
            mainVisual3,
        ])
        
        const onSwiper = (swiper) => {
        };
        const onSlideChange = () => {
        };
        return {
            images,
            Swiper,
            SwiperSlide,
            modules: [Autoplay, EffectFade, Parallax],
        }
    },
};

</script>

<template>
    <swiper 
    :modules="modules" 
    effect="fade"
    :slides-per-view="1" 
    @swiper="onSwiper" 
    @slideChange="onSlideChange" 
    :loop="true"
    :autoplay="true"
    :speed="1000"
    >
        <swiper-slide v-for="image in images" :key="image"><img :src="image"></swiper-slide>
    </swiper>
</template>


<style>
.swiper {
    width: 100%;
    height: 100%;
    overflow: hidden;
}
.swiper .swiper-slide {
    width: 100%;
    height: calc(100vh - 120px);
    color: #FFFFFF;
    background: #000;
}
.swiper .swiper-slide img {
    height: 100%;
    object-fit: cover;
}
</style>