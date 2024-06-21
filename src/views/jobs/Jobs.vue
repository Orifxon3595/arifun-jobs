<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <router-link :to="{name: 'JobDetails', params: {id: job.id}}">
      <h2>{{job.title}}</h2>
    </router-link>
  </div>
</template>

<script>

export default {
    data(){
        return{
            jobs: [
                {title: 'JS developer', id: 1, details: 'lorem'},
                {title: 'React developer', id: 2, details: 'lorem'},
                {title: 'Vue developer', id: 3, details: 'lorem'}
            ]
        }
    }
}
</script>

<style>

</style>