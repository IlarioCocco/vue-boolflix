<template>
  <footer>
      <section class="boxFooter">
            <div class="shop">
                <h3>
                    Goditi Netflix sulla tua TV.
                     <p class="guarda">
                        Guarda Netflix su smart TV, Playstation, Xbox, Chromecast, Apple TV, lettori Blu-ray e molti altri dispositivi.
                     </p>
                </h3>     
            </div>
            <div>
                <div class="our-story-card-img-container">
                    <div class="our-story-card-animation-container">
                        <img alt="" class="our-story-card-img" src="https://assets.nflxext.com/ffe/siteui/acquisition/ourStory/fuji/desktop/tv.png" data-uia="our-story-card-img">
                        <div class="our-story-card-animation">
                            <video class="our-story-card-video" autoplay="" playsinline="" muted="" loop=""><source src="https://assets.nflxext.com/ffe/siteui/acquisition/ourStory/fuji/desktop/video-tv-0819.m4v" type="video/mp4">
                            </video>
                            <div class="our-story-card-animation-text">
                            </div>
                        </div>
                    </div>
                </div>   
            </div>
      </section>
  </footer>
</template>

<script>
export default {
    name: 'Footer'

}
</script>


<style scoped lang="scss">

footer {
    background-color: black;
    border-top: 7px solid rgb(42, 42, 42);
    padding: 0px 0px 30px 0px;
    display: flex;
}


.boxFooter {
    width: 60%;
    margin: auto;
    display: flex;
    justify-content: center;
    align-content: center;
    background-color: black;
    padding: 0px 0px;
    color: rgb(255, 255, 255);
    font-size: 40px;
    // border: 5px solid rgb(47, 92, 224)
}

.our-story-card-img {
    width: 80%;
    z-index: 1;
    position: relative;
}

.our-story-card-img-container{
    position: relative;
    width: 100%;
    
}

.our-story-card-video {
    position: absolute;
    top: 73px;
    left: 61.2px;
    max-width: 58.2%;
    
}

.shop {
    display: flex;
    align-items: center ;
    padding: 0px  55px  0px  0px;
    width: 55%;
}

.guarda {
    font-size: 25px;
    padding-top: 25px;
    font-weight: 400;
}
</style>