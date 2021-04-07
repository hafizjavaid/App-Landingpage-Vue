<template>
  <!-- - Team Section -->
  <section class="team section_padding">
    <div class="container">
      <Title :text1="text1" :text2="text2" :text3="text3"></Title>

      <div class="row">
        <div
          class="col-md-4 col-lg-3 col-sm-6"
          v-for="team in teams"
          :key="team.img"
        >
          <div class="team_item">
            <img :src="team.img" alt="" />
            <h3>{{ team.namee }}</h3>
            <span>{{ team.type }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- - Team Section -->
</template>

<script>
import Title from "./Common/Title";

export default {
  data() {
    return {
      text1: "Team",
      text2: "Member",
      text3: "",
      teams: [
        {
          img: require("@/assets/img/team/1.jpg"),
          namee: "Hafiz Javaid",
          type: "UI Designer",
        },
        {
          img: require("@/assets/img/team/2.jpg"),
          namee: "Hafiz Javaid",
          type: "UI Designer",
        },
        {
          img: require("@/assets/img/team/3.jpg"),
          namee: "Hafiz Javaid",
          type: "UI Designer",
        },
        {
          img: require("@/assets/img/team/4.jpg"),
          namee: "Hafiz Javaid",
          type: "UI Designer",
        },
      ],
    };
  },
  components: {
    Title,
  },
};
</script>

<style lang="scss" scoped>
/* ======================= Team  */
.team {
  background-color: var(--black-100);
}
.team_item {
  //   margin: 15px;
  box-shadow: var(--shadow-100);
  padding: 30px;
  border-radius: 10px;
}
.team_item h3 {
  font-size: 18px;
  color: var(--black-900);
  font-weight: 500;
  margin: 15px 0 5px;
  text-transform: capitalize;
}
.team_item span {
  display: block;
  font-size: 16px;
  font-weight: 300;
  color: var(--black-400);
  text-transform: capitalize;
}

/* --------- Team */
</style>
