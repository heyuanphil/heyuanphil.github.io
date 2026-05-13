---
layout: page
title: Research
permalink: /research/
hide_title: true
---

<style>
/* 标题圆点样式 */
.publication-title {
  font-size: 1em;      
  font-weight: normal;  
  cursor: pointer;
  list-style-type: disc; 
  list-style-position: outside;
  margin-left: 0.5em; /* 给黑点留空间，这里可以微调 */
}

/* 摘要左边距比标题大 */
.pub-abstract {
  margin-left: 0.5em; /* 可以调整这个值，让摘要更靠右 */
}

/* PDF 链接蓝色 */
.pub-abstract a {
  color: #007bff;
  text-decoration: underline;
}

/* 鼠标悬停变蓝（intro + publication） */
.publication-title:hover,
.research-intro:hover {
  color: #007bff;
}

</style>


<p class="research-intro"
   onclick="toggleAbstract('intro')"
   style="cursor:pointer; margin:0;">
My research focuses on epistemic permissivism, its applications to epistemology of metaphysics, particularly metaphysical disagreement, and its interactions with morality, particularly credence wronging. I also work on the frequency-credence link in formal epistemology and the chance-frequency link in metaphysics.
</p>

<div id="intro" class="pub-abstract" style="display:none; text-align:center;">
  <img src="/assets/images/research-overview.PNG" 
       alt="Research Overview" 
       style="width:100%; max-width:800px; margin-top:0.8em;">
</div>



---

## Research Areas

- *Epistemology*: Epistemic permissivism; Credence-frequency link  
- *Epistemology of Metaphysics*: Theoretical virtues in metaphysics; Peer disagreement in metaphysics  
- *Metaphysics*: Laws of nature; Chance-frequency link  

---

## Publications

<ul>
  <li>
    <span class="publication-title" onclick="toggleAbstract('paper1')">
      Epistemic Permissivism and Risk Assessment in Irrationality, <em>Mind</em> (2026)
    </span>
    <div id="paper1" class="pub-abstract" style="display:none;">
      <p>
        A popular version of epistemic Permissivism says that, given the total evidence, sometimes there is a
        permissible credence range towards a proposition. Ginger Schultheis (2018) offers a Dominance Argument
        against it. Schultheis argues that it is irrational to hold a credence at the edge of any permissible range
        because the edge credence takes higher risks of being irrational than the credence in the middle. In this
        paper, I propose two new responses. Firstly, I argue that after the risk assessment in irrationality, a new
        stable range may emerge such that each credence from it does not take more risks than others. Schultheis’s
        Dominance Argument can only shrink the original credence range to this new stable range. Second, I argue
        that sometimes it is rational for us to hold a more risky credence when a safer alternative is available. If
        rationality aims at truth-conduciveness and informativeness, a credence’s higher risks of being irrational
        do not render it irrational when one risks being less truth-conducive in exchange for informativeness.
      </p>
      <p>
        <a href="/assets/papers/epistemic-permissivism.pdf" target="_blank">
          Download PDF 🔗
        </a>
      </p>
    </div>
  </li>
</ul>

---

## In Progress

- A paper arguing that one's rational credence can morally wrong others in cases of epistemic permissivism  
- A paper arguing that theoretical virtues can be truth-conducive in science but fail to do so in metaphysics  
- A paper defending that we should not be highly confident that our world is a computer simulation  

<script>
  // 中文注释的 toggleAbstract 函数
  function toggleAbstract(id) {
    const elem = document.getElementById(id);
    if (elem.style.display === "none" || elem.style.display === "") {
      elem.style.display = "block";
    } else {
      elem.style.display = "none";
    }
  }
</script>

<p style="margin-top:80px; font-size:0.75em; color:#aaa; text-align:right;">
  Last Updated {{ site.time | date: "%B %d, %Y" }}
</p>

