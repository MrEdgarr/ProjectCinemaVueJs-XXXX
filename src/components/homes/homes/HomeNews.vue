<template>
    <div class="wrapper-content">
        <div class="section-heading">
            <h3>Tin tức</h3>
        </div>
        <div class="section-content">
            <v-row class="post-list">
                <v-col cols="12" md="6" class="post-item">
                    <div class="post-thumb">
                        <v-img
                            src="https://images.unsplash.com/photo-1713782522314-caab46f64c79?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwyNnx8fGVufDB8fHx8fA%3D%3D"
                            rounded
                        />
                    </div>
                    <div class="post-content">
                        <div class="post-title">
                            <h5 class="mt-10 mb-5">
                                Lorem ipsum dolor sit amet consectetur
                                adipisicing elit
                            </h5>
                        </div>
                    </div>
                    <div>
                        <v-btn
                            type="button"
                            color="info"
                            size="x-small"
                            class="mr-1"
                        >
                            <v-icon>mdi-thumb-up </v-icon>
                            Thích
                        </v-btn>
                        <v-btn type="button" color="grey-300" size="x-small">
                            <v-icon>mdi-eye-outline</v-icon>
                            804
                        </v-btn>
                    </div>
                </v-col>
                <v-col cols="12" lg="6" class="post-item">
                    <v-row v-for="value in 3" :key="value">
                        <v-col cols="4">
                            <div class="post-thumb">
                                <v-img
                                    src="https://images.unsplash.com/photo-1713782522314-caab46f64c79?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwyNnx8fGVufDB8fHx8fA%3D%3D"
                                    rounded
                                />
                            </div>
                        </v-col>
                        <v-col cols="8">
                            <div class="post-content">
                                <div class="post-title">
                                    <h5>
                                        Lorem ipsum dolor sit amet consectetur
                                        adipisicing elit
                                    </h5>
                                </div>
                            </div>
                            <div>
                                <v-btn
                                    type="button"
                                    color="info"
                                    size="x-small"
                                    class="mr-1"
                                >
                                    <v-icon>mdi-thumb-up </v-icon>
                                    Thích
                                </v-btn>
                                <v-btn
                                    type="button"
                                    color="grey-300"
                                    size="x-small"
                                >
                                    <v-icon>mdi-eye-outline</v-icon>
                                    804
                                </v-btn>
                            </div>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </div>
        <div class="film__footer text-center transition-all duration-300">
            <v-btn class="film__btn" variant="outlined">
                Xem thêm <v-icon>mdi-chevron-right</v-icon>
            </v-btn>
        </div>
    </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
.section-blogslist {
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
        .section-content {
            .post-list {
                .post-content {
                    .post-title {
                        font-size: 24px;
                        line-height: 22px;
                        position: relative;
                        font-weight: 500;
                        margin-block: 5px;
                        h5 {
                            overflow: hidden;
                            -webkit-line-clamp: 2;
                            -webkit-box-orient: vertical;
                            display: -webkit-box;
                        }
                    }
                }
            }
        }
    }
}
</style>
