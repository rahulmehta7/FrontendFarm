<template>
    <section>
        <b-field message="What do you want to add?">
            <b-input v-model="value" placeholder="Add the site..." rounded>
            </b-input>
            <p class="control">
                <b-button type="is-primary" label="Add" />
            </p>
        </b-field>
        <div>{{ value }} </div>
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
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
