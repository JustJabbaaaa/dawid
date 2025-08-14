<script setup>
  const pageTitle = 'Home';
  useHead({
    title: pageTitle,
  });
</script>

<template>
  <div class="app home">
    <Navbar />
    <Header />
    <About />
    <Whyme />
    <Vision/>
    <Banner/>
    <Contact/>
    <Footer/>
  </div>
</template>