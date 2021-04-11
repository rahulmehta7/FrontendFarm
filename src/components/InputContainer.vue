<template>
    <section>
        <b-field message="What do you want to add?">
            <b-input placeholder="Add the site..." rounded>
            </b-input>
            <p class="control">
                <b-button type="is-primary" label="Add" />
            </p>
        </b-field>
    </section>  
</template>

<script>
export default {
  name: 'InputContainer',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
