<template>
    <div class="topbar">
          <div class="weblogo">
              <img src="netflix-logoo.png" class="logoImg" alt="">
          </div>
          <div class="navList">
              <span class="navItem">Home</span>
              <span class="navItem">Movies</span>
              <span class="navItem">Series</span>
              <span class="navItem">Popular</span>
              <span class="navItem">Trends</span>
          </div>
          <div class="profile">
             <span>
              <img src="Netflix-avatar.png" alt="" class="userImg">
             </span>
             <span class="profileHeading">Profile<i class="fa-solid fa-caret-down"></i> </span>
             <span class="theme">
              <span class="sun"><i class="fa-solid fa-sun"></i></span>
              <span class="night"><i class="fa-solid fa-star"></i></span>
              <div class="ball"></div>
             </span>
          </div>
    </div>
      <div class="fixed">
        <div id="sideNav" class="flex z-40 items-center w-[120px] h-screen bg-black relative">
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
  
      </div>
  <div class="mainContainer">
    <video ref="videoPlayer" controls class="w-full h-[1100px]"  loop>
        <source :src="selectedFilm.videoUrl" type="video/mp4" />
      </video>
  
      <div class="button-container">
        <button class="info-button" @click="showMoreInfo">More Info</button>
        <button class="play-button" @click="togglePlay">Play</button>
  
  
      </div>
  
      <div v-if="showMoreInfoModal" class="modal">
        <div class="modal-content">
          <div class="film-info">
            <h2 class="modal-title">{{ selectedFilm.title }}</h2>
          <p class="modal-description">{{ selectedFilm.description }}</p>
          <p class="modal-year">Year: {{ selectedFilm.year }}</p>
          </div>
          
  
          <button class="modal-close-button" @click="closeMoreInfo">Close</button>
        </div>
      </div>
      <br />
      <br>
      <br>
        <div
          class="z-30 bottom--125 right-600  w-[100%] h-[35%] pl-[12px] overflow-y-auto"
        >
          <div class="featured">
            <h5 class="text-[20px] left-10 text-white font-semibold Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
              NETFLIX ORIGINALS
            </h5>
            
            <div class="btnleft">
              <button @click="performaction" class="handle left-handle">
          <div class="text">&#8249;</div>
        </button>
        
            </div>
            <div class="btnright">
              <button @click="performaction1" class="handle right-handle">
          <div class="text">&#8250;</div>
        </button>
            </div>
             <br>
             
            
            
          </div>
          
          
  
          <div class="swiper-container">
            
            
            
            <slot-comp
            
             class="swiper-wrapper" v-for="x in films">
              <button class="swiper-slide" @click="selectFilm(x)">
                <img class="resim" v-bind:src="x.url"/> <br />
                
                <h4>{{ x.title }}</h4>
              </button>
            </slot-comp>
            
            
          </div>
          <br>
          <div class="featured1">
            <h5 class="text-[20px] text-white font-semibold font-Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
              HORROR MOVIES
            </h5>
            
            <div class="btnleft1">
              <button @click="performaction2" class="handle left-handle">
          <div class="text">&#8249;</div>
        </button>
        
            </div>
            <div class="btnright1">
              <button @click="performaction3" class="handle right-handle">
          <div class="text">&#8250;</div>
        </button>
            </div>
             <br>
             <br>
          </div>
  
          <div class="swiper-container1">
            <slot-comp class="swiper-wrapper" v-for="x in films1">
              <button class="swiper-slide" @click="selectFilm(x)">
                <img class="resim" v-bind:src="x.url" /> <br />
                <h4>{{ x.title }}</h4>
              </button>
            </slot-comp>
                  <div class="swiper-button-prev"></div>
                  <div class="swiper-button-next"></div>
            
          </div>
          <div class="featured">
            <h5 class="text-[20px] left-10 text-white font-semibold Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
              NEW RELEASES
            </h5>
            
            <div class="btnleft">
              <button @click="performaction" class="handle left-handle">
          <div class="text">&#8249;</div>
        </button>
        
            </div>
            <div class="btnright">
              <button @click="performaction1" class="handle right-handle">
          <div class="text">&#8250;</div>
        </button>
            </div>
             <br>
             
            
            
          </div>
          
          
  
          <div class="swiper-container">
            
            
            
            <slot-comp
            
             class="swiper-wrapper" v-for="x in films">
              <button class="swiper-slide" @click="selectFilm(x)">
                <img class="resim" v-bind:src="x.url"/> <br />
                
                <h4>{{ x.title }}</h4>
              </button>
            </slot-comp>
            
            
          </div>
          <br>
          
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
  const arrows = document.querySelectorAll(".arrows");
  const moviewrapper = document.querySelectorAll(".movielistContainerWrapper");
  
  let clickCounter = 0 ;
  
  arrows.forEach((arrow,i)=>{
      arrow.addEventListener("click",()=>{
          clickCounter++;
          const check = moviewrapper[i].querySelectorAll(".wrapperItem").length;
          if((clickCounter + 3)-check <0 )
          {
              moviewrapper[i].style.transform = `translateX(${-425*(clickCounter)}px)`;
          }
          else
         { moviewrapper[i].style.transform = `translateX(0px)`;
          clickCounter = 0 ;}
      })
  })
  
  
  
  
  
  
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
  const translateAmount = ref(0);
  let currentIndex = -1;
  const showMoreInfoModal = ref(false);
  const isPlaying = ref(false);
  
  const showMoreInfo = () => {
    showMoreInfoModal.value = true;
  };
  
  const closeMoreInfo = () => {
    showMoreInfoModal.value = false;
  };
  const togglePlay = () => {
    if (videoPlayer.value) {
      if (isPlaying.value) {
        videoPlayer.value.pause();
      } else {
        videoPlayer.value.play();
      }
      isPlaying.value = !isPlaying.value;
    }
  };
  
  
  
  
  const selectFilm = (film) => {
    selectedFilm.value = film;
    videoPlayer.value.load();
    videoPlayer.value.play();
    console.log(selectedFilm.value, "film");
  };
  function performaction(){
    translateAmount.value += 2;
    const swiperContainer = document.querySelector('.swiper-container');
    swiperContainer.style.transform = `translate(${translateAmount.value}px)`;
    currentIndex++;
    
    if (films.value.length > currentIndex) {
      films.value.push(films.value[currentIndex]);
      if(films.value.length > 10){
        
        films.value.shift(); // En baştaki elemanı çıkar
        currentIndex--;
        
        
      }
      
    }
    
    
  }
  
  function performaction1(){
    translateAmount.value -= 2;
    const swiperContainer = document.querySelector('.swiper-container');
    swiperContainer.style.transform = `translate(${translateAmount.value}px)`;
    currentIndex++;
    
    if (films.value.length > currentIndex) {
      films.value.push(films.value[currentIndex]);
      if(films.value.length > 10){
        
        films.value.shift(); // En baştaki elemanı çıkar
        currentIndex--;
        
        
      }
      
    }
   
  }
  function performaction2(){
    translateAmount.value += 2;
    
    const swiperContainer1 = document.querySelector('.swiper-container1');
    swiperContainer1.style.transform = `translate(${translateAmount.value}px)`;
    currentIndex++;
    
    if (films1.value.length > currentIndex) {
      films1.value.push(films1.value[currentIndex]);
      if(films1.value.length > 10){
        
        films1.value.shift(); // En baştaki elemanı çıkar
        currentIndex--;
        
        
      }
      
    }
    
  }
  function performaction3(){
    translateAmount.value -= 2;
    
    const swiperContainer1 = document.querySelector('.swiper-container1');
    swiperContainer1.style.transform = `translate(${translateAmount.value}px)`;
    currentIndex++;
    
    if (films1.value.length > currentIndex) {
      films1.value.push(films1.value[currentIndex]);
      if(films1.value.length > 10){
        
        films1.value.shift(); // En baştaki elemanı çıkar
        currentIndex--;
        
        
      }
      
    }
  }
  
  
  
  onMounted(() => {
    selectedFilm.value = films.value[0];
    
  });
  
  
  </script>
  
  <style>
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700;900&family=Ubuntu:wght@300;400;500;700&display=swap');
  /* 
  font-family: 'Roboto', sans-serif;
  font-family: 'Ubuntu', sans-serif; */
  
  *{
      margin: 0;
      padding: 0;
      background-color: black;
      
  }
  
  .topbar{
      background-color: black;
      width: 100vw;
      height: 70px;
      display: flex;
      align-items: center;
      position: fixed;
      top: 0;
      z-index: 2;
      transition: 0.7s all ease-in-out;
      
  }
  .web-logo{
      width: 127px;
      height: 67px;
  }
  .logoImg{
    object-fit: contain;
      width: 20%;
  }
  .navList{
      display: flex;
      color: white;
      gap:20px;
      margin-left: 116px;
  
  }
  .profile{
      margin-left: 600px;
      color: white;
      display: flex;
      align-items: center;
      font-weight: bold;
      gap: 20px;
      font-size: 1.2rem;
      font-family: 'Ubuntu', sans-serif;
  }
  .navItem{
      font-family:'Roboto', sans-serif ;
      font-weight: bold;
  }
  .userImg{
      height: 40px;
      width: 40px;
      border-radius: 50%;
      object-fit: cover;
  }
  .theme{
      width: 50px;
      height: 20px;
      border-radius: 8px;
      background-color: white;
      display: flex;
      align-items: center;
      position: relative;
      color: goldenrod;
      justify-content: space-between;
      transition: 0.7s all ease-in-out;
  }
  .mainContainer{
    position: absolute;
      width: calc(100vw - 77px);
      height: (100% - 70px);
      left: 100px;
      top: 0px;
      background-color: black;
      transition: 0.7s all ease-in-out;
  
  }
  .resim {
    width: 450px;
    height: 140px;
    background-color: black;
  }
  .swiper-container {
    overflow: visible;
    display: flex;
    transition: all 0.1s ease-out;
    -webkit-animation: scrolling-left1 20s linear infinite;
    animation: scrolling-left1 20s linear infinite;
    
  
    
  }
  .swiper-container1 {
    overflow: visible;
    display: flex;
    transition: all 0.1s ease-out;
   
    
    
  }
  
  .swiper-slide {
    --items-per-screen: 4;
    --slider-index: 0;
    display: flex;
    flex-grow: 1;
    margin: 0 var(--img-gap);
    transform: translateX(calc(var(--slider-index) * -100%));
    transition: transform 250ms ease-in-out;
    
    
  }
  
  .swiper-slide > img {
    border-radius: 5px;
    max-width: 180px;
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
      max-width: 24rem;
    }
    .swiper-button-next,
    .swiper-button-prev {
      display: inline;
    }
  }
  
  @media screen and (max-width: 400px) {
    .swiper-slide img {
      max-width: 15.5rem;
      border-radius: 2px;
    }
  }
  .handle {
    border: none;
    border-radius: 1rem;
    flex-grow: 0;
    flex-shrink: 0;
    background-color: rgba(255, 255, 255, .25);
    z-index: 10;
    margin: var(--img-gap) 0;
    width: var(--handle-size);
    cursor: pointer;
    font-size: 3rem;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    line-height: 0;
    transition: background-color 150ms ease-in-out;
  }
  
  .left-handle {
    border-top-left-radius: 0;
    border-bottom-left-radius: 0;
    
  
      
  
    
  }
  .right-handle {
    border-top-right-radius: 0;
    border-bottom-right-radius: 0;
    margin-left: 1790px;
    height: 2px;
    
  }
  
  .handle:hover,
  .handle:focus {
    background-color: rgba(255, 255, 255, .5);
  }
  @media (max-width: 1000px) {
    .swiper-slide {
      --items-per-screen: 3;
    }
  }
  
  @media (max-width: 500px) {
    .swiper-slide {
      --items-per-screen: 2;
    }
  }
  
  
  
  h1{
      color: white;
  }
  
  .arrows{
      color: lightgrey;
      font-size: 120px;
      position: absolute;
      right: 20px;
      top: 60px;
    z-index: 2;
    opacity: 0.8;
    cursor: pointer;
  }
  .ball
  {
      width: 15px;
      height: 15px;
      border-radius: 50%;
      background-color: black;
      position: absolute;
      padding: 2px;
      bottom: 0.7px;
      cursor: pointer;
      transition: 0.7s all ease-in-out;
  }
  
  .topbar.active{
      background-color: white;
      transition: 0.7s all ease-in-out;
  
  }
  
  .navList.active{
      color: black;
      transition: 0.7s all ease-in-out;
  }
  
  .leftbar.active{
      background-color: white;
      transition: 0.7s all ease-in-out;
  }
  
  .leftbarWrapper.active{
      color: black;
      transition: 0.7s all ease-in-out;
  }
  .mainContainer.active{
      background-color: white;
      transition: 0.7s all ease-in-out;
     
  }
  
  .newreleaseheading.active{
      color: black;
      transition: 0.7s all ease-in-out;
  }
  
  .theme.active{
      background-color: black;
      transition: 0.7s all ease-in-out;
  
  }
  .ball.active{
      background-color: white;
      transform: translateX(30px);
      transition: 0.7s all ease-in-out;
  }
  
  .profileHeading{
      color:white;
      transition: 0.7s all ease-in-out;
  }
  
  .profileHeading.active{
      color: black;
      transition: 0.7s all ease-in-out;
  }
  
  .video {
    width: 80%;
    height: 800px;
    
  }
  
  .button-container {
    position: absolute;
    top: 600px;
    left: 0px;
    display: flex;
    justify-content: space-between;
    z-index: 1;
    margin-left: 100px;
  }
  
  .info-button,
  .play-button {
    background-color: white;
    color: black;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: larger;
    font-family: sans-serif;
  }
  
  .modal {
    position: fixed;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 2;
  }
  
  .modal-content {
    background-color: white;
    padding: 20px;
    border-radius: 4px;
  }
  
  .modal-title {
    font-size: 1.5rem;
    font-weight: bold;
    color: white;
  }
  
  .modal-description {
    margin-top: 10px;
    color: white;
  }
  
  .modal-year {
    margin-top: 10px;
    font-weight: bold;
    color: white;
  }
  
  .modal-close-button {
    margin-top: 20px;
    background-color: #007bff;
    color: white;
    padding: 8px 16px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  
  
  
  
  
  
  </style>