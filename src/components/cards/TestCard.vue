<!-- Mini Card -->
<template>
    <div class="multi-card-row row">
        <div class="container-sm bg-secondary rounded-3 card main-card">
            <h3>Back-end Languages</h3>

            <div class="row">
                <ul class="list-group-flush">
                    <li class="list-group-item">C#</li>
                    <li class="list-group-item">Java</li>
                    <li class="list-group-item">C++</li>
                </ul>
            </div>
        </div>
        <div class="container-sm bg-secondary rounded-3 card main-card">
            <h3>Front-end Technologies</h3>

            <div class="row">
                <ul class="list-group-flush">
                    <li class="list-group-item">HTML/CSS/JavaScript</li>
                    <li class="list-group-item">Vue</li>
                    <li class="list-group-item">Backbone</li>
                </ul>
            </div>
        </div>
        <div class="container-sm bg-secondary rounded-3 card main-card">
            <div class="row">
                <h1 class="display-6">{{title}}</h1>
                <hr />
                <div class="col-sm-4">Test1</div>
                <div class="col-sm-4">Test2</div>
                <div class="col-sm-4">Test3</div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ColumnCard',
        props: {
            title: {
                type: String,
                required: true
            },
            description: {
                type: String,
                required: true
            },
            numberOfColumns: {
                type: Number,
                required: true
            },
            imageSrc: {
                type: String,
                default() {
                    return "";
                }
            }
        },
        mounted() {
            this.bootstrapColumnNumber = 12 / this.numberOfColumns;
        }
    }
</script>

<style lang="scss" scoped>
    .container-sm {
        width: 25%;
        margin: 40px 10px;
    }

    .multi-card-row {
        justify-content: center;
    }
</style>