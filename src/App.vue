<template>
    <NavBar></NavBar>
    <Card type="title" :title="name" :description="titleDescription"></Card>
    <Card type="main" :title="aboutMeTitle" :description="aboutMeDescription"></Card>
</template>

<script>
    import NavBar from './components/NavBar'
    import Card from './components/cards/Card'

    export default {
        name: 'App',
        components: {
            NavBar,
            Card
        },
        data() {
            return {
                name: 'Dylan McIver',
                titleDescription: 'Welcome to my website',
                aboutMeTitle: 'About Me',
                aboutMeDescription: 'About meee'
            }
        }
    }
</script>

<style>
    #app {
      font-family: Avenir, Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
    }

    .card {
        max-width: 1000px;
        margin-top: 40px;
        padding: 10px;
    }
        
</style>
