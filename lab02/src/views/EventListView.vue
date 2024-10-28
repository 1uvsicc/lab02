<script setup lang="ts">
import EventCard from '@/components/EventCard.vue'
import EventInfo from '@/EventInfo.vue'
import type { Event } from '@/types'

import { ref, onMounted } from 'vue'
import EventService from '@/services/EventService'

const events = ref<Event[]>(null)

onMounted(() => {
  EventService.getEvents()

    .then(response => {
      events.value = response.data
    })

    .catch(error => {
      console.error('There was an error!', error)
    })
})
</script>

<template>
  <h1>Events For Good</h1>
  <!-- new element -->

  <div v-for="event in events" :key="event.id" class="event-container">
    <EventCard :event="event" />

    <EventInfo :event="event" />
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: auto;
}

.event-info {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 10px;
}
.event-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 80%;
  padding: 10px;
  margin: 10px auto;
}
.category,
.organizer {
  font-size: 16px;
  margin-left: 8px;
  text-align: center;
}
</style>
