<template>
    <q-layout view="lHh Lpr lFf">
      <q-header>
        <q-toolbar>
          <q-toolbar-title>
            Weather App
          </q-toolbar-title>
          <q-btn flat label="Home" @click="$router.push('/')"></q-btn>
          <q-btn flat label="Tugas 1" @click="$router.push('/tugas1')"></q-btn>
          <q-btn flat label="Tugas 2" @click="$router.push('/tugas2')"></q-btn>
          <q-btn flat label="Tugas 3" @click="$router.push('/tugas3')"></q-btn>
          <q-btn flat label="Tugas 4" @click="$router.push('/tugas4')"></q-btn>
          <q-btn flat label="Tugas 5" @click="$router.push('/tugas5')"></q-btn>
          <q-btn flat label="Tugas 6" @click="$router.push('/tugas6')"></q-btn>
          <q-btn flat label="Tugas 7" @click="$router.push('/tugas7')"></q-btn>
        </q-toolbar>
      </q-header>
  
      <q-page-container>
        <router-view />
      </q-page-container>
    </q-layout>
  </template>
  
  <script>
  export default {
    name: 'MainLayout'
  };
  </script>
  
  <style scoped>
  /* Tambahkan gaya spesifik untuk layout di sini jika diperlukan */
  </style>
  