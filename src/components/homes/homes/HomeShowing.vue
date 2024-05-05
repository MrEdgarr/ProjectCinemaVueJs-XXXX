<template lang="">
    <v-row>
        <v-col cols="6" sm="4" md="3" v-for="value in 7" :key="value">
            <div class="card-image__wrapper">
                <v-img
                    style="width: 100%"
                    src="https://cdn.galaxycine.vn/media/2024/4/15/luca-sneak-500_1713170135558.jpg"
                    rounded="lg"
                />
                <div class="votes">
                    <p class="absolute right-[5px] bottom-10">
                        <v-icon
                            icon="mdi-star"
                            size="smail"
                            color="warning"
                            class="mr-5"
                        ></v-icon>
                        <span class="text-[18px] font-bold text-white"
                            >9.6</span
                        >
                    </p>
                </div>
                <div class="age__limit">
                    <span>K</span>
                </div>
            </div>
            <div class="card-title">
                <h5>Super awesome, Vue 3 is coming soon!</h5>
            </div>
        </v-col>
    </v-row>
    <div class="film__footer text-center transition-all duration-300">
        <router-link to="/movie/showing/">
            <v-btn class="film__btn" variant="outlined">
                Xem thêm <v-icon>mdi-chevron-right</v-icon>
            </v-btn>
        </router-link>
    </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
.section-collection {
    padding-top: 2.5rem;
    margin-block: 2.5rem;

    .v-slide-group.v-tabs {
        margin-bottom: 2rem;
        .v-btn__content {
            font-size: 1.25rem;
            font-weight: 500;
            line-height: 1.1;
            color: rgb(var(--v-theme-grey-500));
            .v-tab__slider {
                // background-color: rgb(var(--v-theme-secondary));
            }
        }
    }

    .v-tab-item--selected {
        .v-btn__content {
            color: rgb(var(--v-theme-grey-900)) !important;
        }
    }
    .card-image__wrapper {
        position: relative;
        overflow: hidden;
        .votes {
            &::before {
                content: "";
                position: absolute;
                bottom: 50px;
                right: -5px;
                padding: 0.75rem 2.8rem;
                background: rgba(0, 0, 0, 0.4);
                transform: skewX(25deg);
            }
            p {
                position: absolute;
                right: 5px;
                bottom: 50px;
                span {
                    display: inline-block;
                    color: white;
                    font-weight: 700;
                    font-size: 18px;
                }
            }
        }
        .age__limit {
            position: absolute;
            bottom: 15px;
            right: 5px;
            span {
                display: inline-flex;
                align-items: center;
                justify-content: center;
                width: 38px;
                height: 1.75rem;
                background-color: rgb(var(--v-theme-secondary));
                font-weight: 700;
                text-align: center;
                border-radius: 0.25rem;
                display: inline-flex;
                color: white;
            }
        }
    }
    .card-title {
        text-align: center;
        text-transform: capitalize;
        position: relative;
        margin-bottom: 0;
        text-align: left;
        line-height: 125%;
        color: #333;
        font-weight: 700;
        font-size: 20px;
        margin-top: 10px;
        cursor: pointer;
        h5 {
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: pre-wrap;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
        }
    }
}
</style>
