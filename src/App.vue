<template>
  <div id="app">
    <header>
      <Header/>
    </header>

    <main>
      <Content/>
    </main>

    <footer>
      <FooterLinks/>
      <Social/>
    </footer>
  </div>
</template>

<script>
  import Header from './components/Header'
  import Content from './components/Content'
  import FooterLinks from './components/FooterLinks'
  import Social from './components/Social'

  export default {
    name: 'App',
    components: {
      Header,
      Content,
      FooterLinks,
      Social

  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

</style>
