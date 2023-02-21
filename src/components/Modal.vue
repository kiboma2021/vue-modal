<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{sale: theme=='sale'}">
            <slot></slot>  
        </div>
    </div>
</template>
<script>
export default {
    props: ['theme'],
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

.modal.sale {
    background-color: greenyellow;
    color: black;
}
</style>
