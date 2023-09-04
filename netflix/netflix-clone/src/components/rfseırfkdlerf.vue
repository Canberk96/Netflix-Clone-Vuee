<template>
    <div class="fixed w-full h-screen bg-black">
      <div
        id="SideNav"
        class="flex z-40 items-center w-[120px] h-screen bg-black relative"
      >
        <img class="absolute top-0 w-[35px] mt-10 ml-10" src="netflix-logo.png" />
        <div>
          <div class="py-2 mx-10 my-6">
            <Magnify fillColor="#FFFFFF" :size="40" class="cursor-pointer" />
          </div>
          <div class="py-2 mx-10 my-6 border-b-4 border-b-red-500">
            <HomeOutLine fillColor="#FFFFFF" :size="40" class="cursor-pointer" />
          </div>
          <div class="py-2 mx-10 my-6">
            <TrendingUp fillColor="#FFFFFF" :size="40" class="cursor-pointer" />
          </div>
          <div class="py-2 mx-10 my-6">
            <Television fillColor="#FFFFFF" :size="40" class="cursor-pointer" />
          </div>
          <div class="py-2 mx-10 my-6">
            <MovieOutLine fillColor="#FFFFFF" :size="40" class="cursor-pointer" />
          </div>
          <div class="py-2 mx-10 my-6">
            <Plus fillColor="#FFFFFF" :size="40" class="cursor-pointer" />
          </div>
        </div>
      </div>
      <div>
        <div
          class="fixed flex z-20 top-0 right-0 w-full h-[50%] bg-black pl-[120px] bg-clip-border"
        >
          <div class="flex flex-col">
            <div
              class="z-40 text-white w-[53%] pt-20 text-[55px] font-semibold font-serif"
            >
              {{ selectedFilm.title }}
            </div>
            <div  class="pt-14 text-xl text-white font-semibold font-serif">
              {{ selectedFilm.description }}
            </div>
            <div
              class="top-[12px] text-[40px] text-white font-semibold font-serif"
            >
              {{ selectedFilm.year }}
            </div>
          </div>
  
          <video
            ref="videoPlayer"
            controls
            class="z-0 h-[600px] right-0 top-0"
            autoplay
            loop
          >
            <source :src="selectedFilm.videoUrl" type="video/mp4" />
          </video>
        </div>
        <br />
        <div
          class="fixed z-30 bottom-0 right-0 w-full h-[35%] pl-[120px] overflow-y-auto"
        >
          <div class="featured">
            <h5 class="text-[30px] text-white font-semibold font-serif">
              FEATURED MOVIES
            </h5>
          </div>
  
          <div class="swiper-container">
            <slot-comp class="swiper-wrapper" v-for="x in films">
              <button class="swiper-slide" @click="selectFilm(x)">
                <img class="resim" v-bind:src="x.url" /> <br />
                <h4>{{ x.title }}</h4>
              </button>
            </slot-comp>
            
          </div>
          <div class="featured">
            <h5 class="text-[30px] text-white font-semibold font-serif">
              HORROR MOVIES
            </h5>
          </div>
  
          <div class="swiper-container">
            <slot-comp class="swiper-wrapper" v-for="x in films1">
              <button class="swiper-slide" @click="selectFilm(x)">
                <img class="resim" v-bind:src="x.url" /> <br />
                <h4>{{ x.title }}</h4>
              </button>
            </slot-comp>
            <div class="swiper-button-next"></div>
            <div class="swiper-button-prev"></div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { onMounted, ref } from "vue";
  import Magnify from "vue-material-design-icons/Magnify.vue";
  import HomeOutLine from "vue-material-design-icons/HomeOutLine.vue";
  import TrendingUp from "vue-material-design-icons/TrendingUp.vue";
  import Television from "vue-material-design-icons/Television.vue";
  import MovieOutLine from "vue-material-design-icons/MovieOutLine.vue";
  import Plus from "vue-material-design-icons/Plus.vue";
  import ChevronLeft from "vue-material-design-icons/ChevronLeft.vue";
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import 'swiper/css';
  
  
  
  const films = ref([
    {
      title: "Avengers",
      genre: "Aksiyon,Macera,Fantastik",
      description:
        "Marvel Studios tarafindan üretilen ve Marvel Comics'in süper kahraman ekibidir..",
      year: "2012",
      videoUrl: "Avengers.mp4",
      url: "Avengers.jpg",
    },
    {
      title: "The Lord of the Rings",
      genre: "Fantastik",
      description:
        "Yüzüklerin Efendisi: Yüzük Kardeşliği, dünyanin kaderini değişterecek olan yüzükten kurtulmak için verilen mücadeleyi konu ediyor..",
      year: "2001",
      videoUrl: "The Lord of the Rings.mp4",
      url: "The Lord of the Rings.jpg",
    },
    {
      title: "Thor Love and Thunder",
      genre: "Fantastik",
      description:
        "Thor: Aşk ve Gök Gürültüsü, tanrilari yok etmeye and içen Gorr the God Butcher'a karşi zorlu bir mücadeleye girişen Thor'un hikayesini konu ediyor.",
      videoUrl: "Thor Love and Thunder.mp4",
      url: "Thor Love and Thunder.jpg",
      year: "2022",
    },
    {
      title: "The Nun",
      genre: "Korku",
      description:
        "Geçmişinde karanlik olaylar yaşamiş Rahip Burke (Demián Bichir) ve rahibe olmak için son aşamalara gelmiş genç rahibe adayi Irene (Taissa Farmiga), kendini öldürmüş bir rahibeyle ilgili araştirma yapmak için Vatikan tarafindan Romanya'nin ücra bir köşesindeki bir manastira gönderilir. Manastirin sirrini öğrenen ikili, sadece hayatlarini değil, hayatlarini adadiklari inançlarini da ortaya koyarak bir rahibe formuna karşilarina çikan şeytani güçle savaşacaktir.",
      videoUrl: "TheNun.mp4",
      url: "TheNun.jpg",
      year: "2018",
    },
    {
      title: "Pirates of the Caribbean",
      genre: "Fantastic",
      description:
        "Jack, Salazar'in gazabindan ve intikamindan kurtulmak için Poseidon Asasinin peşine düşer. Bu efsanevi asayi bulmak içinse güzel ve zeki gökbilimci Carina Smyth ve Kraliyet Donanmasi'ndan  dik başli, genç bir denizci olan Henry ile zorlu bir anlaşma yapar.",
      videoUrl: "Pirates of the Caribbean.mp4",
      url: "Pirates of the Caribbean.jpg",
      year: "2017",
    },
    {
      title: "Dexter",
      genre: "Drama",
      description:
        "Gündüzleri adli tip polisi, geceleri ise seri katil, üstelik ikisinde de çok başarili. Bir katili bir başka katilden daha iyi kim anlayabilir! Öldürme arzusu disinda insani duygulardan yoksun doğan Dexter, ahlaki değerleri olan bir seri katil: Sadece yasalarin elinden kaçmayi başaran canileri öldürüyor..",
      videoUrl: "Dexter.mp4",
      url: "Dexter.jpg",
      year: "2006",
    },
    {
      title: "The Witcher",
      genre: "Fantastic",
      description:
        "Witcher Saga roman serisi sayisiz dile çevrilen, hakkinda film, dizi, oyun ve grafik roman yapilan The Witcher, Netflix ekranlarinda izleyiciyle buluşacak. Video oyunu tüm dünyada 33 milyonun üzerinde satarak çok büyük bir başari yakalayan The Witcher, genç yaşta doğaüstü yetenekleriyle canavarlarla savaşan cadilari anlatmakta.",
      videoUrl: "witcher.mp4",
      url: "witcher.jpg",
      year: "2019",
    },
    {
      title: "Game of Thrones",
      genre: "Drama",
      description:
        "Kis yaklasiyor, hanedan entrikalari, kapali kapilar ardinda dönen oyunlar, birilerinin kuyusunu kazmak icin dusmanina yaklasan kadinlar,kardesler arasi cekismeler hepsi tek bir amac icin demir bir taht.",
      videoUrl: "Game of Thrones.mp4",
      url: "Game of Thrones.jpg",
      year: "2011",
    },
    {
      title: "Knock at the Cabin",
      genre: "Korku",
      description:
        "Kulübeye Tiklat, keyifli başlayan tatilleri, kapilarinda dört yabancinin bitmesiyle kabusa dönen bir ailenin hayatina odaklaniyor. ",
      year: "2023",
      videoUrl: "Knock at the Cabin.mp4",
      url: "Knock at the Cabin.jpg",
    },
    {
      title: "Hatching",
      genre: "Korku",
      description:
        "Hirsli ve takintili annesini tatmin etmek için umutsuzca çabalayan genç bir kiz, bir gün ormanda tuhaf bir yumurta bulur. Yumurtayi sicak tutarak, çatlayana kadar odasinda saklar ancak yumurtanin içinden çikan şey genç kizin hayatini derinden etkileyecektir.",
      year: "2022",
      videoUrl: "hatching.mp4",
      url: "hatching.jpg",
    },
    {
      title: "M3GAN",
      genre: "Korku",
      description:
        "M3GAN dahi bir oyuncak şirketinde çalişan robotik mühendisi olan bir adamin hikayesini konu ediyor. Mühendis, yakin zamanda yetim kalmis olan yeğenine destek olmasi ve arkadaslik etmesi için bir robot tasarlar. Ancak küçük kiz ile duygusal olarak bağ kurmaya programlanmis insansi robot, programlamasi fazla iyi işlediği için yeni arkadaşi konusunda aşiri korumaci bir hale gelir.",
      videoUrl: "m3gan.mp4",
      url: "m3gan.jpg",
      year: "2023",
    },
    {
      title: "Wrong Turn",
      genre: "Korku",
      description:
        " Başlangiç, dağ gezisi yapmak için yola koyulan 6 arkadaşin başlarina gelenleri konu ediyor. New York'ta yaşayan alti arkadaş, Bati Virginia Dağlari'nda yürüyüş yapmak için yola koyulur. Grubun eğlenceli geçen yürüyüşleri, yillarca dağlarda yaşayan ve The Foundation olarak bilinen vahşi bir tarikata rastlamalariyla yerini korku dolu anlara birakir.",
      videoUrl: "wrongturn.mp4",
      url: "wrongturn.jpg",
      year: "2021",
    },
    {
      title: "SMILE",
      genre: "Horror",
      description:
        "Gülümse, yaşadiği tuhaf olaylardan kurtulmak için sorunlu geçmişiyle yüzleşmek zorunda olan bir kadinin hayatina odaklaniyor. Bir hastayi içeren tuhaf, travmatik bir olaya tanik olan Dr. Rose Cotter, açiklayamadiği korkutucu olaylar yaşamaya başlar.",
      videoUrl: "smile.mp4",
      url: "smile.jpg",
      year: "2022",
    },
    {
      title: "Scream 6",
      genre: "Korku",
      description:
        "Çiğlik 6, Hayalet Maskeli cinayetlerinden kurtulduktan sonra Woodsboro kasabasini geride birakip New York'ta yeni bir hayata başkayan dört kişinin hayatina odaklaniyor.",
      videoUrl: "scream6.mp4",
      url: "scream6.jpg",
      year: "2023",
    },
  
    // Diğer filmler...
  ]);
  const films1 = ref([
    {
      title: "Knock at the Cabin",
      genre: "Korku",
      description:
        "Kulübeye Tiklat, keyifli başlayan tatilleri, kapilarinda dört yabancinin bitmesiyle kabusa dönen bir ailenin hayatina odaklaniyor. ",
      year: "2023",
      videoUrl: "Knock at the Cabin.mp4",
      url: "Knock at the Cabin.jpg",
    },
    {
      title: "Hatching",
      genre: "Korku",
      description:
        "Hirsli ve takintili annesini tatmin etmek için umutsuzca çabalayan genç bir kiz, bir gün ormanda tuhaf bir yumurta bulur. Yumurtayi sicak tutarak, çatlayana kadar odasinda saklar ancak yumurtanin içinden çikan şey genç kizin hayatini derinden etkileyecektir.",
      year: "2022",
      videoUrl: "hatching.mp4",
      url: "hatching.jpg",
    },
    {
      title: "M3GAN",
      genre: "Korku",
      description:
        "M3GAN dahi bir oyuncak şirketinde çalişan robotik mühendisi olan bir adamin hikayesini konu ediyor. Mühendis, yakin zamanda yetim kalmis olan yeğenine destek olmasi ve arkadaslik etmesi için bir robot tasarlar. Ancak küçük kiz ile duygusal olarak bağ kurmaya programlanmis insansi robot, programlamasi fazla iyi işlediği için yeni arkadaşi konusunda aşiri korumaci bir hale gelir.",
      videoUrl: "m3gan.mp4",
      url: "m3gan.jpg",
      year: "2023",
    },
    {
      title: "Wrong Turn",
      genre: "Korku",
      description:
        " Başlangiç, dağ gezisi yapmak için yola koyulan 6 arkadaşin başlarina gelenleri konu ediyor. New York'ta yaşayan alti arkadaş, Bati Virginia Dağlari'nda yürüyüş yapmak için yola koyulur. Grubun eğlenceli geçen yürüyüşleri, yillarca dağlarda yaşayan ve The Foundation olarak bilinen vahşi bir tarikata rastlamalariyla yerini korku dolu anlara birakir.",
      videoUrl: "wrongturn.mp4",
      url: "wrongturn.jpg",
      year: "2021",
    },
    {
      title: "SMILE",
      genre: "Horror",
      description:
        "Gülümse, yaşadiği tuhaf olaylardan kurtulmak için sorunlu geçmişiyle yüzleşmek zorunda olan bir kadinin hayatina odaklaniyor. Bir hastayi içeren tuhaf, travmatik bir olaya tanik olan Dr. Rose Cotter, açiklayamadiği korkutucu olaylar yaşamaya başlar.",
      videoUrl: "smile.mp4",
      url: "smile.jpg",
      year: "2022",
    },
    {
      title: "Scream 6",
      genre: "Korku",
      description:
        "Çiğlik 6, Hayalet Maskeli cinayetlerinden kurtulduktan sonra Woodsboro kasabasini geride birakip New York'ta yeni bir hayata başkayan dört kişinin hayatina odaklaniyor.",
      videoUrl: "scream6.mp4",
      url: "scream6.jpg",
      year: "2023",
    },
  
    // Diğer filmler...
  ]);
  const selectedFilm = ref({});
  const videoPlayer = ref(null);
  
  
  const selectFilm = (film) => {
    selectedFilm.value = film;
    videoPlayer.value.load();
    videoPlayer.value.play();
    console.log(selectedFilm.value, "film");
  };
  
  
  
  
  
  
  
  
  
  
  onMounted(() => {
    selectedFilm.value = films.value[0];
  });
  
  
  </script>
  
  <style>
  .resim {
    width: 200px;
    height: 200px;
    background-color: black;
  }
  :root {
    --swiper-theme-color: #e5e5e5 !important;
  }
  .swiper-container {
    overflow: visible;
    display: flex;
  }.swiper-slide {
    transition: all 300ms ease-in-out;
    border-radius: 5px;
  }
  
  .swiper-slide img {
    border-radius: 5px;
    max-width: 18rem;
    cursor: grab;
  }
  
  .swiper-slide img:active {
    cursor: grabbing;
  }
  
  .swiper-slide:hover {
    transform: scale(1.5);
    transition: all 300ms ease-in-out;
    transition-delay: 300ms;
    z-index: 1;
  }
  
  .swiper-slide:hover img {
    transition-delay: 300ms;
    box-shadow: 0 0 5px 1px rgba(0,0,0,0.5);
  }
  
  @media screen and (max-width: 599px) {
    .swiper-slide img {
      max-width: 14rem;
    }
    .swiper-button-next,
    .swiper-button-prev {
      display: inline;
    }
  }
  
  @media screen and (max-width: 400px) {
    .swiper-slide img {
      max-width: 10.5rem;
      border-radius: 2px;
    }
  }
  
  </style>