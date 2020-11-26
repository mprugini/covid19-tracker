<template>
  <div>
    <Country
      v-for="country in topTenCountries"
      :key="country.Slug"
      :country="country"
    ></Country>
  </div>
</template>

<script>
import Country from "./Country";
import _ from 'lodash';
export default {
    components: {
      Country,
    },
  props: ["countries"],
  computed: {
    topTenCountries: function() {
      // sort countries by TotalConfirmed cases and return top 10
      return _.orderBy(this.countries, 'TotalConfirmed', 'desc').slice(0, 10)
    },
  },
};
</script>

<style></style>
