<template>
  <div class="container">
    <Header/>
    <NavigationMenu/>
    <Content/>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import NavigationMenu from "@/components/NavigationMenu.vue";
import Content from "@/components/Content.vue";
export default {
  components: {
    Header,
    NavigationMenu,
    Content
  }
}
</script>
<style>
body {
  margin: 0px;
}
</style>

