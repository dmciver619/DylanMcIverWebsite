<template>
    <div id="contact" class="py-5">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <h1 class="display-1">Contact Me</h1>
                </div>
            </div>
            <div class="row">
                <div class="col-md-4">
                    <i class="fa-brands fa-linkedin" /><a href="https://www.linkedin.com/in/dylan-mciver-824152196/" target="_blank" rel="noopener noreferrer">LinkedIn</a>
                    <p>For connecting with me and what I am interested in</p>
                </div>
                <div class="col-md-4">
                    <i class="fa-brands fa-github" /><a href="https://github.com/dmciver619" target="_blank" rel="noopener noreferrer">GitHub</a>
                    <p>For following me and projects I am working on</p>
                </div>
                <div class="col-md-4">
                    <i class="fa-solid fa-envelope" /><a href="mailto:dmciver619@live.com">Email</a>
                    <p>For getting in contact with me</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    require('../assets/backgrounds/contact-me.jpg');

    export default {
        name: 'ProjectsArea'
    }
</script>

<style lang="scss" scoped>
    #contact {
        background-image: url('../assets/backgrounds/contact-me.jpg');
        background-repeat: no-repeat;
    }

    i {
        color: black;
        padding-right: 5px;
        font-size: 150%;
    }

    a {
        font-size: 150%
    }
</style>