<template>
  <main id="main">
    <div class="container weather-app">

      <h1 class="weather-app__title">What's the weather like in </h1>

      <!-- Search City -->
      <form class="weather-app__form">
        <input
          type="text"
          class="weather-app__form-input"
          placeholder="Enter a city"
        />
      </form>

      <!-- Results Card -->
      <section class="weather-app__card">
        <!-- Background Images to Go Here -->

        <div class="weather-app__card__header">
          <h2 class="weather-app__card__city">Bristol</h2>
          <p class="weather-app__card__country">UK</p>
        </div>

        <div class="weather-app__card__body">
          <p class="weather-app__card__temp">21&deg;C</p>
          <p class="weather-app__card__summary">Light rain</p>
        </div>

        <div class="weather-app__card__footer">
          <div class="weather-app__card__feels-like">
            <h3>Feels like</h3>
            <p class="weather-app__card__feels-like__temp">21&deg;C</p>
          </div>
          <div class="weather-app__card__humidity">
            <h3>Humidity</h3>
            <p class="weather-app__card__humidity-percentage">70%</p>
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
