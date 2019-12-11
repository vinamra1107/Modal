<template>
    <div class="modal-foot">
        <button type="button" class="btn-continue" @click="close" aria-label="Close modal">Continue</button>
    </div>
</template>

<script>
export default {
    name:'modalfooter',
    methods: {
      close() {
        this.$emit('close');
      }
    }
}
</script>

<style>
.modal-foot{
    padding: 10px;
    display: flex;
     border-top: 1px solid #eeeeee;
    color: #4AAE9B;
    justify-content: flex-end;
}
.btn-continue {
	border: none;
    border-radius: 3px;
    font-size: 14px;
    padding:7px;
    cursor: pointer;
    font-weight: bold;
    background-color: rgb(129, 33, 185);
    color: white;
}
</style>
