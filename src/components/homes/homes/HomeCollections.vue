<template>
    <div class="wrapper-content">
        <div class="section-heading">
            <h3>Khuyến mãi</h3>
        </div>
        <div class="section-content">
            <swiper
                :slidesPerView="4"
                :spaceBetween="10"
                :modules="modules"
                :autoplay="{
                    delay: 1000,
                    disableOnInteraction: false,
                }"
                :loop="true"
                :grabCursor="true"
                :speed="2000"
                class="post-list"
            >
                <swiper-slide
                    class="post-item"
                    v-for="value in 10"
                    :key="value"
                >
                    <div class="post-thumb">
                        <v-img
                            src="https://images.unsplash.com/photo-1713782522314-caab46f64c79?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwyNnx8fGVufDB8fHx8fA%3D%3D"
                            rounded
                        />
                    </div>
                </swiper-slide>
            </swiper>
            <div id="containerForBullets"></div>
        </div>
    </div>
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    data() {
        return {
            modules: [Autoplay],
        };
    },
};
</script>
<style lang="scss">
.section-collections {
    margin-bottom: 2rem;
    .wrapper-content {
        .section-heading {
            h3 {
                font-weight: 600;
                font-size: 26px;
                line-height: 36px;
                margin-bottom: 2.5rem;
                margin-top: 2rem;
                white-space: initial;

                overflow: hidden;
                -webkit-line-clamp: 1;
                -webkit-box-orient: vertical;
                display: -webkit-box;
                text-align: center;
            }
        }
    }
}
</style>
