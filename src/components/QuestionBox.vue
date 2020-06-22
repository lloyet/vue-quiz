<template>
    <div>
        <b-jumbotron>
            <template v-slot:lead>
                Question
            </template>
            <hr class="my-4">
            <p>Answers ...</p>
            <b-button @click="fnNext()" v-if="index < 20" variant="primary" href="#">Next</b-button>
            <b-button @click="fnFinish()" v-else variant="success" href="#">Finish</b-button>
        </b-jumbotron>
    </div>
</template>

<script>
export default {
    name: 'QuestionBox',
    props: {
        fnNext: Function,
        fnFinish: Function,
        index: Number,
    },
    methods: {
        test() {
            console.log('hello world !')
        }
    }
}
</script>

<style scoped>
</style>
