<template>
    
  <article class="message" v-show="isVisible">
      
      <div class="message-header">
        {{title}}
        <button type="button" @click="hideModal">x</button>
      </div>

      <div class="message-body">
          {{body}}
      </div>

  </article>
</template>
<script>
  export default {
      data(){
          return{
              isVisible: true
          };
      },
    props:['title','body'],
   
    methods:{
        hideModal(){
            this.isVisible = false;
        }
    }
  }
</script>