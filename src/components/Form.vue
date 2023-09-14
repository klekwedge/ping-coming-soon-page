<template>
  <form @submit.prevent="onHandleSubmit">
    <input
      type="email"
      v-model="email"
      placeholder="Your email address"
      :class="error && 'border-error'"
    />
    <!-- <ErrorMessage v-if="error" /> -->
    <!-- <Button /> -->
  </form>
</template>
<script setup>
import { ref } from "@vue/reactivity";

const email = ref("");
const error = ref(false);

const onHandleSubmit = () => {
  console.log(email.value);
  if (email.value === "") {
    error.value = true;
  } else {
    error.value = false;
  }
};
</script>
<style scoped>
form {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  position: relative;
}

input {
  border: 1px solid var(--paleBlue);
  width: 300px;
  border-radius: 20px;
  padding: 15px;
  font-size: 16px;
}

input:focus {
  outline-color: var(--blue);
}

input::placeholder {
  color: var(--gray);
}

.border-error {
  border: 1px solid var(--lightRed);
}

@media (max-width: 768px) {
  form {
    flex-direction: column;
  }

  input {
    width: 100%;
  }
}
</style>