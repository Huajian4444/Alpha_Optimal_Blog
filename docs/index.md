<style>
  body {
    font-family: 'Segoe UI', '微软雅黑', 'Arial', sans-serif;
    background: #f7fafd;
    color: #222;
  }
  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 1.2rem 0.5rem;
  }
  .main-title {
    font-size: 2rem;
    font-weight: 700;
    color: #1a4fa0;
    letter-spacing: 1px;
    margin-bottom: 0.8rem;
    text-align: center;
  }
  .subtitle {
    font-size: 1rem;
    color: #4a90e2;
    text-align: center;
    margin-bottom: 1.2rem;
    letter-spacing: 0.5px;
  }
  .about-section, .feature-section, .contact-section {
    background: #fff;
    border-radius: 6px;
    padding: 1.2rem 1rem;
    margin-bottom: 1.2rem;
    box-shadow: 0 1px 4px rgba(30,80,200,0.03);
  }
  .about-flex {
    display: flex;
    align-items: center;
    gap: 1.2rem;
    flex-wrap: wrap;
  }
  .about-flex img {
    width: 120px;
    border-radius: 6px;
    box-shadow: 0 1px 4px rgba(30,80,200,0.06);
    background: #eaf1fb;
  }
  .about-text {
    flex: 1;
    font-size: 0.98rem;
    color: #333;
    line-height: 1.5;
  }
  .feature-list {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: space-between;
    margin: 1rem 0 0 0;
  }
  .feature-item {
    flex: 1 1 120px;
    background: #f7fafd;
    border-left: 2px solid #4a90e2;
    padding: 0.7rem 0.7rem 0.7rem 1rem;
    border-radius: 4px;
    font-size: 0.95rem;
    margin-bottom: 0.5rem;
    min-width: 100px;
  }
  .contact-section p {
    margin: 0.3rem 0;
    font-size: 0.98rem;
  }
  @media (max-width: 700px) {
    .about-flex {
      flex-direction: column;
      text-align: center;
    }
    .about-flex img {
      margin-bottom: 0.7rem;
    }
    .feature-list {
      flex-direction: column;
      gap: 0.5rem;
    }
  }
</style>

<div class="container">
  <div class="main-title">Alpha Optimal 多轴仿真优化平台</div>
  <div class="subtitle">专注高端制造 · 智能 · 高效 · 稳定</div>

  <section class="about-section">
    <div class="about-flex">
      <img src="./image/中汇世银大厦.jpg" alt="公司大楼">
      <div class="about-text">
        瑞凡软件位于东莞松山湖高新技术开发区，专注于多轴仿真优化软件的研发与创新。<br>
        <b>Alpha Optimal</b> 软件已被广泛应用于非金属多轴加工领域，年交付超百套，为全球客户提供优化仿真解决方案。
      </div>
    </div>
  </section>

  <section class="feature-section">
    <div style="font-weight:600;font-size:1.05rem;color:#1a4fa0;margin-bottom:0.7rem;">核心优势</div>
    <div class="feature-list">
      <div class="feature-item">多轴联动完全仿真</div>
      <div class="feature-item">智能碰撞检测</div>
      <div class="feature-item">工艺参数优化</div>
      <div class="feature-item">自定义机床&夹具</div>
    </div>
    <div style="margin-top:0.7rem;color:#4a90e2;font-size:0.95rem;">
      支持标准机床与特殊定制设备的全流程数字化，显著提升设备利用率与生产效率。
    </div>
  </section>

  <section class="contact-section">
    <div style="font-weight:600;font-size:1rem;color:#1a4fa0;margin-bottom:0.3rem;">联系我们</div>
    <p>📍 广东省东莞市松山湖园区总部三路20号1栋215室</p>
    <p>📞 138 0963 5904</p>
    <p>✉️ 297380404@qq.com</p>
    <p>🕒 工作日 9:00-18:00</p>
  </section>
</div>