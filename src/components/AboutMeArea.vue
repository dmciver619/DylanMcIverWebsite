<template>
    <div class="container py-5">
        <div class="row">
            <div class="col-lg-12">
                <h1 class="display-1">About Me</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-md-4">
                <img src="../assets/LinkedIn_ProfilePictureCropped.jpg" width="350" height="350" />
            </div>
            <div class="col-lg-8">
                <p>Brief Introduction</p>
                <ul>
                    <li>I am a placement student at Queens University Belfast (QUB) studying MEng Software Engineering with Placement Year.</li>
                    <li>Currently I am working at EventMAP in Belfast.</li>
                    <li>I am a full-stack software engineer, I work with the .NET framework</li>
                    <li>My favourite pastimes are socializing and video games, my favourite video game of all time being Grand Theft Auto: San Andreas</li>
                </ul>

                <p>Professional Experience</p>
                <ul style="margin-bottom:0;">
                    <li>I have been working at EventMAP full-time for nearly a year as an Intern.</li>
                    <li>During this year I have gained experience of a wide array experience of many technologies, through the company and in my own time. Here are just a few</li>
                </ul>
                <ol style="margin-inline-start:30px;">
                    <li>Consuming and testing APIs, both company-owned APIs and 3rd Party APIs (e.g. Microsoft Graph API)</li>
                    <li>Using frameworks and libraries such as: Vue.js, Underscore.js and Bootstrap</li>
                    <li>Writing cloud-based applications</li>
                </ol>
            </div>
        </div>
        <br />
        <div class="row">
            <div class="col-md-3">
                <ul class="list-group-flush">
                    <li class="list-group-item">Key Personality Features</li>
                    <li class="list-group-item">Focused</li>
                    <li class="list-group-item">Self-Driven</li>
                    <li class="list-group-item">Logical</li>
                    <li class="list-group-item">Team-Player</li>
                    <li class="list-group-item">Conscientious</li>
                </ul>
            </div>
            <div class="col-md-6">
                <ul class="list-group-flush">
                    <li class="list-group-item">Languages/Frameworks Experience</li>
                    <li class="list-group-item">C#</li>
                    <li class="list-group-item">HTML/CSS/JavaScript</li>
                    <li class="list-group-item">Vue.js</li>
                    <li class="list-group-item">Bootstrap</li>
                    <li class="list-group-item">Backbone.js</li>
                </ul>
            </div>
            <div class="col-md-3">
                <ul class="list-group-flush">
                    <li class="list-group-item">Goals</li>
                    <li class="list-group-item">Graduate from Queens University Belfast with a 1st Class Honours</li>
                    <li class="list-group-item">Become a well-rounded cloud developer (Microsoft Azure)</li>
                    <li class="list-group-item">Develop web applications in my free time</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AboutMeArea'
    }
</script>

<style lang="scss" scoped>

    .list-group-flush > .list-group-item {
        background-color: antiquewhite;
        text-align: left;
    }

    .list-group-flush > .list-group-item:first-of-type {
        background-color: #D6994C;
        border-bottom: 3px black solid;
    }
</style>