<template>
  <section class="home" id="home">
    <div class="content">
      <h1>
        yo,
        <br>
        I'm Ren
      </h1>
      <p>I do stuff</p>
    </div>
    <div class="icon">
      <img src="../assets/parabeetlev2.png">
    </div>
  </section>
</template>

<script setup lang="ts">


</script>

<style>
@media screen and (max-width: 450px) {
  .home {
    display: flex;
    padding: 2rem 2rem;
    position: relative;
    min-height: 20rem;
    align-items: center;
  }

  .home>div{
    flex: 1 1 40rem;
  
  }

  .home .content {
    color: var(--main-text);
    font-size: 1.5rem;  
    text-align: left;
  }

  .icon>img {
    width: 100%;

  }
}

@media screen and (min-width: 450px) {
  .home {
    display: flex;
    padding: 2rem 1rem;
    align-items: center;
    position: relative;
    min-height: 100vh;
  }
  
  .home>div{
    flex: 1 1 40rem;
    
  }
  
  .home .content {
    font-size: xx-large;
    text-align: left;
  }
}
</style>
