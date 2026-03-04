---
title: "Traffic Dashboard"
summary: "网站访问来源与总量可视化。"
date: 2026-03-04
type: page
show_date: false
show_reading_time: false
---

<style>
  .traffic-wrap {
    margin-top: 0.8rem;
  }
  .traffic-card {
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 14px;
    overflow: hidden;
    box-shadow: 0 12px 30px rgba(0, 0, 0, 0.3);
    background: #020617;
    padding: 1.2rem;
    text-align: center;
  }
  .traffic-note {
    margin-top: 0.8rem;
    color: #94a3b8;
    font-size: 0.92rem;
  }
  .traffic-map {
    min-height: 260px;
  }
</style>

<div class="traffic-wrap">
  <div class="traffic-card">
    <div class="traffic-map">
      <script
        type="text/javascript"
        id="mapmyvisitors"
        src="https://mapmyvisitors.com/map.js?d=m97bUhG_cTH-e4S5sQKYqXCCZA2hoiZkzsPt-lWO6IA&cl=ffffff&w=a"
      ></script>
    </div>
    <p class="traffic-note">Live visitor map and pageview counter.</p>
  </div>
</div>
