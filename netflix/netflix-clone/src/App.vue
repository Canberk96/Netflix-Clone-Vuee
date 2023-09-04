<template>
  
    

    
  <div class="mainContainer">
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
            <div class="searchbox">
              <button class="searchTab" tabindex="0" aria-label="Search" data-uia="search-box-launcher">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="search-icon ltr-0 e1mhci4z1" data-name="MagnifyingGlass" aria-hidden="true">
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M17 10C17 13.866 13.866 17 10 17C6.13401 17 3 13.866 3 10C3 6.13401 6.13401 3 10 3C13.866 3 17 6.13401 17 10ZM15.6177 17.0319C14.078 18.2635 12.125 19 10 19C5.02944 19 1 14.9706 1 10C1 5.02944 5.02944 1 10 1C14.9706 1 19 5.02944 19 10C19 12.125 18.2635 14.078 17.0319 15.6177L22.7071 21.2929L21.2929 22.7071L15.6177 17.0319Z" fill="currentColor"></path>
                </svg>
              </button>
            </div>
            <a href="/Kids">Kids</a>
            <span class="notifications"><button class="notifications-menu" aria-haspopup="true" aria-expanded="false" aria-label="Notifications"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="ltr-0 e1mhci4z1" data-name="Bell" aria-hidden="true"><path fill-rule="evenodd" clip-rule="evenodd" d="M13.0002 4.07092C16.3924 4.55624 19 7.4736 19 11V15.2538C20.0489 15.3307 21.0851 15.4245 22.1072 15.5347L21.8928 17.5232C18.7222 17.1813 15.4092 17 12 17C8.59081 17 5.27788 17.1813 2.10723 17.5232L1.89282 15.5347C2.91498 15.4245 3.95119 15.3307 5.00003 15.2538V11C5.00003 7.47345 7.60784 4.55599 11.0002 4.07086V2H13.0002V4.07092ZM17 15.1287V11C17 8.23858 14.7614 6 12 6C9.2386 6 7.00003 8.23858 7.00003 11V15.1287C8.64066 15.0437 10.3091 15 12 15C13.691 15 15.3594 15.0437 17 15.1287ZM8.62593 19.3712C8.66235 20.5173 10.1512 22 11.9996 22C13.848 22 15.3368 20.5173 15.3732 19.3712C15.3803 19.1489 15.1758 19 14.9533 19H9.0458C8.82333 19 8.61886 19.1489 8.62593 19.3712Z" fill="currentColor"></path></svg>
            </button>
          </span>
            
             <span>
              <img src="Netflix-avatar.png" alt="" class="userImg">
             </span>
             <div class="dropdown">
              <button class="dropbtn">v</button>
              <div class="dropdown-content">
                <div class="flex">
                  <a href="#">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" data-mirrorinrtl="true" class="ltr-0 e1mhci4z1" data-name="Pencil" aria-hidden="true"><path fill-rule="evenodd" clip-rule="evenodd" d="M19.1213 1.7071C17.9497 0.535532 16.0503 0.53553 14.8787 1.7071L13.2929 3.29289L12.5858 4L1.58579 15C1.21071 15.3751 1 15.8838 1 16.4142V21C1 22.1046 1.89543 23 3 23H7.58579C8.11622 23 8.62493 22.7893 9 22.4142L20 11.4142L20.7071 10.7071L22.2929 9.12132C23.4645 7.94975 23.4645 6.05025 22.2929 4.87868L19.1213 1.7071ZM15.5858 7L14 5.41421L3 16.4142L3 19C3.26264 19 3.52272 19.0517 3.76537 19.1522C4.00802 19.2527 4.2285 19.4001 4.41421 19.5858C4.59993 19.7715 4.74725 19.992 4.84776 20.2346C4.94827 20.4773 5 20.7374 5 21L7.58579 21L18.5858 10L17 8.41421L6.70711 18.7071L5.29289 17.2929L15.5858 7ZM16.2929 3.12132C16.6834 2.73079 17.3166 2.73079 17.7071 3.12132L20.8787 6.29289C21.2692 6.68341 21.2692 7.31658 20.8787 7.7071L20 8.58578L15.4142 4L16.2929 3.12132Z" fill="currentColor"></path></svg>
                    Manage Profiles
                  </a>
                </div>
                <a href="#">
                  <svg id="profile-transfer" width="24" height="24" viewBox="0 0 24 24" fill="none"><path fill-rule="evenodd" clip-rule="evenodd" d="M6 1C3.79086 1 2 2.79086 2 5V17C2 19.2091 3.79086 21 6 21H9.58579L8.29289 22.2929L9.70711 23.7071L12.7071 20.7071C13.0976 20.3166 13.0976 19.6834 12.7071 19.2929L9.70711 16.2929L8.29289 17.7071L9.58579 19H6C4.89543 19 4 18.1046 4 17V5C4 3.89543 4.89543 3 6 3H18C19.1046 3 20 3.89543 20 5V17C20 18.1046 19.1046 19 18 19H15V21H18C20.2091 21 22 19.2091 22 17V5C22 2.79086 20.2091 1 18 1H6ZM7.5 10C8.32843 10 9 9.32843 9 8.5C9 7.67157 8.32843 7 7.5 7C6.67157 7 6 7.67157 6 8.5C6 9.32843 6.67157 10 7.5 10ZM18 8.5C18 9.32843 17.3284 10 16.5 10C15.6716 10 15 9.32843 15 8.5C15 7.67157 15.6716 7 16.5 7C17.3284 7 18 7.67157 18 8.5ZM16.402 12.1985C15.7973 12.6498 14.7579 13 13.5 13C12.2421 13 11.2027 12.6498 10.598 12.1985L9.40195 13.8015C10.4298 14.5684 11.9192 15 13.5 15C15.0808 15 16.5702 14.5684 17.598 13.8015L16.402 12.1985Z" fill="currentColor"></path></svg>
                    Transfer Profile</a>
                <a href="#">
                  <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="ltr-0 e1mhci4z1" data-name="User" aria-hidden="true"><path fill-rule="evenodd" clip-rule="evenodd" d="M15 5C15 6.65685 13.6569 8 12 8C10.3431 8 9 6.65685 9 5C9 3.34315 10.3431 2 12 2C13.6569 2 15 3.34315 15 5ZM17 5C17 7.76142 14.7614 10 12 10C9.23858 10 7 7.76142 7 5C7 2.23858 9.23858 0 12 0C14.7614 0 17 2.23858 17 5ZM4 21C4 16.5817 7.58172 13 12 13C16.4183 13 20 16.5817 20 21V21.5136C19.5678 21.5667 18.9844 21.6327 18.2814 21.6988C16.6787 21.8495 14.461 22 12 22C9.53901 22 7.32131 21.8495 5.71861 21.6988C5.01564 21.6327 4.43224 21.5667 4 21.5136V21ZM21.1508 23.3775C21.1509 23.3774 21.151 23.3774 21 22.3889L21.151 23.3774C21.6393 23.3028 22 22.8829 22 22.3889V21C22 15.4772 17.5228 11 12 11C6.47715 11 2 15.4772 2 21V22.3889C2 22.8829 2.36067 23.3028 2.84897 23.3774L3 22.3889C2.84897 23.3774 2.84908 23.3774 2.8492 23.3775L2.84952 23.3775L2.85043 23.3776L2.85334 23.3781L2.86352 23.3796L2.90103 23.3852C2.93357 23.3899 2.98105 23.3968 3.04275 23.4055C3.16613 23.4228 3.3464 23.4472 3.57769 23.4765C4.04018 23.535 4.7071 23.6126 5.5314 23.6901C7.1787 23.8449 9.461 24 12 24C14.539 24 16.8213 23.8449 18.4686 23.6901C19.2929 23.6126 19.9598 23.535 20.4223 23.4765C20.6536 23.4472 20.8339 23.4228 20.9573 23.4055C21.0189 23.3968 21.0664 23.3899 21.099 23.3852L21.1365 23.3796L21.1467 23.3781L21.1496 23.3776L21.1505 23.3775L21.1508 23.3775Z" fill="currentColor"></path></svg>
                  Account</a>
                <a href="#">
                  <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="ltr-0 e1mhci4z1" data-name="CircleQuestionMark" aria-hidden="true"><path fill-rule="evenodd" clip-rule="evenodd" d="M2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12C22 17.5228 17.5228 22 12 22C6.47715 22 2 17.5228 2 12ZM12 0C5.37258 0 0 5.37258 0 12C0 18.6274 5.37258 24 12 24C18.6274 24 24 18.6274 24 12C24 5.37258 18.6274 0 12 0ZM12 8C10.6831 8 10 8.74303 10 9.5H8C8 7.25697 10.0032 6 12 6C13.9968 6 16 7.25697 16 9.5C16 10.8487 14.9191 11.7679 13.8217 12.18C13.5572 12.2793 13.3322 12.4295 13.1858 12.5913C13.0452 12.7467 13 12.883 13 13V14H11V13C11 11.5649 12.1677 10.6647 13.1186 10.3076C13.8476 10.0339 14 9.64823 14 9.5C14 8.74303 13.3169 8 12 8ZM13.5 16.5C13.5 17.3284 12.8284 18 12 18C11.1716 18 10.5 17.3284 10.5 16.5C10.5 15.6716 11.1716 15 12 15C12.8284 15 13.5 15.6716 13.5 16.5Z" fill="currentColor"></path></svg>
                  Help Center</a>
            </div>
             </div>
             
             
          </div>
    </div>
    <div class="video-thumbnail-container" @mouseenter="handleMouseEnter" @mouseleave="handleMouseLeave">
        <img :src="selectedFilm.urlmain" alt="Video Thumbnail" class="video-thumbnail" />
        <video ref="videoPlayer" class="w-[100%] h-[100%]" loop>
          <source :src="selectedFilm.videoUrl" type="video/mp4" />
        </video>
      </div>
      <div class="cm">
        <div class="ftitle" ref="ftitleRef">{{ selectedFilm.title }}</div>
        <div class="fdesc">{{ selectedFilm.description }}</div>
        
      </div>
      
  
      <div class="button-container">
        
          <div class="buttons">
            <div class="pbutton">
              <button class="play-button" @click="togglePlay">
                          <svg width="24" height="24" viewBox="0 0 24 24" fill="gray" xmlns="http://www.w3.org/2000/svg">
                            <path d="M4 2.69127C4 1.93067 4.81547 1.44851 5.48192 1.81506L22.4069 11.1238C23.0977 11.5037 23.0977 12.4963 22.4069 12.8762L5.48192 22.1849C4.81546 22.5515 4 22.0693 4 21.3087V2.69127Z" fill="black"></path>
                              </svg>Play</button>
                              <br>
            </div>
            <div class="ibutton">
              <button class="info-button" @click="showMoreInfo"><i class="bi bi-info-circle" style=" padding: 0%;">
                
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="ltr-0 e1mhci4z1" data-name="CircleI" aria-hidden="true">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2ZM0 12C0 5.37258 5.37258 0 12 0C18.6274 0 24 5.37258 24 12C24 18.6274 18.6274 24 12 24C5.37258 24 0 18.6274 0 12ZM13 10V18H11V10H13ZM12 8.5C12.8284 8.5 13.5 7.82843 13.5 7C13.5 6.17157 12.8284 5.5 12 5.5C11.1716 5.5 10.5 6.17157 10.5 7C10.5 7.82843 11.1716 8.5 12 8.5Z" fill="currentColor"></path>

              </svg></i> More Info</button>

            </div>
                        
                      </div>
                      <div class="embedded-components button-layer">
                        <span class="ActionButtons">
                          <div id="audio" @click="tikla" class="global-supplemental-audio-toggle audio-btn button-layer"><button  aria-label="Turn audio on" class="color-supplementary hasIcon round ltr-11vo9g5" data-uia="audio-toggle-unmuted" type="button"><div class="ltr-1st24vv"><div class="small ltr-iyulz3" role="presentation"><svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="ltr-0 e1mhci4z1" data-name="VolumeHigh" aria-hidden="true"><path fill-rule="evenodd" clip-rule="evenodd" d="M24 12C24 8.28693 22.525 4.72597 19.8995 2.10046L18.4853 3.51468C20.7357 5.76511 22 8.81736 22 12C22 15.1826 20.7357 18.2348 18.4853 20.4852L19.8995 21.8995C22.525 19.2739 24 15.713 24 12ZM11 3.99995C11 3.59549 10.7564 3.23085 10.3827 3.07607C10.009 2.92129 9.57889 3.00685 9.29289 3.29285L4.58579 7.99995H1C0.447715 7.99995 0 8.44767 0 8.99995V15C0 15.5522 0.447715 16 1 16H4.58579L9.29289 20.7071C9.57889 20.9931 10.009 21.0786 10.3827 20.9238C10.7564 20.7691 11 20.4044 11 20V3.99995ZM5.70711 9.70706L9 6.41417V17.5857L5.70711 14.2928L5.41421 14H5H2V9.99995H5H5.41421L5.70711 9.70706ZM16.0001 12C16.0001 10.4087 15.368 8.88254 14.2428 7.75732L12.8285 9.17154C13.5787 9.92168 14.0001 10.9391 14.0001 12C14.0001 13.0608 13.5787 14.0782 12.8285 14.8284L14.2428 16.2426C15.368 15.1174 16.0001 13.5913 16.0001 12ZM17.0709 4.92889C18.9462 6.80426 19.9998 9.3478 19.9998 12C19.9998 14.6521 18.9462 17.1957 17.0709 19.071L15.6567 17.6568C17.157 16.1565 17.9998 14.1217 17.9998 12C17.9998 9.87823 17.157 7.8434 15.6567 6.34311L17.0709 4.92889Z" fill="currentColor"></path></svg></div></div></button></div>
                        </span>
                        <span class="maturity-rating1 "><span class="maturity-number1">13+</span></span>
                      </div>
         
        
  
  
      </div>
      <div v-if="showMoreInfoModal" class="modal">
        <div class="modal-content">
        <div class="video-section">
          <div class="video-thumbnail-container1" @mouseenter="isHovering = true" @mouseleave="isHovering = false">
        <img :src="selectedFilm.url" alt="Video Thumbnail" class="video-thumbnail1" />
        <video ref="videoPlayer"  autoplay class="anavideo" loop>
          <source :src="selectedFilm.videoUrl" type="video/mp4" />
        </video>
      </div>
        </div>
        <div class="movie-details">
          <h2 class="t1">{{ selectedFilm.title }}</h2>
          
          
          <div class="previewModal--detailsMetadata detail-modal has-smaller-buttons" data-uia="previewModal--detailsMetadata">
            <div class="previewModal--detailsMetadata-left">
              <div class="previewModal--detailsMetadata-info">
                <div>
                  <div class>
                    <div data-uia="videoMetadata--container" class="videoMetadata--container">
                      <div class="videoMetadata--first-line">
                        <span class="match-score-wrapper">
                          <div class="show-match-score rating-inner">
                            <div class="meta-thumb-container thumb-down">
                              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="thumb thumb-down-filled svg-icon svg-icon-thumb-thumb-down-filled ltr-0 e1mhci4z1" data-name="ThumbsDownFill" aria-hidden="true">
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M10.593 17.7442L10.687 18.4959C10.8658 19.9265 12.0819 21 13.5236 21C13.7867 21 14 20.7867 14 20.5236V17.2868C14 17.0994 14.0527 16.9157 14.152 16.7568L16.0926 13.6519C16.3548 13.2323 16.7633 12.9248 17.2391 12.7888L19.2747 12.2072C19.704 12.0846 20 11.6922 20 11.2457V5.68387C20 5.30618 19.6938 5 19.3161 5C18.126 5 16.9565 4.68942 15.9232 4.09895L15.75 4C14.6032 3.34469 13.3053 3 11.9844 3H11H8H7.5C6.67157 3 6 3.67157 6 4.5C6 4.88418 6.14443 5.23462 6.38195 5.5H6C5.17157 5.5 4.5 6.17157 4.5 7C4.5 7.53991 4.78525 8.0132 5.21328 8.27737C4.522 8.41118 4 9.01963 4 9.75C4 10.5784 4.67157 11.25 5.5 11.25H5.67055C5.26638 11.5187 5 11.9783 5 12.5C5 13.3284 5.67157 14 6.5 14H10.875L10.593 16.2558C10.5312 16.75 10.5312 17.25 10.593 17.7442Z" fill="currentColor"></path>
                              </svg>
                            </div>
                            <div class="meta-thumb-container thumb-up">
                              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="thumb thumb-up-filled svg-icon svg-icon-thumb-thumb-up-filled ltr-0 e1mhci4z1" data-name="ThumbsUpFill" aria-hidden="true">
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M13.407 6.25579L13.313 5.50407C13.1342 4.07353 11.9181 3 10.4764 3C10.2133 3 10 3.21331 10 3.47644V6.7132C10 6.90062 9.94733 7.08427 9.848 7.2432L7.90742 10.3481C7.64516 10.7677 7.23665 11.0752 6.76086 11.2112L4.72528 11.7928C4.29598 11.9154 4 12.3078 4 12.7543V18.3161C4 18.6938 4.30618 19 4.68387 19C5.874 19 7.04352 19.3106 8.07684 19.9011L8.25 20C9.39679 20.6553 10.6947 21 12.0156 21H13H16H16.5C17.3284 21 18 20.3284 18 19.5C18 19.1158 17.8556 18.7654 17.6181 18.5H18C18.8284 18.5 19.5 17.8284 19.5 17C19.5 16.4601 19.2147 15.9868 18.7867 15.7226C19.478 15.5888 20 14.9804 20 14.25C20 13.4216 19.3284 12.75 18.5 12.75H18.3294C18.7336 12.4813 19 12.0217 19 11.5C19 10.6716 18.3284 10 17.5 10H13.125L13.407 7.74421C13.4688 7.24999 13.4688 6.75001 13.407 6.25579Z" fill="currentColor"></path>
                              </svg>
                            </div>
                            <span class="match-score">98% Match</span>
                          </div>
                        </span>
                      </div>
                      <div class="videoMetadata--second-line">
                        <div class="year">{{ selectedFilm.year }}</div>
                        <span class="duration">3 Seasons</span>
                        <span class="player-feature-badge">HD</span>
                        <div class="ltr-bjn8wh">
                          <div class="ltr-x1hvkl">
                            <div aria-labelledby="episodesAudioDescriptionAvailable" data-tooltip="Audio description is available for some episodes">
                              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="ltr-11ezyu1 e1mhci4z1" data-name="AudioDescription" aria-hidden="true">
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M21.9782 7.52002H22.2621C23.37 8.81831 24.0001 10.4801 24.0001 12.2077C24.0001 13.7414 23.505 15.2301 22.6221 16.4453H22.3348H21.8501H21.5662C22.5598 15.2613 23.1207 13.7691 23.1207 12.2077C23.1207 10.449 22.404 8.75599 21.1611 7.52002H21.445H21.9782ZM6.91381 16.4796H8.87336V7.52661H6.42566L0 16.4796H2.87701L3.63174 15.2956H6.91381V16.4796ZM4.8625 13.4299H6.92592V10.224L4.8625 13.4299ZM12.3019 9.62283C13.621 9.62283 14.6839 10.6926 14.6839 12.0048C14.6839 13.3203 13.621 14.3901 12.3019 14.3901H11.6787V9.62283H12.3019ZM12.5443 16.4743C15.0128 16.4743 17.0208 14.4698 17.0208 12.0048C17.0208 9.52935 15.0335 7.52826 12.565 7.52826H12.5373H9.79883V16.4778H12.5443V16.4743ZM20.0103 7.52002H19.7264H19.1932H18.9093C20.1522 8.75599 20.8689 10.449 20.8689 12.2077C20.8689 13.7691 20.308 15.2613 19.3144 16.4453H19.5983H20.083H20.3634C21.2531 15.2301 21.7482 13.7414 21.7482 12.2077C21.7482 10.4801 21.1181 8.81831 20.0103 7.52002ZM17.4745 7.52002H17.7584C18.8663 8.81831 19.4895 10.4801 19.4895 12.2077C19.4895 13.7414 19.0013 15.2301 18.1116 16.4453H17.8277H17.3464H17.0625C18.0492 15.2613 18.6101 13.7691 18.6101 12.2077C18.6101 10.449 17.9004 8.75599 16.6575 7.52002H16.9344H17.4745Z" fill="currentColor"></path>
                              </svg>
                            </div>
                            <div aria-labelledby="episodesTextClosedCaptionsAvailable" data-tooltip="Subtitles for the deaf and hard of hearing are available for some episodes">
                              <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg" class="ltr-0 e1mhci4z1" data-name="Subtitles" aria-hidden="true">
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M0 1.75C0 1.33579 0.335786 1 0.75 1H15.25C15.6642 1 16 1.33579 16 1.75V12.25C16 12.6642 15.6642 13 15.25 13H12.75V15C12.75 15.2652 12.61 15.5106 12.3817 15.6456C12.1535 15.7806 11.8709 15.785 11.6386 15.6572L6.80736 13H0.75C0.335786 13 0 12.6642 0 12.25V1.75ZM1.5 2.5V11.5H7H7.19264L7.36144 11.5928L11.25 13.7315V12.25V11.5H12H14.5V2.5H1.5ZM6 6.5L3 6.5V5L6 5V6.5ZM13 7.5H10V9H13V7.5ZM3 9V7.5L9 7.5V9L3 9ZM13 5H7V6.5H13V5Z" fill="currentColor"></path>
                              </svg>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="ltr-7t0zr9">
                    <a href="#about">
                      <span class="maturity-rating ">
                        <span class="maturity-number">18+</span>
                      </span>
                    </a>
                    <span class="ltr-1q4vxyr">violence, sex, nudity, language, substances, sexual violence</span>
                  </div>
                </div>
              </div>
              <div class="ltr-s5xdrg"></div>
              <p class="preview-modal-synopsis previewModal--text" data-uia="preview-modal-synopsis">
                <div class="ptrack-content" data-ui-tracking-context="%7B%22evidenceKey%22:%22web_synopsis%7C80025172_INFORMATIVE%7Cen%7C_IFD_%22,%22video_id%22:80025172,%22track_id%22:251769321,%22request_id%22:%220e0bfae2-e497-4fb6-a58f-a3a8d338156c-215920782%22,%22list_id%22:%22%22,%22row%22:0,%22rank%22:0,%22appView%22:%22synopsisEvidence%22,%22usePresentedEvent%22:true%7D" data-tracking-uuid="efb780c0-9d3a-4d45-8a28-a2ac64de29f2">{{ selectedFilm.description }}</div>
              </p>
            </div>
            <div class="previewModal--detailsMetadata-right">
              <div class="previewModal--tags" data-uia="previewModal--tags-person">
                <span class="previewModal--tags-label">Cast</span>
                
              </div>
              <div class="previewModal--tags" data-uia="previewModal--tags-genre">
                <span class="previewModal--tags-label">Genres:</span>
                <span class="tag-item" data-uia="tag-item">
                  <a historystate="[object Object]"> TV DRAMAS,</a>
                </span>
              </div>
            </div>
            <button class="close-button" @click="closeMoreInfo">Close</button>
          </div>
          
        </div>
        
      </div>
      
      </div>
  
      
      
      
      
        <div
          class="dowwsa"
        >
          <div class="featured">
            <h5 class="text-[30px] left-10 text-white font-semibold Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
              NETFLIX ORIGINALS
            </h5>
            
          </div>
          
          
          
          
          
  
          <div class="carousel">
      <div class="carousel-inner" :style="{ transform: `translateX(-${currentIndex1 * 100}%)` }">
        <div class="carousel-item" v-for="(film, index) in films" :key="film.id">
          <div class="front">
            <button class="carousel-slide">
            <img class="resim" :src="film.url" alt="Film Poster" />
            <video ref="videoPlayers" :data-index="index" class="w-[100%] h-[100%]"  :muted="playingIndex !== index"  loop v-on:mouseover="startVideo1(index)" v-on:mouseleave="stopVideo1(index)">
          <source :src="film.videoUrl" type="video/mp4" />
        </video>
            
            
          </button>
          
          </div>
          <div class="back">
            
            <div class="info">
              
              <p class="mname">{{ film.title }}</p>
              <div class="info1">
                <div class="match">99% Match</div>
                <div class="tv">TV-14</div>
                <div class="min">2h 40min</div>
             
              </div>
              <div class="tags">
                <span>Comedy</span>
                <span>Action</span>
              </div>
              <button class="play-button1" @click="selectFilm(film)">
                          <svg width="24" height="24" viewBox="0 0 24 24" fill="gray" xmlns="http://www.w3.org/2000/svg">
                            <path d="M4 2.69127C4 1.93067 4.81547 1.44851 5.48192 1.81506L22.4069 11.1238C23.0977 11.5037 23.0977 12.4963 22.4069 12.8762L5.48192 22.1849C4.81546 22.5515 4 22.0693 4 21.3087V2.69127Z" fill="currentColor"></path>
                              </svg>Play</button>
            </div>
            
          </div>
          <div class="background"></div>
        </div>
      </div>
      <div class="carousel-controls">
        <div
          class="carousel-control"
          v-for="(film, index) in films"
          :key="film.id"
          :class="{ active: index === currentIndex1 }"
          @click="setCurrentIndex(index)"
        ></div>
      </div>
      <div class="carousel-nav">
        <button class="nav-button btnleft" @click="prevSlide" :disabled="currentIndex1 === 0">
          <div class="handle left-handle">&#8249;</div>
        </button>
        <button class="nav-button btnright" @click="nextSlide">
          <div class="handle right-handle">&#8250;</div>
        </button>
      </div>
    </div>
          
          
          <div class="featured1">
            <h5 class="text-[30px] text-white font-semibold font-Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
              HORROR MOVIES
            </h5>
            
            
             
          </div>
          
  
          <div class="carousel">
      <div class="carousel-inner" :style="{ transform: `translateX(-${currentIndex2 * 100}%)` }">
        <div class="carousel-item" v-for="(film, index) in films1" :key="film.id">
          <div class="front">
            <button class="carousel-slide">
            <img class="resim" :src="film.url" alt="Film Poster" />
            <video ref="videoPlayers1" :data-index="index" class="w-[100%] h-[100%]"  :muted="playingIndex !== index"  loop v-on:mouseover="startVideo2(index)" v-on:mouseleave="stopVideo2(index)">
          <source :src="film.videoUrl" type="video/mp4" />
        </video>
            
            
          </button>
          
          </div>
          <div class="back">
            
            <div class="info">
              
              <p class="mname">{{ film.title }}</p>
              <div class="info1">
                <div class="match">99% Match</div>
                <div class="tv">TV-14</div>
                <div class="min">2h 40min</div>
             
              </div>
              <div class="tags">
                <span>Comedy</span>
                <span>Action</span>
              </div>
              <button class="play-button1" @click="selectFilm(film)">
                          <svg width="24" height="24" viewBox="0 0 24 24" fill="gray" xmlns="http://www.w3.org/2000/svg">
                            <path d="M4 2.69127C4 1.93067 4.81547 1.44851 5.48192 1.81506L22.4069 11.1238C23.0977 11.5037 23.0977 12.4963 22.4069 12.8762L5.48192 22.1849C4.81546 22.5515 4 22.0693 4 21.3087V2.69127Z" fill="currentColor"></path>
                              </svg>Play</button>
            </div>
            
          </div>
          <div class="background"></div>
          
        </div>
      </div>
      <div class="carousel-controls">
        <div
          class="carousel-control"
          v-for="(film, index) in films1"
          :key="film.id"
          :class="{ active: index === currentIndex2 }"
          @click="setCurrentIndexx(index)"
        ></div>
      </div>
      <div class="carousel-nav">
        <button class="nav-button btnleft" @click="prevSlide1" :disabled="currentIndex2 === 0">
          <div class="handle left-handle">&#8249;</div>
        </button>
        <button class="nav-button btnright" @click="nextSlide1">
          <div class="handle right-handle">&#8250;</div>
        </button>
      </div>
    </div>
          
          
          <div class="featured">
            <h5 class="text-[30px] left-10 text-white font-semibold Netflix Sans,Helvetica Neue,Segoe UI,Roboto,Ubuntu,sans-serif">
              NEW RELEASES
            </h5>
            
            
          </div>
          
          
          
  
          <div class="carousel">
      <div class="carousel-inner" :style="{ transform: `translateX(-${currentIndex3 * 100}%)` }">
        <div class="carousel-item" v-for="(film, index) in films2" :key="film.id">
          <div class="front">
            <button class="carousel-slide">
            <img class="resim" :src="film.url" alt="Film Poster" />
            <video ref="videoPlayers2" :data-index="index" class="w-[100%] h-[100%]"  :muted="playingIndex !== index"  loop v-on:mouseover="startVideo3(index)" v-on:mouseleave="stopVideo3(index)">
          <source :src="film.videoUrl" type="video/mp4" />
        </video>
            
            
          </button>
          
          </div>
          <div class="back">
            
            <div class="info">
              
              <p class="mname">{{ film.title }}</p>
              <div class="info1">
                <div class="match">99% Match</div>
                <div class="tv">TV-14</div>
                <div class="min">2h 40min</div>
             
              </div>
              <div class="tags">
                <span>Comedy</span>
                <span>Action</span>
              </div>
              <button class="play-button1" @click="selectFilm(film)">
                          <svg width="24" height="24" viewBox="0 0 24 24" fill="gray" xmlns="http://www.w3.org/2000/svg">
                            <path d="M4 2.69127C4 1.93067 4.81547 1.44851 5.48192 1.81506L22.4069 11.1238C23.0977 11.5037 23.0977 12.4963 22.4069 12.8762L5.48192 22.1849C4.81546 22.5515 4 22.0693 4 21.3087V2.69127Z" fill="currentColor"></path>
                              </svg>Play</button>
            </div>
            
          </div>
          <div class="background"></div>
        </div>
      </div>
      <div class="carousel-controls">
        <div
          class="carousel-control"
          v-for="(film, index) in films2"
          :key="film.id"
          :class="{ active: index === currentIndex3 }"
          @click="setCurrentIndexxx(index)"
        ></div>
      </div>
      <div class="carousel-nav">
        <button class="nav-button btnleft" @click="prevSlide2" :disabled="currentIndex3 === 0">
          <div class="handle left-handle">&#8249;</div>
        </button>
        <button class="nav-button btnright" @click="nextSlide2">
          <div class="handle right-handle">&#8250;</div>
        </button>
      </div>
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
    {
      title: "One Piece",
      genre: "Anime",
      description:
        "One Piece, Toei Animation tarafindan üretilen ve Ekim 1999'da Fuji TV'de prömiyeri yapilan bir Japon anime televizyon dizisidir.",
      videoUrl: "onepiece.mp4",
      url: "onepiece.jpg",
      urlmain : "onepiece1.jpg",
      year: "1999",
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
      title: "One Piece",
      genre: "Anime",
      description:
        "One Piece, Toei Animation tarafindan üretilen ve Ekim 1999'da Fuji TV'de prömiyeri yapilan bir Japon anime televizyon dizisidir.",
      videoUrl: "onepiece.mp4",
      url: "onepiece.jpg",
      urlmain : "onepiece1.jpg",
      year: "1999",
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
    {
      title: "One Piece",
      genre: "Anime",
      description:
        "One Piece, Toei Animation tarafindan üretilen ve Ekim 1999'da Fuji TV'de prömiyeri yapilan bir Japon anime televizyon dizisidir.",
      videoUrl: "onepiece.mp4",
      url: "onepiece.jpg",
      urlmain : "onepiece1.jpg",
      year: "1999",
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
  const currentIndex1 = ref(0);
  const currentIndex2 = ref(0);
  const currentIndex3 = ref(0);
  const videoPlaying = ref([]); // Videonun oynayıp oynamadığını takip eden ref
  const videoPlaying1 = ref([]); // Videonun oynayıp oynamadığını takip eden ref
  const videoPlayer1 = ref(null);

const isHovering = ref(false);
const videoPlayers = ref([]);
const videoPlayers1 = ref([]);
const videoPlayers2 = ref([]);
const playingIndex = ref(null);
const filmsPer = ref(null);
const isMuted = ref(false);

const tikla = () => {
  if (videoPlayer.value) {
        isMuted.value = !isMuted.value;
        videoPlayer.value.muted = isMuted.value;
      }

}






  

 





  
  const playVideo = () => {
  if (videoPlayer.value && (isHovering.value || isPlaying.value)) {
    videoPlayer.value.play();
    isPlaying.value = true;
    
    audio.style.opacity = 1;



    
    



    
    

  }
 
};

const pauseVideo = () => {
  if (videoPlayer.value) {
    videoPlayer.value.pause();
    isPlaying.value = false;
    audio.style.opacity = 0;
    



    

   


  }
};
const startVideo1 = (index) => {
  const video = videoPlayers.value[index];
  if (video) {
    video.play();
    if (playingIndex.value !== null && playingIndex.value !== index) {
      videoPlayers.value[playingIndex.value].pause();
    }
    playingIndex.value = index;
  }

};

const stopVideo1 = (index) => {
  const video = videoPlayers.value[index];
  if (video) {
    video.pause();
  }
};
const startVideo2 = (index) => {
  const video = videoPlayers1.value[index];
  if (video) {
    video.play();
    if (playingIndex.value !== null && playingIndex.value !== index) {
      videoPlayers1.value[playingIndex.value].pause();
    }
    playingIndex.value = index;
  }

};

const stopVideo2 = (index) => {
  const video = videoPlayers1.value[index];
  if (video) {
    video.pause();
  }
};
const startVideo3 = (index) => {
  const video = videoPlayers2.value[index];
  if (video) {
    video.play();
    if (playingIndex.value !== null && playingIndex.value !== index) {
      videoPlayers2.value[playingIndex.value].pause();
    }
    playingIndex.value = index;
  }

};

const stopVideo3 = (index) => {
  const video = videoPlayers2.value[index];
  if (video) {
    video.pause();
  }
};




  const setCurrentIndex = (index) => {
    currentIndex1.value = index;
  };
  const setCurrentIndexx = (index) => {
    currentIndex2.value = index;
  };
  const setCurrentIndexxx = (index) => {
    currentIndex3.value = index;
  };
  
  const prevSlide = () => {
    if (currentIndex1.value > 0) {
      currentIndex1.value--;
    }
  };
  
  const nextSlide = () => {
    if (currentIndex1.value < 2) {
      currentIndex1.value++;
      
    }
    else{
      currentIndex1.value = 0;
      
    }
  };
  const prevSlide1 = () => {
    if (currentIndex2.value > 0) {
      currentIndex2.value--;
    }
  };
  
  const nextSlide1 = () => {
    if (currentIndex2.value < 2) {
      currentIndex2.value++;
    }
    else{
      currentIndex2.value = 0;
    }
  };
  const prevSlide2 = () => {
    if (currentIndex3.value > 0) {
      currentIndex3.value--;
    }
  };
  
  const nextSlide2 = () => {
    if (currentIndex3.value < 2) {
      currentIndex3.value++;
    }
    else{
      currentIndex3.value = 0;
    }
  };
  
  
  
  const showMoreInfo = () => {
    showMoreInfoModal.value = true;
  };
  
  const closeMoreInfo = () => {
    showMoreInfoModal.value = false;
  };
  const togglePlay = () => {
    const videoElement = videoPlayer.value;

if (videoElement.requestFullscreen) {
  videoElement.requestFullscreen();
} else if (videoElement.mozRequestFullScreen) {
  videoElement.mozRequestFullScreen();
} else if (videoElement.webkitRequestFullscreen) {
  videoElement.webkitRequestFullscreen();
} else if (videoElement.msRequestFullscreen) {
  videoElement.msRequestFullscreen();
}
};
const handleMouseEnter = () => {
  isHovering.value = true;
  playVideo();
};

const handleMouseLeave = () => {
  isHovering.value = false;
  pauseVideo();
};


  
  
  
  
  const selectFilm = (film) => {
    selectedFilm.value = film;
    videoPlayer.value.load();
    videoPlayer.value.play();
    console.log(selectedFilm.value, "film");
  };
  
  
  
  onMounted(() => {
    selectedFilm.value = films.value[7];
    videoPlayers.value = Array.from({ length: films.length }, () => null);
  videoPlayers.value.forEach((video) => {
    if (video) {
      video.pause();
    }
  });
    setTimeout(() => {
      const fTitle = document.querySelector('.ftitle');
      fTitle.style.transform = 'scale(0.8) translate3d(100px, 400px, 500px)';
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
  @import url('https://fonts.googleapis.com/css2? family= Montserrat & family= Poppins:wght@100;300;400;500;600 & family= Roboto+Flex:opsz@8. .144 & görüntü=takas');
  
  *{
      margin: 0;
      padding: 0;
      background-color: none;
      
  }
  
  .topbar{
      background-color: none;
      width: 100vw;
      height: 70px;
      display: flex;
      align-items: center;
      position: fixed;
      top: 0;
      z-index: 2;
      transition: 0.7s all ease-in-out;
      
  }
  .topbar:hover{
    background-color: black;
  }
  .web-logo{
      width: 127px;
      height: 97px;
      background-color: none;
      
  }
  .logoImg{
    object-fit: contain;
      width: 25%;
      background-color: none;
      margin-left: 40px;
      margin-top: 10px;
  }
  .navList{
      margin-top: 20px;
      display: flex;
      color: #e5e5e5;
      font-family: 'Montserrat', sans-serif;
      gap:40px;
      margin-left: -440px;
      background-color: none;
      font-size: 17px;
  
  }
  .navItem:hover{
    color: #7b7a7a;
  }
  .profile{
      margin-left: 770px;
      color: #e5e5e5;
      display: flex;
      align-items: center;
      font-weight: bold;
      gap: 30px;
      font-size: 17px;
      font-family: 'Montserrat', sans-serif;
      background-color: none;
  }
  .navItem{
    font-family: 'Montserrat', sans-serif;
      font-weight: bold;
      background-color: none;
      cursor: pointer;
  }
  .userImg{
      height: 40px;
      width: 40px;
      border-radius: 50%;
      object-fit: cover;
      background-color: none;
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
    position: fixed;
      width: 100%;
      height: 100%;
      
      background: linear-gradient(to bottom, #201f1f 0%, #141414 42%);
      overflow-y: auto;




      transition: 0.7s all ease-in-out;
  
  }
  .resim {
    width: 400px;
    height: 200px;
    background-color: none;
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
    font-size: 5rem;
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
    margin-bottom: 30px;
    
  
      
  
    
  }
  .right-handle {
    border-top-right-radius: 0;
    border-bottom-right-radius: 0;
    margin-left: 1690px;
    height: 2px;
    margin-bottom: 30px;
    
  }
  
  .handle:hover,
  .handle:focus {
    background-color: rgba(50, 48, 48, 0.5);
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
    width: 100%;
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
    align-items: center;
    padding: 10px;
    background: none;
    
  }
  
  .info-button{
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.8rem;
    cursor: pointer;
    max-height: 42px;
    min-height: 32px;
    font-size: 1.6rem;
    color: white;
    font-weight: 500;

  }
  .play-button {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.8rem;
    cursor: pointer;
    max-height: 42px;
    min-height: 32px;
    font-size: 1.6rem;
    color: black;
    padding-left: 30px;
    font-weight: 500;
    
  }
  
  .modal {
    position: absolute;
    top: 0;
    left: -100px;
    width: 2000px;
    
    margin: 0px 20px;
    border-radius: 46px;
    z-index: 2;
    background-color: var(--modal);
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.25);
    display: flex;
    align-items: center;
    justify-content: center;
    transition: opacity 0.2s linear;
    overflow: hidden;
    
  }
  
  .modal-content {
    background-color: transparent;
    padding: 20px;
    border-radius: 5px;
    height: 850px;
    border-radius: 16px;
    
    width: 900px;
    
    color: white;
    font-family: 'Montserrat', sans-serif;
    font-size: large;
    z-index: 10;
    margin-top: 50px;
    overflow: hidden;
  }
  
  .video-section {
    position: relative;
    padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
    height: 500px;
    overflow: visible;
    margin-bottom: -70px;
  }
  
  
  .movieDetails{
    color: white;
    font-family: 'Montserrat', sans-serif;
    font-size: larger;
    z-index: 2;
    
    
  }
  .close-button {
    font-family: 'Montserrat', sans-serif;
    color: white;
    font-size: x-large;
    font-weight: bolder;
    margin-left: 700px;
    
    
  }
  .video-thumbnail-container {
    position: relative;
    width: 100%;
    min-height: 1080px;
    border-radius: 10px;
  }
  
  .video-thumbnail {
    width: 100%;
    height: 1000px;
    border-radius: 10px;
    
  }
  .video-thumbnail-container1 {
    position: relative;
    width: 100%;
    height: 480px;
  }
  
  .video-thumbnail1 {
    width: 100%;
    height: 480px;
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
  .pbutton:hover{
    background: rgba(255, 255, 255, 0.482); /* Butonun üzerine gelindiğinde hafif bir background efekti */

  }
  .ibutton:hover {
      
     
    background: rgba(255, 255, 255, 0.266); /* Butonun üzerine gelindiğinde hafif bir background efekti */
      border: none; /* Kenarlık yerine border kullanmama kararı aldık */
      
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
    font-family: 'Montserrat', sans-serif;
    background: none;
    font-weight: bolder;
    
    
  }
  .fdesc{
    color: white;
    font-size: 20px;
    font-family: 'Montserrat', sans-serif;
    background: none;
    font-weight: bolder;
    
  
  
  }
  .t1{
    color: white;
    font-size: 30px;
    font-family: 'Montserrat', sans-serif;
    font-weight: bolder;
  }
  .t2{
    color: white;
    font-size: 18px;
    font-family: 'Montserrat', sans-serif;
    font-weight: bolder;
  }
  .t3{
    color: white;
    font-size: 18px;
    font-family: 'Montserrat', sans-serif;
    font-weight: bolder;
  }
  .member-footer {
      color: grey;
      margin: 20px auto 0;
      max-width: 1280px;
      padding: 0 4%;
      margin-bottom: -200px;
      
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
      font-size: 16px;
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
      font-size: 16px;
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
      font-family: 'Montserrat', sans-serif;
  
  }
  button, html input[type=button], input[type=reset], input[type=submit] {
      
      cursor: pointer;
  }
  .member-footer .member-footer-copyright {
      font-size: 16px;
      margin-bottom: 15px;
      font-family: 'Montserrat', sans-serif;
  
  }
  .previewModal--detailsMetadata.detail-modal {
      -moz-column-gap: 2em;
      column-gap: 2em;
      grid-template-columns: minmax(0,2fr) minmax(0,1fr);
  }
  .previewModal--wrapper *, .previewModal--wrapper :after, .previewModal--wrapper :before {
      box-sizing: inherit;
  }
  .previewModal--detailsMetadata {
      background-color: #181818;
      display: grid;
      position: relative;
      width: 100%;
      padding-left: 40px;
  }
  .previewModal--detailsMetadata .previewModal--detailsMetadata-left .previewModal--detailsMetadata-info {
      margin: 0.8em 0;
  }
  .videoMetadata--container {
      align-items: center;
      color: #fff;
      display: flex;
      flex-wrap: wrap;
      justify-content: flex-start;
  }
  .videoMetadata--container .videoMetadata--first-line {
      margin: 0.25em 0.5em 0.25em 0;
      max-width: 100%;
      font-weight: bolder;
  }
  .match-score {
    color: green;
    font-weight: bolder;
  }
  .match-score-wrapper .rating-inner {
      display: flex;
      transition: margin-right .55s cubic-bezier(.86,0,.07,1) 1.65s;
  }
  .videoMetadata--container .videoMetadata--second-line {
      align-items: center;
      color: #bcbcbc;
      display: flex;
      flex-wrap: wrap;
      font-weight: bolder;
    
  }
  .videoMetadata--container .videoMetadata--second-line>* {
      margin-right: 0.5em;
  }
  .videoMetadata--container .videoMetadata--second-line .duration {
      white-space: nowrap;
  }
  .videoMetadata--container .videoMetadata--second-line>.player-feature-badge {
      margin-right: 0.715em;
  }
  .ltr-x1hvkl {
      display: flex;
      gap: 0.75em;
  }
  .ltr-x1hvkl > div {
      display: flex;
      -webkit-box-align: center;
      align-items: center;
      -webkit-box-pack: center;
      justify-content: center;
  }
  .ltr-7t0zr9 {
      margin-top: 0.1rem;
      margin-bottom: 8px;
      font-size: 14px;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
      line-height: 1.5;
  }
  a {
      color: #fff;
      cursor: pointer;
      text-decoration: none;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
  
  }
  a {
      background-color: transparent;
  }
  .maturity-rating {
      display: inline-block;
  }
  .maturity-rating .maturity-number {
      border: 1px solid hsla(0,0%,100%,.4);
      font-family: 'Montserrat', sans-serif;
      overflow: hidden;
      padding: 0 0.4em;
      text-overflow: ellipsis;
      text-transform: uppercase;
      unicode-bidi: normal /*!rtl:plaintext*/;
      white-space: nowrap;
  }
  .ltr-1q4vxyr {
      margin-left: 8px;
  }
  .ltr-7t0zr9 {
      margin-top: 0.1rem;
      margin-bottom: 8px;
      font-size: 14px;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
      line-height: 1.5;
      font-weight: bolder;
      font-family: 'Montserrat', sans-serif;

  }
  .previewModal--detailsMetadata .previewModal--detailsMetadata-left>:not(.new-badge) {
      margin-bottom: 0.5em;
  }
  
  .previewModal--detailsMetadata .previewModal--detailsMetadata-left .preview-modal-synopsis {
      font-size: 14px;
      line-height: 24px;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
  
  }
  .previewModal--detailsMetadata.detail-modal .previewModal--detailsMetadata-right {
      display: flex;
      flex-direction: column;
  }
  .previewModal--tags {
      font-size: 14px;
      line-height: 20px;
      margin: 0.5em 0.5em 0.5em 0;
      word-break: break-word;
      font-family: 'Montserrat', sans-serif;
      font-weight: bolder;
  
      
  }
  .previewModal--tags .tag-item, .previewModal--tags .tag-more {
      color: #ddd;
      cursor: pointer;
      margin: 0;
      outline-color: #fff;
  }
  a {
      color: #fff;
      cursor: pointer;
      text-decoration: none;
      font-family: 'Montserrat', sans-serif;
  
  }
  .carousel {
    display: flex;
    overflow: hidden;
    width: 100%;
    right: -100px;
    margin: -100px;
    position: relative;
    bottom: 100px;
    padding-left: 10px;
  }
  .carousel:hover .carousel-nav{
    opacity: 1;
  }
  
  .carousel-inner {
    display: flex;
    transition: transform 0.5s ease-in-out;
    height: 350px;
  }
  
  
  .carousel-item {
    flex: 0 0 auto; /* Flex büyüklüğünü ayarlayın */
  margin-right: 10px;
  position: relative;
  overflow: hidden;
  border-radius: 5px;
  
  }
  .carousel-item:hover {
  transform: scale(1.5); /* Resmi büyüt */
  opacity: 1.8; /* Saydamlığı azalt */
  box-shadow: 0 25px 40px  rgba(0,0,0,0.5);
  z-index: 10;
  border-radius: 10px;
}
  
  .carousel-item img {
    width: 200px;
    height: 200px;
    
    
    
    vertical-align: top;
    border-radius: 10px;
  }
  .carousel:hover .carousel-controls{
    opacity: 1;
  }
  
  .carousel-controls {
    position: absolute;
    bottom: 270px;
    left: 100%;
    opacity: 0;
    
    
    
  
    transform: translateX(-20%);
    display: flex;
  }
  
  .carousel-control {
    width: 16px;
    height: 2px;
    border-radius: 10%;
    background-color: rgba(255, 255, 255, 0.5);
    margin: 0 2px;
    cursor: pointer;
  }
  .carousel-control.active{
    background-color: white;
  }
  
  .carousel-nav {
    position: absolute;
    bottom: 10px;
    left: 0;
    right: 0;
    display: flex;
    justify-content: space-between; /* Spread buttons to both sides */
    padding: 0 10px;
    align-items: center;
    bottom: 170px;
    opacity: 0;
  }
  
  .nav-button {
    font-size: 24px;
    padding: 5px 10px;
    border: none;
    background-color: none;
    color: #333;
    cursor: pointer;
    transition: background-color 0.3s ease;
    
  }
  
  
  
  .carousel-slide {
    display: inline-block; /* Eski stil display:block; idi, inline-block kullanmayı deneyin */
  transition: transform 250ms ease-in-out;
  border-radius: 10px;
  position: relative; /* Position ekleyin */
  width: 100%; /* Genişliği yüzde olarak belirtin */

  }
  
  .carousel-slide img{
    width: 300px;
    height: 170px;
    border-radius: 10px;
    background: none;
    
    
  }
  
  
  .back{
    opacity: 0;
    position: absolute;
    bottom: 40px;
    left: 0;
    right: 0;
  }
  .back .mname{
    display: block;
          width: 100%;
          font-size: .3vw;
          font-weight: 1900;
          margin-bottom: .1vw;
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    color: white;
    

  }
  .front{
    display: flex;
    width: 100%;
    height: 100%;
    border-radius: 10px;

  }
  .background {
    
    background: hsla(0, 2%, 10%, 0.922);
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: -1;
    
    
    transform: scale(0.01);
    transition: 150ms;
    border: solid;
    border-radius: 10px;
    
  }
  .carousel-item:hover .background {
    transition: 750ms;
  transform: scale(4);
  opacity: 1;
  border: solid 20px;
  border-radius: 35px;
  border-color: none;
  background-color: none;
}
.carousel-item:hover .front{
  transform: translateY(-13%);
}
.carousel-item:hover .back{
  opacity: 1;
}
.front:hover img{
  opacity: 0;
}
.front:hover video{
  opacity: 1;
}
.front .video{
  border-radius: 10px;
}
.play-button1 {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0.8rem;
    cursor: pointer;
    max-height: 32px;
    min-height: 22px;
    font-size: 0.8rem;
    color: white;
    margin-bottom: 33px;
    
    
  }
  .info1{
    display: flex;
          width: 200px;
          margin-bottom: 10px;
          color: white;
          height: 10px;
          background: none;
          font-family: 'Montserrat', sans-serif;
          padding-right: 1px;
          margin: 20px;
          

  }
 .match{
    display: inline-block;
            width: auto;
            font-size: 10px;
            font-weight: 600;
            margin-right: .4vw;
            color: green;
           
  }
  .tv{
    display: inline-block;
            position: relative;
            width: auto;
            font-size: 10px;
            padding: 0 0.4em;
            margin-right: .4vw;
            border: solid;
            color: white;
            height: 20px;
            
  }
  .min{
    display: inline-block;
            width: auto;
            font-size: 10px;
            color: white;
            height: 10px;
  }
  .info .tags{
    display: block;
          width: 100%;
          color: white;
          font-size: 10px;
  }
  .info .tags .span{
    display: inline-block;
            width: auto;
            font-size: 10px;
            margin: 0 .3vw 0 0;
            color: white;
  }
  .featured{
    margin-bottom: 110px;
  }
  .featured1{
    margin-bottom: 110px;
  }
  .dropbtn {
  background-color: none;
  color: white;
  padding: 16px;
  font-size: 18px;
  border: none;
  cursor: pointer;
  font-family: 'Montserrat', sans-serif;
  margin-left: -20px;

}
.dropbtn:hover{
  rotate: 180deg;
  transition: 1s;

}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: black;
  min-width: 300px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
  opacity: 0.9;
  
}

.dropdown-content a {
  color: white;
  padding: 12px 16px;
  text-decoration: none;
  display: flex;
  font-family: 'Montserrat', sans-serif;
  font-size: 13px;
  gap: 10px;
  line-height: 16px;
}
.dropdown-content a:hover{
  text-decoration: underline;
}



.dropdown:hover .dropdown-content {
  display: block;
}

.dropdown:hover .dropbtn {
  background-color: none;
}
.dowwsa{
  padding-left: 70px;
  position: relative;
  top: -250px;
}
.pbutton{
  border: white;
  background-color: white;
  display: flex;
  align-items: center;
  border-radius: 5px;
  padding: 5px;
  width: 150px;
  
}
.ibutton{
  
  border: white;
  background-color: rgb(93, 90, 90);
  display: flex;
  align-items: center;
  border-radius: 5px;
  padding: 5px;
  width: 180px;
  
  
}
.searchTab {
    background: transparent;
    border: none;
    cursor: pointer;
    display: inline-block;
}
.searchBox {
    
    vertical-align: middle;
}
.embedded-components{
  align-items: center;
    bottom: 30%;
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    position: absolute;
    right: 0;
    left: 1850px;
    gap: 30px;
}
.ActionButtons{
  align-items: flex-end;
    display: flex;
    flex-direction: column;
    font-size: 1.35rem;
}
.ltr-11vo9g5.round.color-supplementary {
    background-color: transparent;
    border: 1px solid rgba(255, 255, 255, 0.7);
    color: white;
}
.ltr-11vo9g5.hasIcon {
    padding-left: 0.8rem;
    padding-right: 0.8rem;
}
.ltr-11vo9g5 {
    -webkit-box-align: center;
    align-items: center;
    appearance: none;
    border: 0px;
    cursor: pointer;
    display: flex;
    -webkit-box-pack: center;
    justify-content: center;
    opacity: 1;
    padding: 0.8rem;
    position: relative;
    user-select: none;
    will-change: background-color, color;
    word-break: break-word;
    white-space: nowrap;
    border-radius: 50%;
    
}
.ltr-1st24vv {
    line-height: 0;
}
.ltr-iyulz3.small {
    height: 1.8rem;
    width: 1.8rem;
}
.ltr-iyulz3 {
    display: flex;
    -webkit-align-items: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
}
.ltr-iyulz3 svg {
    height: 100%;
    width: 100%;
}
.maturity-rating1{
  align-items: center;
    background-color: rgba(51,51,51,.6);
    border: 3px #dcdcdc;
    border-left-style: solid;
    box-sizing: border-box;
    display: flex;
    font-size: 1.1vw;
    height: 2.4vw;
    padding: 0.5vw 3.5vw 0.5vw 0.8vw;
}
.maturity-rating1 .maturity-number1 {
    border: 1px solid hsla(0,0%,100%,.4);
    font-family: sans-serif;
    overflow: hidden;
    padding: 0 0.4em;
    text-overflow: ellipsis;
    text-transform: uppercase;
    unicode-bidi: normal /*!rtl:plaintext*/;
    white-space: nowrap;
    color: white;
}


  </style>
  