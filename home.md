---
layout: home
title: ""
---

<div style="display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; margin-top:50px;">

  <!-- 左边文字 -->
  <div style="flex:1; min-width:250px; margin-right:30px;">
    <h1>He Yuan</h1>
    <p style="font-size:1.2em; line-height:1.5;">
      I am a Ph.D. student (2023-) in philosophy at University of Massachusetts Amherst, focusing on epistemology, metaphysics and epistemology of metaphysics. Before starting my PhD, I earned an MA in Philosophy of Science from Wuhan University, where I wrote my thesis on Epistemic Permissivism, and a BSc in Geo-Information Science and Technology from Ocean University of China, where I studied the seasonal and year-to-year changes of Arctic sea ice.
    </p>

    <p style="margin-top:10px; font-size:1em;">
      How to pronounce my first name:
    </p>

    <div style="display:flex; align-items:center; gap:10px; margin-top:5px;">
      <button id="playBtn"
              style="border:none; background-color:#007bff; color:white; cursor:pointer; 
                     padding:6px; border-radius:50%; width:32px; height:32px;
                     display:flex; align-items:center; justify-content:center;">
        🔊
      </button>

      <input id="progressBar" type="range" value="0" min="0" max="100"
             style="flex:1;">
    </div>

    <audio id="heAudio" src="/assets/audio/He.m4a" preload="none"></audio>

    <script>
      const audio = document.getElementById('heAudio');
      const playBtn = document.getElementById('playBtn');
      const progressBar = document.getElementById('progressBar');

      playBtn.addEventListener('click', () => {
        if (audio.paused) {
          audio.play();
          playBtn.textContent = '⏸️';
        } else {
          audio.pause();
          playBtn.textContent = '🔊';
        }
      });

      audio.addEventListener('timeupdate', () => {
        if (!isNaN(audio.duration)) {
          progressBar.value = (audio.currentTime / audio.duration) * 100;
        }
      });

      progressBar.addEventListener('input', () => {
        audio.currentTime = (progressBar.value / 100) * audio.duration;
      });

      audio.addEventListener('ended', () => {
        playBtn.textContent = '🔊';
        progressBar.value = 0;
      });
    </script>
  </div>

  <!-- 右边图片（关键在这里） -->
  <div style="flex:0 0 auto; width:260px; text-align:center;">
    <img src="/assets/images/profile.jpg"
         alt="He Yuan"
         style="width:230px; border-radius:50%; border:2px solid #ccc;">
  </div>

</div>
