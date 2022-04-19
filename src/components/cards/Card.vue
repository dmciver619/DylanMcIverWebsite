<template>
    <div @click="click" class="card mb-3 bg-primary">
        <div v-on:click="click" class="card-header">
            <h3 class="card-title">{{title}}</h3>
        </div>
        <div class="card-body">
            <p class="card-text">{{description}}</p>
            <p v-if="learningPoints">
                In this project, I learnt:
                <ul>
                    <li v-for="learningPoint in learningPoints" :key="learningPoint">{{learningPoint}}</li>
                </ul>
            </p>
        </div>
        <div v-if="projectLink" class="card-footer">
            <i class="fa-brands fa-github" /> <a :href="projectLink">Link to {{title}} source code</a>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Card',
        props: {
            title: {
                type: String,
                required: true
            },
            description: {
                type: String,
                required: true
            },
            learningPoints: {
                type: Array,
                default() {
                    return null;
                }
            },
            projectLink: {
                type: String,
                default() {
                    return null;
                }
            }
        },
        methods: {
            click: function () {
                debugger;
            }
        }
    }
</script>

<style scoped>
    .card {
        border: black 3px solid;
    }

    .card-body,
    .card-footer {
        background-color: darkgray
    }
</style>