<template>
  <div class="skills flex-column">
    <form @submit.prevent="addSkill" class="flex">
      <input placeholder="Enter your skills" type="text" v-model="skill" />
      <button>Add</button>
    </form>
    <p>{{ skill }}</p>

    <ul class="flex-column">
      <li v-for="(data, index) in skills" :key="index">
        {{ data.skill }}
        <p v-on:click="remove(index)" class="flex">x</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SkillsTable",
  data() {
    return {
      skill: "",
      skills: [{ skill: "html,css" }, { skill: "vue" }],
    };
  },
  methods: {
    addSkill() {
      if (this.skill.length > 0) {
        this.skills.push({ skill: this.skill });
        this.skill = "";
      }
    },
    remove(id) {
      this.skills.splice(id, 1);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.skills {
  margin: 2rem 0;
}
form {
  width: 85%;
  justify-content: space-between;
}
.skills input {
  border: none;
  width: 100%;
  font-size: 1.4rem;
  padding: 5px;
  color: rgb(56, 10, 45);
}
button {
  background: rgb(56, 10, 45);
  color: white;
  font-size: 1.4rem;
  padding: 3px;
  cursor: pointer;
  transition: all 0.3s;
}
button:hover {
  background: white;
  color: rgb(56, 10, 45);
}
.skills input::placeholder {
  color: rgb(56, 10, 45);
}
.skills ul {
  gap: 3px;
  width: 85%;
  margin: 5px auto;
  /* background: red; */
  list-style: none;
  padding-left: 0;
}
.skills ul li {
  width: 100%;
  background: rgb(56, 10, 45);
  font-size: 1.2rem;
  padding: 5px;
  color: white;
}
li {
  position: relative;
}
li p {
  position: absolute;
  right: 10px;
  bottom: 0;
  font-size: 1.5rem;
  width: 40px;
  height: 30px;
  cursor: pointer;
  background: white;
  color: rgb(56, 10, 45);
  /* padding: 3px; */
  border: 1px solid transparent;
  transition: all 0.3s;
}

li p:hover {
  color: white;
  background: rgb(56, 10, 45);
  border: 1px solid white;
}
</style>
