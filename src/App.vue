<script setup lang="ts">
 import TheHeader from './header.vue' 
 import MarkdownIt from 'markdown-it'
 import raw from '/content/main.md?raw'
  
 const lel1 = new MarkdownIt({html: true}).render(raw)
 </script>

<style lang="scss" src="/src/styles/main.scss"></style>

<template >
    <TheHeader />

    <main>
      <div>  
        <h1 class="h">Bebsite</h1>
      </div>

      <div class="text">
        <p>Welcome to Bebsite!</p>
        <p>An assignment website for one of my cs classes</p>
      </div>

      <!-- @ts-ignore -->
      <div class="md" v-html="lel1" />

    </main>
</template>


