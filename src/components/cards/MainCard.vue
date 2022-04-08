<template>
    <div class="container-sm bg-secondary rounded-3 card main-card">
        <div class="row">
            <h1 class="display-6">{{title}}</h1>
            <hr />
            <p>{{description}}</p>
        </div>
    </div>

</template>

<script>
    export default {
        name: 'MainCard',
        props: {
            title: {
                type: String,
                required: true
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
            }
        }
    }
</script>

<style scoped>
    h1 {
        margin-bottom: 0;
    }

    hr {
        height: 5px;
        max-width: 50%;
        margin: auto;
    }

    p {
        padding: 10px;
    }

</style>