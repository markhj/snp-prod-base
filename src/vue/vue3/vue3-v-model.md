[
  id: vue3-v-model
  tags:
  locations:
]: #

# v-model in Vue3

````jsx
<script>
  export default {
    props: {
      modelValue: Object,
    },
    emits: ['update:modelValue'],
  }
</script>
````

When value is updated:

````jsx
this.$emit('update:modelValue', this.modelValue);
````

> 💁‍♂️ Tip: You can emit from a watcher
