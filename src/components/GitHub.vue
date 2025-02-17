<template>
<Header />
  <div class="github">
    <h2>GitHub Projects &#x1F419;</h2>
    <h5>Here are some of my open-source projects</h5>
    <div v-if="loading">Loading...</div>
    <div v-else-if="error">Error: {{ error }}</div>
    <div v-else class="grid-container">
      <div v-for="repo in data" :key="repo.id" class="grid-item">
        <h3>{{ repo.name }}</h3>
        <p>{{ repo.description || "No description available." }}</p>
        <a :href="repo.html_url" target="_blank" class="repo-link">View on GitHub</a>
      </div>
    </div>
   
  </div>
<Footer />
</template>

<script>
import axios from 'axios'; // Import axios
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';

export default {
  components: {
    Header,
    Footer,
  },
  data() {
    return {
      data: [],
      loading: true,
      error: null,
    };
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      try {
        const url = process.env.VUE_APP_GitHub_API_URL;  // Use the correct variable name with the VUE_APP_ prefix
    const token = process.env.VUE_APP_GitHub_API_TOKEN; 
        const response = await axios.get(
          `${url}/users/sarath-sk/repos?type=public`,
          {
            headers: {
              Authorization: `Bearer ${token}`, // Add your token here
            },
          }
        );
        console.log(response.data);
        this.data = response.data;
        this.loading = false;
      } catch (err) {
        console.error('Error fetching data:', err);
        this.error = err.message;
        this.loading = false;
      }
    },
  },
};
</script>


<style scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    color: white;
}

h2{
    color: #72BAA9;
}

.github{
    padding: 5rem;
}

.grid-container{
    display: grid;
    padding: 2rem;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
    justify-content: center;
    margin: 0 5rem;
    align-items: center;
}

h3{
    color: #c7b198;
}

.grid-container > div{
    padding: 2rem;
    text-align: start;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    background-color: #00204a;
    border-radius: 0.5rem;

}
</style>