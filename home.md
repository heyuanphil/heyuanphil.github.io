---
layout: home
title: ""
---

<div style="display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; margin-top:50px;">

  <!-- 左边文字 -->
  <div style="flex:1; min-width:250px; margin-right:30px;">
    <h1>He Yuan</h1>
    <p style="font-size:1.2em; line-height:1.5;">
      I’ve been a PhD student in philosophy at UMass Amherst since 2023, focusing on epistemology, the epistemology of metaphysics, and metaphysics. Before starting my PhD, I earned an MA in Philosophy of Science from Wuhan University, where I wrote my thesis on Epistemic Permissivism, and a BSc in Geo-Information Science and Technology from Ocean University of China, where I studied the seasonal and year-to-year changes of Arctic sea ice.<br>
    </p>

    <!-- 发音行 -->
    <p style="margin-top:10px; font-size:1em; line-height:1.5; display:flex; align-items:center;">
      How to pronounce my first name:
      <button onclick="document.getElementById('heAudio').play()" 
              style="border:none; background-color:#007bff; color:white; cursor:pointer; 
                     padding:6px; margin-left:10px; border-radius:50%; width:32px; height:32px;
                     display:flex; align-items:center; justify-content:center; transition: transform 0.2s;">
        🔊
      </button>
    </p>
    <audio id="heAudio" src="/assets/audio/He.m4a" preload="none"></audio>

    <script>
      const btn = document.querySelector('button');
      btn.addEventListener('mouseover', () => btn.style.transform = 'scale(1.2)');
      btn.addEventListener('mouseout', () => btn.style.transform = 'scale(1)');
    </script>
  </div>

  <!-- 右边图片 -->
  <div style="flex:0 0:260px; text-align:center;">
    <img src="/assets/images/profile.jpg"
         alt="He Yuan"
         style="width:230px; border-radius:50%; border:2px solid #ccc;">
  </div>

</div>
