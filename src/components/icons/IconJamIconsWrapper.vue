<template>
    <img :class="['icon-jam-icons-wrapper', className]" alt="Icon jam icons"
        src="https://c.animaapp.com/ujIwT5MJ/img/icon---jam-icons---outline---logos---computer-alt-1.svg" />
</template>

<script>
export default {
    name: "IconJamIconsWrapper",
    props: {
        className: {
            type: String,
            default: "",
        },
    },
};
</script>

<style>
.icon-jam-icons-wrapper {
    height: 24px;
    left: 0;
    position: absolute;
    top: 0;
    width: 24px;
}
</style>
