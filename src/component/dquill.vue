<template>
    <div>
        <div ref="dquill"></div>
    </div>
</template>

<script>
import Quill from 'quill'

export default {
    name: 'd-quill',
    data(){

    },
    mounted() {
      this.initialize()
    },
    beforeDestroy() {
      this.quill = null
      delete this.quill
    },
    methods:{
        initialize(){
            this.quill = new Quill(this.$refs.dquill)
        }
    }
}
</script>