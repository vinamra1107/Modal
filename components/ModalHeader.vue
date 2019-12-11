<template>
    <div class="modal-head">
        <p>Modal Title</p>
        <button type="button" class="btn-close" @click="close" aria-label="Close modal">x</button>
    </div>
</template>

<script>
export default {
    name:'modalheader',
    methods: {
      close() {
        this.$emit('close');
      }
    }
}
</script>

<style>
.modal-head{
    padding: 10px;
    display: flex;
     border-bottom: 1px solid #eeeeee;
    color: #4AAE9B;
    justify-content: space-between;
}
p{
    padding: 5px;
}
.btn-close {
	border: none;
    font-size: 20px;
    padding: 5px;
    cursor: pointer;
    font-weight: bold;
    color: rgb(32, 13, 13);
    background: transparent;
}
</style>
