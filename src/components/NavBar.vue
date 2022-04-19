<template>
    <nav id="navBar" class="navbar sticky navbar-expand-lg navbar-dark bg-primary">
        <div class="container-fluid">
            <span class="navbar-brand">Dylan McIver</span>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#aboutMe">About Me</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#experience">Experience</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#projects">Projects</a>
                    </li>
                </ul>
                <form class="d-flex">
                    <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                    <button class="btn btn-outline-success" type="submit">Search</button>
                </form>
            </div>
        </div>
    </nav>
</template>

<script>
    export default {
        name: 'NavBar',
        mounted() {
            window.addEventListener('scroll', this.onScroll);
        },
        methods: {
            onScroll: function () {
                if (window.scrollY > 90) {
                    document.getElementById('navBar').classList.add('fixed-top');
                    // add padding top to show content behind navbar
                    var navbar_height = document.querySelector('.navbar').clientHeight;
                    document.body.style.paddingTop = navbar_height + 'px';
                } else {
                    document.getElementById('navBar').classList.remove('fixed-top');
                    // remove padding top from body
                    document.body.style.paddingTop = '0';
                }
            }
        }
    }
</script>

<style>
</style>