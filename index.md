---
layout: page
---

# About Me

<img src="/images/jianshen.jpg" class="floatpic">

Here is **Junzhe Ma (glacier Bc)**.<br>

I am an undergraduate student in the Department of [Civil Engineering](https://city.wsyu.edu.cn/) at the [College of Smart City and Life Health](https://city.wsyu.edu.cn/) of the **Wuchang Shouyi University**. During my university years, I mainly used **Go** and **Python** to develop some **campus-related products**, and they were successfully implemented. 

Civil Engineering has trained me to think structurally and analytically, while my self-directed learning and project experience during university have shown me that I am more passionate and motivated by using technology to drive change and create value. Rather than limiting me, my interdisciplinary background gives me an additional perspective when solving complex problems.

Recently, I have been working on an AI-powered food service project called **Shou Shang Zhi Shi**. Based on the **MCP protocol**, I connected a large language model with our team database, allowing users to query real-time merchant and dish information directly through conversations with AI. I also integrated the **DeepSeek** large language model and implemented streaming content delivery through **SSE**.

I am not only writing code; I am also solving real problems for users. For example, when developing **Shou Shang Map**, I used **X-Y coordinates** to manage map locations, allowing points to be maintained dynamically through the backend without modifying the source code. When excessive data returned by the NBS page caused performance issues, I introduced pagination based on year, month, and day, and optimized the **MySQL** queries, reducing the response time by approximately **70%**, from 300 milliseconds to 80 milliseconds.

Currently, I am mainly studying **AI** and **AI Agents**. I have also received awards in competitions such as the **Challenge Cup** and the **China Collegiate Computer Design Competition**. Through these experiences, I hope to continue exploring how software engineering, artificial intelligence, and practical product development can work together to create meaningful value.<br>

## Work Experience

<div class="timeline">
  <div class="timeline-progress" id="timeline-progress"></div>

  <div class="timeline-item timeline-item--current">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/apple.svg" alt="Apple">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Software Engineer <span class="timeline-sep">|</span> <span class="timeline-company">Apple Inc.</span></div>
        <span class="timeline-time">Jan. 2026 - Present</span>
      </div>
      <div class="timeline-details">
        Developed AI agent tools for iPhone hardware testing, enhancing automated diagnostics workflows and improving large-scale test efficiency.
      </div>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/upenn.svg" alt="UPenn">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Research Assistant <span class="timeline-sep">|</span> <span class="timeline-company">University of Pennsylvania</span></div>
        <span class="timeline-time">Nov. 2025 - Jan. 2026</span>
      </div>
      <div class="timeline-details">
        ViT-driven image geolocation.
      </div>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/sf.svg" alt="SF Express">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Software Engineer <span class="timeline-sep">|</span> <span class="timeline-company">SF Express</span></div>
        <span class="timeline-time">May. 2025 - Jul. 2025</span>
      </div>
      <div class="timeline-details">
        Delivered microservice modules for the order management system.
      </div>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/boc.svg" alt="Bank of China">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Software Engineer <span class="timeline-sep">|</span> <span class="timeline-company">Bank of China</span></div>
        <span class="timeline-time">Jul. 2024 - Sep. 2024</span>
      </div>
      <div class="timeline-details">
        Involved in the deployment and fine-tuning of large language models in internal banking systems.
      </div>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-dot" style="background: #ffffff;">
      <img src="/images/logo/szu.svg" alt="Shenzhen University">
    </div>
    <div class="timeline-card">
      <div class="timeline-header">
        <div class="timeline-role">Research Assistant <span class="timeline-sep">|</span> <span class="timeline-company"><a href="https://bdsc.szu.edu.cn/">Big Data Institute, Shenzhen University</a></span></div>
        <span class="timeline-time">2023 - 2024</span>
      </div>
      <div class="timeline-details">
        Supervised by Distinguished Professor <a href="https://dblp.org/pid/h/JoshuaZhexueHuang.html">Joshua Zhexue Huang</a>. Carried out optimizations on data processing and clustering algorithms by leveraging distributed approximate computing techniques.
      </div>
    </div>
  </div>

</div>

<script>
(function() {
  var timelineProgress = document.getElementById('timeline-progress');
  var timeline = document.querySelector('.timeline');
  if (!timelineProgress || !timeline) return;

  var items = timeline.querySelectorAll('.timeline-item');

  // IntersectionObserver for in-view class
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('in-view');
        }
      });
    }, { rootMargin: '0px 0px -15% 0px' });

    items.forEach(function(item, idx) {
      if (idx < 3) {
        // Reveal first 3 immediately on load (still gets the stagger transition)
        item.classList.add('in-view');
      } else {
        observer.observe(item);
      }
    });
  } else {
    items.forEach(function(item) { item.classList.add('in-view'); });
  }

  // Scroll progress bar
  window.addEventListener('scroll', function() {
    var rect = timeline.getBoundingClientRect();
    var totalHeight = timeline.offsetHeight;
    var windowH = window.innerHeight;
    var lineTop = 30;
    var lineBottom = 30;
    var lineHeight = totalHeight - lineTop - lineBottom;

    if (rect.top < windowH && rect.bottom > 0) {
      var scrolled = Math.min(1, Math.max(0, (windowH - rect.top - lineTop) / (totalHeight - lineTop + windowH * 0.4)));
      timelineProgress.style.height = Math.min(scrolled * lineHeight, lineHeight) + 'px';
    }
  }, { passive: true });
})();
</script>

If you are interested in any aspect of me, I am always open to discussions and collaborations. Feel free to reach out to me at - bcglacier_1@qq.com

**<font color="#990000">Seeking Software Engineer and AI-related positions. Feel free to reach out!</font>**

---

## Publications

<div class="publications-grid">

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper1.svg" alt="Innovative covariance-based framework">
      <a href="https://www.tandfonline.com/doi/abs/10.1080/03610918.2026.2635000" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://www.tandfonline.com/doi/abs/10.1080/03610918.2026.2635000" target="_blank" rel="noopener">Innovative covariance-based framework: symmetry assessment and exponentiality testing under multiplicative distortion measurement Errors</a>
      </div>
      <div class="publication-authors"><strong class="author-highlight">Siming Deng</strong>, Jun Zhang, Jiongtao Zhong</div>
      <div class="publication-conference"><span class="pub-venue">Communications in Statistics - Simulation and Computation, 2026</span> <a href="https://www.tandfonline.com/doi/abs/10.1080/03610918.2026.2635000" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, first author</div>
    </div>
  </div>

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper2.svg" alt="A New Logarithmic Multiplicative Distortion">
      <a href="https://onlinelibrary.wiley.com/doi/10.1002/sam.11708" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://onlinelibrary.wiley.com/doi/10.1002/sam.11708" target="_blank" rel="noopener">A New Logarithmic Multiplicative Distortion for Correlation Analysis</a>
      </div>
      <div class="publication-authors"><strong class="author-highlight">Siming Deng</strong>, Jun Zhang</div>
      <div class="publication-conference"><span class="pub-venue">Statistical Analysis and Data Mining, 2024</span> <a href="https://onlinelibrary.wiley.com/doi/10.1002/sam.11708" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, JCR: Q1, first author, Top Cited Article - WILEY 2025</div>
    </div>
  </div>

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper3.svg" alt="A Revisit to Pearson Correlation Coefficient">
      <a href="https://www.tandfonline.com/doi/full/10.1080/03610918.2024.2333352" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://www.tandfonline.com/doi/full/10.1080/03610918.2024.2333352" target="_blank" rel="noopener">A Revisit to Pearson Correlation Coefficient under Multiplicative Distortions</a>
      </div>
      <div class="publication-authors"><strong class="author-highlight">Siming Deng</strong>, Jun Zhang, Yingcong Huang, Jiongtao Zhong & Xiaozhen Yang</div>
      <div class="publication-conference"><span class="pub-venue">Communications in Statistics - Simulation and Computation, 2024</span> <a href="https://www.tandfonline.com/doi/full/10.1080/03610918.2024.2333352" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, first author, Highly Cited Paper - Web of Science</div>
    </div>
  </div>

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper4.svg" alt="Covariance Ratio under Multiplicative Distortion">
      <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2295240" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2295240" target="_blank" rel="noopener">Covariance Ratio under Multiplicative Distortion Measurement Errors</a>
      </div>
      <div class="publication-authors">Jiongtao Zhong, <strong class="author-highlight">Siming Deng</strong>, Jun Zhang & Zhenghui Feng</div>
      <div class="publication-conference"><span class="pub-venue">Communications in Statistics - Theory and Methods, 2023</span> <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2295240" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, 2nd-author</div>
    </div>
  </div>

  <div class="publication-card">
    <div class="publication-thumb">
      <img src="/images/papers/paper5.svg" alt="Estimation of Correlation Coefficient">
      <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2288794" class="publication-overlay" target="_blank" rel="noopener">
        <span>View Paper</span>
      </a>
    </div>
    <div class="publication-info">
      <div class="publication-title">
        <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2288794" target="_blank" rel="noopener">Estimation of Correlation Coefficient with Monotone Transformation and Multiplicative Distortions</a>
      </div>
      <div class="publication-authors">Jun Zhang, Xuan Yu, <strong class="author-highlight">Siming Deng</strong>, Jiongtao Zhong, Yisheng Zhou & Bingqing Lin</div>
      <div class="publication-conference"><span class="pub-venue">Communications in Statistics - Theory and Methods, 2023</span> <a href="https://www.tandfonline.com/doi/full/10.1080/03610926.2023.2288794" target="_blank">[paper]</a></div>
      <div class="publication-details">SCI, 3rd-author</div>
    </div>
  </div>

</div>

<script>
(function() {
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-in');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.08, rootMargin: '0px 0px -40px 0px' });
    document.querySelectorAll('.publication-card').forEach(function(card) {
      observer.observe(card);
    });
  } else {
    document.querySelectorAll('.publication-card').forEach(function(card) {
      card.classList.add('animate-in');
    });
  }
})();
</script>

---

## Research Interests

- ML Systems & AI Infrastructure
- Efficient & On-Device Inference (Apple MLX, SGLang)
- Agentic AI (multi-agent orchestration & tool use)
- Machine Learning
- Nonparametric Statistics

I currently work at the intersection of **AI infrastructure and applied ML**, building agent runtimes and optimizing LLM inference.

Previously, my research centered on **nonparametric statistics** and **measurement-error modeling**, unobservable-variable estimation under multiplicative distortion frameworks, where I developed calibration methods and simulation studies to improve correlation-coefficient estimation in complex industrial settings, resulting in five SCI publications.
<img src="/images/hangzhou.jpg">

---

## News and Updates

<div class="news-grid">
  <div class="news-card news-card--publication">
    <div class="news-meta">
      <span class="news-date">February 2026</span>
      <span class="news-tag news-tag--publication">Publication</span>
    </div>
    <p>First-Author Paper: <a href="https://www.tandfonline.com/doi/abs/10.1080/03610918.2026.2635000"><strong>Innovative covariance-based framework: symmetry assessment and exponentiality testing under multiplicative distortion measurement Errors</strong></a> Now Officially Published in <a href="https://www.tandfonline.com/journals/lssp20">Communications in Statistics - Simulation and Computation</a></p>
  </div>

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">Jan 2026</span>
      <span class="news-tag news-tag--milestone">Milestone</span>
    </div>
    <p>Excited to have received an offer from Apple!</p>
  </div>

  <div class="news-card news-card--milestone">
    <div class="news-meta">
      <span class="news-date">March 2025</span>
      <span class="news-tag news-tag--milestone">Milestone</span>
    </div>
    <p>Thrilled to have received an offer from UPenn Engineering!</p>
  </div>

  <div class="news-card news-card--publication">
    <div class="news-meta">
      <span class="news-date">August 2024</span>
      <span class="news-tag news-tag--publication">Publication</span>
    </div>
    <p>First-Author Paper: <a href="https://onlinelibrary.wiley.com/doi/10.1002/sam.11708"><strong>A New Logarithmic Multiplicative Distortion for Correlation Analysis</strong></a> Now Officially Published in <a href="https://onlinelibrary.wiley.com/journal/19321872">Statistical Analysis and Data Mining</a> (JCR Q1)</p>
  </div>
</div>

<script>
(function() {
  if ('IntersectionObserver' in window) {
    var observer = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-in');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.08, rootMargin: '0px 0px -60px 0px' });
    document.querySelectorAll('.news-card').forEach(function(card) {
      observer.observe(card);
    });
  } else {
    document.querySelectorAll('.news-card').forEach(function(card) {
      card.classList.add('animate-in');
    });
  }
})();
</script>
