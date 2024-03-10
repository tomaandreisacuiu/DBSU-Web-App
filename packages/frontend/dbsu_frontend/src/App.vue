<script setup>
  import { ref, provide } from 'vue';
import TopNav from './components/TopNav.vue';
import DeviceCard from './components/DeviceCard.vue';

const devices = ref([
    {name: 'Device1', song: 'Song A'},
    {name: 'Device2', song: 'Song B'},
    {name: 'Device3', song: 'Song C'},
])

const currentIndex = ref(null);
const playSong = (index) => {
  currentIndex.value = index;
};

// Provide the playSong function and currentIndex to child components
provide('playSong', playSong);
provide('currentIndex', currentIndex);

</script>

<template>
<div id="app-body">
    <TopNav/>

    <div class="cards">
        <DeviceCard
        v-for="(device, index) in devices"
        :key="index"
        :deviceName="device.name"
        :songName="device.song"
        :isPlaying="currentIndex === index"
        @play="playSong(index)"
        />
    </div>
</div>
</template>

<style scoped>
</style>
