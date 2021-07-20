<template>
  <div modal="true">
    <div>
      <div v-if="visible" :data-modal="name" class="modal">
        <div
          aria-modal="true"
          data-reach-dialog-content="true"
          tabindex="-1"
          class="modal__mask"
        >
          <div class="modal__body">
            <slot :payload="payload" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VModal from './handle'
export default {
  
  props: {
    name: {
      type: string,
      require: true
    }
  },
  data() {
    return {
      payload: null,
      visible: false
    }
  },
  beforeMount() {
    //open event
    VModal.EventBUs.$on('open', param => {
      if(this.name === params.name) {
        this.open(params)
      }
    })
    //close event
    VModal.EventBUs.$on('close', param => {
      if(this.name === params.name) {
        this.close(params)
      }
    })
  },
  methods: {
    close(params) {
      this.visible = false
    },
    open(params) {
      this.visible = true
    }
  },
  
}
</script>