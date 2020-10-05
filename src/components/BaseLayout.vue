<template>
  <div>
    <header>
      <h1><slot name="header"> </slot></h1>
    </header>
    <main><slot></slot></main>
    <footer>
      <h2><slot name="footer"></slot></h2>
    </footer>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
