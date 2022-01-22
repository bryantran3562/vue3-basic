<template>

<!-- BT - This is exactly the for loop syntax -->

<h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>

<!-- BT - Accessing an array of objects -->

<h2 v-for="fullName in fullNames" :key="fullName.first">{{ fullName.first }} {{ fullName.last }}</h2>

<!-- BT - Array within an objects in an Array -->

<h2 v-for="actor in actors" :key="actor.name">{{ actor.name }}
  <div v-for="movie in actor.movies" :key="movie"> {{ movie }}</div>
</h2>

<!-- BT - Object: Note: value, key, index must be in this order. Otherwise, it will not work -->

<h2 v-for="(value, key, index)  in info" :key="value"> {{ index }} {{ key }} {{ value }} </h2>

</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {

  name: 'App',

  data(){
    return {

        names: ['trong', 'quynh', 'jay'],
        fullNames: [
          {first: 'trong', last: 'tran'},
          {first: 'jay', last: 'tran'},
          {first: 'quynh', last: 'bui'}
        ],
        actors: [
          { name: 'test1',
            movies: ['movie1', 'movies1']
          },
          { name: 'test2',
            movies: ['movie2', 'movie2']
          }
        ],
        info: {
          name: 'trong',
          age: 58,
          sex: 'male'
        }

      }
    }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
