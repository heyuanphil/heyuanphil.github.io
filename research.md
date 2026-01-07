---
layout: page
title: Research
permalink: /research/
hide_title: true
---

<style>
/* 只影响 Publications 标题，不影响 Markdown 列表 */
.publication .pub-title {
  font-size: 1em;      /* 与列表字体一致 */
  font-weight: normal;  /* 不加粗 */
  cursor: pointer;
}

/* PDF 链接蓝色 */
.publication .pub-abstract a {
  color: #007bff;
  text-decoration: underline;
}

/* 鼠标悬停标题变蓝 */
.publication .pub-title:hover {
  color: #007bff;
}
</style>

## Research Areas

*Epistemology*: Epistemic permissivism and its applications；Credence-frequency link  
*Epistemology of Metaphysics*: Theoretical virtues in metaphysics；Formal epistemology of metaphysics；Metaphysical disagreement  
*Metaphysics*: Laws of nature；Chance-frequency link  

---

## Publications

<div class="publication">
  <p class="pub-title" onclick="toggleAbstract('paper1')">
    Epistemic Permissivism and Risk Assessment in Irrationality, <em>Mind</em> (forthcoming)
  </p>
  <div id="paper1" class="pub-abstract" style="display:none; margin-left: 1em;">
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
      <a href="/assets/papers/epistemic-permissivism.pdf">Download PDF</a>
    </p>
  </div>
</div>

---

## In Progress

- A paper arguing that an agent’s rational credence can sometimes morally wrong others in cases of epistemic permissivism  
- A paper arguing that theoretical virtues can be truth-conducive in science but may fail to do so in metaphysics  
- A paper defending that we should not be highly confident that our world is a simulation  

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
