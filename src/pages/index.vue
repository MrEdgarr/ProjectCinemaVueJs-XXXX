<template>
  <div>
    <div class="section-slider">
      <HomeSlideBar />
      <HomeQuickBuy />
    </div>
    <div class="section-collection">
      <v-container>
        <v-tabs v-model="tab" align-tabs="center" color="">
          <v-tab :value="1" :ripple="false">Đang chiếu</v-tab>
          <v-tab :value="2" :ripple="false">Sắp chiếu</v-tab>
        </v-tabs>
        <v-window v-model="tab" class="disable-tab-transition">
          <v-window-item :value="1">
            <HomeShowing />
          </v-window-item>
          <v-window-item :value="2">
            <HomeUpcoming />
          </v-window-item>
        </v-window>
      </v-container>
    </div>
    <v-divider :thickness="5" color="grey-300"></v-divider>
    <div class="section-blogslist">
      <v-container>
        <HomeNews />
      </v-container>
    </div>
    <v-divider :thickness="5" color="grey-300"></v-divider>
    <div class="section-collections">
      <v-container>
        <HomeCollections />
      </v-container>
    </div>
    <v-divider :thickness="5" color="grey-300"></v-divider>
  </div>
</template>

<script>
export default {
  data: () => ({
    tab: null,
  }),
};
</script>
