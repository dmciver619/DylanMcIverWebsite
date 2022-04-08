<template>
    <TitleCard v-if="type == 'title'" :title="title" :description="description" :imageSrc="imageSrc"></TitleCard>
    <MainCard v-else-if="type == 'main'" :title="title" :description="description"></MainCard>
    <div v-else>Error</div>

</template>

<script>
    import TitleCard from './TitleCard'
    import MainCard from './MainCard'
    
    export default {
        name: 'Card',
        components: {
            TitleCard,
            MainCard
        },
        props: {
            type: {
                type: String,
                required: true,
                validator: function (data) {
                    return data == "main" || data == "title";
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

    </style>