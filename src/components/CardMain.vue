<template>
  <main class="main">
    <div class="card">
      <div class="card-img">
        <img src="../assets/bg-pattern-card.svg" alt="background card" />
      </div>
      <div class="card-person">
        <div class="card-person__img">
          <img src="../assets/image-victor.jpg" alt="image person" />
        </div>
        <h2 class="card-person__name">
          {{ person.name
          }}<span class="card-person__age">{{ person.age }}</span>
        </h2>
        <p class="card-person__city">{{ person.city }}</p>
      </div>
      <CardStats />
    </div>
  </main>
</template>

<script>
import CardStats from "./CardStats.vue";
export default {
  components: { CardStats },
  name: "CardMain",
  data() {
    return {
      person: {
        name: "Victor Crest",
        age: "26",
        city: "London",
      },
    };
  },
};
</script>

<style scoped>
.main {
  max-width: 35rem;
  background-color: var(--primary-white);
  border-radius: 1rem;
  overflow: hidden;
  margin: 0 1.5rem;
}
.card-img {
  display: flex;
}
.card-img img {
  width: 100%;
}
.card-person {
  text-align: center;
  position: relative;
  padding: 7.3rem 0 2rem;
  border-bottom: 1px solid #ededed;
}
.card-person__img {
  position: absolute;
  top: 0;
  left: 50%;
  transform: translate(-50%, -50%);
  border: 0.5rem solid var(--primary-white);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}
.card-person__name {
  font-size: 1.8rem;
  color: var(--primary-very-dark-desaturated-blue);
  margin-bottom: 1rem;
}
.card-person__age {
  font-weight: 400;
  margin-left: 1rem;
  color: var(--primary-dark-grayish-blue);
}
.card-person__city {
  font-size: 1.4rem;
  color: var(--primary-dark-grayish-blue);
}
</style>