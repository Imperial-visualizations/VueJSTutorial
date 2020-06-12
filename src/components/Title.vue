<template>
    <div>
        <h1>{{actualText}}</h1>
        <button @click="resetText">Toggle Text</button>
    </div>
</template>

<script>
export default {
    props:[
        "text"
    ],
    data(){
        return{
            showDefaultText:false,
            defaultText:"Hello I'm the default text"
        }
    },
    methods:{
        resetText(){
            this.showDefaultText = !this.showDefaultText;
        }
    },
    computed:{
       actualText(){
           if(this.showDefaultText){
               return this.defaultText
           } else {
               return this.text
           }
       } 
    }

}
</script>

<style scoped>
h1 {
    font-family: "cursive";
    color:blue;
}
</style>