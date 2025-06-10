<style>
  body {
    font-family: 'Segoe UI', '微软雅黑', 'Arial', sans-serif;
    background: linear-gradient(135deg,rgb(96, 113, 126) 0%,rgb(189, 204, 223) 50%, #f0f4ff 100%);
    color: #222;
    min-height: 100vh;
    margin: 0;
    position: relative;
    overflow-x: hidden;
  }
  /* 科技感背景装饰 */
  .tech-bg {
    position: fixed;
    top: 0; left: 0; width: 100vw; height: 100vh;
    pointer-events: none;
    z-index: 0;
  }
  .tech-bg svg {
    width: 100vw;
    height: 100vh;
    opacity: 0.18;
  }
  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 3.5rem 1rem 2rem 1rem;
    text-align: center;
    position: relative;
    z-index: 1;
  }
  .main-title {
    font-size: 2.2rem;
    font-weight: 600;
    color: #1a4fa0;
    letter-spacing: 3px;
    margin-bottom: 4.5rem;
    cursor: pointer;
    transition: color 0.2s;
    user-select: none;
    text-align: left; /* 左对齐 */
    text-shadow: 0 4px 24pxrgb(62, 126, 223), 0 1px 0 #fff;
    background: linear-gradient(90deg, #1a4fa0 30%, #4a90e2 70%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    line-height: 1.0; /* 调小主标题多行间距 */
  }
  .main-title:hover {
    color:rgb(120, 215, 219);
    -webkit-text-fill-color:rgb(93, 150, 185);
    background: none;
  }
  .subtitle {
    font-size: 1.1rem;
    color: #4a90e2;
    margin-bottom: 2.2rem;
    font-weight: 400;
    letter-spacing: 1px;
  }
  .desc-block {
    display: flex;
    flex-direction: column;
    align-items: flex-start; /* 左对齐 */
    gap: 0.7rem;
    margin-bottom: 2.2rem;
  }
  .desc-line {
    font-size: 1.0rem;
    color: #222;
    background: rgba(196, 199, 211, 0.54);
    border-radius: 8px;
    padding: 0.5rem 1.2rem;
    box-shadow: 0 2px 8px #eaf1fb;
    display: inline-block;
    font-weight: 500;
    letter-spacing: 1px;
    text-align: left; /* 左对齐 */
    width: 100%;      /* 占满父容器宽度 */
    box-sizing: border-box;
  }
  .feature-list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: minmax(40px, auto);
    gap: 1.2rem;
    margin-top: 2.5rem;
    min-height: 120px;
    justify-items: stretch;
    align-items: center;
    transition: all 0.7s cubic-bezier(.4,2,.6,1);
    z-index: 1;
  }
  .feature-item {
    opacity: 1;
    transform: none;
    background: linear-gradient(100deg, #fafdff 60%, #eaf6ff 100%);
    border-left: 4px solid #4a90e2;
    border-radius: 8px;
    padding: 0.6rem 1.2rem;
    font-size: 1rem;
    color: #1a4fa0;
    font-weight: 600;
    box-shadow: 0 2px 12px #eaf1fb;
    min-width: 120px;
    min-height: 40px;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    text-align: left;
    position: relative;
    z-index: 1;
    border-bottom: 1px solid #e3eafc;
    /* 移除动画相关属性 */
    /* transition: opacity 1s, transform 1s; */
  }
  .feature-item.visible {
    /* 不再需要任何动画效果 */
  }
  @media (max-width: 900px) {
    .feature-list {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  @media (max-width: 600px) {
    .main-title { font-size: 1.1rem; }
    .feature-list {
      grid-template-columns: 1fr;
      gap: 0.7rem;
    }
    .feature-item { font-size: 0.95rem; padding: 0.5rem 0.7rem; min-width: 80px; }
    .container { padding: 1.2rem 0.2rem; }
    .desc-block { align-items: flex-start; }
    .desc-line { font-size: 1rem; padding: 0.4rem 0.7rem; }
  }
</style>

<!-- 科技感SVG背景 -->
<div class="tech-bg">
  <svg>
    <defs>
      <linearGradient id="techline" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0%" stop-color="#4a90e2"/>
        <stop offset="100%" stop-color="#1a4fa0"/>
      </linearGradient>
    </defs>
    <circle cx="80" cy="120" r="60" fill="none" stroke="url(#techline)" stroke-width="2"/>
    <circle cx="90%" cy="80" r="40" fill="none" stroke="url(#techline)" stroke-width="2"/>
    <rect x="60%" y="70%" width="120" height="60" rx="20" fill="none" stroke="url(#techline)" stroke-width="2"/>
    <polyline points="0,400 200,300 400,350 600,320 900,400" fill="none" stroke="url(#techline)" stroke-width="2"/>
    <polyline points="0,600 300,500 700,600 900,550" fill="none" stroke="url(#techline)" stroke-width="2"/>
  </svg>
</div>

<div class="container">
  <div class="main-title" id="mainTitle">
    AlphaOptimal</p> 是一种先进的生产工具
  </div>
  <div class="desc-block">
    <div class="desc-line">操作人员能轻易的把设备的性能发挥到它的物理极限</div>
  </div>
  <div class="feature-list" id="featureList">
    <div class="feature-item">多轴联动完全仿真</div>
    <div class="feature-item">智能碰撞检测</div>
    <div class="feature-item">工艺参数优化</div>
    <div class="feature-item">自定义机床&夹具</div>
    <div class="feature-item">显著提升生产效率</div>
  </div>
</div>

#