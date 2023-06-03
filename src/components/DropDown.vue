<template>
    <div class="box">

        <ol>
            <li><router-link active-class="active" to="/">Home</router-link></li>
            <li><router-link active-class="active" to="/projects">Projects</router-link></li>
            <li><router-link active-class="active" to="/about">About</router-link></li>
            <li><router-link active-class="active" to="/contact">Contact</router-link></li>
        </ol>

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
    height: var(--drop-down-height);
}

a {
    text-decoration: none;
}

a:visited {
    color: black;
}

a:hover, a.active {
    background-color: indianred;
}

ol {
    margin-top: 14vh;
    height: calc(var(--drop-down-height) - 14vh);
    display: flex;
    flex-direction: column;
    justify-content: center;
}

li {
    /* padding: 1em; */
    max-width: 100%;
    max-height: 100%;
    font-size: x-large;
    flex-grow: 1;
}



</style>