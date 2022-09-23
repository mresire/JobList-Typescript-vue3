<template>
  <div class="app">
    <p>{{ jobs[0].location}}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs} from 'vue';
import Job from './types/Job'

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    // const state = reactive({
    //   name: 'Link',
    //   age: 29 as string | number
    // })

    // state.name = 123 // cannot change type
    // return {
    //   ...toRefs(state)
    // }

    // const name = ref('Link')
    // const age = ref<number | string >(29) 

    // return { name, age}

    const jobs = ref<Job[]>([
      { title: 'DevOps', location: 'Silicon valley', salary: 150000, id:'1'},
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
    ])

    return { jobs}

  }
  // data () {
  //   return {
  //     name: 'Link',
  //     age: 29 as number | string
  //   }
  // },
  // methods: {
  //   changeName(name: string) {
  //     this.name = name;
  //   },
  //   changeAge(age: number | string ) {
  //     this.age = age;
  //   }
  // }
});
</script>

<style>
</style>
