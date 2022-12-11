<template>
  <!-- view-Home-->
  <div class="container">
    <!-- <home-page-action /> -->
    <!-- Цитаты -->
    <div class="mt-2 mb-2">
      <div class="card text-dark bg-light">
        <template v-for="tt in getNextThought()">
          <div class="card-body">
            <img src="/photos/Logo_horizontal_small.jpg" class="rounded float-start me-2 d-none d-lg-block" />
            <h5 class="card-title">Мысли о животных</h5>
            <p class="card-text">
              <span class="font-italic">
                {{ tt.text }}
              </span>
            </p>
            <a href="{{ tt.authorLink }}"
              target="_blank" class="card-link">{{ tt.author}}</a>
            <br /><br />
            <a href="tel:+998909653034" type="button" class="btn btn-primary bt-3 btn-lg" id="liveAlertBtn">
              Звоните на номер: (90) 965 30 34
            </a>
          </div>
        </template>
      </div>
    </div>
    <!-- <div class="container"> -->
    <home-page-carousel />
    <!-- </div> -->
  </div>
</template>

<script setup lang="ts">
import HomePageCarousel from "@/components/HomePageCarousel.vue";
// import HomePageAction from "@/components/HomePageAction.vue";

interface thought {
  text: string;
  author: string;
  authorLink?: string;
}

const thoughtsOfTheGreats: thought[][] = [
  [
    {
      text: "Животные суть не что иное, как прообразы наших добродетелей и пороков, блуждающих пред нашим взором, призраки наших душ...",
      author: "© В. Гюго",
      authorLink: "https://ru.wikipedia.org/wiki/%D0%93%D1%8E%D0%B3%D0%BE,_%D0%92%D0%B8%D0%BA%D1%82%D0%BE%D1%80",
    },
  ],
  [
    {
      text: "Моральный прогресс нации можно измерить тем, как эта нация относится к животным.",
      author: "© Махатма Ганди",
      authorLink: "https://citaty.su/zhivotnye-citaty-i-aforizmy-o-zhivotnyx",
    },
  ],
  [
    {
      text: "Следует спрашивать не о том, могут ли животные мыслить или говорить, а о том, могут ли они страдать.",
      author: "© Иеремия Бентам",
      authorLink: "#https://citaty.su/zhivotnye-citaty-i-aforizmy-o-zhivotnyx",
    },
  ],
  [
    {
      text: "Звери — не братья и не слуги. Это другие расы, вместе с нами пойманные в сеть земного существования.",
      author: "© Генри Бестон",
      authorLink: "https://citaty.su/zhivotnye-citaty-i-aforizmy-o-zhivotnyx",
    },
  ],
];

// Иеремия Бентам

function getNextThought(): thought[] {
  return thoughtsOfTheGreats[Math.floor(Math.random()*thoughtsOfTheGreats.length)];
}
</script>
