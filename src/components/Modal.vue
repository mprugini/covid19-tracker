<template>
  <div class="modal">
      <span>
          Country: <b>{{ country.Country.toLocaleString() }}</b>
      </span>
      <br>
      <br>
      <span>
          New Confirmed Cases: <span class="number">{{ country.NewConfirmed.toLocaleString() }}</span>
      </span>
      <br>
      <span>
          Total Confirmed: <span class="number">{{ country.TotalConfirmed.toLocaleString() }}</span>
      </span>
      <br>
      <span>
          New Deaths: <span class="number">{{ country.NewDeaths.toLocaleString() }}</span>
      </span>
      <br>
      <span>
          Total Deaths: <span class="number">{{ country.TotalDeaths.toLocaleString() }}</span>
      </span>
      <br>
      <span>
          New Recovered: <span class="number">{{ country.NewRecovered.toLocaleString() }}</span>
      </span>
      <br>
      <span>
          Total Recovered: <span class="number">{{ country.TotalRecovered.toLocaleString() }}</span>
      </span>
  </div>
</template>

<script>
export default {
    props: ['country'],
};
</script>

<style scoped>
.modal {
    text-align: center;
    padding: 70px 0;
    font-family:Lucida Console;
}

.number {
    font-weight: bold;
}
</style>
