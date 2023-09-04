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
    <div class="video-thumbnail-container" @mouseenter="isHovering = true" @mouseleave="isHovering = false">
        <img :src="selectedFilm.urlmain" alt="Video Thumbnail" class="video-thumbnail" />
        <video ref="videoPlayer" controls autoplay class="w-[100%] h-[95%]" loop>
          <source :src="selectedFilm.videoUrl" type="video/mp4" />
        </video>
      </div>
      <div class="cm">
        <div class="ftitle" ref="ftitleRef">{{ selectedFilm.title }}</div>
        <div class="fdesc">{{ selectedFilm.description }}</div>
        
      </div>
      
  
      <div class="button-container">
        
          <div class="buttons">
                        <button class="play-button" @click="togglePlay">
                          <svg width="24" height="24" viewBox="0 0 24 24" fill="gray" xmlns="http://www.w3.org/2000/svg">
                            <path d="M4 2.69127C4 1.93067 4.81547 1.44851 5.48192 1.81506L22.4069 11.1238C23.0977 11.5037 23.0977 12.4963 22.4069 12.8762L5.48192 22.1849C4.81546 22.5515 4 22.0693 4 21.3087V2.69127Z" fill="currentColor"></path>
                              </svg>Play</button>
                              <br>
                        <button class="info-button" @click="showMoreInfo"><i class="bi bi-info-circle" style=" padding: 0%;"></i> More Info</button>
                      </div>
         
        
  
  
      </div>
      <div v-if="showMoreInfoModal" class="modal">
        <div class="modal-content">
        <div class="video-section">
          <div class="video-thumbnail-container1" @mouseenter="isHovering = true" @mouseleave="isHovering = false">
        <img :src="selectedFilm.url" alt="Video Thumbnail" class="video-thumbnail1" />
        <video ref="videoPlayer" controls autoplay class="w-[100%] h-[95%]" loop>
          <source :src="selectedFilm.videoUrl" type="video/mp4" />
        </video>
      </div>
        </div>
        <div class="movie-details">
          <h2 class="t1">{{ selectedFilm.title }}</h2>
          <p class="t2">{{ selectedFilm.description }}</p>
          <p class="t3">{{ selectedFilm.year }}</p>
        </div>
        <button class="close-button" @click="closeMoreInfo">Close</button>
      </div>
      </div>
  
      
      
      
      
        <div
          class="z-30 top--100 right-600  w-[100%] h-[35%] pl-[12px] overflow-y-auto"
        >
          <div class="featured">
            <h5 class="text-[30px] left-10 text-white font-semibold Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
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
          <br>
          
          
          
  
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
          <br>
          <div class="featured1">
            <h5 class="text-[30px] text-white font-semibold font-Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
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
                <div class="movietext">
                  <h4>{{ x.title }}</h4>
                </div>
                
              </button>
            </slot-comp>
                  <div class="swiper-button-prev"></div>
                  <div class="swiper-button-next"></div>
            
          </div>
          <br>
          <br>
          <div class="featured">
            <h5 class="text-[30px] left-10 text-white font-semibold Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
              NEW RELEASES
            </h5>
            
            <div class="btnleft2">
              <button @click="performaction4" class="handle left-handle">
          <div class="text">&#8249;</div>
        </button>
        
            </div>
            <div class="btnright2">
              <button @click="performaction5" class="handle right-handle">
          <div class="text">&#8250;</div>
        </button>
            </div>
             <br>
             
            
            
          </div>
          <br>
          
          
  
          <div class="swiper-container2">
            
            
            
            <slot-comp
            
             class="swiper-wrapper" v-for="x in films2">
              <button class="swiper-slide" @click="selectFilm(x)">
                <img class="resim" v-bind:src="x.url"/> <br />
                
                <h4>{{ x.title }}</h4>
              </button>
            </slot-comp>
            
            
          </div>
          <br>
          <br>
          <br>
          <div role="contentinfo" class="member-footer" id="member-footer">
            <div class="social-links">
              <a class="social-link" href="https://www.facebook.com/netflixturkiye" target="_blank" aria-label="facebook">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="svg-icon svg-icon-facebook-logo ltr-0 e1mhci4z1" data-name="Facebook" aria-hidden="true">
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M13.987 13.1621V21.9841H10.042V13.1621H6.84198V9.51207H10.047V6.73207C10.047 3.56707 11.932 1.82007 14.815 1.82007C15.7618 1.83321 16.7063 1.91577 17.641 2.06707V5.17307H16.045C15.4954 5.10007 14.9424 5.28088 14.5421 5.66447C14.1417 6.04807 13.9375 6.59284 13.987 7.14507V9.51207H17.487L16.928 13.1621H13.987Z" fill="currentColor"></path>
                </svg>
              </a>
              <a class="social-link" href="https://www.instagram.com/netflixturkiye" target="_blank" aria-label="instagram">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="svg-icon svg-icon-instagram-logo ltr-0 e1mhci4z1" data-name="Instagram" aria-hidden="true">
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M21.93 16.123C21.9584 17.6765 21.3789 19.1796 20.315 20.312C19.1851 21.3804 17.6797 21.9607 16.125 21.927C14.474 22.021 9.52499 22.021 7.87499 21.927C6.32126 21.9551 4.81792 21.3757 3.68499 20.312C2.61754 19.1819 2.03744 17.6772 2.06999 16.123C1.97699 14.472 1.97699 9.523 2.06999 7.873C2.03955 6.31886 2.61933 4.81466 3.68499 3.683C4.81767 2.61952 6.32162 2.04163 7.87499 2.073C9.52599 1.979 14.475 1.979 16.125 2.073C17.6789 2.04394 19.1826 2.62353 20.315 3.688C21.3825 4.81813 21.9625 6.32278 21.93 7.877C22.023 9.528 22.023 14.472 21.93 16.123ZM20.2 12C20.2 10.545 20.32 7.422 19.8 6.106C19.4572 5.23679 18.7692 4.54875 17.9 4.206C16.588 3.689 13.461 3.806 12.006 3.806C10.551 3.806 7.42799 3.685 6.11199 4.206C5.24298 4.54905 4.55505 5.23699 4.21199 6.106C3.69499 7.418 3.81199 10.545 3.81199 12C3.81199 13.455 3.69099 16.578 4.21199 17.894C4.55535 18.7628 5.24318 19.4506 6.11199 19.794C7.42399 20.311 10.552 20.194 12.006 20.194C13.46 20.194 16.584 20.315 17.9 19.794C18.769 19.451 19.4569 18.763 19.8 17.894C20.319 16.582 20.2 13.455 20.2 12ZM17.13 12C17.13 14.8312 14.8352 17.1264 12.004 17.127C9.17282 17.1276 6.8771 14.8332 6.87599 12.002C6.87489 9.17083 9.16882 6.87466 12 6.87299C13.3608 6.87034 14.6666 7.40959 15.629 8.37161C16.5914 9.33363 17.1311 10.6392 17.129 12H17.13ZM15.336 12C15.336 10.1596 13.8444 8.66756 12.004 8.667C10.1636 8.66645 8.6711 10.1576 8.66999 11.998C8.66889 13.8384 10.1596 15.3313 12 15.333C13.8406 15.3319 15.3328 13.8406 15.335 12H15.336ZM17.336 7.85901C16.6733 7.85901 16.136 7.32174 16.136 6.659C16.136 5.99626 16.6733 5.459 17.336 5.459C17.9987 5.459 18.536 5.99626 18.536 6.659C18.5379 6.97731 18.4124 7.28317 18.1876 7.50853C17.9628 7.73389 17.6573 7.86008 17.339 7.85901H17.336Z" fill="currentColor"></path>
                </svg>
              </a>
              <a class="social-link" href="https://twitter.com/netflixturkiye" target="_blank" aria-label="twitter">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="svg-icon svg-icon-twitter-logo ltr-0 e1mhci4z1" data-name="Twitter" aria-hidden="true">
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M20.768 8.207C20.7914 11.5932 19.4565 14.8475 17.062 17.242C14.6675 19.6365 11.4132 20.9714 8.027 20.948C5.58923 20.9544 3.20152 20.2564 1.151 18.938C1.50998 18.9771 1.87091 18.9955 2.232 18.993C4.24768 18.9984 6.20639 18.3245 7.792 17.08C5.87438 17.0472 4.18971 15.799 3.6 13.974C3.87982 14.0187 4.16264 14.0421 4.446 14.044C4.84354 14.0428 5.23935 13.9914 5.624 13.891C3.53637 13.4667 2.0367 11.6303 2.038 9.5V9.441C2.65835 9.78765 3.3519 9.98262 4.062 10.01C2.08979 8.69332 1.48225 6.06954 2.675 4.02C4.94972 6.82016 8.30596 8.52336 11.909 8.706C11.8375 8.369 11.8009 8.02551 11.8 7.681C11.8014 5.84295 12.9248 4.19204 14.6341 3.51625C16.3434 2.84047 18.2921 3.2768 19.55 4.617C20.5522 4.42342 21.5131 4.05731 22.39 3.535C22.0556 4.56894 21.3555 5.44538 20.421 6C21.3102 5.89965 22.1795 5.66709 23 5.31C22.3866 6.20228 21.6273 6.98489 20.754 7.625C20.768 7.82 20.768 8.014 20.768 8.207Z" fill="currentColor"></path>
                </svg>
              </a>
              <a class="social-link" href="https://www.youtube.com/channel/UCeZOywU-zg9j3SxYG0FdLtw" target="_blank" aria-label="youtube">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="svg-icon svg-icon-youtube-logo ltr-0 e1mhci4z1" data-name="Youtube" aria-hidden="true">
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M22.54 6.67C22.288 5.71873 21.549 4.97331 20.6 4.713C18.88 4.25 12 4.25 12 4.25C12 4.25 5.11997 4.25 3.39997 4.713C2.45094 4.97331 1.71199 5.71873 1.45997 6.67C1.14265 8.42869 0.988663 10.213 0.99997 12C0.988663 13.787 1.14265 15.5713 1.45997 17.33C1.71288 18.2825 2.45401 19.0282 3.40497 19.287C5.11997 19.75 12.005 19.75 12.005 19.75C12.005 19.75 18.885 19.75 20.6 19.287C21.549 19.0267 22.288 18.2813 22.54 17.33C22.8573 15.5713 23.0113 13.787 23 12C23.0113 10.213 22.8573 8.42869 22.54 6.67ZM9.74997 15.27V8.729L15.5 12L9.74997 15.27Z" fill="currentColor"></path>
                </svg>
              </a>
  
            </div>
            <ul class="member-footer-links">
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="/browse/audio-description">
                  <span class="member-footer-link-content">Audio Description</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="https://help.netflix.com/">
                  <span class="member-footer-link-content">Help Center</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="/redeem">
                  <span class="member-footer-link-content">Gift Cards</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="https://media.netflix.com/">
                  <span class="member-footer-link-content">Media Center</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="http://ir.netflix.com/">
                  <span class="member-footer-link-content">Investor Relations</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="https://jobs.netflix.com/">
                  <span class="member-footer-link-content">Jobs</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="https://help.netflix.com/legal/termsofuse">
                  <span class="member-footer-link-content">Terms of Use</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="https://help.netflix.com/legal/privacy">
                  <span class="member-footer-link-content">Privacy</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="https://help.netflix.com/legal/notices">
                  <span class="member-footer-link-content">Legal Notices</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="/Cookies">
                  <span class="member-footer-link-content">Cookie Preferences</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="https://help.netflix.com/legal/corpinfo">
                  <span class="member-footer-link-content">Corporate Information</span>
                </a>
              </li>
              <li class="member-footer-link-wrapper">
                <a class="member-footer-link" href="https://help.netflix.com/contactus">
                  <span class="member-footer-link-content">Contact Us</span>
                </a>
              </li>
            </ul>
            <div class="member-footer-service">
              <button class="service-code">Service Code</button>
            </div>
            <div class="member-footer-copyright">
              <span>© 1997-2023 Netflix, Inc.</span>
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
      urlmain: "avenger.jpg"
    },
    {
      title: "The Lord of the Rings",
      genre: "Fantastik",
      description:
        "Yüzüklerin Efendisi: Yüzük Kardeşliği, dünyanin kaderini değişterecek olan yüzükten kurtulmak için verilen mücadeleyi konu ediyor..",
      year: "2001",
      videoUrl: "The Lord of the Rings.mp4",
      url: "The Lord of the Rings.jpg",
      urlmain: "lotr.jpg",
    },
    {
      title: "Thor Love and Thunder",
      genre: "Fantastik",
      description:
        "Thor: Aşk ve Gök Gürültüsü, tanrilari yok etmeye and içen Gorr the God Butcher'a karşi zorlu bir mücadeleye girişen Thor'un hikayesini konu ediyor.",
      videoUrl: "Thor Love and Thunder.mp4",
      url: "Thor Love and Thunder.jpg",
      urlmain: "thor.jpg",
      year: "2022",
    },
    {
      title: "The Nun",
      genre: "Korku",
      description:
        "Geçmişinde karanlik olaylar yaşamiş Rahip Burke (Demián Bichir) ve rahibe olmak için son aşamalara gelmiş genç rahibe adayi Irene (Taissa Farmiga), kendini öldürmüş bir rahibeyle ilgili araştirma yapmak için Vatikan tarafindan Romanya'nin ücra bir köşesindeki bir manastira gönderilir. Manastirin sirrini öğrenen ikili, sadece hayatlarini değil, hayatlarini adadiklari inançlarini da ortaya koyarak bir rahibe formuna karşilarina çikan şeytani güçle savaşacaktir.",
      videoUrl: "TheNun.mp4",
      url: "TheNun.jpg",
      urlmain: "nun.jpg",
      year: "2018",
    },
    {
      title: "Pirates of the Caribbean",
      genre: "Fantastic",
      description:
        "Jack, Salazar'in gazabindan ve intikamindan kurtulmak için Poseidon Asasinin peşine düşer. Bu efsanevi asayi bulmak içinse güzel ve zeki gökbilimci Carina Smyth ve Kraliyet Donanmasi'ndan  dik başli, genç bir denizci olan Henry ile zorlu bir anlaşma yapar.",
      videoUrl: "Pirates of the Caribbean.mp4",
      url: "Pirates of the Caribbean.jpg",
      urlmain: "pirate.jpg",
      year: "2017",
    },
    {
      title: "Dexter",
      genre: "Drama",
      description:
        "Gündüzleri adli tip polisi, geceleri ise seri katil, üstelik ikisinde de çok başarili. Bir katili bir başka katilden daha iyi kim anlayabilir! Öldürme arzusu disinda insani duygulardan yoksun doğan Dexter, ahlaki değerleri olan bir seri katil: Sadece yasalarin elinden kaçmayi başaran canileri öldürüyor..",
      videoUrl: "Dexter.mp4",
      url: "Dexter.jpg",
      urlmain: "dexter1.jpg",
      year: "2006",
    },
    {
      title: "The Witcher",
      genre: "Fantastic",
      description:
        "Witcher Saga roman serisi sayisiz dile çevrilen, hakkinda film, dizi, oyun ve grafik roman yapilan The Witcher, Netflix ekranlarinda izleyiciyle buluşacak. Video oyunu tüm dünyada 33 milyonun üzerinde satarak çok büyük bir başari yakalayan The Witcher, genç yaşta doğaüstü yetenekleriyle canavarlarla savaşan cadilari anlatmakta.",
      videoUrl: "witcher.mp4",
      url: "witcher.jpg",
      urlmain: "witcher1.jpeg",
      year: "2019",
    },
    {
      title: "Game of Thrones",
      genre: "Drama",
      description:
        "Kis yaklasiyor, hanedan entrikalari, kapali kapilar ardinda dönen oyunlar, birilerinin kuyusunu kazmak icin dusmanina yaklasan kadinlar,kardesler arasi cekismeler hepsi tek bir amac icin demir bir taht.",
      videoUrl: "Game of Thrones.mp4",
      url: "Game of Thrones.jpg",
      urlmain: "got.jpg",
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
      urlmain: "knock at the cabin.jpeg",
    },
    {
      title: "Hatching",
      genre: "Korku",
      description:
        "Hirsli ve takintili annesini tatmin etmek için umutsuzca çabalayan genç bir kiz, bir gün ormanda tuhaf bir yumurta bulur. Yumurtayi sicak tutarak, çatlayana kadar odasinda saklar ancak yumurtanin içinden çikan şey genç kizin hayatini derinden etkileyecektir.",
      year: "2022",
      videoUrl: "hatching.mp4",
      url: "hatching.jpg",
      urlmain: "hatching1.png",
    },
    {
      title: "M3GAN",
      genre: "Korku",
      description:
        "M3GAN dahi bir oyuncak şirketinde çalişan robotik mühendisi olan bir adamin hikayesini konu ediyor. Mühendis, yakin zamanda yetim kalmis olan yeğenine destek olmasi ve arkadaslik etmesi için bir robot tasarlar. Ancak küçük kiz ile duygusal olarak bağ kurmaya programlanmis insansi robot, programlamasi fazla iyi işlediği için yeni arkadaşi konusunda aşiri korumaci bir hale gelir.",
      videoUrl: "m3gan.mp4",
      url: "m3gan.jpg",
      urlmain: "m3gan1.jpg",
      year: "2023",
    },
    {
      title: "Wrong Turn",
      genre: "Korku",
      description:
        " Başlangiç, dağ gezisi yapmak için yola koyulan 6 arkadaşin başlarina gelenleri konu ediyor. New York'ta yaşayan alti arkadaş, Bati Virginia Dağlari'nda yürüyüş yapmak için yola koyulur. Grubun eğlenceli geçen yürüyüşleri, yillarca dağlarda yaşayan ve The Foundation olarak bilinen vahşi bir tarikata rastlamalariyla yerini korku dolu anlara birakir.",
      videoUrl: "wrongturn.mp4",
      url: "wrongturn.jpg",
      urlmain: "wrongturn1.jpg",
      year: "2021",
    },
    {
      title: "SMILE",
      genre: "Horror",
      description:
        "Gülümse, yaşadiği tuhaf olaylardan kurtulmak için sorunlu geçmişiyle yüzleşmek zorunda olan bir kadinin hayatina odaklaniyor. Bir hastayi içeren tuhaf, travmatik bir olaya tanik olan Dr. Rose Cotter, açiklayamadiği korkutucu olaylar yaşamaya başlar.",
      videoUrl: "smile.mp4",
      url: "smile.jpg",
      urlmain: "smile1.jpg",
      year: "2022",
    },
    {
      title: "Scream 6",
      genre: "Korku",
      description:
        "Çiğlik 6, Hayalet Maskeli cinayetlerinden kurtulduktan sonra Woodsboro kasabasini geride birakip New York'ta yeni bir hayata başkayan dört kişinin hayatina odaklaniyor.",
      videoUrl: "scream6.mp4",
      url: "scream6.jpg",
      urlmain : "scream6-1.jpg",
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
      urlmain: "knock at the cabin.jpeg",
    },
    {
      title: "Hatching",
      genre: "Korku",
      description:
        "Hirsli ve takintili annesini tatmin etmek için umutsuzca çabalayan genç bir kiz, bir gün ormanda tuhaf bir yumurta bulur. Yumurtayi sicak tutarak, çatlayana kadar odasinda saklar ancak yumurtanin içinden çikan şey genç kizin hayatini derinden etkileyecektir.",
      year: "2022",
      videoUrl: "hatching.mp4",
      url: "hatching.jpg",
      urlmain: "hatching1.png",
    },
    {
      title: "M3GAN",
      genre: "Korku",
      description:
        "M3GAN dahi bir oyuncak şirketinde çalişan robotik mühendisi olan bir adamin hikayesini konu ediyor. Mühendis, yakin zamanda yetim kalmis olan yeğenine destek olmasi ve arkadaslik etmesi için bir robot tasarlar. Ancak küçük kiz ile duygusal olarak bağ kurmaya programlanmis insansi robot, programlamasi fazla iyi işlediği için yeni arkadaşi konusunda aşiri korumaci bir hale gelir.",
      videoUrl: "m3gan.mp4",
      url: "m3gan.jpg",
      urlmain: "m3gan1.jpg",
      year: "2023",
    },
    {
      title: "Wrong Turn",
      genre: "Korku",
      description:
        " Başlangiç, dağ gezisi yapmak için yola koyulan 6 arkadaşin başlarina gelenleri konu ediyor. New York'ta yaşayan alti arkadaş, Bati Virginia Dağlari'nda yürüyüş yapmak için yola koyulur. Grubun eğlenceli geçen yürüyüşleri, yillarca dağlarda yaşayan ve The Foundation olarak bilinen vahşi bir tarikata rastlamalariyla yerini korku dolu anlara birakir.",
      videoUrl: "wrongturn.mp4",
      url: "wrongturn.jpg",
      urlmain: "wrongturn1.jpg",
      year: "2021",
    },
    {
      title: "SMILE",
      genre: "Horror",
      description:
        "Gülümse, yaşadiği tuhaf olaylardan kurtulmak için sorunlu geçmişiyle yüzleşmek zorunda olan bir kadinin hayatina odaklaniyor. Bir hastayi içeren tuhaf, travmatik bir olaya tanik olan Dr. Rose Cotter, açiklayamadiği korkutucu olaylar yaşamaya başlar.",
      videoUrl: "smile.mp4",
      url: "smile.jpg",
      urlmain: "smile1.jpg",
      year: "2022",
    },
    {
      title: "Scream 6",
      genre: "Korku",
      description:
        "Çiğlik 6, Hayalet Maskeli cinayetlerinden kurtulduktan sonra Woodsboro kasabasini geride birakip New York'ta yeni bir hayata başkayan dört kişinin hayatina odaklaniyor.",
      videoUrl: "scream6.mp4",
      url: "scream6.jpg",
      urlmain : "scream6-1.jpg",
      year: "2023",
    },
  
    // Diğer filmler...
  ]);
  const films2 = ref([
    {
      title: "Avengers",
      genre: "Aksiyon,Macera,Fantastik",
      description:
        "Marvel Studios tarafindan üretilen ve Marvel Comics'in süper kahraman ekibidir..",
      year: "2012",
      videoUrl: "Avengers.mp4",
      url: "Avengers.jpg",
      urlmain: "avenger.jpg"
    },
    {
      title: "The Lord of the Rings",
      genre: "Fantastik",
      description:
        "Yüzüklerin Efendisi: Yüzük Kardeşliği, dünyanin kaderini değişterecek olan yüzükten kurtulmak için verilen mücadeleyi konu ediyor..",
      year: "2001",
      videoUrl: "The Lord of the Rings.mp4",
      url: "The Lord of the Rings.jpg",
      urlmain: "lotr.jpg",
    },
    {
      title: "Thor Love and Thunder",
      genre: "Fantastik",
      description:
        "Thor: Aşk ve Gök Gürültüsü, tanrilari yok etmeye and içen Gorr the God Butcher'a karşi zorlu bir mücadeleye girişen Thor'un hikayesini konu ediyor.",
      videoUrl: "Thor Love and Thunder.mp4",
      url: "Thor Love and Thunder.jpg",
      urlmain: "thor.jpg",
      year: "2022",
    },
    {
      title: "The Nun",
      genre: "Korku",
      description:
        "Geçmişinde karanlik olaylar yaşamiş Rahip Burke (Demián Bichir) ve rahibe olmak için son aşamalara gelmiş genç rahibe adayi Irene (Taissa Farmiga), kendini öldürmüş bir rahibeyle ilgili araştirma yapmak için Vatikan tarafindan Romanya'nin ücra bir köşesindeki bir manastira gönderilir. Manastirin sirrini öğrenen ikili, sadece hayatlarini değil, hayatlarini adadiklari inançlarini da ortaya koyarak bir rahibe formuna karşilarina çikan şeytani güçle savaşacaktir.",
      videoUrl: "TheNun.mp4",
      url: "TheNun.jpg",
      urlmain: "nun.jpg",
      year: "2018",
    },
    {
      title: "Pirates of the Caribbean",
      genre: "Fantastic",
      description:
        "Jack, Salazar'in gazabindan ve intikamindan kurtulmak için Poseidon Asasinin peşine düşer. Bu efsanevi asayi bulmak içinse güzel ve zeki gökbilimci Carina Smyth ve Kraliyet Donanmasi'ndan  dik başli, genç bir denizci olan Henry ile zorlu bir anlaşma yapar.",
      videoUrl: "Pirates of the Caribbean.mp4",
      url: "Pirates of the Caribbean.jpg",
      urlmain: "pirate.jpg",
      year: "2017",
    },
    {
      title: "Dexter",
      genre: "Drama",
      description:
        "Gündüzleri adli tip polisi, geceleri ise seri katil, üstelik ikisinde de çok başarili. Bir katili bir başka katilden daha iyi kim anlayabilir! Öldürme arzusu disinda insani duygulardan yoksun doğan Dexter, ahlaki değerleri olan bir seri katil: Sadece yasalarin elinden kaçmayi başaran canileri öldürüyor..",
      videoUrl: "Dexter.mp4",
      url: "Dexter.jpg",
      urlmain: "dexter1.jpg",
      year: "2006",
    },
    {
      title: "The Witcher",
      genre: "Fantastic",
      description:
        "Witcher Saga roman serisi sayisiz dile çevrilen, hakkinda film, dizi, oyun ve grafik roman yapilan The Witcher, Netflix ekranlarinda izleyiciyle buluşacak. Video oyunu tüm dünyada 33 milyonun üzerinde satarak çok büyük bir başari yakalayan The Witcher, genç yaşta doğaüstü yetenekleriyle canavarlarla savaşan cadilari anlatmakta.",
      videoUrl: "witcher.mp4",
      url: "witcher.jpg",
      urlmain: "witcher1.jpeg",
      year: "2019",
    },
    {
      title: "Game of Thrones",
      genre: "Drama",
      description:
        "Kis yaklasiyor, hanedan entrikalari, kapali kapilar ardinda dönen oyunlar, birilerinin kuyusunu kazmak icin dusmanina yaklasan kadinlar,kardesler arasi cekismeler hepsi tek bir amac icin demir bir taht.",
      videoUrl: "Game of Thrones.mp4",
      url: "Game of Thrones.jpg",
      urlmain: "got.jpg",
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
      urlmain: "knock at the cabin.jpeg",
    },
    {
      title: "Hatching",
      genre: "Korku",
      description:
        "Hirsli ve takintili annesini tatmin etmek için umutsuzca çabalayan genç bir kiz, bir gün ormanda tuhaf bir yumurta bulur. Yumurtayi sicak tutarak, çatlayana kadar odasinda saklar ancak yumurtanin içinden çikan şey genç kizin hayatini derinden etkileyecektir.",
      year: "2022",
      videoUrl: "hatching.mp4",
      url: "hatching.jpg",
      urlmain: "hatching1.png",
    },
    {
      title: "M3GAN",
      genre: "Korku",
      description:
        "M3GAN dahi bir oyuncak şirketinde çalişan robotik mühendisi olan bir adamin hikayesini konu ediyor. Mühendis, yakin zamanda yetim kalmis olan yeğenine destek olmasi ve arkadaslik etmesi için bir robot tasarlar. Ancak küçük kiz ile duygusal olarak bağ kurmaya programlanmis insansi robot, programlamasi fazla iyi işlediği için yeni arkadaşi konusunda aşiri korumaci bir hale gelir.",
      videoUrl: "m3gan.mp4",
      url: "m3gan.jpg",
      urlmain: "m3gan1.jpg",
      year: "2023",
    },
    {
      title: "Wrong Turn",
      genre: "Korku",
      description:
        " Başlangiç, dağ gezisi yapmak için yola koyulan 6 arkadaşin başlarina gelenleri konu ediyor. New York'ta yaşayan alti arkadaş, Bati Virginia Dağlari'nda yürüyüş yapmak için yola koyulur. Grubun eğlenceli geçen yürüyüşleri, yillarca dağlarda yaşayan ve The Foundation olarak bilinen vahşi bir tarikata rastlamalariyla yerini korku dolu anlara birakir.",
      videoUrl: "wrongturn.mp4",
      url: "wrongturn.jpg",
      urlmain: "wrongturn1.jpg",
      year: "2021",
    },
    {
      title: "SMILE",
      genre: "Horror",
      description:
        "Gülümse, yaşadiği tuhaf olaylardan kurtulmak için sorunlu geçmişiyle yüzleşmek zorunda olan bir kadinin hayatina odaklaniyor. Bir hastayi içeren tuhaf, travmatik bir olaya tanik olan Dr. Rose Cotter, açiklayamadiği korkutucu olaylar yaşamaya başlar.",
      videoUrl: "smile.mp4",
      url: "smile.jpg",
      urlmain: "smile1.jpg",
      year: "2022",
    },
    {
      title: "Scream 6",
      genre: "Korku",
      description:
        "Çiğlik 6, Hayalet Maskeli cinayetlerinden kurtulduktan sonra Woodsboro kasabasini geride birakip New York'ta yeni bir hayata başkayan dört kişinin hayatina odaklaniyor.",
      videoUrl: "scream6.mp4",
      url: "scream6.jpg",
      urlmain : "scream6-1.jpg",
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
  const ftitleRef = ref(null);
  
  
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
    translateAmount.value += 3;
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
    translateAmount.value -= 3;
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
    translateAmount.value += 3;
    
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
    translateAmount.value -= 3;
    
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
  function performaction4(){
    translateAmount.value += 3;
    const swiperContainer2 = document.querySelector('.swiper-container2');
    swiperContainer2.style.transform = `translate(${translateAmount.value}px)`;
    currentIndex++;
    
    if (films2.value.length > currentIndex) {
      films2.value.push(films2.value[currentIndex]);
      if(films2.value.length > 10){
        
        films2.value.shift(); // En baştaki elemanı çıkar
        currentIndex--;
        
        
      }
      
    }
    
    
  }
  
  function performaction5(){
    translateAmount.value -= 3;
    const swiperContainer2 = document.querySelector('.swiper-container2');
    swiperContainer2.style.transform = `translate(${translateAmount.value}px)`;
    currentIndex++;
    
    if (films2.value.length > currentIndex) {
      films2.value.push(films2.value[currentIndex]);
      if(films2.value.length > 10){
        
        films2.value.shift(); // En baştaki elemanı çıkar
        currentIndex--;
        
        
      }
      
    }
   
  }
  
    
    
  
  
  
  onMounted(() => {
    selectedFilm.value = films.value[0];
    setTimeout(() => {
      const fTitle = document.querySelector('.ftitle');
      fTitle.style.transform = 'scale(0.8) translate3d(100px, 550px, 500px)';
      fTitle.style.transformOrigin = 'left bottom';
      fTitle.style.transition = 'transform 1300ms';
  
      const fDesc = document.querySelector('.fdesc');
      fDesc.style.opacity = '0';
  
  
      
  
  
      
    }, 13000); // 13 saniye
    
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
    width: 400px;
    height: 200px;
    background-color: black;
  }
  .swiper-container {
    overflow: visible;
    display: flex;
    transition: all 5s ease-out;
    -webkit-animation: scrolling-left1 20s linear infinite;
    animation: scrolling-left1 20s linear infinite;
    
  
    
  }
  .swiper-container1 {
    overflow: visible;
    display: flex;
    transition: all 5s ease-out;
    -webkit-animation: scrolling-left1 20s linear infinite;
    animation: scrolling-left1 20s linear infinite;
   
    
    
  }
  .swiper-container2 {
    overflow: visible;
    display: flex;
    transition: all 5s ease-out;
    -webkit-animation: scrolling-left1 20s linear infinite;
    animation: scrolling-left1 20s linear infinite;
   
    
    
  }
  
  .swiper-slide {
    --items-per-screen: 4;
    --slider-index: 0;
    display: flex;
    flex-grow: 1;
    margin: -20px;
    transform: translateX(calc(var(--slider-index) * -100%));
    transition: transform 250ms ease-in-out;
    
    
  }
  .swiper-wrapper{
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .swiper-slide h4 {
    
   
    position: absolute;
    
   
    top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      
     
    opacity: 0;
    font-size: 10px;
    color: white;
    font-family: sans-serif;
    font-weight: bolder;
    background: none;
    
   
  color: white;
    padding: 8px;
    border-radius: 5px;
    
   
  transition: opacity 300ms ease-in-out;
    }
    .swiper-slide:hover h4 {
    
   
    opacity: 1;
    }  
  
  .swiper-slide > img {
    border-radius: 5px;
    max-width: 280px;
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
    top: 700px;
    left: 0px;
    display: flex;
    justify-content: space-between;
    z-index: 1;
    margin-left: 100px;
    align-items: center;
    padding: 10px;
    background: none;
  }
  
  .info-button,
  .play-button {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.8rem;
    cursor: pointer;
    max-height: 42px;
    min-height: 32px;
    font-size: 1.6rem;
    color: white;
    
  }
  
  .modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 1870px;
    
    margin: 20px 20px;
    border-radius: 6px;
    z-index: 2;
    background-color: var(--modal);
    box-shadow: rgb(0 0 0 / 75%) 0px 3px 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: opacity 0.2s linear;
    
  }
  
  .modal-content {
    background-color: black;
    padding: 20px;
    border-radius: 5px;
    height: 800px;
    
    width: 800px;
    
    color: white;
    font-family: sans-serif;
    font-size: large;
  }
  
  .video-section {
    position: relative;
    padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
    height: 500px;
    overflow: visible;
    margin-bottom: 20px;
  }
  
  
  .movieDetails{
    color: white;
    font-family: sans-serif;
    font-size: larger;
  }
  .close-button {
    font-family: sans-serif;
    color: white;
    font-size: x-large;
    
  }
  .video-thumbnail-container {
    position: relative;
    width: 100%;
    height: 1100px;
    top: 0px;
  }
  
  .video-thumbnail {
    width: 100%;
    height: 1000px;
  }
  .video-thumbnail-container1 {
    position: relative;
    width: 100%;
    height: 500px;
  }
  
  .video-thumbnail1 {
    width: 100%;
    height: 450px;
  }
  
  video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    transition: opacity 2s ease-in-out;
  }
  
  .video-thumbnail-container:hover video {
    opacity: 1;
  }
  .video-thumbnail-container1:hover video {
    opacity: 1;
  }
  
  
  .buttons{
    
    justify-content: center;
    display: flex;
    gap: 10px;
    background: none;
    cursor: pointer;
  }
  .play-button:hover,
  .info-button:hover {
      
     
  background: rgba(255, 255, 255, 0.1); /* Butonun üzerine gelindiğinde hafif bir background efekti */
      border: none; /* Kenarlık yerine border kullanmama kararı aldık */
      color: white; /* Buton içeriği rengi */
  }
  
  /* Butonlara tıklanabilirlik hissi vermek için */
  .play-button:active,
  .info-button:active {
      transform: translateY(2px);
  }
  .cm{
    color: white;
    position: absolute;
    top: 200px;
    left: 0;
    display: flex;
    flex-direction: column; /* Metinleri dikey olarak yerleştirir */
    
    z-index: 1;
    margin-left: 10px;
    padding: 10px;
    background: none;
    width: 450px;
    
  }
  .ftitle{
    color: white;
    font-size: 34px;
    font-family: sans-serif;
    background: none;
    font-weight: bolder;
    
    
  }
  .fdesc{
    color: white;
    font-size: 20px;
    font-family: sans-serif;
    background: none;
    font-weight: bolder;
    
  
  
  }
  .t1{
    color: white;
    font-size: 30px;
    font-family: sans-serif;
    font-weight: bolder;
  }
  .t2{
    color: white;
    font-size: 18px;
    font-family: sans-serif;
    font-weight: bolder;
  }
  .t3{
    color: white;
    font-size: 18px;
    font-family: sans-serif;
    font-weight: bolder;
  }
  .member-footer {
      color: grey;
      margin: 20px auto 0;
      max-width: 1280px;
      padding: 0 4%;
      
  }
  .member-footer .social-links {
      display: flex;
      margin-bottom: 1em;
  }
  .member-footer .social-links {
      display: flex;
      margin-bottom: 1em;
      
  }
  a {
      color: #fff;
      cursor: pointer;
      text-decoration: none;
  }
  a {
      background-color: transparent;
  }
  .member-footer .social-links .social-link .svg-icon {
      fill: grey;
      height: 35px;
      width: 36px;
      margin: 20px;
  }
  .t_17d527 .svg-icon {
      border: 1px solid transparent;
      margin: 0 -1px;
      overflow: visible;
      transform: scale(1);
  }
  .member-footer .member-footer-links {
      align-items: flex-start;
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      font-size: 19px;
      margin: 0 0 14px;
      padding: 0;
      
  }
  .member-footer .member-footer-link-wrapper {
     justify-content: center;
      box-sizing: border-box;
      flex: 0 0 25%;
      list-style-type: none;
      margin-bottom: 16px;
      padding-right: 16px;
  }
  li {
      display: list-item;
      text-align: -webkit-match-parent;
  }
  .member-footer .member-footer-link {
      color: grey;
      text-decoration: none;
  }
  .member-footer .service-code {
      font-size: 19px;
      margin-bottom: 20px;
      padding: 0.5em;
  }
  .service-code {
      background: transparent;
      border: 1px solid grey;
      color: grey;
      font-size: 1.3rem;
      padding: 0.5rem;
      font-weight: bolder;
  }
  button, html input[type=button], input[type=reset], input[type=submit] {
      -webkit-appearance: button;
      cursor: pointer;
  }
  .member-footer .member-footer-copyright {
      font-size: 19px;
      margin-bottom: 15px;
  }
  
  
  
  </style>
  