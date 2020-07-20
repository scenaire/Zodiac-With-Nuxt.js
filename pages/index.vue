<template>
  <div class="container">
    <b-row class="vh-100 text-center" align-v="center">
      <div class="wrapper">
        <div>
        <h1 class="title">
          Chinese Zodiac
        </h1>
      </div>

      <br>

      <div class="links">
        <nuxt-link
          to="/zodiacTable"
          class="button--green"
        >
          Table
        </nuxt-link>
        <nuxt-link
          to="/zodiacInformation"
          class="button--grey"
        >
          Information
        </nuxt-link>
      </div>
      </div>
    </b-row>
  </div>
</template>

<script>
export default {}
</script>

<style>

.wrapper {
  width: 100%;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

</style>
