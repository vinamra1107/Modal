<template>
    <transition name="modal-fade">
        <div class="bg-modal" @click="close">
            <div class="modal-contents" role="dialog"
                aria-labelledby="modalTitle"
                aria-describedby="modalDescription" @click.stop>
                <!-- # components- Header , Body and Footer -->
                <modalheader @close="close"/>
                <modalbody />
                <modalfooter @close="close"/>
            </div>
        </div>
    </transition>
</template>

<script>
import modalheader from './ModalHeader.vue';
import modalbody from './ModalBody.vue';
import modalfooter from './ModalFooter.vue';
export default {
    name: 'modal',
    components:{modalheader, modalbody,modalfooter},
    methods:{
        close(){
            this.$emit('close');
        }
    }
    
}
</script>

<style>
.bg-modal {
    
	position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, 0.6);
    display: flex;
    justify-content: center;
    align-items: center;
}

.modal-contents {
    border-radius: 3%;
	background: #FFFFFF;
    width: auto;
    height: auto;
    max-height: 90%;
    max-width: 60%;
    min-width: 20%;
    box-shadow: 2px 2px 20px 1px;
    overflow-x: auto;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.modal-fade-enter,.modal-fade-leave-active {
    opacity: 0;
  }

.modal-fade-enter-active,.modal-fade-leave-active {
    transition: opacity .3s ease
  }

</style>
