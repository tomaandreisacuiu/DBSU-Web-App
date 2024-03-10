<template>
    <div class="top-nav">
      <div class="title">MoodWave</div>
      <button class="refresh-button" @click="refreshPage">Refresh</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const refreshPage = () => {
    alert("Button was clicked");
  };
  </script>
  
  <style>
  .top-nav {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 10vh;
    padding: 0 20px;
    background-color: #D38F06;
    color: #F9F7F3;
    box-sizing: border-box;
  }
  
  .title {
    font-size: 2em;
    color: #3A3933;
  }
  
  .refresh-button {
    padding: 10px 20px;
    background-color: #BD2218; /* Original button color */
    color: #F9F7F3; /* Text color */
    border: none; /* Removes the default border */
    cursor: pointer; /* Changes cursor to pointer on hover */
    outline: none; /* Removes the outline on focus for clicks */
    transition: background-color 0.3s; 
  }
  
  /* Change color on hover */
  .refresh-button:hover {
    background-color: #3A3933; /* New color for hover */
  }
  
  /* Ensure no border or outline when clicked (:active) or focused (:focus) */
  .refresh-button:active,
  .refresh-button:focus {
    border: none;
    outline: none;
  }
  </style>
  
  