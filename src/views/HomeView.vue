<template>
  <div class="container mx-auto p-6 bg-gray-200 min-h-screen flex flex-col items-center justify-center text-center">
    <h1 class="text-3xl font-bold">Welcome to My Portfolio</h1>
    <p class="mt-4 text-lg">Explore my projects and skills.</p>

    <img alt="Daria" src="../assets/DB.jpg" class="w-48 h-48 rounded-full mx-auto mt-4 shadow-lg">

    <div class="mt-6 max-w-2xl">
      <h2 class="text-2xl font-bold">About Me</h2>
      <p class="mt-2 text-lg">
        My name is Daria. I am currently learning programming and do not have much experience yet, but I am excited to start an internship soon.<br>
        I come from Poland and moved to Sweden in 2016. I am a certified graphic designer, but I have developed a strong interest in coding.<br>
        I believe programming is a fantastic way to practice logical thinking and analytical skills, which I absolutely love.
      </p>
    </div>

    <router-link to="/portfolio" class="portfolio-button mt-6">Take me to Portfolio</router-link>
  </div>
</template>

<style scoped>
.centered-image {
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.portfolio-button {
  background-color: #62de66;
  padding: 16px 20px;
  border-radius: 8px;
  margin-bottom: 5px;
  display: inline-block;
  text-align: center;
  width: auto;
  text-decoration: none;
  color: black;
  font-weight: bold;
  font-size: 18px;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.portfolio-button:hover {
  background-color: #4caf50;
  transform: scale(1.1);
}

p {
  font-size: 18px;
  line-height: 1.6;
}
</style>
