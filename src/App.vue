<template>
  <div id="app">
    <Header
        :index="questionIndex"
        :max="questionMax"
    />
    <b-container class="bv-example-row" v-if="!correctMode">
        <b-row>
            <b-col sm="6" offset-sm="3">
                <QuestionBox
                    :fnNext="next"
                    :fnFinish="finish"
                    :index="questionIndex"
                />
            </b-col>
        </b-row>
    </b-container>
    <p v-else>Correction</p>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import QuestionBox from './components/QuestionBox.vue'

export default {
    name: 'App',
    components: {
        Header,
        QuestionBox
    },
    data: function() {
        return {
            correctMode: false,
            allowCorrection: true,
            questionIndex: 1,
            questionMax: 20,
            questions: [],
            answers: []
        }
    },
    methods: {
        next() {
            this.questionIndex += this.questionIndex + 1 < this.questionMax + 1 ? 1 : 0;
        },
        finish() {
            this.correctMode = this.allowCorrection ? true : false;
        }
    }
}
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
