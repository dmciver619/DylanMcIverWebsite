<template>
    <NavBar></NavBar>
    <TitleArea></TitleArea>
    

    <div class="container py-5">
        <div class="row">
            <div class="col-lg-12">
                <h1 class="display-1">About Me</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-md-4">
                <img src="./assets/LinkedIn_ProfilePictureCropped.jpg" width="300" height="300" />
            </div>
            <div class="col-lg-8">
                <br />
                <p>
                    I am a student at Queens University Belfast (QUB) studying MEng Software Engineering with Placement Year.<br />
                    I hope to finish my degree with a 1st Class with Honours.
                </p>
                <p>
                    I have 1 year professional experience.<br />
                    Within this year professional experience, I have been able to achieve a broad skillset; ranging from consuming and testing APIs (such as Microsoft Graph API) to learning recent technologies such as Vue.js
                </p>
            </div>
        </div>
        <br />
        <div class="row">
            <div class="col-md-3">
                <ul class="list-group-flush">
                    <li class="list-group-item">Key features</li>
                    <li class="list-group-item">Focused</li>
                    <li class="list-group-item">Self-Driven</li>
                    <li class="list-group-item">Logical</li>
                    <li class="list-group-item">Team-Player</li>
                    <li class="list-group-item">Conscientious</li>
                </ul>
            </div>
            <div class="col-md-6">
                <ul class="list-group-flush">
                    <li class="list-group-item">Languages/Frameworks</li>
                    <li class="list-group-item">C#</li>
                    <li class="list-group-item">HTML/CSS/JavaScript</li>
                    <li class="list-group-item">Vue.js</li>
                    <li class="list-group-item">Backbone.js</li>
                </ul>
            </div>
            <div class="col-md-3">
                <ul class="list-group-flush">
                    <li class="list-group-item">Random Facts</li>
                    <li class="list-group-item">My favourite animal is a fox</li>
                    <li class="list-group-item">My favourite pizza topping is <a href="#">popcorn chicken</a></li>
                    <li class="list-group-item">My favourite game is Grand Theft Auto: San Andreas</li>
                </ul>
            </div>
        </div>
    </div>

    <hr class="page-breaker" size="5" />


    <div class="container py-5">
        <div class="row">
            <div class="col-lg-12">
                <h1 class="display-1">Experience</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-sm-4">
                <h1 class="display-1">EventMAP</h1>
            </div>
        </div>
        <div class="row">
            <p>
                During my time at EventMAP, I worked on their two largest software solutions.
                EventMAP exposed me to:
            </p>
        </div>
        <div class="row">
            <ul>
                <li>Developing requests that came direct from customers</li>
                <li>Approving and suggesting better approaches to code written by other developers</li>
                <li>Learning how to optimise my code and rewrite code to utilize more performant code</li>
            </ul>
        </div>
        <br />

    </div>

    <hr class="page-breaker" size="5" />
    <div class="container py-5">
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
            <h3>PROJECT GOES HERE</h3>
        </div>
        <br />

    </div>

    <hr class="page-breaker" size="5" />

    <div class="container py-5">
        <div class="row">
            <div class="col-lg-12">
                <h1 class="display-1">Contact Me</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-md-4">
                <p>LinkedIn</p>
            </div>
            <div class="col-md-4">
                <p>GitHub</p>
            </div>
            <div class="col-md-4">
                <p>Email</p>
            </div>
        </div>
    </div>

</template>

<script>
    // Import Components
    import NavBar from './components/NavBar'
    import TitleArea from './components/TitleArea'

    export default {
        name: 'App',
        components: {
            NavBar,
            TitleArea
        }
    }
</script>

<style lang="scss">
    #app {
      font-family: Avenir, Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
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

    .list-group-flush > .list-group-item {
        background-color: none;
        text-align: left;
    }

    .list-group-flush > .list-group-item:first-of-type {
        border-bottom: 3px black solid;
    }
        
</style>
