<template>
    <div>
        <div>12333333333333333{{ifds}}{{title}}{{data_lj}}{{countNum}})</div>
        <!-- <el-button>1111222</el-button>  -->
    </div>
    
</template>  
<script>
    export default {
        name: 'Good',
        props: ['title','data_lj'],
        data () {
            return{
                ifds:'qqqq1',
                count:12,
                // Title:this.title,
                // Data_lj:this.data_lj
            }
            
        },
        methods:{
            
        },
        mounted(){
            console.log(this.$route.query);
        },
        computed:{
            countNum:function(){
                return this.count+1
            }
        }
    }

</script>