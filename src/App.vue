<script setup lang="ts"></script>
<script setup>
 import TheHeader from './header.vue' 
 import MarkdownIt from 'markdown-it'
 import raw from '/content/home.md?raw'
  
 const lel1 = new MarkdownIt().render(raw)
 </script>

<style lang="scss" src="/src/styles/main.scss"></style>

<template >
    <TheHeader />

    <main>
      <div>  
        <h1 class="h">WAFFLES</h1>
      </div>

      <div class="text">
        <p>sample text</p>
      </div>

      <div class="md" v-html="lel1" />

    </main>
</template>


