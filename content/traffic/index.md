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
  .traffic-stats {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 0.9rem;
    margin-bottom: 1rem;
  }
  .traffic-item {
    border: 1px solid rgba(148, 163, 184, 0.28);
    border-radius: 12px;
    padding: 0.9rem;
    background: rgba(15, 23, 42, 0.7);
  }
  .traffic-label {
    color: #94a3b8;
    font-size: 0.9rem;
    margin-bottom: 0.3rem;
  }
  .traffic-value {
    color: #f8fafc;
    font-size: 1.45rem;
    font-weight: 700;
    line-height: 1.2;
  }
</style>

<div class="traffic-wrap">
  <div class="traffic-card">
    <div class="traffic-stats">
      <div class="traffic-item">
        <div class="traffic-label">Main counter - total page views</div>
        <div class="traffic-value" id="busuanzi_value_site_pv">--</div>
      </div>
      <div class="traffic-item">
        <div class="traffic-label">Main counter - total visitors</div>
        <div class="traffic-value" id="busuanzi_value_site_uv">--</div>
      </div>
      <div class="traffic-item">
        <div class="traffic-label">Traffic page views</div>
        <div class="traffic-value" id="busuanzi_value_page_pv">--</div>
      </div>
    </div>
    <div class="traffic-map">
      <script
        type="text/javascript"
        id="mapmyvisitors"
        src="https://mapmyvisitors.com/map.js?d=m97bUhG_cTH-e4S5sQKYqXCCZA2hoiZkzsPt-lWO6IA&cl=ffffff&w=a"
      ></script>
    </div>
    <p class="traffic-note">
      Main counter tracks all pages globally; map shows geographic distribution.
    </p>
  </div>
</div>
