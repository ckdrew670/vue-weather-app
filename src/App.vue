<template>
  <main id="main">
    <div class="container weather-app">

      <h1 class="weather-app__title">Check the weather</h1>

      <!-- Search City -->
      <form class="form weather-app__form">
        <label class="hidden" for="search">
          Search for a city
        </label>
        <input
          id="search"
          type="text"
          class="form-input"
          placeholder="Enter a city"
        />
        
      </form>


      <!-- Results Card -->
      <section class="card weather-app__card">
        <!-- Background Images to Go Here -->

        <div class="card__header">
          <h2 class="card__city">Bristol</h2>
          <p class="card__country">UK</p>
        </div>

        <div class="card__body">
          <p class="card__temp">21&deg;C</p>
          <p class="card__summary">Light rain</p>
        </div>

        <div class="card__footer">
          <div class="card__feels-like">
            <h3>Feels like</h3>
            <p class="card__feels-like__temp">21&deg;C</p>
          </div>
          <div class="card__humidity">
            <h3>Humidity</h3>
            <p class="card__humidity-percentage">70%</p>
          </div>
        </div>
      </section>
    </div>
  </main>
</template>

<script>


export default {
  name: 'App',
}
</script>


