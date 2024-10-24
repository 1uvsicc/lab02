<template>
    <div class="event-info">
      <div class="category">{{ event.category }}</div>
      <div class="organizer">{{ event.organizer }}</div>
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
  .event-info {
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
  
  .category, .organizer {
    font-size: 16px; 
    text-align: right;
  }
  </style>