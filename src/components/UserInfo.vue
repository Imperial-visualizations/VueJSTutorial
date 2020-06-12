<template>
    <div class="user-box">
        <p>User name: <strong>{{username}}</strong></p>
        <p>Name: <strong>{{fullName}}</strong></p>
        <input @input="$emit('usernamechange',$event.target.value)">
    </div>
</template>

<script>
export default {
    model:{
        prop:"username",
        event:"usernamechange"
    },
    props:{
        username:{
            type:String,
            required:true
        },
        fullName:{
            type:String,
            default:"Name not provided"
        },
        nameChangeCallback:Function
    },
    methods:{

    }
}
</script>

<style>
.user-box{
    border: 2px solid #777;
    background-color:#bbb;
    text-align: left;
    margin: 0 150px;
    padding: 0px 10px;
    box-shadow: #aaa 1px 1px 10px 3px;
}
</style>