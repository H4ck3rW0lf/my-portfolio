<template>
  <div class="container mx-auto p-6 bg-gray-200 min-h-screen text-center">
    <h1 class="text-3xl font-bold">My Projects</h1>
    <p class="mt-4">Click on a project to see the details.</p>

    <ul class="mt-6 list-none">
      <li v-for="project in projects" :key="project.id" class="no-bullets">
        <button @click="selectProject(project)" class="portfolio-button">
          {{ project.name }}
        </button>
      </li>
    </ul>

    <div v-if="selectedProject" class="project-details mt-8 p-6 bg-white shadow-lg rounded-lg">
      <h2 class="text-2xl font-bold">{{ selectedProject.name }}</h2>
      <p class="mt-4">{{ selectedProject.description }}</p>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-6">
        <img v-for="(image, index) in selectedProject.images" :key="index" :src="image" class="w-full h-auto rounded shadow-md" />
      </div>

      <button @click="selectedProject = null" class="portfolio-button mt-6">Close</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          name: "FizzBuzz",
          description: "A C# console program that prints numbers 1 to 100, replacing multiples of 3 with 'Fizz', multiples of 5 with 'Buzz', and multiples of both with 'FizzBuzz'.",
          images: ["/images/FizzBuzz.png", "/images/FizzBuzz1.png"]
        },
        {
          id: 2,
          name: "Workout Diary",
          description: "An MVC training diary where users log exercises, dates, and performance metrics.",
          images: ["/images/TrainingApplication/TDatabase.png", "/images/TrainingApplication/TExerciseM.png", "/images/TrainingApplication/TWorkoutSM.png", "/images/TrainingApplication/TExerciseC.png", "/images/TrainingApplication/TWorkouSC.png", "/images/TrainingApplication/TExercise List.jpeg", "/images/TrainingApplication/TWorkoutS Details.jpeg", "/images/TrainingApplication/TAdd Workout.jpeg", "/images/TrainingApplication/TDelete Workout.jpeg", "/images/TrainingApplication/TDelete Exercise.jpeg"]
        },
        {
          id: 3,
          name: "Recipe Site",
          description: "An MVC web application that stores and displays recipes with images and SQL database integration.",
          images: ["/images/RecipesApplication/RSQLTabel.png", "/images/RecipesApplication/RSQL.png", "/images/RecipesApplication/RDatabase.png", "/images/RecipesApplication/RM.png", "/images/RecipesApplication/RC.png", "/images/RecipesApplication/RIndex.png", "/images/RecipesApplication/RCreate.png", "/images/RecipesApplication/RDetails.png", "/images/RecipesApplication/R Add New.jpeg", "/images/RecipesApplication/R List.jpeg", "/images/RecipesApplication/R Instruktions.jpeg"]
        },
        {
          id: 4,
          name: "Loans Web API",
          description: "An API managing loans with CRUD operations for book borrowing and database integration.",
          images: ["/images/LoansWebAPI/LSQLTabel.png", "/images/LoansWebAPI/LDatabase.png","/images/LoansWebAPI/LM.png", "/images/LoansWebAPI/LC.png", "/images/LoansWebAPI/LStartSida.jpeg", "/images/LoansWebAPI/LGET.jpeg", "/images/LoansWebAPI/LPOST.jpeg", "/images/LoansWebAPI/LGET&LPOST.jpeg", "/images/LoansWebAPI/LGETid.jpeg", "/images/LoansWebAPI/LPUTid.jpeg", "/images/LoansWebAPI/LGETResponse.jpeg", "/images/LoansWebAPI/LDELETEid.jpeg", "/images/LoansWebAPI/LDELETE&LGET.jpeg"]
        }
      ],
      selectedProject: null,
    };
  },
  methods: {
    selectProject(project) {
      this.selectedProject = project;
    }
  }
};
</script>

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

.project-details {
  margin-top: 20px;
  border: 1px solid #ddd;
  padding: 20px;
  background-color: #ffffff;
  max-width: 80%;
  border-radius: 10px;
  margin-left: auto;
  margin-right: auto;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

li.no-bullets {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

img {
  max-width: 100%;
  height: auto;
  margin-top: 10px;
  border-radius: 8px;
  border: 1px solid #ccc;
  transition: transform 0.2s;
}

img:hover {
  transform: scale(1.05);
}
</style>
