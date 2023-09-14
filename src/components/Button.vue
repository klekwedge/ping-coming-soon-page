<template>
  <button>Notify me</button>
</template>
<style scoped>
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
  button {
    width: 100%;
  }
}
</style>