<script setup>
import Header from "./Header.vue";
import SideBar from "./SideBar.vue";  
import Player from "./Player.vue"
import LiveChat from "./LiveChat.vue"
import Home from "./Home.vue"; 

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