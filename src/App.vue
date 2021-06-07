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
    </footer>
  </div>
</template>

<script>
  import Header from './components/Header'
  import Content from './components/Content'
  import FooterLinks from './components/FooterLinks'

  export default {
    name: 'App',
    components: {
      Header,
      Content,
      FooterLinks

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
