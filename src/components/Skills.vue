<template>
  <div class="skills flex-column">
    <input placeholder="Enter your skills" type="text" />

    <ul class="flex-column">
      <li>lakssfhgd</li>
      <li>lakssfhgd</li>
      <li>lakssfhgd</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SkillsTable",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.skills {
  margin: 2rem 0;
}
.skills input {
  border: none;
  width: 85%;
  font-size: 1.4rem;
  padding: 5px;
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
</style>
