<template>
    <div id='clear-button-container' @click='handleButton(value)'>
        Clear
    </div>
</template>

<script>

export default {
    props:['handleButton'],
    name:'clearButton',
    data: function(){
        return{
            value:'clear'
        }
    }
}
</script>

<style scoped>
    #clear-button-container{
        width:20vw;
        height:5vw;
        background:#FF534E;
        color:white;
        border-radius: 10px;
        font-size:30px;
        display:flex;
        justify-content: center;
        align-items: center;
        margin:10px;
        transition:.3s;
    }
    
    #clear-button-container:hover{
        color:deeppink;
        background: darkslateblue;
    }

    #clear-button-container:active{
        transition:.1s;
        border: 2px white solid;
    }
</style>