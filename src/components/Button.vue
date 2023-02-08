<template>
    <button 
    @click="onClick()" 
    :style="{background: color}"
    class="btn" 
    data-bs-target="#collapseTarget" 
    data-bs-toggle="collapse" >
        {{ text }}
    </button>
</template>

<script>
export default {
    name : 'Button',
    props: {
        text: String,
        color: String,
    },
    methods: {
        onClick(){
            this.$emit('btn-click')
        },
    },
}
</script>

<style scoped>
    .btn{
        color:#fff;
        box-shadow: 2px 3px 7px #000;
    }
</style>

