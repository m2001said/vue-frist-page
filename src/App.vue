<template>
  <div>
    <nav class="flex">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </nav>

    <!-- to show routes in all pages -->
    <router-view />
    <!-- <SkillsTable /> -->
  </div>
</template>

<script>
// import SkillsTable from "./components/Skills.vue";

// export default {
//   name: "App",
//   components: {
//     SkillsTable,
//   },
// };
</script>

<style>
* {
  margin: 0;
}
body {
  background: rgb(207, 179, 179);

  margin: 0 auto;
}
.flex,
.flex-column {
  display: flex;
  align-items: center;
  justify-content: center;
}
.flex-column {
  flex-direction: column;
}
nav {
  gap: 2rem;
  background: white;
  padding: 1rem 0;
  box-shadow: 3px 3px 2px 0px rgba(0, 0, 0, 0.3);
}
nav a {
  background: white;
  color: gray;
  font-size: 1.5rem;
  transition: all 0.3s;
  text-decoration: none;
}
nav a:hover {
  color: rgb(177, 153, 153);
}
</style>
