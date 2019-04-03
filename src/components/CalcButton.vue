<template>
    <div id='button-container' @click='handleButton(value)'>
        {{value}}
    </div>
</template>

<script>

export default {
    props:['value', 'handleButton'],
    name:'button'
}
</script>

<style>
    #button-container{
        width:5vw;
        height:5vw;
        background:#9FA19E;
        color:white;
        border-radius: 10px;
        font-size:30px;
        display:flex;
        justify-content: center;
        align-items: center;
        margin:10px;
        transition:.3s;
    }

    #button-container:hover{
        color:deeppink;
        background: darkslateblue;
    }

    #button-container:active{
        transition:.1s;
        border: 2px white solid;
    }
</style>
