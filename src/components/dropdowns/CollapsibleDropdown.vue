<template>
    <div class="card mb-3 bg-primary" style="border: black 3px solid">
        <a data-bs-toggle="collapse" :href="'#' + dropdownJson.title" class="card-header d-flex" aria-expanded="false" aria-controls="test" style="justify-content:space-between; align-items: center">
            <div style="display:flex;">
                <img :src="loadImg(dropdownJson.imageSrc)" height="30" width="30" style="margin-right: 20px" />
                <h3 class="card-title">{{dropdownJson.title}}</h3>
            </div>
            <i class="fa-solid fa-caret-down"></i>
        </a>
        <div :id="dropdownJson.title" class="collapsible collapse" style="background-color: darkgray">
            <div class="row">
                <div class="col-md-10">
                    <div class="card-body" style="background-color: darkgray">
                        <p class="card-text">{{dropdownJson.description}}</p>
                        <p v-if="dropdownJson.featuresWorkedOn">
                            I worked on features such as:
                            <ul>
                                <li v-for="feature in dropdownJson.featuresWorkedOn" :key="feature">{{feature}}</li>
                            </ul>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    const images = require.context('../../assets/logos/', false, /\.png$|\.jpg$/)

    export default {
        name: 'Card',
        props: {
            dropdownJson: {
                type: Object,
                required: true
            }
        },
        methods: {
            loadImg: function (imageUri) {
                return images('./' + imageUri);
            }
        }
    }
</script>

<style lang="scss" scoped>
    a {
        color: white;
        text-decoration: none;

        i
        {
            font-size: 2em;
        }

        &:hover {
            color: white;
        }
    }

    .card {
        background-color: grey
    }
</style>