---
title: "Group Members"
type: landing

design:
  spacing: "0"

sections:
  # ─────────────────────────────────────────────────────────
  # 0. GLOBAL STYLE (同步主页、Research、News 的全站视觉规范)
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      text: |
        <style>
          /* ===== 1. 框架间距与宽度修正 ===== */
          .blox-page-header, .main-content, main {
            padding-top: 0 !important;
            margin-top: 0 !important;
          }
          section.hbb-section {
            padding-top: 10px !important;
            padding-bottom: 10px !important;
          }
          .max-w-prose, .prose, .container, .mx-auto { 
            max-width: 100% !important; 
            width: 100% !important; 
          }
          .home-outer-wrapper {
            width: 95%;
            max-width: 1400px;
            margin: 0 auto;
            clear: both;
          }

          /* ===== 2. 导航栏标准化 (修正 SEISAD 显现和图标挤压问题) ===== */
          header, .page-header {
            background-color: #008a85 !important;
            padding: 0 !important;
          }
          
          /* 强制隐藏左侧所有的 Brand/Logo 文本 */
          .navbar-brand, .navbar-brand-mobile, .brand-logo {
            display: none !important;
          }
          
          .navbar {
            background-color: #008a85 !important;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1) !important;
            min-height: 60px;
            padding: 0 2rem !important; /* 给导航栏左右留出安全边距 */
          }
          
          /* 导航栏容器：使用 space-between 让中间菜单居中，两侧撑开 */
          .navbar > .container, .navbar > .container-xl {
            display: flex !important;
            justify-content: space-between !important; 
            max-width: 1400px !important; /* 与内容宽度一致 */
          }
          
          /* 中间菜单部分 */
          .navbar-collapse {
            flex-grow: 1 !important;
            display: flex !important;
            justify-content: center !important; /* 确保菜单项整体在中间 */
          }
          
          .navbar-nav {
            flex-direction: row !important;
            align-items: center !important;
          }
          
          .nav-item {
            display: flex !important;
            align-items: center !important;
          }
          
          .nav-link {
            color: #ffffff !important;
            font-weight: bold !important;
            font-size: 1.5rem !important; /* 稍微调小一点，防止在小屏幕挤压 */
            /* 关键：通过 padding 统一单词间的物理间距 */
            padding: 0 1.5rem !important; 
            transition: background-color 0.3s;
          }
          
          .nav-link:hover {
            background-color: rgba(255, 255, 255, 0.15) !important;
            border-radius: 4px;
          }
          
          /* 右侧图标部分 (搜索、月亮) */
          .navbar-nav-btns {
            display: flex !important;
            align-items: center !important;
            margin-left: 2rem !important; /* 强制与 "Contact" 保持距离 */
          }
          
          .navbar-nav-btns .nav-link {
            padding: 0 0.8rem !important; /* 图标之间的间距小一点 */
          }
          
          /* 针对移动端的微调：如果屏幕太小，隐藏图标或调整 */
          @media (max-width: 768px) {
            .nav-link { padding: 0 0.8rem !important; font-size: 0.9rem !important; }
          }

          /* ===== 3. 统一标题横条 ===== */
          .main-title-container {
            background-color: #f0f9f8;
            border-top: 6px solid #008a85;
            padding: 2.5rem 1.5rem;
            margin: 0.5rem 0 3rem 0;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.03);
            border-radius: 0 0 8px 8px;
          }
          .full-name {
            font-size: 1.5rem;
            font-weight: bold;
            color: #718096;
            text-transform: uppercase;
            letter-spacing: 2px;
            display: block;
            margin-bottom: 0.8rem;
          }
          .brand-name-bold {
            font-size: 2.6rem;
            color: #008a85;
            font-weight: 900;
            letter-spacing: 4px;
            line-height: 1;
          }

          /* ===== 4. Members 专用网格与卡片 ===== */
          .people-grid {
            display: grid;
            grid-template-columns: 1fr 1fr; 
            gap: 40px;
            margin-bottom: 50px;
          }
          .person-card {
            display: flex;
            align-items: flex-start;
            gap: 25px;
            background: #ffffff;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.06);
            border: 1px solid #eee;
            transition: transform 0.3s;
          }
          .person-card:hover { transform: translateY(-5px); }
          .person-img {
            width: 140px;
            height: 185px;
            object-fit: cover;
            border-radius: 8px;
            flex-shrink: 0;
            background: #f0f0f0;
          }
          .person-info { text-align: left; flex: 1; }
          .person-name { font-size: 1.5rem; font-weight: bold; color: #008a85; margin-bottom: 5px; }
          .person-title { font-style: italic; color: #555; font-size: 0.95rem; margin-bottom: 12px; border-bottom: 1px solid #eee; padding-bottom: 5px; }
          .person-bio { font-size: 0.9rem; line-height: 1.6; color: #444; margin-bottom: 15px; }
          .person-links { font-size: 0.85rem; }
          .person-links div { margin-bottom: 6px; display: flex; align-items: center; gap: 8px; }
          .person-links a { color: #008a85 !important; text-decoration: none; font-weight: 600; }
          .person-links a:hover { text-decoration: underline; }

          /* ===== 5. 全宽自定义页脚 ===== */
          .custom-footer-container {
            background-color: #008a85; 
            color: #ffffff;            
            padding: 1.5rem 0 !important; 
            width: 100vw;
            position: relative;
            left: 50%;
            right: 50%;
            margin-left: -50vw;
            margin-right: -50vw;
            margin-top: 60px;
            margin-bottom: -50px; 
          }
          .footer-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 40px; }
          .footer-column h3 {
            color: #ffffff !important;
            font-size: 1.1rem;
            margin-bottom: 1.2rem;
            font-weight: bold;
            border-bottom: 2px solid rgba(255,255,255,0.3);
            display: inline-block;
            padding-bottom: 5px;
          }
          .footer-column p, .footer-column li { font-size: 0.85rem; color: rgba(255,255,255,0.95) !important; }
          .footer-column a { color: #ffffff !important; text-decoration: underline; }

          /* 隐藏系统默认 */
          footer, .site-footer, .powered-by, .copyright { display: none !important; }

          @media (max-width: 1100px) {
            .people-grid { grid-template-columns: 1fr; }
            .footer-grid { grid-template-columns: 1fr; text-align: center; }
          }
        </style>

  # ─────────────────────────────────────────────────────────
  # 1. TITLE BAR (视觉一致性 + 解决贴顶问题)
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      text: |
        <div class="home-outer-wrapper">
          <div class="main-title-container">
            <span class="full-name">Our Research Team</span>
            <div class="brand-name-bold">GROUP MEMBERS</div>
          </div>
        </div>
    design:
      full_width: true

  # ─────────────────────────────────────────────────────────
  # 2. PERMANENT MEMBERS
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      text: |
        <style>
          .people-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr); /* This forces 2 columns */
            gap: 30px;
            width: 100%;
            margin: 0 auto;
          }
          .person-card {
            display: flex;
            flex-direction: row;
            align-items: flex-start;
            background: #fff;
            border: 1px solid #eee;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
          }
          .person-img {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            object-fit: cover;
            flex-shrink: 0;
            margin-right: 20px;
          }
          .person-info { padding: 0; }
          .person-name { font-weight: bold; font-size: 1.2rem; color: #333; }
          .person-title { color: #666; font-style: italic; font-size: 1.1rem; margin-bottom: 10px; }
          .person-bio { font-size: 1.1rem; margin-bottom: 15px; min-height: 40px; }
          .person-links { font-size: 1rem; line-height: 1.5; }         
          /* Responsive: Stack in 1 column on small mobile screens */
          @media (max-width: 600px) {
            .people-grid { grid-template-columns: 1fr; }
          }
        </style>
        <div class="home-outer-wrapper">
          <h2 style="text-align:center; color:#333; margin-bottom:40px; font-weight:900; text-transform:uppercase; letter-spacing:1px;">Permanent Members</h2>
          <div class="people-grid">
            <!-- Anne Varenne -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/xxx.jpg" class="person-img" alt="Anne Varenne">
              <div class="person-info">
                <div class="person-name">Prof. Anne Varenne</div>
                <div class="person-title">Head of SEISAD, Professor</div>
                <div class="person-bio">Electrochemistry and surface analysis.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:anne.varenne@chimieparistech.psl.eu">anne.varenne@chimieparistech.psl.eu</a></div>
                  <div><span>Tel:</span> +33 x xx xx xx xx</div>
                  <div><a href="https://scholar.google.com/citations?user=ndfeauUAAAAJ&hl=fr" target="_blank">Google Scholar</a></div>
                  <div><a href="/SEISAD_website/media/people/Anne-CV.pdf" target="_blank">CV (PDF)</a></div>
                </div>
              </div>
            </div>
            <!-- Zijun Wang -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/ZijunWang.jpg" class="person-img" alt="Zijun Wang">
              <div class="person-info">
                <div class="person-name">Dr. Zijun Wang</div>
                <div class="person-title">Junior Professor (CPJ)</div>
                <div class="person-bio">Luminescent nanomaterials and bioapplications.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:zijun.wang@chimieparistech.psl.eu">zijun.wang@chimieparistech.psl.eu</a></div>
                  <div><a href="https://scholar.google.com/citations?user=h7Bt-MkAAAAJ&hl=en" target="_blank">Google Scholar</a></div>
                  <div><a href="/SEISAD_website/media/people/Zijun-CV.pdf" target="_blank">CV (PDF)</a></div>
                </div>
              </div>
            </div>
            <!-- Row 2: Person 3 -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/placeholder.jpg" class="person-img" alt="Name">
              <div class="person-info">
                <div class="person-name">Member Name</div>
                <div class="person-title">Position Title</div>
                <div class="person-bio">Research interests and expertise description.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:email@domain.com">email@...</a></div>
                </div>
              </div>
            </div>
            <!-- Row 2: Person 4 -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/placeholder.jpg" class="person-img" alt="Name">
              <div class="person-info">
                <div class="person-name">Member Name</div>
                <div class="person-title">Position Title</div>
                <div class="person-bio">Research interests and expertise description.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:email@domain.com">email@...</a></div>
                </div>
              </div>
            </div>
            <!-- Row 3: Person 5 -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/placeholder.jpg" class="person-img" alt="Name">
              <div class="person-info">
                <div class="person-name">Member Name</div>
                <div class="person-title">Position Title</div>
                <div class="person-bio">Research interests and expertise description.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:email@domain.com">email@...</a></div>
                </div>
              </div>
            </div>
            <!-- Row 3: Person 6 -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/placeholder.jpg" class="person-img" alt="Name">
              <div class="person-info">
                <div class="person-name">Member Name</div>
                <div class="person-title">Position Title</div>
                <div class="person-bio">Research interests and expertise description.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:email@domain.com">email@...</a></div>
                </div>
              </div>
            </div>
            <!-- Row 4: Person 7 -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/placeholder.jpg" class="person-img" alt="Name">
              <div class="person-info">
                <div class="person-name">Member Name</div>
                <div class="person-title">Position Title</div>
                <div class="person-bio">Research interests and expertise description.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:email@domain.com">email@...</a></div>
                </div>
              </div>
            </div>
            <!-- Row 4: Person 8 -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/placeholder.jpg" class="person-img" alt="Name">
              <div class="person-info">
                <div class="person-name">Member Name</div>
                <div class="person-title">Position Title</div>
                <div class="person-bio">Research interests and expertise description.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:email@domain.com">email@...</a></div>
                </div>
              </div>
            </div>
          </div>
        </div>
    design:
      full_width: true

  # ─────────────────────────────────────────────────────────
  # 3. STUDENTS & RESEARCHERS
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      text: |
        <div class="home-outer-wrapper">
          <h2 style="text-align:center; color:#333; margin-bottom:40px; font-weight:900; text-transform:uppercase; letter-spacing:1px;">Students & Researchers</h2>
          <div class="people-grid">
            <!-- Matthieu Sagot -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/Matthieu Sagot.JPG" class="person-img" alt="Matthieu Sagot">
              <div class="person-info">
                <div class="person-name">Matthieu SAGOT</div>
                <div class="person-title">Postdoc</div>
                <div class="person-bio">Developing an all-in-one microfluidic analytical platform coupling an electrophoretic separation with a multi-parametric detection scheme (Fluorescence, UV, Raman, DLS) for the characterization of nanoplastics.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:matthieu.sagot@chimieparistech.psl.eu">matthieu.sagot@chimieparistech.psl.eu</a></div>
                  <div><a href="https://scholar.google.com/citations?user=idvRp8MAAAAJ&hl=fr" target="_blank">Google Scholar</a></div>
                  <div><a href="https://www.linkedin.com/in/matthieu-sagot-3497aa391/" target="_blank">LinkedIn Profile</a></div>
                </div>
              </div>
            </div>
             <!-- Xingyuan XU -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/XingyuanXu.png" class="person-img" alt="Xingyuan XU">
              <div class="person-info">
                <div class="person-name">Xingyuan Xu</div>
                <div class="person-title">PhD Student</div>
                <div class="person-bio">Leveraging natural language processing to recognize emotions in cancer patients and recommend personalized well-being advice.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:xingyuan.xu@chimieparistech.psl.eu">xingyuan.xu@chimieparistech.psl.eu</a></div>
                  <div><a href="https://www.linkedin.com/in/xingyuan-xu-a125293a9/" target="_blank">LinkedIn Profile</a></div>
                </div>
              </div>
            </div>
             <!-- Lucas Castro -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/XXX.png" class="person-img" alt="Lucas Castro">
              <div class="person-info">
                <div class="person-name">Lucas Castro</div>
                <div class="person-title">PhD Student</div>
                <div class="person-bio">Development of a multi-omics microfluidic platform integrating electrochemical cell lysis, proteolysis, and biomolecular separation for downstream analysis.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:lucas.castro@chimieparistech.psl.eu">lucas.castro@chimieparistech.psl.eu</a></div>
                </div>
              </div>
            </div>
             <!-- Lucas Castro -->
            <div class="person-card">
              <img src="/SEISAD_website/media/people/XXX.png" class="person-img" alt="XXX">
              <div class="person-info">
                <div class="person-name">XXX</div>
                <div class="person-title">PhD Student</div>
                <div class="person-bio">XXX.</div>
                <div class="person-links">
                  <div><span>Email:</span> <a href="mailto:XXX@chimieparistech.psl.eu">XXX@chimieparistech.psl.eu</a></div>
                </div>
              </div>
            </div>
          </div>
        </div>
    design:
      full_width: true
      background:
        color: "#f8fafc"

  # ─────────────────────────────────────────────────────────
  # 4. CUSTOM FOOTER (全站同步)
  # ─────────────────────────────────────────────────────────
  - block: markdown
    content:
      text: |
        <div class="custom-footer-container">
          <div class="home-outer-wrapper">
            <div class="footer-grid">
              <div class="footer-column">
                <h3>Address</h3>
                <p>Chimie ParisTech - PSL University<br>i-CLeHS (CNRS UMR 8060)<br>11 Rue Pierre et Marie Curie<br>75005 Paris, France</p>
              </div>
              <div class="footer-column">
                <h3>Contact</h3>
                <p>Tel: +33 1 XX XX XX XX<br>Email: <a href="mailto:contact@seisad.com">contact@seisad.com</a><br>Twitter: <a href="https://twitter.com/MakeOwnable" target="_blank">@MakeOwnable</a></p>
              </div>
              <div class="footer-column">
                <h3>Quick Links</h3>
                <ul style="list-style:none; padding:0;">
                  <li><a href="https://www.chimieparistech.psl.eu/" target="_blank">Chimie ParisTech</a></li>
                  <li><a href="https://www.cnrs.fr/" target="_blank">CNRS</a></li>
                  <li><a href="https://psl.eu/" target="_blank">PSL University</a></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
    design:
      full_width: true
---
