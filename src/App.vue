<template>
  <main id="main">
    <div class="container weather-app">

      <h1 class="weather-app__title">Check the weather</h1>

      <!-- NOTE: 'v-on:submit.prevent' adds event listener and prevents default reload of page -->
      
      <form 
        class="form weather-app__form"
        v-on:submit.prevent="getWeather"
      >
        <label class="hidden" for="search">
          Search for a city
        </label>
        <input
          v-model="search"
          id="search"
          type="text"
          class="form__input"
          placeholder="Enter a city"
        />
        <button class="form__button">
          Submit
        </button>
        
      </form>


      <!-- Results Card -->
      <section class="card weather-app__card">
        <!-- Background Images to Go Here -->

        <div class="card__header">
          <h2 class="card__city">{{ weather.city }}</h2>
          <p class="card__country">{{ weather.country }}</p>
        </div>

        <div class="card__body">
          <p class="card__temp">{{ weather.temp }}&deg;C</p>
          <p class="card__summary">{{ weather.description }}</p>
        </div>

        <div class="card__footer">
          <div class="card__feels-like">
            <h3>Feels like</h3>
            <p class="card__feels-like__temp">{{ weather.feelsLike }}&deg;C</p>
          </div>
          <div class="card__humidity">
            <h3>Humidity</h3>
            <p class="card__humidity-percentage">{{ weather.humidity }}%</p>
          </div>
        </div>
      </section>
    </div>
  </main>
</template>

<script>


export default {
  data() {
    return {
      search: "",
      weather: {
        city: "Exeter",
        country: "UK",
        temp: 3,
        description: "Light Rain",
        feelsLike: 2,
        humidity: 30
      }
    };
  },
  methods: {
    // this method is called on submitting the form
    getWeather: async function() {
      // API call
      const baseURL = `http://api.openweathermap.org/data/2.5/weather?q=${this.search}&appid=${process.env.VUE_APP_KEY}&units=metric`;
      const response = await fetch(baseURL);
      const data = await response.json();
      console.log(data);
      // reset to blank field
      this.search = ""
    }
  }
}
</script>


