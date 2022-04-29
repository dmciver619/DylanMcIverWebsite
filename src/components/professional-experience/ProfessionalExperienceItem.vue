<template>
    <div class="row">
        <div class="col-sm-4">
            <h1 class="display-3">{{companyJson.name}}</h1>
        </div>
    </div>
    <div class="row">
        <div class="col-md-2">
            <img :src="loadImg(companyJson.imageSrc)" height="200" width="200" />
        </div>
        <div class="col-lg-10" style="white-space:pre-line;">
            <div v-if="companyJson.responsibilities">
                <h3>Responsibilities</h3>
                {{companyJson.responsibilitiesDescription}}
                <ul>
                    <li v-for="responsibility in companyJson.responsibilities" :key="responsibility">{{responsibility}}</li>
                </ul>
            </div>
            <div v-if="companyJson.achievements">
                <h3>Noteworthy Achievements</h3>
                {{companyJson.achievementsDescription}}
                <ul>
                    <li v-for="achievement in companyJson.achievements" :key="achievement">{{achievement}}</li>
                </ul>
            </div>
        </div>
    </div>
    <div v-if="companyJson.projects" class="row my-3">
        <div v-for="project in companyJson.projects" :key="project.title" :class="'col-md-' + 12 / Object.keys(companyJson.projects).length">
            <CollapsibleDropdown :dropdownJson="project"></CollapsibleDropdown>
        </div>
    </div>
</template>

<script>
    import CollapsibleDropdown from '../../components/dropdowns/CollapsibleDropdown'

    require('../../assets/backgrounds/experience.jpg')

    const images = require.context('../../assets/logos/', false, /\.png$|\.jpg$/)

    export default {
        name: 'ProfessionalExperienceArea',
        components: {
            CollapsibleDropdown
        },
        props: {
            companyJson: {
                type: Object,
                required: true
            }
        },
        methods: {
            loadImg: function (imageUri) {
                return images('./' + imageUri)
            }
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