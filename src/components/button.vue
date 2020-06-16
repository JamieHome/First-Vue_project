<template>
    <div>
        <span class="button" @click="add" :style="{background:background_color,color:color,}">{{id}}</span>
    </div>
</template> 
<script>
export default {
    name:"Button",
    props:['color','background_color'],
    data () {
        return{
            id:111,
            // red_color:"red",
        }
    },
    methods:{
        add:function(){
            this.id = this.id+1;
            console.log(this.id);
        }
    },
    watch:{
        id:function (newQuestion, oldQuestion) {
            console.log("newQuestion",newQuestion);
            console.log("oldQuestion",oldQuestion);
        }
    },
    mounted(){
        console.log("parent",this.$parent)
    }
}
</script> 
<style>
.button{
    padding: 5px 10px;
    border-radius: 5px;
    display: inline-block;
}
</style>
