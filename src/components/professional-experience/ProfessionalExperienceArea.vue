<template>
    <div id="experience" class="py-5">
        <div class="container py-3">
            <div class="row">
                <div class="col-lg-12">
                    <h1 class="display-1">Professional Experience</h1>
                </div>
            </div>
            <div v-for="experience in professionalExperiences" :key="experience">
                <ProfessionalExperienceItem :companyJson="experience"></ProfessionalExperienceItem>
            </div>
        </div>
    </div>
</template>

<script>
    import ProfessionalExperienceContent from '../../assets/json/professional-experience'
    import ProfessionalExperienceItem from '../professional-experience/ProfessionalExperienceItem'

    require('../../assets/backgrounds/experience.jpg')

    export default {
        name: 'ProfessionalExperienceArea',
        components: {
            ProfessionalExperienceItem
        },
        data() {
            return {
                professionalExperiences: ProfessionalExperienceContent
            }
        },
        methods: {
            
        }
    }
</script>

<style lang="scss" scoped>
    #experience {
        background-image: url('../../assets/backgrounds/experience.jpg');
        background-repeat: no-repeat;
        background-size: 150%;
    }

    .collapsing {
        transition: height 0.75s ease-in-out;
    }
</style>