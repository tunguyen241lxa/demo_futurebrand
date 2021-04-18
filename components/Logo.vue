<template>
  <div class="future-brand-logo">
    <img src="~/static/img/brand.png" alt="Kitten">

  </div>
</template>

<style lang="scss">
.future-brand-logo {
  display: flex;
  justify-content: center;
  margin-top: 80px;

  img {
    width: 50%;
  }
}

.NuxtLogo {
  animation: 1s appear;
  margin: auto;
}

@keyframes appear {
  0% {
    opacity: 0;
  }
}
</style>
