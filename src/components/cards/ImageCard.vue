<template>
    <div class="card mb-3 bg-primary" style="border: black 3px solid">
        <a data-bs-toggle="collapse" :href="'#' + id" class="card-header"  aria-expanded="false" aria-controls="test">
            <h3 class="card-title">{{title}}</h3>
        </a>
        <div :id="id" class="collapsible collapse" style="background-color: darkgray">
            <div class="row">
                <div v-if="imageSrc" class="col-md-2" style="align-self:center">
                    <img :src="mapImageUrl(imageSrc)" />
                </div>
                <div class="col-md-10">
                    <div class="card-body" style="background-color: darkgray">
                        <p class="card-text">{{description}}</p>
                        <p v-if="featuresWorkedOn">
                            I worked on features such as:
                            <ul>
                                <li v-for="feature in featuresWorkedOn" :key="feature">{{feature}}</li>
                            </ul>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    var images = require.context('../../assets/', false, /\.png$/)

    export default {
        name: 'ImageCard',
        data() {
            return {
                toggleCollapse: true
            }
        },
        props: {
            id: {
                type: String,
                required: true,
                validator(value) {
                    return !value.includes(' ');
                }
            },
            title: {
                type: String,
                required: true,
                default() {
                    return ''
                }
            },
            description: {
                type: String,
                required: true
            },
            imageSrc: {
                type: String,
                default() {
                    return null;
                }
            },
            featuresWorkedOn: {
                type: Array,
                default() {
                    return null;
                }
            }
        },
        methods: {
            mapImageUrl: function (relativeUrl) {
                return images('./' + relativeUrl);
            }
        }
    }
</script>

<style lang="scss" scoped>


    img {
        transform: rotate(-90deg) translateY(-50%);
        width: 250px;
    }

    a {
        color:white;

        &:hover {
            color:antiquewhite
        }
    }
</style>