<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        Modal
      </h1>
      <div class="links">
        <button class="button--green" @click="showModal">
          Click Here!
        </button>
      </div>
      </div>
    <!-- Modal Component -->
    <modal v-show="isModalVisible"
          @close="closeModal"
        />
  </div>
  
</template>

<script>
import Logo from '~/components/Logo.vue';
import modal from '~/components/Modal.vue';

export default {
  components: {
    Logo,
    modal
  },
  data () {
      return {
        isModalVisible: false,
      };
    },
    methods: {
      showModal() {
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      }
    }
      
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: White;
  letter-spacing: 1px;
}


.links {
  padding-top: 15px;
}
button{
  cursor: pointer;
}
</style>
