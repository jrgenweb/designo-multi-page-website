<script setup>
useHead({
  title: 'Designo - Home'
})
</script>

<template>
  <div>
    <main>
      <Navbar></Navbar>
      <NuxtPage></NuxtPage>
    </main>
    <Footer></Footer>
  </div>
</template>

<style scoped>
main {
  max-width: 1190px;
  padding-inline: 40px;
  margin: 0 auto;
}

@media screen and (max-width:768px) {
  main {
    padding-inline: 24px;
  }
}
</style>
