<template>
    <div class="wrapper-quickbuy hidden-sm-and-down">
        <v-select
            :items="items"
            variant="plain"
            placeholder="Chọn phim"
            prepend-icon="mdi-numeric-1-circle"
            item-color="secondary"
        ></v-select>
        <v-select
            :items="items"
            variant="plain"
            placeholder="Chọn rạp"
            prepend-icon="mdi-numeric-2-circle"
            item-color="secondary"
        ></v-select>
        <v-select
            :items="items"
            variant="plain"
            placeholder="Chọn ngày"
            prepend-icon="mdi-numeric-3-circle"
            item-color="secondary"
        ></v-select>
        <v-select
            :items="items"
            variant="plain"
            placeholder="Chọn suất"
            prepend-icon="mdi-numeric-4-circle"
            item-color="secondary"
        ></v-select>
        <v-btn color="secondary" class="rounded-0">Mua vé nhanh</v-btn>
    </div>
</template>
<script>
export default {
    data: () => ({
        items: ["Foo", "Bar", "Fizz", "Buzz"],
    }),
};
</script>
<style lang="scss">
.wrapper-quickbuy {
    display: grid;
    background-color: white;
    border-radius: 0.25rem;
    grid-template-columns: repeat(11, minmax(0, 1fr));
    max-width: 72rem;
    width: 100%;
    height: 3.5rem;
    z-index: 500;
    bottom: 0;
    position: absolute;
    left: 50%;
    transform: translate(-50%, 50%) rotate(0) skewX(0) skewY(0) scaleX(1)
        scaleY(1);
    box-shadow: 0 0 #0000, 0 0 #0000, 0 0 #0000, 0 0 #0000,
        0 25px 50px -12px rgba(0, 0, 0, 0.25);
    .v-input {
        height: 100%;
        grid-column: span 3 / span 3;
        position: relative;

        .v-input__prepend {
            margin-left: 5px;
            margin-right: 5px;
            font-size: 14px;
            color: rgb(var(--v-theme-secondary));
        }
    }
    .v-input:not(:first-child),
    .v-btn {
        height: 3.5rem;
        grid-column: span 2 / span 2;
        position: relative;
    }
    .v-btn {
        border-top-right-radius: 0.25rem !important;
        border-bottom-right-radius: 0.25rem !important;
    }
}
</style>
