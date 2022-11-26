<script setup>
import { ref } from 'vue'

// games data
const games = ref([
  {
    id: 0,
    title: "Quixort",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/quixortGameTile_v1.jpg",
  },
  {
    id: 1,
    title: "Nonsensory",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/NS_WebTile_635x291.jpg",
  },
  {
    id: 2,
    title: "Roomerang",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/gameTile_635x291.jpg",
  },
  {
    id: 3,
    title: "Junktopia",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/JunkgameTitle.jpg",
  },
  {
    id: 4,
    title: "Fibbage 4",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2022/09/Fibbage4-tile.jpg",
  },
  {
    id: 5,
    title: "The Wheel Of Enormous Proportions",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/09/WebsiteTileImage_635x291.jpg",
  },
  {
    id: 6,
    title: "The Poll Mine",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/09/Website-Tile-Image.jpg",
  },
  {
    id: 7,
    title: "The Poll Mine",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/09/TPM-Website-Tile.jpg",
  },
  {
    id: 8,
    title: "Job Job",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/10/tile-1x-1.png",
  },
  {
    id: 9,
    title: "Drawful Animate",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/09/DA_TileImage-1.jpg",
  },
  {
    id: 10,
    title: "Blather 'Round",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/BlatherTileImage.jpg",
  },
  {
    id: 11,
    title: "Talking Points",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/Talking-Points-Website-Tile-Image.png",
  },
  {
    id: 12,
    title: "Champ’D Up",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/Website-Tile-Image.jpg",
  },
  {
    id: 13,
    title: "The Devil and the Details",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/Tile-Images.jpg",
  },
  {
    id: 14,
    title: "Quiplash 3",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2020/09/q3_websiteTile_v1.jpg",
  },
  {
    id: 15,
    title: "Push the Button",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/08/TJPP6_PushTheButton.jpg",
  },
  {
    id: 16,
    title: "Dictionarium",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/08/TJPP6_Dictionarium.png",
  },
  {
    id: 17,
    title: "Role Models",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/08/TJPP6_RoleModels.jpg",
  },
  {
    id: 18,
    title: "Joke Boat",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2021/10/tile-1x-1.png",
  },
  {
    id: 19,
    title: "Trivia Murder Party 2",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/08/TMP2_tile.jpg",
  },
  {
    id: 20,
    title: "Zepple Dome",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/ZD-5.jpg",
  },
  {
    id: 21,
    title: "Mad Verse City",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/MVC-4.jpg",
  },
  {
    id: 22,
    title: "Patently Stupid",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/3-PS.png",
  },
  {
    id: 23,
    title: "Split the Room",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/2-STR.png",
  },
  {
    id: 24,
    title: "You Don't Know Jack: Full Steam",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/05/1-YDKJ.png",
  },
  {
    id: 25,
    title: "Civic Doodle",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/CivicDoodle.jpg",
  },
  {
    id: 26,
    title: "Bracketeering",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Bracketeering.jpg",
  },
  {
    id: 27,
    title: "Monster Seeking Monster",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/MonsterSeekingMonster.jpg",
  },
  {
    id: 28,
    title: "Survive the Internet",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/SurviveTheInternet.jpg",
  },
  {
    id: 29,
    title: "Fibbage 3",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Fibbage3_EAU.png",
  },
  {
    id: 30,
    title: "Fakin' It",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_FakinIt.jpg",
  },
  {
    id: 31,
    title: "Tee K.O.",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_TKO.jpg",
  },
  {
    id: 32,
    title: "Guesspionage",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_Guess.jpg",
  },
  {
    id: 33,
    title: "Trivia Murder Party",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_TMP.jpg",
  },
  {
    id: 34,
    title: "Quiplash 2",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/PP3Tile_Quiplash2.jpg",
  },
  {
    id: 35,
    title: "Quiplash XL",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/QuiplashXLtile.jpg",
  },
  {
    id: 36,
    title: "Earwax",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Earwaxtile.jpg",
  },
  {
    id: 37,
    title: "Bomg Corp.",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/BombCorptile.jpg",
  },
  {
    id: 38,
    title: "Bidiots",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Bidiotstile.jpg",
  },
  {
    id: 39,
    title: "Fibbage 2",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Fibbage2tile.jpg",
  },
  {
    id: 40,
    title: "Lie Swatter",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/LieSwattertile.jpg",
  },
  {
    id: 41,
    title: "Word Spud",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/WordSpudtile.jpg",
  },
  {
    id: 42,
    title: "Drawful",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/Drawfultile.jpg",
  },
  {
    id: 43,
    title: "Fibbage XL",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/FibbageXLtile.jpg",
  },
  {
    id: 44,
    title: "You Don't Know Jack 2015",
    thumbnail: "https://jackboxgames.b-cdn.net/wp-content/uploads/2019/06/YDKJ2015tile.jpg",
  }
])
</script>

<template>

</template>

<style scoped>

</style>
