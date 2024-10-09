<template>
  <header>
    <nav>
      <RouterLink to="/">
        <img src="/youtube.png" alt="logo you tube">
      </RouterLink>
      <form >
        <input type="text" placeholder="Recherche...">
      </form>
      <font-awesome-icon icon="magnifying-glass" />
    </nav>
  </header>
  <RouterView />
</template>

<script>
export default {
  name: 'App',
}
</script>

