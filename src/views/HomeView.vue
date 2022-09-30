<script setup lang="ts">
// import TheWelcome from '../components/TheWelcome.vue'
import { reactive, computed } from 'vue'

interface Book {
  title: String,
  year?: number
}
const book: Book = reactive({ title: '鲁本' })


const comBook = computed(()=>{
  return book.title  === '本'? 'Yes': 'No'
})
</script>

<template>
  <main>
    <!-- <TheWelcome /> -->
    {{ book.title }}
    {{comBook}}
  </main>
</template>
