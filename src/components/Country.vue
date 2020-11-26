<template>
  <div class="country-box">
    <div>
      <h2>
        Country: {{ country.Country }}
      </h2>
      <p>
        Total Infected: <b>{{ country.TotalConfirmed.toLocaleString() }}</b>
      </p>
      <button class="button" @click="viewDetails(country)">View Details</button>
    </div>
  </div>
</template>

<script>
import Modal from "./Modal";
export default {
  props: ["country"],
  methods: {
    viewDetails(country) {
      this.$modal.show(Modal, { country: country }, { width: "300px" });
    },
  },
};
</script>

<style scoped>
.country-box {
  display: inline-block;
  width: 400px;
  padding: 30px;
  border: 1px solid gray;
  margin: 20px;
  border-radius: 5px;
  box-shadow: 5px 10px gray;
  text-align: center;
}

@media only screen and (max-width: 600px) {
  .country-box {
    width: 200px;
    height: 200px;
  }
}

.button {
  background-color: #F43325 ;
  border: none;
  color: #1a171e;
  padding: 10px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}
</style>
