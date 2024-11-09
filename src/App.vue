<template>
    <ul>
        <learning-resource v-for="res in storedResources" :key="res.id"
            :title="res.title"
            :description="res.description"
            :link="res.link"
        >
        </learning-resource>
    </ul>
</template>

<script>

import LearningResource from './components/learning-resources/LearningResource.vue';

export default {
    components: {
        LearningResource,
    },
    data() {
        return {
            // Array
            storedResources: [
                // Objects
                {
                    id: 'official-guide',
                    title: 'Official Gudie',
                    description: 'The oficial Vue.js documentation',
                    link: 'https://vue.org',
                },
                {
                    id: 'Google',
                    title: 'Official Google site',
                    description: 'The oficial google documentation',
                    link: 'https://google.com',
                }
            ]
        };
    }
}
</script>

<style>
@import url("http://fonts.googleapis.com/css?family=Roboto' rel='stylesheet' type='text/css'");

* {
    box-sizing: border-box;
}

html {
    font-family: 'Roboto', sans-serif;
}

body {
    margin: 0;
}
</style>