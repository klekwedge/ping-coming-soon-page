<template>
  <form @submit.prevent="onHandleSubmit">
    <input
      type="text"
      v-model="email"
      placeholder="Your email address"
      :class="error && 'border-error'"
    />
    <span class="error" v-if="error">Please provide a valid email address</span>
    <button>Notify me</button>
  </form>
</template>

<script setup>
import { ref } from "@vue/reactivity";

const email = ref("");
const error = ref(false);

const onHandleSubmit = () => {
  if (email.value === "" || !/.+@.+\..+/.test(email.value)) {
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

.error {
  position: absolute;
  bottom: -20px;
  left: 10px;
  font-size: 13px;
  font-style: italic;
  color: var(--lightRed);
}

button {
  padding: 15px 40px;
  border-radius: 20px;
  background-color: var(--blue);
  border: none;
  color: var(--white);
  font-weight: 600;
  font-size: 14px;

  box-shadow: 0 0 25px var(--paleBlue);
}

button:hover {
  cursor: pointer;
  background-color: var(--blueHover);
}

@media (max-width: 768px) {
  form {
    flex-direction: column;
  }

  input {
    width: 100%;
  }

  button {
    width: 100%;
  }
}
</style>