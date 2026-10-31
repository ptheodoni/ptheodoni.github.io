---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi there fellow human.. or are you not?

 I'm Yotta, from Athens, Greece; a physicist, theoretical & computational cognitive neuroscientist with a strong interest in philosophy.


Currently, I am 
- Caregiver of my mom with dementia  
- Independent Researcher
- Adjunct Professor of computational neuroscience, [Open University of Cyprus](https://www.ouc.ac.cy/), [MSc Cognitive Systems](https://www.ouc.ac.cy/index.php/en/studies/master/cos)
- Graduate student of the [MA in Philosophy](http://en.philosophymaster.philosophy.uoa.gr/overview.html) at the [Department of Philosophy](https://en.philosophy.uoa.gr/) of the [University of Athens (NKUA)](https://en.wikipedia.org/wiki/New_York_University)
- Developing [FemMe Radio](https://femme-radio.gr/en/), [Logoplex](https://logoplex.app), and [Noes](https://www.noes.gr/en/)  


My main research interest is in the foundations of science.

<!-- FemMe Radio: plays the live stream right here, without leaving the page -->
<div style="display:flex;flex-wrap:wrap;align-items:center;gap:.4em 1em;margin:.8em 0;">
<button id="femmeBtn" type="button" style="display:inline-flex;align-items:center;gap:.5em;padding:.6em 1.3em;border:0;border-radius:999px;background:#4b1d6e;color:#fff;font-weight:600;font-size:1em;cursor:pointer;"><svg viewBox="0 0 24 24" width="20" height="20" aria-hidden="true" style="flex:none"><rect x="9" y="2.5" width="6" height="11" rx="3" fill="#fff"/><path d="M6 11a6 6 0 0 0 12 0M12 17v4M8.5 21h7" fill="none" stroke="#fff" stroke-width="1.8" stroke-linecap="round"/></svg><span id="femmeLbl">&#9654; Listen live · FemMe Radio</span></button>
<span id="femmeNow" style="font-size:.85em;color:#666;"></span>
</div>
<audio id="femmeAudio" preload="none" src="https://radio.femme-radio.gr/listen/femme_radio/radio.mp3"></audio>
<script>
(function () {
  var a = document.getElementById("femmeAudio"), b = document.getElementById("femmeBtn"), n = document.getElementById("femmeNow"), l = document.getElementById("femmeLbl");
  var src = a.getAttribute("src");
  function nowPlaying() {
    fetch("https://radio.femme-radio.gr/api/nowplaying/femme_radio").then(function (r) { return r.json(); }).then(function (d) {
      var s = d && d.now_playing && d.now_playing.song;
      if (s && !a.paused) n.textContent = "Now playing: " + (s.artist ? s.artist + " – " : "") + (s.title || "");
    }).catch(function () {});
  }
  var timer;
  b.onclick = function () {
    if (a.paused) {
      a.src = src; a.play();
      l.innerHTML = "&#10074;&#10074; Pause · FemMe Radio";
      n.textContent = "Connecting…"; nowPlaying(); timer = setInterval(nowPlaying, 20000);
    } else {
      a.pause(); a.removeAttribute("src"); a.load();
      l.innerHTML = "&#9654; Listen live · FemMe Radio"; n.textContent = ""; clearInterval(timer);
    }
  };
  a.onerror = function () { if (l.innerHTML.indexOf("Pause") > -1) n.innerHTML = 'Could not connect — <a href="https://femme-radio.gr/en/" target="_blank" rel="noopener">open femme-radio.gr</a>'; };
})();
</script>


  
New! 
---
Our paper [***Comparisons of the structure and function of higher cortical circuits in marmosets and macaques: Models for mental health disorders***](https://www.sciencedirect.com/science/article/pii/S0006322326015155?casa_token=bODuTLe7tWQAAAAA:mZPi7CI2qxLz0weAthtjDtu9w2mnHpNttWfDExp6eSnFylxbttTlRavzJRxu5G5_Zf2hqA8L#appsec1) by Mary Kate P. Joyce, Raymond Ka Wong, Courtney Glavis-Bloom, Susheel Vijayraghavan, Judith Burkart, Panagiota Theodoni, Diego B. Piza, Claudia Perez-Cruz, Stefan Everling, and Angela C. Roberts,  
is published in *Biological Psychiatry*, September 2026  

Chrysi Serefidou, the graduate student of the MSc Cognitive Science of the University of Athens, whose master thesis I supervised, submitted her thesis on [Θεωρητικές προσεγγίσεις της συνειδητότητας μέσα από την κβαντική φυσική](https://pergamos.lib.uoa.gr/uoa/dl/object/5402181) (Theoretical approaches to consciousness through quantum physics), May 2026    


Our paper [*From comparative connectomics to large-scale working memory modeling in macaque and marmoset*](https://www.cell.com/cell-reports/fulltext/S2211-1247(25)01619-5)  
Loïc Magrou+, Panagiota Theodoni+, Amy F.T. Arnsten, Marcello G.P. Rosa, Xiao-Jing Wang  
is published in *Cell Reports*, January 2026  
(+: equal contribution)  
