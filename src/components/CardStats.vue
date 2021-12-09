<template>
  <div class="card-stats">
    <div class="card-stats__box" v-for="item in stats" :key="item">
      <h3 class="card-stats_number">{{ item.number }}</h3>
      <div class="card-stats__activity">{{ item.activity }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardStats",
  data(){
    return{
      stats: [
        {
          number: "80K",
          activity: "Followers",
        },
        {
          number: "803K",
          activity: "Likes",
        },
        {
          number: "1.4K",
          activity: "Photos",
        },
      ],
    }
  }
};
</script>

<style scoped>
.card-stats {
  padding: 2.3rem;
  display: flex;
  justify-content: space-around;
}
.card-stats__box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-self: center;
}
.card-stats_number {
  font-size: 1.8rem;
  font-weight: 700;
  color: var(--primary-very-dark-desaturated-blue);
  margin-bottom: 0.6rem;
  text-align: center;
}
.card-stats__activity {
  font-size: 1rem;
  color: var( --primary-dark-grayish-blue);
  text-align: center;
  letter-spacing: 0.2rem;
}
</style>