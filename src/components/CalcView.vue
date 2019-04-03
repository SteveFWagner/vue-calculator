<template>
    <div id='view-container'>
        {{display}}
    </div>
</template>

<script>
export default {
    props:['display'],
    name:'CalcView'
}
</script>

<style>
    #view-container{
        width:20vw;
        height:10vh;
        background:#397D34;
        color:#29F81A;
        font-size:2em;
        border-radius: 10px;
        margin-top:4vh;
        display:flex;
        align-items: center;
        justify-content: flex-end;
        padding:5px;
        overflow:hidden;
    }
</style>

