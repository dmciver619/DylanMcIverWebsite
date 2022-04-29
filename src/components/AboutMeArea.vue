<template>
    <div id="aboutMe" class="py-5">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <h1 class="display-1">About Me</h1>
                </div>
            </div>
            <div class="row">
                <div class="col-md-4" style="display: flex; justify-content: center;">
                    <img src="../assets/LinkedIn_ProfilePictureCropped.jpg" width="350" height="350" />
                </div>
                <div class="col-lg-8">
                    <h3>Brief Introduction</h3>

                    <h5>University</h5>
                    <ul>
                        <li>I am a placement student at Queens University Belfast (QUB) studying MEng Software Engineering with Placement Year.</li>
                    </ul>

                    <h5>Current Employment</h5>
                    <ul>
                        <li>Currently I am working at EventMAP in Belfast.</li>
                        <li>I am employed as a full-stack software engineer, I work with the .NET framework</li>
                    </ul>

                    <h5>Who am I</h5>
                    <ul>
                        <li>A full-stack programmer with a passion for learning and writing efficient and clean code</li>
                    </ul>
                    <hr size="5" />
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
    </div>
</template>

<script>
    require('../assets/backgrounds/wp2406589.jpg');

    export default {
        name: 'AboutMeArea',
        data() {
            return {
                img: "../assets/test.jpg"
            }
        }
    }
</script>

<style lang="scss" scoped>
    #aboutMe {
        background-image: url('../assets/backgrounds/wp2406589.jpg');
        background-repeat: no-repeat;
        background-size: 150%;
        padding: 0 50px;
    }

    .list-group-flush > .list-group-item {
        background-color: antiquewhite;
        text-align: left;
    }

    .list-group-flush > .list-group-item:first-of-type {
        background-color: #DE973E;
        border-bottom: 3px black solid;
    }

    img {
        border-radius: 30px;
    }

</style>