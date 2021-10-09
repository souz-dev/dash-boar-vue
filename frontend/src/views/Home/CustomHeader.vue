<template>
  <header class="header">
    <div class="header_container">
      <div class="class-teste">
        <div class="w-28 lg:w-36">
          <img
            class="w-full"
            src="../../assets/images/logo_white.png"
            alt="logo-feedbacks"
          />
        </div>
        <div class="flex">
          <button @click="() => emit('create-account')" class="invisible-button">Crie uma conta</button>
          <button @click="() => emit('login')" class="button">Entrar</button>
        </div>
      </div>
      <div class="flex flex-col mt-28">
        <h1 class="text-4xl font-black text-white">
          Tenha um feedback. <br />
          E faça seus clientes mais <br class="hidden lg:inline-block" />
          felizes!
        </h1>
        <p class="text-lg font-black text-white">
          Receba ideias, reclamações e feedbacks com um
          <br class="hidden lg:inline-block" />
          simples widget na página.
        </p>
        <div>
          <button class="mt-10 button">Crie uma conta grátis</button>
        </div>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  setup (_, { emit }) {
    return { emit }
  }
}
</script>
<style lang="postcss" scoped>
.class-teste {
  @apply flex
  items-center
  justify-between
  py-10
}
.header_container {
  @apply flex
  flex-col
  w-4/5
  max-w-6xl;
}
.header {
  @apply bg-brand-main
  w-full
  flex
  justify-center;
  height: 700px;
}
.button {
  @apply px-6 py-2
  font-bold
  bg-white
  rounded-full
  text-brand-main
  focus:outline-none;
}
.invisible-button {
  @apply px-6 py-2
  font-bold
  text-white
  rounded-full
  focus:outline-none;
}

@media (min-width: 640px) {
  .header_container {
    background-image: url(../../assets/images/blue_balloons.png);
    background-size: 628px;
    background-position: 90% 100%;
    background-repeat: no-repeat;
  }
}
</style>
