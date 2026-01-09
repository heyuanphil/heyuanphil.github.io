title: "He Yuan"
author: "He Yuan"
description: "PhD student, Umass Amherst"
permalink: /:title/
lang: "en"
excerpt_separator: "\n\n\n"
date_format: "%B %d, %Y"

# Layout

show_excerpts: true             # show article excerpts instead of archive list on the home page
show_frame: true                # display a grey frame on large screens
show_sidebar: false             # show a sidebar instead of the usual header
show_minimal: false             # remove all clutter

#show_frame: "/assets/images/background.svg"

# Menu                          # for available icons see https://fontawesome.com/v5/icons/

navigation:                     # accepts {file, title, url, icon, sidebaricon}
  - {file: "home.md", title: "Home", sidebaricon: comments}
  - {file: "research.md", title: "Research", sidebaricon: comments}
  - {file: "teaching.md", title: "Teaching", sidebaricon: comments}
  - {file: "talking.md", title: "Talk", sidebaricon: comments} 
  - {file: "reading.md", title: "Reading Group", sidebaricon: comments} 



external:                       # accepts {file, title, url, icon, sidebaricon}
  - {title: Mail, icon: envelope, url: "mailto:heyuan@umass.edu"}

comments:
#  disqus_shortname: ""         # see https://disqus.com
#  isso_domain: ""              # see https://isso-comments.de

---
layout: home
title: ""
---

<div style="display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; margin-top:50px;">

  <!-- 左边文字 -->
  <div style="flex:1; min-width:250px; margin-right:30px;">
    <h1>He Yuan</h1>
    <p style="font-size:1.2em; line-height:1.5;">
      I am a Ph.D. student (2023-) in philosophy at University of Massachusetts Amherst, focusing on epistemology, metaphysics and epistemology of metaphysics. Before starting my PhD, I earned an MA in Philosophy of Science from Wuhan University, where I wrote my thesis on Epistemic Permissivism, and a BSc in Geo-Information Science and Technology from Ocean University of China, where I studied the seasonal and year-to-year changes of Arctic sea ice.<br>
    </p>

    <!-- 发音说明 -->
    <p style="margin-top:10px; font-size:1em; line-height:1.5;">
      How to pronounce my first name:
    </p>

    <!-- 播放器 -->
    <div style="display:flex; align-items:center; gap:10px; margin-top:5px;">
      <!-- 播放按钮 -->
      <button id="playBtn"
              style="border:none; background-color:#007bff; color:white; cursor:pointer; 
                     padding:6px; border-radius:50%; width:32px; height:32px;
                     display:flex; align-items:center; justify-content:center; transition: transform 0.2s;">
        🔊
      </button>

      <!-- 进度条 -->
      <input id="progressBar" type="range" value="0" min="0" max="100"
             style="flex:1; cursor:pointer;">
    </div>

    <audio id="heAudio" src="/assets/audio/He.m4a" preload="none"></audio>

    <script>
      const audio = document.getElementById('heAudio');
      const playBtn = document.getElementById('playBtn');
      const progressBar = document.getElementById('progressBar');

      // 播放 / 暂停
      playBtn.addEventListener('click', () => {
        if (audio.paused) {
          audio.play();
          playBtn.textContent = '⏸️';
        } else {
          audio.pause();
          playBtn.textContent = '🔊';
        }
      });

      // 悬停动画
      playBtn.addEventListener('mouseover', () => {
        playBtn.style.transform = 'scale(1.2)';
      });
      playBtn.addEventListener('mouseout', () => {
        playBtn.style.transform = 'scale(1)';
      });

      // 更新进度条
      audio.addEventListener('timeupdate', () => {
        if (!isNaN(audio.duration)) {
          progressBar.value = (audio.currentTime / audio.duration) * 100;
        }
      });

      // 拖动跳转
      progressBar.addEventListener('input', () => {
        audio.currentTime = (progressBar.value / 100) * audio.duration;
      });

      // 播放结束复位
      audio.addEventListener('ended', () => {
        playBtn.textContent = '🔊';
        progressBar.value = 0;
      });
    </script>
  </div>

  <!-- 右边图片 -->
  <div style="flex:0 0:260px; text-align:center;">
    <img src="/assets/images/profile.jpg"
         alt="He Yuan"
         style="width:230px; border-radius:50%; border:2px solid #ccc;">
  </div>

</div>
