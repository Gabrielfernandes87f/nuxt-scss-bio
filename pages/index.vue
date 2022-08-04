<template>
  <div>
    <p>{{ cont }}</p>
    <p v-for="todos in feito" :key="todos.id">
      {{ todos.curso }}
      {{ todos.id }}
      {{ todos.done }}
    </p>
    <button @click="finalizar">finalizar</button>
  </div>
</template>
//
<script>
export default {
  name: "IndexPage",
  data() {
    return {
      todos: [],
    };
  },
  created() {
    this.todos = [
      {
        id: "1",
        curso: "vuejs",
        done: true,
      },
      {
        id: "2",
        curso: "angular",
        done: false,
      },
      {
        id: "3",
        curso: "react",
        done: false,
      },
      {
        id: "4",
        curso: "nodejs",
        done: true,
      },
      {
        id: "5",
        curso: "php",
        done: true,
      },
      {
        id: "6",
        curso: "mysql",
        done: true,
      },
      {
        id: "7",
        curso: "mongodb",
        done: false,
      },
      {
        id: "8",
        curso: "html",
        done: true,
      },
      {
        id: "9",
        curso: "css",
        done: true,
      },
      {
        id: "10",
        curso: "javascript",
        done: true,
      },
      {
        id: "11",
        curso: "python",
        done: false,
      },
      {
        id: "12",
        curso: "c++",
        done: false,
      },
      {
        id: "13",
        curso: "c#",
        done: false,
      },
      {
        id: "14",
        curso: "java",
        done: false,
      },
      {
        id: "15",
        curso: "ruby",
        done: false,
      },
      {
        id: "16",
        curso: "php",
        done: true,
      },
      {
        id: "17",
        curso: "python",
        done: false,
      },
      {
        id: "18",
        curso: "c++",
        done: false,
      },
      {
        id: "19",
        curso: "c#",
        done: false,
      },
      {
        id: "20",
        curso: "java",
        done: false,
      },
    ];
  },
  watch: {
    cont(valor) {
      console.log(valor);
    },
  },
  computed: {
    cont() {
      return this.todos.filter((todo) => todo.done).length;
    },
    feito() {
      return this.todos.filter((todo) => todo.done);
    },
  },
  methods: {
    finalizar() {
      this.todos.forEach((todo) => {
        todo.done = true;
      });
    },
  },
};
</script>
