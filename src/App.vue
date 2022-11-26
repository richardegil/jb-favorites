<template>
  <h1>Rank Your Favorite Jackbox Games</h1>

  // test drop-zone
  <section class="ranking--container">
    <div class="heading">
      <h2>Love it</h2>
    </div>
    <div class="drop-zone">
      <div class="game drag-element" v-for="{id, title, thumbnail} in getList(2)" :key="id">
        <p>{{ title }}</p>
        <img :src="thumbnail" :alt=title>
      </div>
    </div>
  </section>

  <section class="games--container drop-zone">
    <div class="game drag-element" v-for="{id, title, thumbnail} in getList(1)" :key="id">
      <p>{{ title }}</p>
      <img :src="thumbnail" :alt=title>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// games data
const games = ref([
  {
    id: 0,
    title: "Quixort",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/quixortGameTile_v1.jpg",
    list: 1
  },
  {
    id: 1,
    title: "Nonsensory",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/NS_WebTile_635x291.jpg",
    list: 2
  },
  {
    id: 2,
    title: "Roomerang",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/gameTile_635x291.jpg",
    list: 1
  },
  {
    id: 3,
    title: "Junktopia",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/JunkgameTitle.jpg",
    list: 1
  },
  {
    id: 4,
    title: "Fibbage 4",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/Fibbage4-tile.jpg",
    list: 1
  },
  {
    id: 5,
    title: "The Wheel Of Enormous Proportions",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/09/WebsiteTileImage_635x291.jpg",
    list: 1
  },
  {
    id: 6,
    title: "The Poll Mine",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/09/Website-Tile-Image.jpg",
    list: 1
  },
  {
    id: 7,
    title: "The Poll Mine",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/09/TPM-Website-Tile.jpg",
    list: 1
  },
  {
    id: 8,
    title: "Job Job",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/10/tile-1x-1.png",
    list: 1
  },
  {
    id: 9,
    title: "Drawful Animate",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/09/DA_TileImage-1.jpg",
    list: 1
  },
  {
    id: 10,
    title: "Blather 'Round",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/BlatherTileImage.jpg",
    list: 1
  },
  {
    id: 11,
    title: "Talking Points",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/Talking-Points-Website-Tile-Image.png",
    list: 1
  },
  {
    id: 12,
    title: "Champ’D Up",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/Website-Tile-Image.jpg",
    list: 1
  },
  {
    id: 13,
    title: "The Devil and the Details",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/Tile-Images.jpg",
    list: 1
  },
  {
    id: 14,
    title: "Quiplash 3",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/q3_websiteTile_v1.jpg",
    list: 1
  },
  {
    id: 15,
    title: "Push the Button",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/08/TJPP6_PushTheButton.jpg",
    list: 1
  },
  {
    id: 16,
    title: "Dictionarium",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/08/TJPP6_Dictionarium.png",
    list: 1
  },
  {
    id: 17,
    title: "Role Models",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/08/TJPP6_RoleModels.jpg",
    list: 1
  },
  {
    id: 18,
    title: "Joke Boat",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/10/tile-1x-1.png",
    list: 1
  },
  {
    id: 19,
    title: "Trivia Murder Party 2",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/08/TMP2_tile.jpg",
    list: 1
  },
  {
    id: 20,
    title: "Zepple Dome",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/ZD-5.jpg",
    list: 1
  },
  {
    id: 21,
    title: "Mad Verse City",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/MVC-4.jpg",
    list: 1
  },
  {
    id: 22,
    title: "Patently Stupid",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/3-PS.png",
    list: 1
  },
  {
    id: 23,
    title: "Split the Room",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/2-STR.png",
    list: 1
  },
  {
    id: 24,
    title: "You Don't Know Jack: Full Steam",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/1-YDKJ.png",
    list: 1
  },
  {
    id: 25,
    title: "Civic Doodle",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/CivicDoodle.jpg",
    list: 1
  },
  {
    id: 26,
    title: "Bracketeering",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Bracketeering.jpg",
    list: 1
  },
  {
    id: 27,
    title: "Monster Seeking Monster",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/MonsterSeekingMonster.jpg",
    list: 1
  },
  {
    id: 28,
    title: "Survive the Internet",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/SurviveTheInternet.jpg",
    list: 1
  },
  {
    id: 29,
    title: "Fibbage 3",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Fibbage3_EAU.png",
    list: 1
  },
  {
    id: 30,
    title: "Fakin' It",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_FakinIt.jpg",
    list: 1
  },
  {
    id: 31,
    title: "Tee K.O.",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_TKO.jpg",
    list: 1
  },
  {
    id: 32,
    title: "Guesspionage",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_Guess.jpg",
    list: 1
  },
  {
    id: 33,
    title: "Trivia Murder Party",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_TMP.jpg",
    list: 1
  },
  {
    id: 34,
    title: "Quiplash 2",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_Quiplash2.jpg",
    list: 1
  },
  {
    id: 35,
    title: "Quiplash XL",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/QuiplashXLtile.jpg",
    list: 1
  },
  {
    id: 36,
    title: "Earwax",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Earwaxtile.jpg",
    list: 1
  },
  {
    id: 37,
    title: "Bomg Corp.",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/BombCorptile.jpg",
    list: 1
  },
  {
    id: 38,
    title: "Bidiots",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Bidiotstile.jpg",
    list: 1
  },
  {
    id: 39,
    title: "Fibbage 2",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Fibbage2tile.jpg",
    list: 1
  },
  {
    id: 40,
    title: "Lie Swatter",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/LieSwattertile.jpg",
    list: 1
  },
  {
    id: 41,
    title: "Word Spud",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/WordSpudtile.jpg",
    list: 1
  },
  {
    id: 42,
    title: "Drawful",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Drawfultile.jpg",
    list: 1
  },
  {
    id: 43,
    title: "Fibbage XL",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/FibbageXLtile.jpg",
    list: 1
  },
  {
    id: 44,
    title: "You Don't Know Jack 2015",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/YDKJ2015tile.jpg",
    list: 1
  }
])

// method to get all the items that belong to a list
const getList = (list) => {
  return games.value.filter((item) => item.list == list)
}

</script>

<style scoped>

section {
  padding: 0rem 0 4rem;
}
.ranking--container {
    display: grid;
    grid-template-columns: 100px 1fr;
    grid-template-rows: auto;
    grid-template-areas: 'heading drop';
    width: 100%;
    max-width: 1200px;
    min-height: 100px;
    outline: 1px solid pink;
  }

  .ranking--container .heading {
    grid-area: heading;
    writing-mode: vertical-lr;
  }

  .ranking--container .heading h2 {
    rotate: 180deg;
  }

  .ranking--container .drop-zone {
    grid-area: drop;
    background-color: grey;
  }
  .games--container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-evenly;
    gap: 1rem;
    width: 100%;
    max-width: 1200px;
    height: auto;
    outline: 1px solid red;
  }

  .game {
    display: flex;
    flex-direction: column-reverse;
    flex: 0 0 18%;
    width: 100%;
    height: auto;
  }

  .game img {
    width: 100%;
    max-width: 100%;
    height: auto;
  }
</style>
