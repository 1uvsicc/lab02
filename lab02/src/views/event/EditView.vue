<script setup lang="ts">
import { toRefs } from 'vue'
import { type Event } from '@/types'
import { useMessageStore } from '@/stores/message'; 
import { useRouter } from 'vue-router';
const props = defineProps<{
  event: Event
  id: String
}>()

const { event } = toRefs(props)
const router = useRouter();
const messageStore = useMessageStore();
const eventDetailView = () => {
 
  messageStore.updateMessage('Data has been updated')
  setTimeout(() => {
   messageStore.resetMessage()
 }, 3000)
  router.push({ name: 'event-detail-view', params: { id: props.event.id } });
};

</script>
<template>
  
  <p>Edit event here</p>
  <button @click="eventDetailView">edit</button>
</template>
