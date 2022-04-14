<template>
    <NavBar></NavBar>
    <TitleArea></TitleArea>
    <AboutMeArea></AboutMeArea>
    <ProfessionalExperienceArea></ProfessionalExperienceArea>
    <ProjectsArea></ProjectsArea>
    <ContactArea></ContactArea>

    

</template>

<script>
    // Import Components
    import NavBar from './components/NavBar'
    import TitleArea from './components/TitleArea'
    import AboutMeArea from './components/AboutMeArea'
    import ProfessionalExperienceArea from './components/ProfessionalExperienceArea'
    import ProjectsArea from './components/ProjectsArea'
    import ContactArea from './components/ContactArea'

    export default {
        name: 'App',
        components: {
            NavBar,
            TitleArea,
            AboutMeArea,
            ProfessionalExperienceArea,
            ProjectsArea,
            ContactArea
        }
    }
</script>

<style lang="scss">
    #app {
      font-family: Avenir, Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      color: #2c3e50;
      overflow-x:hidden;
    }

    p {
        font-size: 15pt;
    }

    hr.page-breaker {
        color: white;
    }

    .container {
        color: white;
    }
            
</style>
