<template>
    <div class="container py-5">
        <div class="row">
            <div class="col-lg-12">
                <h1 class="display-1">Professional Experience</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-sm-4">
                <h1 class="display-3">EventMAP</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-md-2">
                <img src="../assets/EventMAP_Logo.jpg" height="200" width="200" />
            </div>
            <div class="col-lg-10">
                <h3>Responsibilities</h3>
                During my time at EventMAP, I worked on their two largest software solutions.
                EventMAP exposed me to:
                <ul>
                    <li>Developing requests that came direct from customers</li>
                    <li>Approving and suggesting better approaches to code written by other developers</li>
                    <li>Learning how to optimise my code and rewrite code to utilize more performant code</li>
                </ul>

                <h3>Noteworthy Achievements</h3>
                Notable pieces of work during my time at EventMAP include:
                <ul>
                    <li>Securing a graduate job due to outstanding performance.</li>
                    <li>Gave customers ability to create parking space bookings, as well as allowing privileged users to restrict booking users.</li>
                    <li>
                        Worked on Error Handling for Outlook Synchronisation.
                        Customers that create bookings will see their calendar populated, however the Microsoft Graph API will sometimes throw Http error codes that need handled
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ProfessionalExperienceArea'
    }
</script>

<style lang="scss" scoped>
</style>