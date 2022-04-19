<template>
    <NavBar></NavBar>
    <TitleArea></TitleArea>
    <AboutMeArea class="section"></AboutMeArea>
    <hr size="5" />
    <ProfessionalExperienceArea class="section"></ProfessionalExperienceArea>
    <hr size="5" />
    <ProjectsArea class="section"></ProjectsArea>
    <hr size="5" />
    <ContactArea class="section"></ContactArea>



</template>

<script>
    // Import Components
    import NavBar from './components/NavBar'
    import TitleArea from './components/TitleArea'
    import AboutMeArea from './components/AboutMeArea'
    import ProfessionalExperienceArea from './components/professional-experience/ProfessionalExperienceArea'
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

    .fa-brands {
        color: black;
    }

    p {
        font-size: 15pt;
    }

    hr {
        margin: 0 !important;
        color:white !important;
    }

    hr.page-breaker {
        color: white;
    }

    .container {
        color: white;
        border-radius: 20px;
        padding: 2rem !important;
        margin: 3em 0;
        background-color: rgba(128, 128, 128, 0.95);
    }            
</style>
