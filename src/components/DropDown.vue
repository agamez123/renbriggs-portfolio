<template>
    <div class="box">
        <div class="center">
            <ol>
                <li>Projects</li>
                <li>About</li>
                <li>Contact</li>
            </ol>
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
    margin-top: 13vh;
}

li {
    padding: 1em;
    font-size: x-large;
}


</style>