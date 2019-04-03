<template>
    <div id='calc-container'>
        <CalcView :display='display'/>
        <div id='buttons-container'>
            <CalcButton v-for='(value,i) in values' :key='i' :value='value' :handleButton='handleButton'/>
            <ClearButton :handleButton='handleButton'/>
        </div>
    </div>
</template>

<script>
import CalcButton from './CalcButton'
import CalcView from './CalcView'
import ClearButton from './ClearButton'

export default {
    name:'Calculator',
    data: function(){
        return{
            values:[7,8,9,'/',4,5,6,'*',1,2,3,'-',0,'.','=','+'],
            display:0,
            input:[]
        }
    },
    methods:{
        handleButton: function(val){
            if(val === 'clear'){
                this.display = 0
                this.input = []
            }else if(val === '='){
                let answer =  eval(this.display)
                this.display = answer
                this.input = []
            }else{
                this.input.push(val)
                this.display = this.input.join('')
            }
        }
    },
    components:{
        CalcButton,
        CalcView,
        ClearButton
    }
}
</script>

<style scoped>
    #calc-container{
        height:80vh;
        width:30vw;
        background: #4E504E;
        border-radius: 20px;
        display:flex;
        flex-direction: column;
        align-items: center;
    }
    #buttons-container{
        display:flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
    }
</style>

