<template>
    <div class="backdrop">
        <div class="modal">
            <slot></slot>  
        </div>
    </div>
</template>
<script>
export default {
    methods: {
        closeModal(){
            this.$emit('close')
        }
    }
    
}
</script>

<style scoped>
.modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    border-radius: 10px;
    background: white;
}

.backdrop {
    top: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.507);
    position: fixed;
}
</style>
