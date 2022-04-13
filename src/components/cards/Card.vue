<template>
    <TitleCard v-if="type == 'title'" :title="title" :description="description" :imageSrc="imageSrc"></TitleCard>
    <MainCard v-else-if="type == 'main'" :title="title" :description="description"></MainCard>
    <TestCard v-else>Error</TestCard>

</template>

<script>
    import TitleCard from './TitleCard'
    import MainCard from './MainCard'
    import TestCard from './TestCard'
    
    export default {
        name: 'Card',
        components: {
            TitleCard,
            MainCard,
            TestCard
        },
        props: {
            type: {
                type: String,
                required: true,
                validator: function (data) {
                    return data == "main" || data == "title" || data == "list";
                }
            },
            title: {
                type: String,
                required: true
            },
            description: {
                type: String,
                required: true
            },
            listItems: {
                type: Array,
                default() {
                    return [];
                }
            },
            imageSrc: {
                type: String,
                default() {
                    return "";
                }
            }
        }
    }
</script>

<style scoped>
    h1 {
        margin-bottom: 0;
    }

    </style>