<template>
    <div class="backdrop">
        <div class="modal">
            <slot></slot>  
        </div>
    </div>
</template>
<script>
export default {
    props: ['header','secondheader']
}
</script>

<style scoped>
h1 {
    color: rgb(128, 57, 194);
}

.modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    border-radius: 10px;
    background: yellow;
}
</style>
