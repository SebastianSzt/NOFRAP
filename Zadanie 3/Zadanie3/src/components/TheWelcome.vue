<template>
  <div class="home">
    <h1>To jest strona "Home"</h1>
  </div>
</template>

<style>
  .home {
    margin-top: 100px;
    text-align: center;
  }

  @media (min-width: 1024px) {
    .home {
      margin-top: 0;
      min-height: 100vh;
      display: flex;
      align-items: center;
    }
  }
</style>