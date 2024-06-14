<template>
    <div>
        <h2>{{ foodName }}
            <img src="/img_quality.svg" v-show="isFavorite">
        </h2>
        <p>{{ foodDesc }}</p>
    </div>
</template>
<script>
    export default{
        props: {
            foodName: {
                type: String,
                required: true
            },
            foodDesc: {
                type: String,
                required: false,
                default: 'Esta e a descricao padrao.',
                validator: function(value){
                    if(20 < value.length && value.length < 50){
                        return true;
                    }else{
                        return false;
                    }
                }
            },
            isFavorite: {
                type: Boolean,
                required: false,
                default: false
            }
        }
        
    }
</script>
<style>
    img{
        height: 1.5em;
        float: right;
    }
</style>