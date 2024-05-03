<template>
  <v-app-bar>
    <v-container>
      <v-toolbar flat class="mainHeader" color="white">
        <router-link to="/index.html" class="border-none">
          <v-img src="@/assets/1.svg" height="60" width="150" max-width="150"
        /></router-link>
        <v-spacer></v-spacer>

        <template v-for="(value, index) in links" :key="index">
          <router-link :to="value.path">
            <v-btn class="hidden-sm-and-down">
              {{ value.name }}
            </v-btn>
          </router-link>
        </template>

        <v-spacer></v-spacer>

        <v-btn :ripple="false">
          <v-icon
            icon="mdi mdi-account"
            size="large"
            color="secondary"
          ></v-icon>
          Đăng Nhập
        </v-btn>

        <div class="hidden-md-and-up">
          <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        </div>
      </v-toolbar>
    </v-container>
  </v-app-bar>
  <v-navigation-drawer v-model="drawer" temporary>
    <v-sheet color="grey-lighten-4" class="pa-4 text-center">
      <v-avatar class="mb-4" color="grey-darken-1" size="64">
        <v-img src="https://randomuser.me/api/portraits/women/17.jpg" />
      </v-avatar>

      <div>john@google.com</div>
    </v-sheet>

    <v-divider></v-divider>
    <v-list>
      <v-list-item v-for="(value, index) in links" :key="index" link>
        <v-list-item-title>{{ value.name }}</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>
<script>
export default {
  data: () => ({
    drawer: null,
    links: [
      {
        name: "Trang chủ",
        path: "/index.html",
      },
      {
        name: "Lịch chiếu",
        path: "/showtimes/",
      },
      {
        name: "Tin Tức",
        path: "/news",
      },
    ],
  }),
};
</script>
