<template>
  <div class="flex items-center justify-center w-full p-4">
    <div class="text-right mr-4 text-base">{{ event.category }}</div>
    <div class="text-right text-base">{{ event.organizer }}</div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
import type { Event } from '@/types'

defineProps<{
  event: Event
}>()
</script>

<style scoped>
/*  .event-info {
  display: flex;
  text-align: center;
  width: 100%;
  padding: 10px;
}

.category,
.organizer {
  font-size: 16px;
  display: inline-block; 
  text-align: right;
  margin-left: 10px;
}
.organizer {
  margin-right: 0;
}*/
</style>
