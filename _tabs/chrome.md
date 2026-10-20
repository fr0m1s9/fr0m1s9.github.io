---
layout: page
title: Chrome
permalink: /target/browser/chrome/
---

{% include research-style.html %}

<section class="chrome-overview" aria-label="Chrome research">
  <div class="research-crumb"><a href="{{ '/target/' | relative_url }}">Target</a> / <a href="{{ '/target/browser/' | relative_url }}">Browser</a> / Chrome</div>
  <div class="research-kicker">BROWSER SECURITY / CHROME</div>
  <p class="research-intro">Chrome와 V8 엔진의 내부 구조를 분석하고, 직접 수행한 실험과 취약점 연구 과정을 기록합니다.</p>
  <div class="research-grid chrome-main-grid">
    <a class="research-card" href="{{ '/target/browser/chrome/study/' | relative_url }}" aria-label="Chrome Study 목록 열기">
      <span class="research-icon"><i class="fas fa-book-open" aria-hidden="true"></i></span>
      <span class="chrome-card-number">01 / RESEARCH NOTES</span>
      <h2>Study</h2>
      <p>V8 Object, 메모리 구조, 실행 파이프라인과 소스 코드 분석을 정리합니다.</p>
      <span class="research-arrow">View Study <i class="fas fa-arrow-right" aria-hidden="true"></i></span>
    </a>
    <a class="research-card" href="{{ '/target/browser/chrome/exploit-lab/' | relative_url }}" aria-label="Chrome Exploit Lab 목록 열기">
      <span class="research-icon"><i class="fas fa-flask" aria-hidden="true"></i></span>
      <span class="chrome-card-number">02 / HANDS-ON LABS</span>
      <h2>Exploit Lab</h2>
      <p>취약점 재현, Debugging, Root Cause Analysis 및 Exploitation 실습 결과를 기록합니다.</p>
      <span class="research-arrow">View Exploit Labs <i class="fas fa-arrow-right" aria-hidden="true"></i></span>
    </a>
  </div>
</section>
<style>
.chrome-main-grid .research-card { min-height: 255px; display:flex; flex-direction:column; }
.chrome-main-grid .research-card .research-icon { margin-bottom:1rem; }
.chrome-main-grid .research-card .chrome-card-number { font-size:.7rem;letter-spacing:.12em;font-weight:700;color:var(--text-muted-color,#999); }
.chrome-main-grid .research-card h2 { margin:.6rem 0 .7rem!important;font-size:1.65rem; }
.chrome-main-grid .research-card p { flex-grow:1; }
.chrome-main-grid .research-card .research-arrow { margin-top:auto; }
</style>
