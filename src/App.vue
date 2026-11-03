<script setup lang="ts">
 import TheHeader from './header.vue' 
 import MarkdownIt from 'markdown-it'
 import raw from '/content/README.md?raw'
  
 const lel1 = new MarkdownIt().render(raw)
 </script>

<style lang="scss" src="/src/styles/main.scss"></style>

<template >
    <TheHeader />

    <main>
      <div>  
        <h1 class="h">Yusuf's Website</h1>
      </div>

      <div class="text">
        <p>sample text</p>
      </div>

      <!-- @ts-ignore -->
      <div class="md" v-html="lel1" />

    </main>
</template>


