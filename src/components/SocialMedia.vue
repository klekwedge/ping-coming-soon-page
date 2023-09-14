<template>
  <section class="icons">
    <a href="/">
      <i class="bx bxl-github bx-md"></i>
    </a>
    <a href="/">
      <i class="bx bxl-linkedin-square bx-md"></i>
    </a>
    <a href="/">
      <i class="bx bxl-instagram bx-md"></i>
    </a>
  </section>
</template>

<style scoped>
.icons {
  display: flex;
  gap: 1.5rem;
}

a {
  color: var(--blue);
  border: solid 1px var(--paleBlue);
  border-radius: 35px;
  height: 45px;
  width: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  box-shadow: 0 0 25px var(--paleBlue);
}

a:hover {
  color: var(--white);
  background-color: var(--blue);
}
</style>