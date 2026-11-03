<script setup lang="ts">
 import TheHeader from './header.vue' 
 import MarkdownIt from 'markdown-it'
 import raw from '/content/home.md?raw'
  
 const lel = new MarkdownIt().render(raw)
</script>

<style lang="scss" src="/src/styles/main.scss"></style>

<template>

    <TheHeader />

    <main>
        <div class="h">STEAM HAPPY</div>

        
        <div class="img"><img src="/img/steamhappy.png"></img></div>    

        <div class="md" v-html="lel" />
    </main>
</template>