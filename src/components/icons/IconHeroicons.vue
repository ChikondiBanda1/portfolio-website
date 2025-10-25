<template>
    <img :class="['icon-heroicons', className]" alt="Icon heroicons"
        src="https://c.animaapp.com/ujIwT5MJ/img/icon---heroicons---outline---search-1.svg" />
</template>

<script>
export default {
    name: "IconHeroicons",
    props: {
        className: {
            type: String,
            default: "",
        },
    },
};
</script>

<style>
.icon-heroicons {
    height: 100%;
    left: 0;
    position: absolute;
    top: 0;
    width: 100%;
}
</style>
