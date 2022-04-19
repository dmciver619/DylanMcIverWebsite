<template>
    <div id="projects" class="py-5">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <h1 class="display-1">Projects</h1>
                </div>
            </div>
            <div class="row">
                <p>
                    During my placement year, I have found myself with more experience and more time
                    to develop my own personal projects.
                    I have so far only written a simple paint-brush project, but as I find myself with more
                    free time, I see myself developing more projects
                </p>
            </div>
            <div class="row">
                <div v-for="project in projectsJson" :key="project.title" class="col-md-4">
                    <Card :title="project.title" :description="project.description" :learningPoints="project.learningPoints" :projectLink="project.projectLink"></Card>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    require('../assets/backgrounds/projects.jpg');

    import Card from './cards/Card'
    import ProjectsJson from '../assets/projects'

    export default {
        name: 'ProjectsArea',
        components: {
            Card
        },
        data() {
            return {
                projectsJson: ProjectsJson
            }
        }
    }
</script>

<style lang="scss" scoped>
    #projects {
        background-image: url('../assets/backgrounds/projects.jpg');
        background-repeat: no-repeat;
        background-size: 150%;
    }


</style>