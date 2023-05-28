<template>
    <div class="box">
        <div class="center">
            <li>Projects</li>
            <li>About</li>
            <li>Contact</li>
        </div>
    </div>
</template>


<script setup lang="ts">

</script>


<style scoped>
.box {
    position: fixed;
    width: 100vw;
    height: 0vh;
    background: var(--light-bg);
    overflow: hidden;
    transition-timing-function: ease-in;
    transition: height 1s;
}

.isDropped {
    height: var(--drop-down-height);
}

.center {
    height: auto;
}
</style>