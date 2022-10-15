

<script>
import tracks from "./Tracks.vue"; 
export default {
    data () {
        return{
          tracks,
          player: new Audio()
        }
    }, 


   
}
</script>

<template>

     <div class="main" id="player">

<div id = "main-container">
<!--  <video src="../pics/FREUNDE VOL1.mp4" autoplay muted loop></video> -->

<div>
     <div id="sliderContainer">
         <input type="range" min="0"  max="500" step="0.05" value="0" id="seekSlider" title="seekSlider">
     </div> 
      <div class="controls" id="controls"> 
        {{tracks.track_list}}
              <button  name ="play/pause" id="play" class="action-btn" type="button" aria-label="Play/Pause" @click="playSong"> 
                PLAY
              </button>

              <div id="soundWrapper">
                  <button name="mute" class="action-btn" id="soundBtn" type="button" aria-label="Mute/Unmute"> 
                    SOUND
                  </button>            
                  <input type="range" name="volume" class="volume" id ="volSlider" min="0" max="1" step="0.05" title="-">
              </div>

              <div id="image-container"> 
                 <!--<img src="../pics/BLONDED.jpg" alt="" width="60px"> -->
              </div>

              <div>
                 <div id="songName"></div>
                 <div>
                     <h6 id="artist"> </h6> 
                 </div>
              </div>

       </div>
</div>
</div>                    
      
</div> 
</template>

<style lang="scss">
$remsize-mar: 3rem; 
$remsize-pad: 1rem; 
$layer2color: linear-gradient(to bottom, rgba(6, 5, 8, 0.154), rgb(67, 66, 68, 1));
$layer1color: linear-gradient(to top, rgba(6, 5, 8, 0.902), rgba(6, 5, 8, 1));
$layer0color: #050506; 

   .main{
flex:1.75;
display: flex;
overflow: auto;
color: white;
background-image: $layer1color;
flex-direction: column;
overflow:hidden;
min-height: 100vh; 

#main-container{

flex: 1;
border: none;
color:white; 
// margin-top :2rem;
margin-left: 1rem;
margin-right: 1rem;
border-radius: 16px;
margin-bottom: $remsize-mar;
padding-top: $remsize-pad;
background-image: $layer2color;
transition: 1s; 
    display:flex;
    flex-direction: column;
    justify-content: flex-end;

    #sliderContainer{
        display: flex;
        align-items: flex-end;

        #seekSlider {
            flex: 1;
            appearance: none;
            height: 2.5px;
            width: 15rem; 
            border: none;
            z-index: 2;
            transition: all 0.25s ease;

            &::-webkit-slider-thumb {
                -webkit-appearance: none;
                appearance: none;
                border: 1px solid #000000;
                border-radius: 64px;
                height: 12px;
                width: 12px;
                background: #000000;
                z-index: 1;
                cursor: pointer;
                transition: all 0.5s ease;

                }
        }
    }

    

.controls {
    display:flex;
    align-items: center;
    border-bottom-left-radius: 16px;
    border-bottom-right-radius: 16px;
    background-image: $layer1color;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 2;
    opacity: 0.75;
    justify-content: space-evenly;
    color:white; 
    
    &:hover {
    opacity: 1;
    }

        #volSlider{
        appearance: none;
            height: 5px;
            width:0rem ; 
            border-radius: 3px;
            flex: 0.1;
            transition:  0.5s linear;
            z-index: 3;

        &::-webkit-slider-thumb {
        -webkit-appearance: none;
        appearance: none;
        border: 1px solid #000000;
        height: 16px;
        width: 16px;
        border-radius: 30px;
        background: $layer2color;
        cursor: pointer;
        }
        
    }

        .action-btn {
            cursor: pointer;
            border: none;
            border-radius: 2rem;
            margin: 0.1rem;
            padding: 0.75rem;
            background-color:inherit;
            opacity: 0.75;
    

            &:active {
                transform:scale(0.95,0.95);
            }
            &:hover{
                opacity: 1;
            }
        }

        #soundWrapper{
            display:inline-flex;
            align-items: center;
            justify-content: center;
            background-color: inherit;
            order:3;
        }

        #soundBtn{
            color:white; 
            &:hover {
                transform: translateX(2,2);
            }
        }

        #play {
            flex: none; 
            margin-left:2rem ;
            margin-right: 2rem;
            order: 2;
            color:white; 
        }

        i{
            font-size:medium;
            color: whitesmoke;
            transition: 0.5s;
        } 

        #songName{
            transition: all ease 1s;
        }

        h6 {
            display: block;
            font-size: 0.67em;
            margin: 0;
            font-weight: bold;
            color: #424243;
            color:white
        }
    }
}
   }
</style>