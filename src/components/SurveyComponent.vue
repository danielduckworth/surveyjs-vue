<template>
    <survey :survey="survey"  />
</template>
<script>
    import Vue from "vue";
    import { StylesManager, Model } from "survey-vue";
    import "survey-vue/defaultV2.css";
    import "./index.css";
    import { json } from "./json";
    StylesManager.applyTheme("defaultV2");
    export default {
        name: "surveyjs-component",
        data() {
            const survey = new Model(json);
            return {
                survey: survey
            };
        }
    };
</script>
<style scoped>
</style>
