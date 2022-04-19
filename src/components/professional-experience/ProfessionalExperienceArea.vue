<template>
    <div id="experience" class="py-5">
        <div class="container py-3">
            <div class="row">
                <div class="col-lg-12">
                    <h1 class="display-1">Professional Experience</h1>
                </div>
            </div>
            <div v-for="experience in professionalExperiences" :key="experience">
                <div class="row">
                    <div class="col-sm-4">
                        <h1 class="display-3">{{experience.key}}</h1>
                    </div>
                </div>
                <div class="row">
                    <div class="col-md-2">
                        <img src="../../assets/logos/EventMAP_Logo.jpg" height="200" width="200" />
                    </div>
                    <div class="col-lg-10" style="white-space:pre-line;">
                        <div v-if="experience.values.responsibilities">
                            <h3>Responsibilities</h3>
                            During my time at EventMAP, I worked on their two largest software solutions.
                            EventMAP exposed me to:
                            <ul>
                                <li v-for="responsibility in experience.values.responsibilities" :key="responsibility">{{responsibility}}</li>
                            </ul>
                        </div>
                        <div v-if="experience.values.achievements">
                            <h3>Noteworthy Achievements</h3>
                            Notable pieces of work during my time at EventMAP include:
                            <ul>
                                <li v-for="achievement in experience.values.achievements" :key="achievement">{{achievement}}</li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div v-if="experience.values.projects" class="row my-3">
                    <div v-for="project in experience.values.projects" :key="project" :class="'col-md-' + 12 / Object.keys(this.professionalExperiences[0].values.projects).length">
                        <CollapsibleDropdown  :dropdownJson="project"></CollapsibleDropdown>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import CollapsibleDropdown from '../../components/dropdowns/CollapsibleDropdown'
    import WebsiteTextContent from '../../assets/professional-experience'

    require('../../assets/backgrounds/experience.jpg')

    export default {
        name: 'ProfessionalExperienceArea',
        components: {
            CollapsibleDropdown
        },
        data() {
            return {
                professionalExperiences: WebsiteTextContent
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