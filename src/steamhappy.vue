<script setup lang="ts">
 import TheHeader from './header.vue' 
 import MarkdownIt from 'markdown-it'
 import raw from '/content/home.md?raw'
  
 const lel = new MarkdownIt({html: true}).render(raw)
</script>

<style lang="scss" src="/src/styles/main.scss"></style>

<template>

    <TheHeader />

    <main>
        <div class="h">STEAM HAPPY</div>

        <p class="text">(My most favorite emoji on the internet)</p>
        
        <div style="margin-top: 100px;"></div>

        <div class="img"><img src="/img/steamhappy.png"></img></div>    

        <div class="md" v-html="lel" />
    </main>
</template>