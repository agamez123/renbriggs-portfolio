<template>
    <div class="box">
        <div class="box" id="transition">

        </div>
    </div>
</template>


<script setup lang="ts">

</script>


<style scoped>
.box {
    position: fixed;
    width: 100%;
    height: 0vh;
    background: var(--light-bg);
    overflow: hidden;
    transition-timing-function: ease-in;
    transition: height 1s;
}

.isDropped {
    height: 45vh;
}

</style>