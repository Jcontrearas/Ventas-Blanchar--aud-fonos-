<template>
    <div>
      <v-toolbar
        image="https://img.freepik.com/fotos-premium/auriculares-varios-colores-dispuestos-linea-sobre-fondo-verde_1028938-341040.jpg"
        dark
        height="150"
      >
        <v-app-bar-nav-icon class="menu"></v-app-bar-nav-icon>
  
        <v-toolbar-title  
        ><h1 class="title">SONIC HAVEN</h1></v-toolbar-title>
  
        <v-spacer></v-spacer>
  
        <carrito class="mr-5"
         :productos="productos"
        >

        </carrito>
      </v-toolbar>
      
    </div>
  </template>
  <script>
  export default {
    props:{
      productos : Array,
    }
  }
  </script>
  <style scoped>
  .title {
    font-family: sans-serif;
    font-size: 2.4rem;
    color:#fff;
    text-shadow: 0px 0px 5px #fff;
  }
  .menu {
    color: #fff
  }
   
  </style>