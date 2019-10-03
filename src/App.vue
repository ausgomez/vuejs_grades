<template>
  <div id="app">
    <div class="background">
    </div>
    <div class="container">
        <div class="panel">
          <Grades />
        </div>
        <div class="sub-panel">
            <h1>Average</h1>
            <h3></h3>
            <h1>Highest</h1>
            <h3></h3>
            <h1>Lowest</h1>
            <h3></h3>
            <h1>Middle</h1>
            <h3></h3>
        </div>
    </div>
  </div>
</template>

<script>
import Grades from './components/Grades'

export default {
  name: 'app',
  components: {
    Grades
  }
}
</script>

<style>
*{
    font-family: 'Roboto', sans-serif;
}

div.background{
    background: #0D46FF;
    background: -webkit-linear-gradient(top left, #0D46FF, #41B4FC);
    background: -moz-linear-gradient(top left, #0D46FF, #41B4FC);
    background: linear-gradient(to bottom right, #0D46FF, #41B4FC);
    width: 100%;
    height: 100%;
    position: fixed; 
    z-index: -1;
    left: 0px;
    top: -20%;
    transform: skewY(10deg);
}

div.container{
    display: flex;
    margin: 15% 7% auto;
}

div.panel{
    padding: 10px;
    width: 80%;  /* Or whatever */
    margin-right: 3%;
    color: rgb(77, 75, 75);
    background-color: white;
    border-radius: 5px;
    /*box-shadow: 5px 5px 10px #888888;*/
}

div.sub-panel{
    padding: 10px;
    width: 30%;  /* Or whatever */
    color: rgb(77, 75, 75);
    background-color: white;
    border-radius: 5px;
    border-color: blue;
    
    /*box-shadow: 5px 5px 10px #202020;*/
}

div.grades-input{
    margin-bottom: 5px;
}

input {
    width: 100%;
}

input[type=text] {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    box-sizing: border-box;
    border-radius: 5px;
}

a.button{
    background-color: #2477FD;
    padding: 10px;
    margin-top: 1%;
    color:  white;
    border-radius: 5px;
    cursor: pointer;
}

a.danger{
    background-color: red;
}

ul {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  padding-right: 0;
}

li {
  list-style: none;
  display: inline-block;
  width: calc(100% / 5);
  margin: 1%;
}

</style>
