<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand style="font-family: 'Lilita One', cursive !important;" href="/">
        Kanban
      </b-navbar-brand>
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" v-model="title" placeholder="Title">
            </b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit" @click.prevent="createNew">
              Add
            </b-button>
          </b-nav-form>
        </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'navbar',
  data() {
    return {
      title: '',
    };
  },
  methods: {
    createNew() {
      this.$emit('add', this.title);
      this.title = '';
    },
  },
};
</script>

<style scoped>
/* b-navbar-brand {
  font-family: 'Lilita One', cursive !important;
} */
</style>
