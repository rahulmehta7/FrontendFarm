<template>
    <section>
        <b-field message="What do you want to add?">
            <b-input v-model="value" placeholder="Add the site..." rounded>
            </b-input>
            <p class="control">
                <b-button @click="add()" type="is-primary" label="Add" />
            </p>
        </b-field>
    </section>  
</template>

<script>
export default {
  name: 'InputContainer',
  data(){
      return {
        value: ''
      }
  },
  methods: {
      add()
      {
          this.$emit('emit-to-add', this.value)
      }
  },
}
</script>

<style>
.input-container{
 width: 50%;
}

</style>
