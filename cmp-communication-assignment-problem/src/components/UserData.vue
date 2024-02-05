<template>
  <form @submit.prevent="updateUser">
    <div>
      <label for="">Name</label>
      <input type="text" v-model="enteredName" />
    </div>
    <div>
      <label for="">Age</label>
      <input type="text" v-model="enteredAge" />
    </div>
    <div>
      <button>Update User</button>
    </div>
  </form>
</template>

<script>
export default {
  emits: ["update-user"],
  data() {
    return {
      enteredAge: "",
      enteredName: "",
    };
  },
  methods: {
    updateUser() {
      this.$emit("update-user", this.enteredName, this.enteredAge);
    //   this.enteredName = '',
    //   this.enteredAge = ''
    },
  },
};
</script>
