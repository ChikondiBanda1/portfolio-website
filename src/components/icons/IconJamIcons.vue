<template>
  <img :class="['icon-jam-icons', className]" alt="Icon jam icons"
    src="https://c.animaapp.com/ujIwT5MJ/img/icon---jam-icons---outline---logos---pencil-1.svg" />
</template>

<script>
export default {
  name: "IconJamIcons",
  props: {
    className: {
      type: String,
      default: "",
    },
  },
};
</script>

<style>
.icon-jam-icons {
  height: 24px;
  left: 0;
  position: absolute;
  top: 0;
  width: 24px;
}
</style>
