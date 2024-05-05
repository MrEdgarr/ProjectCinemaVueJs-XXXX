<template>
    <swiper
        :navigation="true"
        :pagination="true"
        :keyboard="true"
        :grabCursor="true"
        :loop="true"
        :modules="modules"
        class="mySwiper"
    >
        <swiper-slide>
            <v-img
                class="hidden-sm-and-down"
                src="@/assets/image/cai-gia-cua-hanh-phuc-2_1712733220607.jpg"
            />
            <v-img
                class="hidden-md-and-up"
                src="@/assets/image/cai-gia-cua-hanh-phuc-1_1712733234561.jpg"
            />
        </swiper-slide>
        <swiper-slide>
            <v-img
                class="hidden-sm-and-down"
                src="@/assets/image/luca-sneak-2048_1713170236165.jpg"
            />
            <!-- <v-img
        class="hidden-md-and-up"
        src="@/assets/image/luca-sneak-750_1713170237157.jpg"
      /> -->
        </swiper-slide>
        <swiper-slide>
            <v-img
                class="hidden-sm-and-down"
                src="@/assets/image/ghostbusters-frozen-empire-2048_1712719876429.jpg"
            />
            <v-img
                class="hidden-md-and-up"
                src="@/assets/image/ghostbusters-frozen-empire-750_1712719877413.jpg"
            />
        </swiper-slide>
    </swiper>
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Pagination, Keyboard } from "swiper/modules";
import "swiper/css/navigation";
import "swiper/css/pagination";
export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    data() {
        return {
            modules: [Navigation, Pagination, Keyboard],
        };
    },
};
</script>
<style lang="scss">
.section-slider {
    position: relative;
    .swiper {
        width: 100%;
        height: 100%;

        &-slide {
            display: flex;
            justify-content: center;
            align-items: center;
            img {
                display: block;
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }

        .swiper-button-next {
            right: -35px;
            &::after {
                margin-right: 35%;
                background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAAQCAYAAAAvf+5AAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAABMSURBVHgB3dLBCQAgDANAcQJHcTQ3qJs6QkeIFQpi0frWQB6FI68GAFnKUgpeBDTMkAcr1nyPSzxZc6fdGpm1+gRSyFekcLxZc5GkA1JCBQ0g0YWBAAAAAElFTkSuQmCC);
            }
        }
        .swiper-button-prev {
            left: -35px;
            &::after {
                margin-left: 35%;
                background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAAQCAYAAAAvf+5AAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAABMSURBVHgB3dLBCQAgDANAcQJHcTQ3qJs6QkeIFQpi0frWQB6FI68GAFnKUgpeBDTMkAcr1nyPSzxZc6fdGpm1+gRSyFekcLxZc5GkA1JCBQ0g0YWBAAAAAElFTkSuQmCC);
                transform: rotate(-180deg);
            }
        }
        .swiper-button-next,
        .swiper-button-prev {
            z-index: 999;
            height: 60px;
            width: 60px;
            border-radius: 50%;
            // background: #464444c4;
            background-color: rgb(var(--v-theme-secondary));
            &::after {
                content: "";
                font-size: 20px;
                display: block;
                width: 9.71px;
                height: 16px;
                opacity: 1;
                font-family: slick;
                line-height: 1;
                color: #fff;
                -webkit-font-smoothing: antialiased;
                -moz-osx-font-smoothing: grayscale;
            }
        }
        .swiper-pagination-bullet {
            width: 50px;
            height: 4px;
            margin-inline: 5px;
            border-radius: 0;
            margin: 0 2px 20px 2px;
            background-color: rgb(var(--v-theme-secondary));
        }
    }
}
</style>
