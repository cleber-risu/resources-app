<script>
export default {
  props: {
    id: String,
    title: String,
    description: String,
    link: String,
  },
  inject: ['deleteResource'],
};
</script>

<template>
  <li>
    <base-card>
      <div>
        <header>
          <h3>{{ title }}</h3>
          <base-button mode="flat" @click="deleteResource(id)"
            >Delete</base-button
          >
        </header>
      </div>
      <p>{{ description }}</p>
      <nav>
        <a :href="link" target="_blank">View resource</a>
      </nav>
    </base-card>
  </li>
</template>

<style scoped>
li {
  margin: auto;
  max-width: 40rem;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
}

a {
  text-decoration: none;
  color: #ce5c00;
}

a:hover,
a:active {
  color: #c89300;
}
</style>
