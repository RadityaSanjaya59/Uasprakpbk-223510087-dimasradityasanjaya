<template>
    <q-card>
      <q-card-section>
        <q-input
          v-model="searchCity"
          label="Masukkan nama kota"
          outlined
          @keyup.enter="fetchWeather"
        ></q-input>
        <q-btn
          label="Search"
          @click="fetchWeather"
          color="primary"
          class="q-mt-md"
        ></q-btn>
      </q-card-section>
      <q-card-section v-if="city">
        <div class="text-h6">{{ city }}</div>
        <div class="text-subtitle1">{{ weatherDescription }}</div>
        <div class="text-subtitle2">{{ temperature }}°C</div>
      </q-card-section>
    </q-card>
  </template>
  
  <script>
  export default {
    data() {
      return {
        searchCity: '',
        city: '',
        weatherDescription: '',
        temperature: '',
      };
    },
    methods: {
      async fetchWeather() {
        const apiKey = 'faa31350a445d3f856f11db6bfc27f00'; 
        const city = this.searchCity;
        if (city === '') {
          return;
        }
        try {
          const response = await fetch(
            `https://api.openweathermap.org/data/2.5/weather?q=${city}&units=metric&appid=${apiKey}`
          );
          if (!response.ok) {
            throw new Error('City not found');
          }
          const data = await response.json();
          this.city = data.name;
          this.weatherDescription = data.weather[0].description;
          this.temperature = data.main.temp;
        } catch (error) {
          this.city = '';
          this.weatherDescription = '';
          this.temperature = '';
          alert(error.message);
        }
      },
    },
  };
  </script>
  
  <style scoped>
  .q-card {
    max-width: 300px;
    margin: auto;
  }
  </style>
  