<template>
  <section class="main-information">
    <h1>We are launching <strong>soon!</strong></h1>
    <p>Subscribe and get notified</p>
    <Form />
  </section>
</template>

<script setup>
import Form from "./Form.vue";
</script>

<style scoped>
.main-information {
  text-align: center;
}

h1 {
  font-size: 42px;
  color: var(--gray);
  font-weight: 300;
  letter-spacing: 1px;
  margin: 20px 0;
}

strong {
  color: var(--darkBlue);
  font-weight: 700;
}

p {
  margin: 20px 0;
}

@media (max-width: 768px) {
  h1 {
    font-size: 32px;
  }
}

@media (max-width: 600px) {
  h1 {
    font-size: 25px;
  }
}
</style>