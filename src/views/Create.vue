<template>
  <div class="max-v-screen-md mx-auto px-4 py-10">
    <!--Status message-->
    <div v-if="statusMsg || errorMsg" class="mb-10 p-4 bg-light-grey rounded-md shadow-lg">
    <p class="text-at-light-green">
      {{statusMsg}}
      </p>
    <p class="text-red-500">
      {{errorMsg}}
      </p>
    </div>
    <!--Create-->
    <div class="p-8 flex items-start bg-light-grey rounded-md shadow-lg">
    <!--Form-->
    <form class="flex flex-col gap-y-5 w-full">
      <h1 class="text-2xl text-at-light-green">Record workout</h1>
    

      <!--Workout name-->
      <div class="flex flex-col">
      <label for="workout-name" class="mb-1 text-sm text-at-light-green">
        Workout name</label>
        <input 
        type="text" 
        required 
        class="p-2 text-grey-500 focus:outline-none" 
        id="workout-name"
        v-model="workoutName"
        />
      </div>

      <!--Workout type-->
      <div class="flex flex-col">
        <label for="workout-type" class="mb-1 text-sm text-at-light-green">
        Workout type</label>

        <select 
        id="workout-type" 
        class="p-2 text-grey-500 focus:outline-none" 
        required
        v-model="workoutType"
        >
        
        <!--her legger jeg til de forskjellige valuesa her må jeg kanskje adde sirkel og kampsport etterhvert-->
        <option value="select-workout">Select workout</option>
        <option value="strength">Strength training</option>
        <option value="cardio">Cardio</option>
        </select>
      </div>
    </form>
  </div>
</div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: "create",
  setup() {
    // Create data
    const workoutName = ref('');
    const workoutType = ref('select-workout');
    const exercises = ref([]);
    const statusMsg =  ref(null);
    const errorMsg = ref(null);
    // Add exercise

    // Delete exercise

    // Listens for chaging of workout type input

    // Create workout

    return {workoutName, workoutType, exercises, statusMsg, errorMsg};
  },
};
</script>
