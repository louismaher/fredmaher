---
layout: layouts/home
title: J'attends l'printemps
metaTitle: J'attends l'printemps - Fred Maher
metaDesc: Site de l'auteur-compositeur-interprète Fred Maher
postsHeading: Dernières nouvelles
archiveButtonText: Voir toutes les nouvelles
permalink: /
---
<head>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/amplitudejs@5.1.0/dist/amplitude.js"></script>

<style>
.video a{
color:#fff; 
font-size:12px;
background:#577F2E;
padding:4px;
margin-left:8px;
text-decoration:none
}
.album-art{
  background-image: url("https://fredmahermusique.com/images/fredmaher.jpg");
  height: 264px; /* You must set a specified height */
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
  background-size: cover; /* Resize the background image to cover the entire container */
}
/*
  1. Base
*/

/*
  2. Components
*/
h1 {
    font-style:italic;
    }
#blue-playlist-container{margin-top:80px}
div#amplitude-player {
  background:transparent;
  margin: auto;
  margin-top: 0px;
  margin-bottom: 0px;
  display: flex;
  max-width: 1200px; }

/* Small only */
@media screen and (max-width: 39.9375em) {
  div#amplitude-player {
    flex-direction: column; } }
/* Medium only */
@media screen and (min-width: 40em) and (max-width: 63.9375em) {
  div#amplitude-player {
    max-height: 715px; } }
/* Large and up */
@media screen and (min-width: 64em) {
  div#amplitude-player {
    max-height: 1200px; } }
div#amplitude-left {
  padding: 0px;
  border-right: 0px solid #CFD8DC;
  width: 50%;
  display: flex;
  flex-direction: column; }
  div#amplitude-left img.album-art {
    width: 100%; }
  div#amplitude-left div#player-left-bottom {
    flex: 1;
    background-color:transparent;
    padding: 20px 10px; }
    div#amplitude-left div#player-left-bottom div#volume-container:after {
      content: "";
      display: table;
      clear: both; }

/* Small only */
@media screen and (max-width: 39.9375em) {
  div#amplitude-player div#amplitude-left {
    width: 100%; }
    div#amplitude-player div#amplitude-left img[amplitude-song-info="cover_art_url"] {
      width: auto;
      height: auto; } }
div#amplitude-right {
  padding: 0;
  /*overflow-y: scroll;*/
  width: 50%;
  display: flex;
  flex-direction: column; }
  div#amplitude-right div.song {
    cursor: pointer;
    padding: 0 0 0 10px;
    }
    div#amplitude-right div.song div.song-now-playing-icon-container {
      float: left;
      width: 20px;
      height: 20px;
      margin-right: 20px; }
      div#amplitude-right div.song div.song-now-playing-icon-container img.now-playing {
        display: none;
        margin-top: 12px; }
    div#amplitude-right div.song div.play-button-container {
      display: none;
      background: url("https://521dimensions.com/img/open-source/amplitudejs/blue-player/list-play-light.png") no-repeat;
      width: 22px;
      height: 22px;
      margin-top: 11px; }
    div#amplitude-right div.song div.play-button-container:hover {
      background: url("https://521dimensions.com/img/open-source/amplitudejs/blue-player/list-play-hover.png") no-repeat; }
    div#amplitude-right div.song.amplitude-active-song-container div.song-now-playing-icon-container img.now-playing {
      display: block;}
    div#amplitude-right div.song.amplitude-active-song-container:hover div.play-button-container {
      display: none; }
    div#amplitude-right div.song div.song-meta-data {
      float: left;
      width: calc( 100% - 110px ); }
      div#amplitude-right div.song div.song-meta-data span.song-title {
        color: #6ea43b;
        font-size: 14px;
        display: block;
        font-weight: 700;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
        padding-top:10px;
        padding-left:0px }
      div#amplitude-right div.song div.song-meta-data span.song-artist {
        color: #fff;
        font-size: 14px;
        font-weight: 400;
        display: block;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis; }
    div#amplitude-right div.song img.bandcamp-grey {
      float: left;
      display: block;
      margin-top: 10px;
      display:none }
    div#amplitude-right div.song img.bandcamp-white {
      float: left;
      display: none;
      margin-top: 10px; }
    div#amplitude-right div.song span.song-duration {
      float: left;
      width: 55px;
      text-align: right;
      line-height: 45px;
      color: #6ea43b;
      font-size: 14px;
      font-weight: 500;
      padding-left:0px }
  div#amplitude-right div.song:after {
    content: "";
    display: table;
    clear: both; }

/* Small only */
@media screen and (max-width: 39.9375em) {
  div#amplitude-player div#amplitude-right {
    width: 100%; } }
div#progress-container {
  width: 70%;
  float: left;
  position: relative;
  height: 20px;
  cursor: pointer;
  /*
    IE 11
  */ }
  div#progress-container:hover input[type=range].amplitude-song-slider::-webkit-slider-thumb {
    display: block; }
  div#progress-container:hover input[type=range].amplitude-song-slider::-moz-range-thumb {
    visibility: visible; }
  div#progress-container progress#song-played-progress {
    width: 100%;
    position: absolute;
    left: 0;
    top: 8px;
    right: 0;
    width: 100%;
    z-index: 60;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    height: 4px;
    border-radius: 5px;
    background: transparent;
    border: none;
    /* Needed for Firefox */ }
  @media all and (-ms-high-contrast: none) {
    div#progress-container *::-ms-backdrop, div#progress-container progress#song-played-progress {
      color: #ffffff;
      border: none;
      background-color: #CFD8DC; } }
  @supports (-ms-ime-align: auto) {
    div#progress-container progress#song-played-progress {
      color: #ffffff;
      border: none; } }
  div#progress-container progress#song-played-progress[value]::-webkit-progress-bar {
    background: none;
    border-radius: 5px; }
  div#progress-container progress#song-played-progress[value]::-webkit-progress-value {
    background-color: #ffffff;
    border-radius: 5px; }
  div#progress-container progress#song-played-progress::-moz-progress-bar {
    background: none;
    border-radius: 5px;
    background-color: #ffffff;
    height: 5px;
    margin-top: -2px; }
  div#progress-container progress#song-buffered-progress {
    position: absolute;
    left: 0;
    top: 8px;
    right: 0;
    width: 100%;
    z-index: 10;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    height: 4px;
    border-radius: 5px;
    background: transparent;
    border: none;
    background-color: #D7DEE3; }
  div#progress-container progress#song-buffered-progress[value]::-webkit-progress-bar {
    background-color: #CFD8DC;
    border-radius: 5px; }
  div#progress-container progress#song-buffered-progress[value]::-webkit-progress-value {
    background-color: #78909C;
    border-radius: 5px;
    transition: width .1s ease; }
  div#progress-container progress#song-buffered-progress::-moz-progress-bar {
    background: none;
    border-radius: 5px;
    background-color: #78909C;
    height: 5px;
    margin-top: -2px; }
  div#progress-container progress::-ms-fill {
    border: none; }
@-moz-document url-prefix() {
  div#progress-container progress#song-buffered-progress {
    top: 9px;
    border: none; } }
  @media all and (-ms-high-contrast: none) {
    div#progress-container *::-ms-backdrop, div#progress-container progress#song-buffered-progress {
      color: #78909C;
      border: none; } }
  @supports (-ms-ime-align: auto) {
    div#progress-container progress#song-buffered-progress {
      color: #78909C;
      border: none; } }
  div#progress-container input[type=range] {
    -webkit-appearance: none;
    width: 100%;
    margin: 7.5px 0;
    position: absolute;
    z-index: 9999;
    top: -7px;
    height: 20px;
    cursor: pointer;
    background-color: inherit; }
  div#progress-container input[type=range]:focus {
    outline: none; }
  div#progress-container input[type=range]::-webkit-slider-runnable-track {
    width: 100%;
    height: 0px;
    cursor: pointer;
    box-shadow: 0px 0px 0px rgba(0, 0, 0, 0), 0px 0px 0px rgba(13, 13, 13, 0);
    background: #0075a9;
    border-radius: 0px;
    border: 0px solid #010101; }
  div#progress-container input[type=range]::-webkit-slider-thumb {
    box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
    border: 1px solid #ffffff;
    height: 15px;
    width: 15px;
    border-radius: 16px;
    background: #ffffff;
    cursor: pointer;
    -webkit-appearance: none;
    margin-top: -7.5px; }
  div#progress-container input[type=range]:focus::-webkit-slider-runnable-track {
    background: #00adfb; }
  div#progress-container input[type=range]::-moz-range-track {
    width: 100%;
    height: 0px;
    cursor: pointer;
    box-shadow: 0px 0px 0px rgba(0, 0, 0, 0), 0px 0px 0px rgba(13, 13, 13, 0);
    background: #0075a9;
    border-radius: 0px;
    border: 0px solid #010101; }
  div#progress-container input[type=range]::-moz-range-thumb {
    box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
    border: 1px solid #ffffff;
    height: 15px;
    width: 15px;
    border-radius: 16px;
    background: #ffffff;
    cursor: pointer; }
  div#progress-container input[type=range]::-ms-track {
    width: 100%;
    height: 0px;
    cursor: pointer;
    background: transparent;
    border-color: transparent;
    color: transparent; }
  div#progress-container input[type=range]::-ms-fill-lower {
    background: #003d57;
    border: 0px solid #010101;
    border-radius: 0px;
    box-shadow: 0px 0px 0px rgba(0, 0, 0, 0), 0px 0px 0px rgba(13, 13, 13, 0); }
  div#progress-container input[type=range]::-ms-fill-upper {
    background: #0075a9;
    border: 0px solid #010101;
    border-radius: 0px;
    box-shadow: 0px 0px 0px rgba(0, 0, 0, 0), 0px 0px 0px rgba(13, 13, 13, 0); }
  div#progress-container input[type=range]::-ms-thumb {
    box-shadow: 0px 0px 0px #000000, 0px 0px 0px #0d0d0d;
    border: 1px solid #ffffff;
    height: 15px;
    width: 15px;
    border-radius: 16px;
    background: #ffffff;
    cursor: pointer;
    height: 0px;
    display: block; }
  @media all and (-ms-high-contrast: none) {
    div#progress-container *::-ms-backdrop, div#progress-container input[type="range"].amplitude-song-slider {
      padding: 0px; }
    div#progress-container *::-ms-backdrop, div#progress-container input[type=range].amplitude-song-slider::-ms-thumb {
      height: 15px;
      width: 15px;
      border-radius: 10px;
      cursor: pointer;
      margin-top: -8px; }
    div#progress-container *::-ms-backdrop, div#progress-container input[type=range].amplitude-song-slider::-ms-track {
      border-width: 15px 0;
      border-color: transparent; }
    div#progress-container *::-ms-backdrop, div#progress-container input[type=range].amplitude-song-slider::-ms-fill-lower {
      background: #ffffff;
      border-radius: 10px; }
    div#progress-container *::-ms-backdrop, div#progress-container input[type=range].amplitude-song-slider::-ms-fill-upper {
      background: #ffffff;
      border-radius: 10px; } }
  @supports (-ms-ime-align: auto) {
    div#progress-container input[type=range].amplitude-song-slider::-ms-thumb {
      height: 15px;
      width: 15px;
      margin-top: 3px; } }
  div#progress-container input[type=range]:focus::-ms-fill-lower {
    background: #0075a9; }
  div#progress-container input[type=range]:focus::-ms-fill-upper {
    background: #00adfb; }

div#control-container {
  margin-top: 25px;
  margin-top: 20px; }
  div#control-container div#repeat-container {
    width: 25%;
    float: left;
    padding-top: 20px; }
    div#control-container div#repeat-container div#repeat {
      width: 24px;
      height: 19px;
      cursor: pointer; }
      div#control-container div#repeat-container div#repeat.amplitude-repeat-off {
        background: url("images/repeat-off.svg"); }
      div#control-container div#repeat-container div#repeat.amplitude-repeat-on {
        background: url("images/repeat-on.svg"); }
    div#control-container div#repeat-container div#shuffle {
      width: 23px;
      height: 19px;
      cursor: pointer;
      float: right; }
      div#control-container div#repeat-container div#shuffle.amplitude-shuffle-off {
        background: url("images/shuffle-off.svg"); }
      div#control-container div#repeat-container div#shuffle.amplitude-shuffle-on {
        background: url("images/shuffle-on.svg"); }
  @media all and (-ms-high-contrast: none) {
    div#control-container *::-ms-backdrop, div#control-container div#control-container {
      margin-top: 40px;
      float: none; } }
  div#control-container div#central-control-container {
    width: 50%;
    float: left; }
    div#control-container div#central-control-container div#central-controls {
      width: 130px;
      margin: auto; }
      div#control-container div#central-control-container div#central-controls div#previous {
        display: inline-block;
        width: 40px;
        height: 40px;
        cursor: pointer;
        background: url("images/prev.svg");
        background-repeat: no-repeat;
        float: left;
        margin-top: 10px;
        margin-right: -5px; }
      div#control-container div#central-control-container div#central-controls div#play-pause {
        display: inline-block;
        width: 60px;
        height: 60px;
        cursor: pointer;
        float: left; }
        div#control-container div#central-control-container div#central-controls div#play-pause.amplitude-paused {
          background: url("images/play.svg"); }
        div#control-container div#central-control-container div#central-controls div#play-pause.amplitude-playing {
          background: url("images/pause.svg"); }
      div#control-container div#central-control-container div#central-controls div#next {
        display: inline-block;
        width: 40px;
        height: 40px;
        cursor: pointer;
        background: url("images/next.svg");
        background-repeat: no-repeat;
        float: left;
        margin-top: 10px;
        margin-left: -5px; }
  div#control-container div#volume-container {
    width: 25%;
    float: left;
    padding-top: 20px; }
    div#control-container div#volume-container div#shuffle-right {
      width: 23px;
      height: 19px;
      cursor: pointer;
      margin: auto; }
      div#control-container div#volume-container div#shuffle-right.amplitude-shuffle-off {
        background: url("images/shuffle-off.svg"); }
      div#control-container div#volume-container div#shuffle-right.amplitude-shuffle-on {
        background: url("images/shuffle-on.svg"); }
  div#control-container div.amplitude-mute {
    cursor: pointer;
    width: 25px;
    height: 19px;
    float: left; }
    div#control-container div.amplitude-mute.amplitude-not-muted {
      background: url("images/volume.svg");
      background-repeat: no-repeat; }
    div#control-container div.amplitude-mute.amplitude-muted {
      background: url("https://521dimensions.com/img/open-source/amplitudejs/blue-player/mute.svg");
      background-repeat: no-repeat; }

div#control-container:after {
  content: "";
  display: table;
  clear: both; }

/* Small only */
@media screen and (max-width: 39.9375em) {
  div#amplitude-player div#repeat-container div#repeat {
    margin-left: auto;
    margin-right: auto;
    float: none; }
  div#amplitude-player div#repeat-container div#shuffle {
    display: none; }
  div#amplitude-player div#volume-container div.volume-controls {
    display: none; }
  div#amplitude-player div#volume-container div#shuffle-right {
    display: block; } }
/* Medium only */
@media screen and (min-width: 40em) and (max-width: 63.9375em) {
  div#amplitude-player div#repeat-container div#repeat {
    margin-left: auto;
    margin-right: auto;
    float: none; }
  div#amplitude-player div#repeat-container div#shuffle {
    display: none; }
  div#amplitude-player div#volume-container div.volume-controls {
    display: none; }
  div#amplitude-player div#volume-container div#shuffle-right {
    display: block; } }
/* Large and up */
@media screen and (min-width: 64em) {
  div#amplitude-player div#repeat-container div#repeat {
    margin-left: 10px;
    margin-right: 20px;
    float: left; }
  div#amplitude-player div#volume-container div#shuffle-right {
    display: none; } }
input[type=range].amplitude-volume-slider {
  -webkit-appearance: none;
  width: calc( 100% - 33px);
  float: left;
  margin-top: 10px;
  margin-left: 5px; }

@-moz-document url-prefix() {
  input[type=range].amplitude-volume-slider {
    margin-top: 0px; } }
@supports (-ms-ime-align: auto) {
  input[type=range].amplitude-volume-slider {
    margin-top: 3px;
    height: 12px;
    background-color: rgba(255, 255, 255, 0) !important;
    z-index: 999;
    position: relative; }

  div.ms-range-fix {
    height: 1px;
    background-color: #A9A9A9;
    width: 67%;
    float: right;
    margin-top: -6px;
    z-index: 9;
    position: relative; } }
@media all and (-ms-high-contrast: none) {
  *::-ms-backdrop, input[type=range].amplitude-volume-slider {
    margin-top: -24px;
    background-color: rgba(255, 255, 255, 0) !important; } }
input[type=range].amplitude-volume-slider:focus {
  outline: none; }

input[type=range].amplitude-volume-slider::-webkit-slider-runnable-track {
  width: 75%;
  height: 1px;
  cursor: pointer;
  animate: 0.2s;
  background: #CFD8DC; }

input[type=range].amplitude-volume-slider::-webkit-slider-thumb {
  height: 10px;
  width: 10px;
  border-radius: 10px;
  background: #ffffff;
  cursor: pointer;
  margin-top: -4px;
  -webkit-appearance: none; }

input[type=range].amplitude-volume-slider:focus::-webkit-slider-runnable-track {
  background: #CFD8DC; }

input[type=range].amplitude-volume-slider::-moz-range-track {
  width: 100%;
  height: 1px;
  cursor: pointer;
  animate: 0.2s;
  background: #CFD8DC; }

input[type=range].amplitude-volume-slider::-moz-range-thumb {
  height: 10px;
  width: 10px;
  border-radius: 10px;
  background: #ffffff;
  cursor: pointer;
  margin-top: -4px; }

input[type=range].amplitude-volume-slider::-ms-track {
  width: 100%;
  height: 1px;
  cursor: pointer;
  animate: 0.2s;
  background: transparent;
  /*leave room for the larger thumb to overflow with a transparent border */
  border-color: transparent;
  border-width: 15px 0;
  /*remove default tick marks*/
  color: transparent; }

input[type=range].amplitude-volume-slider::-ms-fill-lower {
  background: #CFD8DC;
  border-radius: 10px; }

input[type=range].amplitude-volume-slider::-ms-fill-upper {
  background: #CFD8DC;
  border-radius: 10px; }

input[type=range].amplitude-volume-slider::-ms-thumb {
  height: 10px;
  width: 10px;
  border-radius: 10px;
  background: #ffffff;
  cursor: pointer;
  margin-top: 2px; }

input[type=range].amplitude-volume-slider:focus::-ms-fill-lower {
  background: #CFD8DC; }

input[type=range].amplitude-volume-slider:focus::-ms-fill-upper {
  background: #CFD8DC; }

input[type=range].amplitude-volume-slider::-ms-tooltip {
  display: none; }

div#time-container span.current-time {
  color: #ffffff;
  font-size: 14px;
  font-weight: 700;
  float: left;
  width: 15%;
  text-align: center; }
div#time-container span.duration {
  color: #ffffff;
  font-size: 14px;
  font-weight: 700;
  float: left;
  width: 15%;
  text-align: center; }

div#time-container:after {
  content: "";
  display: table;
  clear: both; }

div#meta-container {
  text-align: center;
  margin-top: 5px; }
  div#meta-container span.song-name {
    display: block;
    color: #6ea43b;
    font-size: 20px;
    font-family: 'Open Sans', sans-serif;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis; }
  div#meta-container div.song-artist-album {
    color: #ffffff;
    font-size: 14px;
    font-weight: 700;
    text-transform: uppercase;
    font-family: 'Open Sans', sans-serif;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis; }
    div#meta-container div.song-artist-album span {
      display: block; }

/*
  3. Layout
*/

div.amplitude-wave-form{
    margin-top: -14px;
}
      
 div.amplitude-wave-form svg{
      stroke: #ffffff;
      height: 50px;
      width: 100%;
      stroke-width: .5px;
      display:none;
}
 div.amplitude-wave-form svg g{
   stroke: #ffffff;
   height: 50px;
   width: 100%;
}
 div.amplitude-wave-form svg g path{
   stroke: #ffffff;
   height: 50px;
   width: 100%;
}

div#large-visualization{
    width: 100%;
    background-color: black;
    visibility: hidden;
  }
/*
  4. Pages
*/
/*
  5. Themes
*/
/*
  6. Utils
*/
/*
  7. Vendors
*/

/*# sourceMappingURL=app.css.map */
</style>

</head>
<div id="blue-playlist-container">
            <!-- Amplitude Player -->
            <div id="amplitude-player">
                <!-- Left Side Player -->
                <div id="amplitude-left">
                <span class="album-art"></span>
          <div class="amplitude-visualization" id="large-visualization">
            </div>
                    <div id="player-left-bottom">
                        <div id="time-container">
                            <span class="current-time">
                                <span class="amplitude-current-minutes" ></span>:<span class="amplitude-current-seconds"></span>
                            </span>
                            <div id="progress-container">
                                <div class="amplitude-wave-form">
                        </div>
                <label><input type="range" class="amplitude-song-slider"/></label>
                                <progress id="song-played-progress" class="amplitude-song-played-progress"></progress>
                                <progress id="song-buffered-progress" class="amplitude-buffered-progress" value="0"></progress>
                            </div>
                            <span class="duration">
                                <span class="amplitude-duration-minutes"></span>:<span class="amplitude-duration-seconds"></span>
                            </span>
                        </div>
                        <div id="control-container">
                            <div id="repeat-container">
                                <div class="amplitude-repeat" id="repeat"></div>
                                <div class="amplitude-shuffle amplitude-shuffle-off" id="shuffle"></div>
                            </div>
                            <div id="central-control-container">
                                <div id="central-controls">
                                    <div class="amplitude-prev" id="previous"></div>
                                    <div class="amplitude-play-pause" id="play-pause"></div>
                                    <div class="amplitude-next" id="next"></div>
                                </div>
                            </div>
                            <div id="volume-container">
                                <div class="volume-controls">
                                    <div class="amplitude-mute amplitude-not-muted"></div>
                                    <label><input type="range" class="amplitude-volume-slider"/></label>
                                    <div class="ms-range-fix"></div>
                                </div>
                                <div class="amplitude-shuffle amplitude-shuffle-off" id="shuffle-right"></div>
                            </div>
                        </div>
                        <div id="meta-container">
                            <span data-amplitude-song-info="name" class="song-name"></span>
                            <!--<div class="song-artist-album">                            <span data-amplitude-song-info="artist"></span>
                                <span data-amplitude-song-info="album"></span>
                            </div>-->
                            <a class="bandcamp" href="https://fredmahermusique.bandcamp.com">
          <br>L'album numérique est disponible sur<br><br><img src="images/bandcamp.svg" alt="Logo Bandcamp"></a>
                        </div>
                    </div>
                </div>
                <!-- End Left Side Player -->
                <!-- Right Side Player -->
                <div id="amplitude-right">
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="0">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg" alt="now-playing"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">J'attends l'printemps<span class="video"><a href="posts/video-j-attends-l-printemps/">VIDÉO
        </a></span></span>
                        </div>
                        <span class="song-duration">3:33</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="1">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Jamais loin</span>
                        </div>
                        <span class="song-duration">2:01</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="2">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Cheveux au vent<span class="video"><a href="posts/video-de-cheveux-au-vent/">VIDÉO
        </a></span></span>
                        </div>
                        <span class="song-duration">3:54</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="3">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Ainsi soit-il<span class="video"><a href="posts/video-ainsi-soit-il/">VIDÉO
        </a></span></span>
                        </div>
                        <span class="song-duration">2:31</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="4">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Amoureux seul</span>
                        </div>
                        <span class="song-duration">3:44</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="5">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Lentement mais sûrement</span>
                        </div>
                        <span class="song-duration">2:50</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="6">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">On a eu peur</span>
                        </div>
                        <span class="song-duration">3:29</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="7">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">En courant</span>
                        </div>
                        <span class="song-duration">3:08</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="8">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">J'ai pas l'choix</span>
                        </div>
                        <span class="song-duration">3:31</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="9">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Si j'te trouvais</span>
                        </div>
                        <span class="song-duration">3:04</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="10">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Marcher</span>
                        </div>
                        <span class="song-duration">3:01</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="11">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Ce n'est pas par hasard</span>
                            <span class="time-callbacks"></span>
                        </div>
                        <span class="song-duration">2:43</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="12">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Masson<span class="video"><a href="posts/video-masson/">VIDÉO
        </a></span></span>
                        </div>
                        <span class="song-duration">2:57</span>
                    </div>
                    <div class="song amplitude-song-container amplitude-play-pause" data-amplitude-song-index="13">
                        <div class="song-now-playing-icon-container">
                            <div class="play-button-container">
                            </div>
                            <img class="now-playing" src="images/now-playing.svg"/>
                        </div>
                        <div class="song-meta-data">
                            <span class="song-title">Le secret de l'amour</span>
                        </div>
                        <span class="song-duration">2:28</span>
                    </div>
                </div>
                <!-- End Right Side Player -->
            </div>
            <!-- End Amplitdue Player -->
</div>
<script>
 /*
	When the bandcamp link is pressed, stop all propagation so AmplitudeJS doesn't
	play the song.
*/
let bandcampLinks = document.getElementsByClassName('bandcamp-link');
for( var i = 0; i < bandcampLinks.length; i++ ){
	bandcampLinks[i].addEventListener('click', function(e){
		e.stopPropagation();
	});
}
let songElements = document.getElementsByClassName('song');
for( var i = 0; i < songElements.length; i++ ){
	/*
		Ensure that on mouseover, CSS styles don't get messed up for active songs.
	*/
	songElements[i].addEventListener('mouseover', function(){
		this.style.backgroundColor = 'transparent';
		this.querySelectorAll('.song-meta-data .song-title')[0].style.color = '#ffffff';
			/*this.querySelectorAll('.song-meta-data .song-artist')[0].style.color = '#ffffff';*/
		if( !this.classList.contains('amplitude-active-song-container') ){
			this.querySelectorAll('.play-button-container')[0].style.display = 'block';
		}
		this.quer
    /*ySelectorAll('img.bandcamp-grey')[0].style.display = 'none';
		this.querySelectorAll('img.bandcamp-white')[0].style.display = 'block';*/
		this.querySelectorAll('.song-duration')[0].style.color = '#ffffff';
	});
	/*
		Ensure that on mouseout, CSS styles don't get messed up for active songs.
	*/
	songElements[i].addEventListener('mouseout', function(){
		this.style.backgroundColor = 'transparent';
		this.querySelectorAll('.song-meta-data .song-title')[0].style.color = '#6ea43b';
			/*this.querySelectorAll('.song-meta-data .song-artist')[0].style.color = '#ffffff';*/
		this.querySelectorAll('.play-button-container')[0].style.display = 'none';
		/*this.querySelectorAll('img.bandcamp-grey')[0].style.display = 'block';
		this.querySelectorAll('img.bandcamp-white')[0].style.display = 'none';*/
		this.querySelectorAll('.song-duration')[0].style.color = '#6ea43b';
	});
	/*
		Show and hide the play button container on the song when the song is clicked.
	*/
	songElements[i].addEventListener('click', function(){
		this.querySelectorAll('.play-button-container')[0].style.display = 'none';
	});
}
/*
	Initializes AmplitudeJS
*/
Amplitude.init({
	"songs": [
		{
      "name": "J'attends l'printemps",
			"artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/j-attends-l-printemps.mp3",
    },
    {
      "name": "Jamais loin",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/jamais-loin.mp3",
    },
    {
      "name": "Cheveux au vent",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/cheveux-au-vent.mp3",
    },
    {
			"name": "Ainsi soit-il",
			"artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/ainsi-soit-il.mp3",
    },
    {
			"name": "Amoureux seul",
			"artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/amoureux-seul.mp3",
    },
    {
      "name": "Lentement mais sûrement",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/lentement-mais-surement.mp3",
    },
    {
      "name": "On a eu peur",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/on-a-eu-peur.mp3",
    },
    {
      "name": "En courant",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/en-courant.mp3",
		},
		{
			"name": "J'ai pas l'choix",
			"artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/j-ai-pas-l-choix.mp3",
    },
    {
      "name": "Si j'te trouvais",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/si-j-te-trouvais.mp3",
    },
    {
      "name": "Marcher",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/marcher.mp3",
    },
    {
      "name": "Ce n'est pas par hasar",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/ce-n-est-pas-par-hasard.mp3",
    },
    {
      "name": "Masson",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/masson.mp3",
    },
		{
      "name": "Le secret de l'amour",
      "artist": "Fred Maher",
			"album": "J'attends l'printemps",
			"url": "/mp3/le-secret-de-l-amour.mp3",
    }
	]
});
</script>