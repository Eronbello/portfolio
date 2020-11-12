<template>
  <div>
    <Header />
    <Home />
    <About />
    <Portfolio />
    <Contact />
  </div>
</template>

<script>
export default {
  components: {
    header: import('../components/Header'),
    home: import('../components/Home'),
    contact: import('../components/Contact'),
    portfolio: import('../components/Portfolio'),
    about: import('../components/About'),
  },
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Raleway:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
body {
  font-family: 'Raleway', sans-serif;
}
section {
  min-height: 100vh;
}
</style>
