<template>
  <section>
    <active-users
      :username="users.name"
      :userage="users.age"
    ></active-users>
    <header>Update User</header>
    <user-data @update-user="updateUser"></user-data>
  </section>
</template>

<script>
export default {
  data() {
    return {
      users: 
        {
          name: "John Doe",
          age: 28,
        },
      
    };
  },
  methods: {
    updateUser(name, age) {
      this.users = {
        name: name,
        age: +age,
      };
    },
  },
};
</script>
