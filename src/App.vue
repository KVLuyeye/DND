<script setup>
import Header from "../src/components/Header.vue";
import SideBar from "./components/SideBar.vue";  
import Player from "./components/Player.vue"
import LiveChat from "./components/LiveChat.vue"
</script>

<template>
  <header>
    <Header />
  </header>

  <main>

    <aside id="sideBar">
    <SideBar/>
  </aside>

    <Player/> 
   
  <aside>
    <LiveChat/>
  </aside>

  </main>

</template>

<style lang="scss">

body {
font-family: sans-serif;
 min-height: 100vh; 
 color: white;
    }

 #app{
   display: flex; 
   flex-direction: column;
   min-height: 100vh; 
   margin: 0;
 }

 main{
  display: flex;
  min-height: 94vh; 
 }   
</style>