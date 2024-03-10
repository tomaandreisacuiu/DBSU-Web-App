<script setup>
    const props = defineProps({
        deviceName: String,
        songName: String,
        isPlaying: Boolean
    })

    const playPauseSong = () => {
        if (!props.isPlaying) {
            console.log("play song");
        } else {
            console.log("stop current song, start the new one")
        }
    }
</script>

<template>
    <div class = "device-card">

        <div class = "song-information">
            <h3>{{ deviceName }}</h3>
            <h5>{{ songName }}</h5>
        </div>

        <button id="button" @click="playPauseSong">{{ isSongPlaying ? 'Pause' : 'Play' }}</button>

    </div>
</template>

<style scoped>
.device-card {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  border: 0px solid #ccc;
  margin-bottom: 10px;
  background-color: #D38F06;
  width: 50vh;
}

.song-information h3,
.song-information h5 {
  margin: 0;
  color: #3A3933;
}

#button {
    background-color: #BD2218;
}
</style>