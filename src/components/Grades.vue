<template>
    <div id="grades-input">
        <h1>My Grades</h1>
        <label v-bind:class="{ hide: isHidden }" for="gcount">How Many grades would you like to add?</label>
        <input type="text" id="gcount" v-bind:class="{ hide: isHidden }" v-model="countGrades">
        <p></p>
        <a class="button" v-on:click="addGrades()" v-bind:class="{ hide: isHidden }">Add</a>
        <ul>
            <li v-for="(grade, index) in grades" :key="index">
                <label for="grade"><strong>{{index + 1}}.</strong></label>
                <input id="grade" type="text" v-model="grade.value">
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Grades',
    data(){
        return {
            isHidden: false,
            countGrades: 0,
            grades: []
        }
    },
    methods: {
        addGrades(){
            if(this.countGrades > 0){
                var i;
                for (i = 0; i < this.countGrades; i++) {
                    this.grades.push( {value: 0} );
                }
                this.isHidden = true;
            }
        }
    }
}
</script>

<style>
    .hide{
        display: none
    }
</style>