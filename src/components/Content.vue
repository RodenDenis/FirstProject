<template>
    <div class="content-container">
        <Popular/>
        <div class="main-content">
            <Projects/>
            <Advertising/>
        </div>
    </div>
</template>
<script>
import Popular from "@/components/Popular.vue";
import Projects from "@/components/Projects.vue";
import Advertising from "@/components/Advertising.vue";

export default {
    components: {
        Popular,
        Projects,
        Advertising
    },
}

</script>

<style>
.content-container {
    width: 1320px;
    margin-left: 7%;
    min-height: 400px;
    display: inline-block;
}
.main-content {
    width: 1320px;
    border-top: 1px solid #e7e7e7;
    display: grid;
    grid-template-columns: 6fr 2fr;
}
</style>
