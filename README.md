<!DOCTYPE html>
<html lang="en-US">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resume - Marco Lucas Casserone</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a365d;
            --secondary: #2d3748;
            --accent: #3182ce;
            --bg: #f8fafc;
            --white: #ffffff;
            --text: #1a202c;
            --light-text: #4a5568;
            --border: #e2e8f0;
            --line-subtle: rgba(0, 0, 0, 0.05);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.5;
            color: var(--text);
            background-color: var(--bg);
            padding: 20px;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            background: var(--white);
            display: grid;
            grid-template-columns: 320px 1fr;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
            min-height: 100vh;
        }

        /* Sidebar */
        aside {
            background-color: #f1f5f9;
            color: var(--text);
            padding: 40px 30px;
            border-right: 1px solid var(--border);
        }

        .sidebar-section {
            margin-bottom: 35px;
            page-break-inside: avoid;
        }

        .sidebar-section h2 {
            font-size: 1.1rem;
            color: var(--primary);
            text-transform: uppercase;
            letter-spacing: 1.2px;
            margin-bottom: 15px;
            border-bottom: 2px solid var(--accent);
            padding-bottom: 5px;
        }

        .contact-list {
            list-style: none;
            font-size: 0.9rem;
        }

        .contact-list li {
            margin-bottom: 10px;
            word-wrap: break-word;
        }

        .contact-list a {
            color: var(--accent);
            text-decoration: none;
        }

        .skill-category {
            margin-bottom: 20px;
        }

        .skill-category h3 {
            font-size: 0.85rem;
            color: var(--light-text);
            text-transform: uppercase;
            margin-bottom: 8px;
        }

        .skill-list {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
        }

        .skill-list li {
            font-size: 0.8rem;
            background: var(--white);
            border: 1px solid var(--border);
            padding: 4px 10px;
            border-radius: 4px;
            color: var(--secondary);
        }

        /* Main Content */
        main {
            padding: 50px;
            background-color: var(--white);
        }

        header {
            margin-bottom: 40px;
            page-break-after: avoid;
        }

        h1 {
            font-size: 2.8rem;
            color: var(--primary);
            line-height: 1.1;
            margin-bottom: 8px;
        }

        .target-position {
            font-size: 1.4rem;
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 15px;
        }

        .summary-box {
            background: #f8fafc;
            padding: 20px;
            border-left: 4px solid var(--primary);
            margin-bottom: 40px;
            page-break-inside: avoid;
        }

        section {
            margin-bottom: 45px;
        }

        h2.section-title {
            font-size: 1.3rem;
            color: var(--primary);
            text-transform: uppercase;
            letter-spacing: 1px;
            border-bottom: 1px solid var(--border);
            padding-bottom: 8px;
            margin-bottom: 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            page-break-after: avoid;
        }

        .experience-item {
            margin-bottom: 35px;
            position: relative;
            page-break-inside: avoid;
        }

        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            margin-bottom: 8px;
            page-break-after: avoid;
        }

        .company {
            font-size: 1.2rem;
            font-weight: 800;
            color: var(--text);
        }

        .date-location {
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--light-text);
        }

        .role {
            display: block;
            font-size: 1.05rem;
            font-weight: 600;
            color: var(--accent);
            margin-bottom: 12px;
        }

        .bullet-list {
            list-style: none;
            padding-left: 5px;
        }

        .bullet-list > li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 10px;
            font-size: 0.95rem;
            color: var(--secondary);
            text-align: justify;
        }

        .bullet-list > li::before {
            content: "•";
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
        }

        .sub-bullets {
            list-style: none;
            margin-top: 5px;
            padding-left: 15px;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .sub-bullets li {
            font-size: 0.8rem;
            color: var(--light-text);
            background: var(--bg);
            padding: 2px 8px;
            border-radius: 3px;
        }

        .metrics-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-top: 20px;
        }

        .metric-card {
            border: 1px solid var(--border);
            padding: 28px 20px;
            border-radius: 8px;
            text-align: center;
            background: #fafbfc;
        }

        .metric-card:hover {
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .metric-value {
            display: block;
            font-size: 2.2rem;
            font-weight: 800;
            color: var(--accent);
            margin-bottom: 10px;
        }

        .metric-label {
            font-size: 0.8rem;
            text-transform: uppercase;
            color: var(--primary);
            font-weight: 700;
            letter-spacing: 0.5px;
            margin-bottom: 12px;
        }

        .metric-description {
            font-size: 0.85rem;
            color: var(--light-text);
            line-height: 1.4;
        }

        .cert-item {
            margin-bottom: 15px;
            page-break-inside: avoid;
        }

        .cert-title {
            font-weight: 700;
            color: var(--secondary);
        }

        .cert-details {
            font-size: 0.85rem;
            color: var(--light-text);
            display: block;
        }

        /* Utilities */
        .text-highlight { color: var(--primary); font-weight: 700; }

        /* Responsive */
        @media (max-width: 1024px) {
            .metrics-grid { grid-template-columns: repeat(2, 1fr); }
        }

        @media (max-width: 900px) {
            .container { grid-template-columns: 1fr; }
            aside { border-right: none; border-bottom: 1px solid var(--border); }
            main { padding: 30px; }
            .metrics-grid { grid-template-columns: 1fr; }
        }

        @media print {
            * { 
                box-shadow: none !important; 
                transition: none !important;
            }
            
            html, body { 
                background: white; 
                padding: 0;
                margin: 0;
                font-size: 10pt;
                height: auto;
                overflow: visible;
            }
            
            .container { 
                max-width: 100%;
                margin: 0;
                box-shadow: none; 
                grid-template-columns: 260px 1fr;
                min-height: auto;
                page-break-after: avoid;
                height: auto;
            }
            
            aside { 
                background: white;
                padding: 30px 20px;
                border-right: 2px solid #000;
                max-height: none;
                overflow: visible;
                height: auto;
            }
            
            main { 
                padding: 30px 25px;
                background: white;
                max-height: none;
                overflow: visible;
                height: auto;
            }
            
            header { margin-bottom: 20px; }
            
            h1 { 
                font-size: 1.8rem;
                margin-bottom: 4px;
            }
            
            .target-position { 
                font-size: 1rem;
                margin-bottom: 10px;
            }
            
            .summary-box { 
                background: white;
                border: 1px solid #000;
                border-left: 3px solid #000;
                padding: 15px;
                margin-bottom: 25px;
                page-break-inside: avoid;
            }
            
            section { 
                margin-bottom: 20px;
                page-break-inside: avoid;
            }
            
            h2.section-title {
                font-size: 1rem;
                margin-bottom: 15px;
                padding-bottom: 5px;
                border-bottom: 1px solid #000;
            }
            
            .experience-item {
                margin-bottom: 18px;
                page-break-inside: avoid;
            }
            
            .company {
                font-size: 1rem;
            }
            
            .role {
                font-size: 0.9rem;
                margin-bottom: 8px;
            }
            
            .bullet-list > li {
                font-size: 0.85rem;
                margin-bottom: 6px;
                text-align: left;
            }
            
            .metrics-grid { 
                grid-template-columns: repeat(3, 1fr);
                gap: 12px;
                margin-top: 15px;
            }
            
            .metric-card {
                background: white;
                border: 1px solid #000;
                padding: 15px 12px;
                border-radius: 0;
                page-break-inside: avoid;
            }
            
            .metric-value {
                font-size: 1.4rem;
                margin-bottom: 6px;
            }
            
            .metric-label {
                font-size: 0.7rem;
                margin-bottom: 6px;
            }
            
            .metric-description {
                font-size: 0.75rem;
            }
            
            .sidebar-section { margin-bottom: 25px; }
            
            .sidebar-section h2 {
                font-size: 0.85rem;
                margin-bottom: 10px;
                border-bottom: 1px solid #000;
            }
            
            .contact-list {
                font-size: 0.8rem;
            }
            
            .contact-list li {
                margin-bottom: 6px;
            }
            
            .contact-list a {
                color: #000;
                text-decoration: underline;
            }
            
            .sub-bullets li { 
                background: white;
                border: 1px solid #000;
                font-size: 0.7rem;
                padding: 2px 6px;
            }
            
            .cert-item {
                margin-bottom: 12px;
                page-break-inside: avoid;
            }
            
            .cert-title {
                font-size: 0.9rem;
                margin-bottom: 4px;
            }
            
            .cert-details {
                font-size: 0.8rem;
            }
            
            /* Competência badges - otimizado para print */
            div[style*="display: flex; flex-wrap: wrap"] {
                page-break-inside: avoid;
            }
            
            span[style*="padding: 6px 12px"] {
                font-size: 0.75rem;
                padding: 4px 8px !important;
                border-radius: 0;
            }
            
            /* Palavras-chave */
            #keywords-section {
                font-size: 0.8rem;
                column-count: 2;
                column-gap: 15px;
            }
            
            /* Avoid page breaks */
            .experience-header {
                page-break-inside: avoid;
            }
            
            /* Print-specific color scheme - high contrast */
            body { color: #000; }
            var(--text) { color: #000; }
            var(--light-text) { color: #333; }
        }
    </style>
</head>
<body>

<div class="container">
    <aside role="complementary">
        <section class="sidebar-section">
            <h2>Contact</h2>
            <ul class="contact-list">
                <li>📍 Brooklin, São Paulo – SP</li>
                <li>📞 <a href="tel:+5511947639729">(11) 94763-9729</a></li>
                <li>📧 <a href="mailto:marcolucascasserone@gmail.com">marcolucascasserone@gmail.com</a></li>
                <li>🔗 <a href="https://linkedin.com/in/lucascasserone" target="_blank" rel="noopener">linkedin.com/in/lucascasserone</a></li>
            </ul>
        </section>

        <section class="sidebar-section">
            <h2>Languages</h2>
            <ul class="contact-list">
                <li><strong>Portuguese:</strong> Native</li>
                <li><strong>English:</strong> Professional Fluency</li>
                <li><strong>Spanish:</strong> Professional</li>
            </ul>
        </section>
    </aside>

    <main role="main">
        <header>
            <h1>Marco Lucas Casserone</h1>
            <p class="target-position">Planning & Business Intelligence Leadership</p>
        </header>

        <section class="summary">
            <div class="summary-box">
                <p>
                    Planning & Business Intelligence leader with expertise in <span class="text-highlight">business acumen, data-driven decision making (enterprise-level architectures like Datalake) and leading multidisciplinary teams</span>. Solid background in <span class="text-highlight">Manufacturing, Financial Services, and Retail (On/Off)</span>, orchestrating analytics transformations that delivered direct impact: <span class="text-highlight">+12 p.p. forecast accuracy improvement</span>, <span class="text-highlight">-40% in analysis cycles</span>, and <span class="text-highlight">$2B+ USD in managed revenue</span>. Expert in <span class="text-highlight">Processes, Projects, and Systems</span> and <span class="text-highlight">Revenue and Digital Management</span>, focused on strategic value delivery and continuous optimization.
                </p>
            </div>
        </section>

        <section>
            <h2 class="section-title">Consolidated Results</h2>
            <div class="metrics-grid">
                <div class="metric-card">
                    <span class="metric-value">$2B+</span>
                    <span class="metric-label">Managed Revenue</span>
                    <span class="metric-description">Pricing, demand, and supply chain strategies under analytics intelligence.</span>
                </div>
                <div class="metric-card">
                    <span class="metric-value">+12 p.p.</span>
                    <span class="metric-label">MAPE Forecast</span>
                    <span class="metric-description">Gain in forecast accuracy for demand planning and budgeting.</span>
                </div>
                <div class="metric-card">
                    <span class="metric-value">-40%</span>
                    <span class="metric-label">Analytics Cycle Time</span>
                    <span class="metric-description">Reduction in analysis cycles via automation, DW/Lake, and D+0 governance.</span>
                </div>
                <div class="metric-card">
                    <span class="metric-value">-15%</span>
                    <span class="metric-label">Stock Outages</span>
                    <span class="metric-description">Increased availability and supply efficiency via intelligent algorithms.</span>
                </div>
                <div class="metric-card">
                    <span class="metric-value">20h/mo</span>
                    <span class="metric-label">Automation</span>
                    <span class="metric-description">Hours recovered via elimination of manual processes and optimized ETL.</span>
                </div>
                <div class="metric-card">
                    <span class="metric-value">D+0</span>
                    <span class="metric-label">KPI Monitoring</span>
                    <span class="metric-description">Real-time access to critical metrics via scalable, governed infrastructure.</span>
                </div>
            </div>
        </section>

        <section>
            <h2 class="section-title">Professional Experience</h2>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Avenida</span>
                    <span class="date-location">Sep/2025 – Present | São Paulo</span>
                </div>
                <span class="role">Planner</span>
                <ul class="bullet-list">
                    <li>Orchestrated <span class="text-highlight">D+0 commercial planning for strategic demand</span> via predictive AI and econometric modeling, structuring automation pipeline with Power Automate.</li>
                    <li>Implemented <span class="text-highlight">+12 p.p. accuracy improvement</span> in demand forecasting by refining forecasting models and establishing data governance.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Electrolux Group</span>
                    <span class="date-location">Jun/2023 – Apr/2025 | São Paulo</span>
                </div>
                <span class="role">BI & Digital Supervisor</span>
                <ul class="bullet-list">
                    <li>Led complete digital transformation with <span class="text-highlight">30% reduction in dashboard delivery time</span> via Azure/Power BI pipeline standardization and Agile methodology.</li>
                    <li>Managed data governance by structuring <span class="text-highlight">D+0 monitoring</span> of critical KPIs, aligning 5+ global multidisciplinary teams.</li>
                    <li>Built <span class="text-highlight">20+ executive dashboards</span> reducing strategic decision cycle by <span class="text-highlight">-40%</span>.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Electrolux Group</span>
                    <span class="date-location">Jul/2022 – Jun/2023 | São Paulo</span>
                </div>
                <span class="role">BI & Digital Specialist</span>
                <ul class="bullet-list">
                    <li>Developed BI solutions ecosystem in Power BI/DAX accelerating <span class="text-highlight">insight access from D+1 to D+0</span>, integrating Azure Data Lake and GCP BigQuery.</li>
                    <li>Mentored <span class="text-highlight">6+ analysts</span> establishing dimensional modeling practices and DAX performance optimization.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Banco Safra</span>
                    <span class="date-location">Aug/2021 – Jul/2022 | São Paulo</span>
                </div>
                <span class="role">Sr. BI Analyst — Digital Performance</span>
                <ul class="bullet-list">
                    <li>Built analytics ecosystem for apps/web capturing <span class="text-highlight">+15% conversion improvement</span> via advanced Web Analytics (Adobe Analytics, GCP BigQuery).</li>
                    <li>Led attribution and sales funnel studies optimizing digital marketing investment with <span class="text-highlight">ROAS +18%</span>.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Carrefour</span>
                    <span class="date-location">Sep/2020 – Aug/2021 | São Paulo</span>
                </div>
                <span class="role">Sr. BI Analyst — Digital</span>
                <ul class="bullet-list">
                    <li>Automated <span class="text-highlight">20+ ETL workflows</span> with SQL/Python/Alteryx eliminating <span class="text-highlight">20 hours/month</span> of manual work and reducing errors by <span class="text-highlight">-95%</span>.</li>
                    <li>Integrated SAP + digital sources building <span class="text-highlight">360° customer view</span>, accelerating consumption trend identification by <span class="text-highlight">-30% time</span>.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Lojas Eskala</span>
                    <span class="date-location">Jul/2019 – Aug/2020 | São Paulo</span>
                </div>
                <span class="role">Sr. Commercial Planning Analyst</span>
                <ul class="bullet-list">
                    <li>Created intelligent allocation algorithms reducing stock outages by <span class="text-highlight">-15%</span> and increasing seasonal turnover by <span class="text-highlight">+22%</span>.</li>
                    <li>Implemented performance monitoring across <span class="text-highlight">80+ store clusters</span>, triggering regionalized campaigns with <span class="text-highlight">+8% margin improvement</span>.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Lojas Eskala</span>
                    <span class="date-location">Sep/2018 – Jul/2019 | São Paulo</span>
                </div>
                <span class="role">Commercial Planning Analyst</span>
                <ul class="bullet-list">
                    <li>Developed automatic inventory allocation algorithms increasing distribution accuracy by <span class="text-highlight">+18%</span> across <span class="text-highlight">critical assortment clusters</span>.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">SKY Brasil</span>
                    <span class="date-location">Jul/2018 – Sep/2018 | São Paulo</span>
                </div>
                <span class="role">Jr. Data Intelligence Analyst</span>
                <ul class="bullet-list">
                    <li>Monitored <span class="text-highlight">12+ marketing dashboards</span> capturing daily insights for campaign optimization and digital engagement growth.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Anahp</span>
                    <span class="date-location">Feb/2018 – Jul/2018 | São Paulo</span>
                </div>
                <span class="role">Intern</span>
                <ul class="bullet-list">
                    <li>Structured SQL hospital productivity analyses and clinical dashboards supporting bed optimization and operational cost reduction of <span class="text-highlight">-12%</span>.</li>
                </ul>
            </article>

            <article class="experience-item">
                <div class="experience-header">
                    <span class="company">Lojas Marisa</span>
                    <span class="date-location">Sep/2017 – Feb/2018 | São Paulo</span>
                </div>
                <span class="role">Planning Intern</span>
                <ul class="bullet-list">
                    <li>Produced sales performance and product mix analyses identifying <span class="text-highlight">repositioning opportunities</span> across <span class="text-highlight">7 critical retail points</span>.</li>
                </ul>
            </article>
        </section>

        <section>
            <h2 class="section-title">Education</h2>
            <div class="experience-header">
                <span class="company">Production Engineering (Bachelor's Degree)</span>
                <span class="date-location">2015 – 2020</span>
            </div>
            <p>Pontifícia Universidade Católica de São Paulo (PUC-SP)</p>
        </section>

        <section>
            <h2 class="section-title">Certifications & Specializations</h2>
            
            <p style="font-size: 0.9rem; color: var(--light-text); margin-bottom: 20px; line-height: 1.6;">
                Strategic formation in analytical leadership, <span class="text-highlight">AI applied to retail</span> and corporate operations automation. 
                Certifications aligned with data-driven decision making, digital transformation, and team scalability.
            </p>

            <!-- AI APPLIED TO BUSINESS -->
            <div style="margin-bottom: 26px;">
                <h3 style="font-size: 0.95rem; font-weight: 700; color: var(--primary); margin-bottom: 14px;">🤖 AI Applied to Business</h3>
                
                <div class="cert-item" style="margin-bottom: 14px;">
                    <span class="cert-title">Advanced AI Agents (2026)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>Bain & Company</i> — Implement intelligent agents and <strong>LLMs</strong> for automating analytical workflows and autonomous decision-making.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#LLMs</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Automation</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#GenerativeAI</span>
                    </span>
                </div>

                <div class="cert-item">
                    <span class="cert-title">Machine Learning & NLP (2021)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>USP</i> — Build <strong>Machine Learning</strong> models and natural language processing for consumer insights.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#MachineLearning</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#NLP</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#PredictiveModels</span>
                    </span>
                </div>
            </div>

            <!-- DATA & ANALYTICS -->
            <div style="margin-bottom: 26px;">
                <h3 style="font-size: 0.95rem; font-weight: 700; color: var(--primary); margin-bottom: 14px;">📊 Data & Analytics</h3>
                
                <div class="cert-item" style="margin-bottom: 14px;">
                    <span class="cert-title">Data Engineer (2023)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>DIO</i> — Architect scalable data pipelines <strong>(DW/Lake)</strong> for real-time corporate analytics.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#DataEngineering</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#ETL</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#CloudArchitecture</span>
                    </span>
                </div>

                <div class="cert-item">
                    <span class="cert-title">Power BI Advanced for Analytics (2020)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>Data Science Academy</i> — Design executive dashboards with advanced <strong>DAX</strong> for decision-making.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#PowerBI</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#DAX</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#ExecutiveDashboards</span>
                    </span>
                </div>
            </div>

            <!-- LEADERSHIP AND MANAGEMENT -->
            <div style="margin-bottom: 26px;">
                <h3 style="font-size: 0.95rem; font-weight: 700; color: var(--primary); margin-bottom: 14px;">🎯 Leadership and Management</h3>
                
                <div class="cert-item" style="margin-bottom: 14px;">
                    <span class="cert-title">Projects and Team Management (2026)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>Santander Open Academy</i> — Coordinate complex projects and multidisciplinary teams for value delivery and high performance.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Leadership</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#ProjectManagement</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#HighPerformance</span>
                    </span>
                </div>

                <div class="cert-item" style="margin-bottom: 14px;">
                    <span class="cert-title">Change Management (2025)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>PUCRS</i> — Lead organizational transformations focusing on cultural change and process adoption.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#CulturalChange</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Transformation</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#StakeholderMgmt</span>
                    </span>
                </div>

                <div class="cert-item">
                    <span class="cert-title">Crisis Management (2025)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>FAAP</i> — Manage critical situations with quick response and mitigation of operational risks.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#CrisisManager</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#RiskMitigation</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#InternalControl</span>
                    </span>
                </div>
            </div>

            <!-- AGILE METHODOLOGIES -->
            <div style="margin-bottom: 26px;">
                <h3 style="font-size: 0.95rem; font-weight: 700; color: var(--primary); margin-bottom: 14px;">⚡ Agile Methodologies</h3>
                
                <div class="cert-item" style="margin-bottom: 14px;">
                    <span class="cert-title">Professional Scrum Specialist (2025)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>FM2S</i> — Master advanced <strong>Scrum</strong> frameworks to maximize agility and continuous value delivery.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Scrum</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Agile</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#ContinuousDelivery</span>
                    </span>
                </div>

                <div class="cert-item" style="margin-bottom: 14px;">
                    <span class="cert-title">Scrum Master Certified (2022)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>Exin</i> — Facilitate <strong>Scrum</strong> ceremonies and remove impediments to optimize delivery cycles.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#ScrumMaster</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Facilitation</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Retrospectives</span>
                    </span>
                </div>

                <div class="cert-item">
                    <span class="cert-title">Scrum Fundamentals Certified (2021)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>VMEdu / Vtutor</i> — Apply fundamental agility principles in corporate projects.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#ScrumFundamentals</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Iterations</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Collaboration</span>
                    </span>
                </div>
            </div>

            <!-- AUTOMATION AND SCRIPTING -->
            <div style="margin-bottom: 26px;">
                <h3 style="font-size: 0.95rem; font-weight: 700; color: var(--primary); margin-bottom: 14px;">💻 Automation and Scripting</h3>
                
                <div class="cert-item">
                    <span class="cert-title">Python for Data Science & ML (2020)</span>
                    <span class="cert-details" style="display: block; margin-bottom: 6px;"><i>Udemy</i> — Program in <strong>Python</strong> for ETL, exploratory analysis, and building predictive models.</span>
                    <span style="font-size: 0.8rem; color: var(--accent); display: flex; flex-wrap: wrap; gap: 8px; margin-top: 4px;">
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Python</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#ETL</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#DataScience</span>
                        <span style="background: rgba(49, 130, 206, 0.1); padding: 3px 8px; border-radius: 3px;">#Automation</span>
                    </span>
                </div>
            </div>

            <!-- CERTIFIED TECHNICAL HIGHLIGHTS -->
            <div style="background: #f8fafc; border-left: 4px solid var(--accent); padding: 18px; border-radius: 4px; margin-top: 28px;">
                <h3 style="font-size: 0.95rem; font-weight: 700; color: var(--primary); margin-bottom: 12px;">✓ Certified Technical Highlights</h3>
                <ul style="list-style: none; padding: 0; font-size: 0.9rem; color: var(--secondary); line-height: 1.7;">
                    <li style="padding-left: 20px; position: relative; margin-bottom: 8px;">
                        <span style="position: absolute; left: 0; color: var(--accent); font-weight: 600;">▸</span>
                        Data architecture and <strong>ETL</strong> pipelines for real-time decision support <strong>(D+0)</strong>
                    </li>
                    <li style="padding-left: 20px; position: relative; margin-bottom: 8px;">
                        <span style="position: absolute; left: 0; color: var(--accent); font-weight: 600;">▸</span>
                        Predictive modeling and <strong>AI applied</strong> to Revenue Management and Demand Planning
                    </li>
                    <li style="padding-left: 20px; position: relative; margin-bottom: 8px;">
                        <span style="position: absolute; left: 0; color: var(--accent); font-weight: 600;">▸</span>
                        Leadership of digital transformation in multidisciplinary and global contexts
                    </li>
                    <li style="padding-left: 20px; position: relative; margin-bottom: 8px;">
                        <span style="position: absolute; left: 0; color: var(--accent); font-weight: 600;">▸</span>
                        Automation of analytical workflows with <strong>Python</strong>, <strong>Power BI</strong>, and intelligent agents
                    </li>
                    <li style="padding-left: 20px; position: relative;">
                        <span style="position: absolute; left: 0; color: var(--accent); font-weight: 600;">▸</span>
                        Excellence in <strong>Scrum</strong> framework for continuous value delivery in strategic projects
                    </li>
                </ul>
            </div>
        </section>

        <section>
            <h2 class="section-title">Keywords (ATS)</h2>
            <p id="keywords-section" style="font-size: 0.85rem; color: var(--light-text); font-style: italic; line-height: 1.8;">
                Business Intelligence Strategy | BI Leader | Head of Analytics | Head of Data | Analytics Leader | Data Strategy | Data Governance | Data Architecture | Lakehouse | Data Warehouse (DW) | Real-time Analytics | D+0 Monitoring | ETL Pipeline | Revenue Management | Demand Planning | Forecasting | Accuracy Improvement | Marketing Analytics | Sales Analytics | Attribution Modeling | Web Analytics | Supply Chain Analytics | Stakeholder Management | Team Leadership | Business Partnership | Cross-functional Collaboration | Change Management | Crisis Management | Transformation Leadership | Agile / Scrum | Project Management | Agentic AI | Machine Learning | Predictive Modeling | NLP | Workflow Automation | RPA | Optimization Algorithms | Power BI | SQL | Python | DAX | Azure Data Lake | GCP BigQuery | SAP | Oracle Retail | Data-Driven Decision Making | KPI Management | Digital Transformation | Performance Digital | Financial Analytics | Mentoring | High-Performance Teams | Change Management Certification | AI Certification | Scrum Master | Professional Scrum Specialist.
            </p>
        </section>

        <section>
            <h2 class="section-title">Technical & Management Competencies (ATS)</h2>
            
            <!-- DATA STRATEGY & BI -->
            <div style="margin-bottom: 32px;">
                <h3 style="font-size: 1rem; font-weight: 700; color: var(--primary); margin-bottom: 12px; text-transform: uppercase; letter-spacing: 0.5px;">📊 Data Strategy & BI</h3>
                <p style="font-size: 0.9rem; color: var(--light-text); margin-bottom: 12px;">Design of scalable architectures (DW/Lakehouse), D+0 data governance and BI ecosystems for supporting strategic decision-making at executive level.</p>
                <div style="display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 10px;">
                    <span style="background: #e6f3ff; border: 1px solid #3182ce; color: #1a365d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Data Architecture (DW/Lakehouse)</span>
                    <span style="background: #e6f3ff; border: 1px solid #3182ce; color: #1a365d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Real-time Analytics (D+0)</span>
                    <span style="background: #e6f3ff; border: 1px solid #3182ce; color: #1a365d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Data Governance & Lineage</span>
                    <span style="background: #e6f3ff; border: 1px solid #3182ce; color: #1a365d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">ETL/ELT Pipeline Design</span>
                    <span style="background: #e6f3ff; border: 1px solid #3182ce; color: #1a365d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Financial & Demand Analytics</span>
                </div>
                <p style="font-size: 0.8rem; color: var(--accent); font-weight: 600;">Impact: -40% in analysis cycle | D+0 in KPI monitoring | Forecast accuracy +12 p.p.</p>
            </div>

            <!-- MARKETING & SALES ANALYTICS -->
            <div style="margin-bottom: 32px;">
                <h3 style="font-size: 1rem; font-weight: 700; color: var(--primary); margin-bottom: 12px; text-transform: uppercase; letter-spacing: 0.5px;">📈 Marketing & Sales Analytics</h3>
                <p style="font-size: 0.9rem; color: var(--light-text); margin-bottom: 12px;">Optimization of sales funnel, advanced web analytics, revenue management and econometric modeling to maximize ROI in campaigns and commercial operations.</p>
                <div style="display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 10px;">
                    <span style="background: #fff5e6; border: 1px solid #ed8936; color: #7c2d11; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Revenue Management</span>
                    <span style="background: #fff5e6; border: 1px solid #ed8936; color: #7c2d11; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Marketing Analytics & Attribution</span>
                    <span style="background: #fff5e6; border: 1px solid #ed8936; color: #7c2d11; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Web Analytics & Conversion</span>
                    <span style="background: #fff5e6; border: 1px solid #ed8936; color: #7c2d11; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Demand Planning & Forecasting</span>
                    <span style="background: #fff5e6; border: 1px solid #ed8936; color: #7c2d11; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Pricing Strategy & Elasticity</span>
                    <span style="background: #fff5e6; border: 1px solid #ed8936; color: #7c2d11; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Supply Chain Analytics</span>
                </div>
                <p style="font-size: 0.8rem; color: var(--accent); font-weight: 600;">Impact: $2B+ USD under management | +18% ROAS in campaigns | -15% stock outages | +22% seasonal turnover</p>
            </div>

            <!-- LEADERSHIP & BUSINESS PARTNERING -->
            <div style="margin-bottom: 32px;">
                <h3 style="font-size: 1rem; font-weight: 700; color: var(--primary); margin-bottom: 12px; text-transform: uppercase; letter-spacing: 0.5px;">👥 Leadership & Business Partnering</h3>
                <p style="font-size: 0.9rem; color: var(--light-text); margin-bottom: 12px;">Strategic IT/Business interface, alignment of multidisciplinary stakeholders (Marketing, Sales, Operations), talent management and translation of business demands into scalable solutions.</p>
                <div style="display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 10px;">
                    <span style="background: #f0fdf4; border: 1px solid #22c55e; color: #166534; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Stakeholder Management</span>
                    <span style="background: #f0fdf4; border: 1px solid #22c55e; color: #166534; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Team Leadership & Mentoring</span>
                    <span style="background: #f0fdf4; border: 1px solid #22c55e; color: #166534; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Cross-functional Collaboration</span>
                    <span style="background: #f0fdf4; border: 1px solid #22c55e; color: #166534; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Business Partnership Model</span>
                    <span style="background: #f0fdf4; border: 1px solid #22c55e; color: #166534; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">KPI Design & Monitoring</span>
                    <span style="background: #f0fdf4; border: 1px solid #22c55e; color: #166534; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Communication & Advocacy</span>
                </div>
                <p style="font-size: 0.8rem; color: var(--accent); font-weight: 600;">Impact: Leadership of 5+ global teams | Mentoring of 6+ analysts | 360° alignment in transformations</p>
            </div>

            <!-- AGILITY, PROJECTS & CHANGE -->
            <div style="margin-bottom: 32px;">
                <h3 style="font-size: 1rem; font-weight: 700; color: var(--primary); margin-bottom: 12px; text-transform: uppercase; letter-spacing: 0.5px;">⚡ Agility, Projects & Change</h3>
                <p style="font-size: 0.9rem; color: var(--light-text); margin-bottom: 12px;">Advanced Scrum certification, corporate crisis management, organizational transformation leadership, cultural change and risk mitigation in high-pressure contexts.</p>
                <div style="display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 10px;">
                    <span style="background: #faf5ff; border: 1px solid #a855f7; color: #581c87; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Scrum Master / Agile Leadership</span>
                    <span style="background: #faf5ff; border: 1px solid #a855f7; color: #581c87; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Change Management (PUCRS)</span>
                    <span style="background: #faf5ff; border: 1px solid #a855f7; color: #581c87; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Crisis Management & Continuity</span>
                    <span style="background: #faf5ff; border: 1px solid #a855f7; color: #581c87; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Transformation Leadership</span>
                    <span style="background: #faf5ff; border: 1px solid #a855f7; color: #581c87; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Project Management & PMO</span>
                    <span style="background: #faf5ff; border: 1px solid #a855f7; color: #581c87; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Risk Mitigation & Compliance</span>
                </div>
                <p style="font-size: 0.8rem; color: var(--accent); font-weight: 600;">Impact: Continuous delivery in agile cycles | -30% in analysis lead time | Digital transformation of 100+ users</p>
            </div>

            <!-- AI AND INTELLIGENT AUTOMATION -->
            <div style="margin-bottom: 32px;">
                <h3 style="font-size: 1rem; font-weight: 700; color: var(--primary); margin-bottom: 12px; text-transform: uppercase; letter-spacing: 0.5px;">🤖 AI & Intelligent Automation</h3>
                <p style="font-size: 0.9rem; color: var(--light-text); margin-bottom: 12px;">Certification in Advanced AI Agents (Bain & Company), predictive modeling, natural language processing, workflow automation and implementation of LLMs for autonomous decision-making.</p>
                <div style="display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 10px;">
                    <span style="background: #fef2f2; border: 1px solid #ef4444; color: #7f1d1d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Agentic AI & LLMs (Bain & Company)</span>
                    <span style="background: #fef2f2; border: 1px solid #ef4444; color: #7f1d1d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Machine Learning & Predictive Modeling</span>
                    <span style="background: #fef2f2; border: 1px solid #ef4444; color: #7f1d1d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">NLP & Text Analytics</span>
                    <span style="background: #fef2f2; border: 1px solid #ef4444; color: #7f1d1d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Workflow Automation</span>
                    <span style="background: #fef2f2; border: 1px solid #ef4444; color: #7f1d1d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Intelligent ETL & RPA</span>
                    <span style="background: #fef2f2; border: 1px solid #ef4444; color: #7f1d1d; padding: 6px 12px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Optimization Algorithms</span>
                </div>
                <p style="font-size: 0.8rem; color: var(--accent); font-weight: 600;">Impact: -95% in manual errors | 20 hours/month recovered | Intelligent allocation algorithms +18% accuracy</p>
            </div>

            <!-- PRIMARY TECHNOLOGY STACK -->
            <div style="background: #f8fafc; border-left: 4px solid var(--accent); padding: 20px; border-radius: 4px;">
                <h3 style="font-size: 1rem; font-weight: 700; color: var(--primary); margin-bottom: 14px; text-transform: uppercase; letter-spacing: 0.5px;">💻 Primary Technology Stack</h3>
                <div style="display: flex; flex-wrap: wrap; gap: 8px;">
                    <span style="background: var(--white); border: 1px solid var(--border); color: var(--text); padding: 8px 14px; border-radius: 4px; font-size: 0.9rem; font-weight: 600;">SQL (Advanced)</span>
                    <span style="background: var(--white); border: 1px solid var(--border); color: var(--text); padding: 8px 14px; border-radius: 4px; font-size: 0.9rem; font-weight: 600;">Power BI (Advanced DAX)</span>
                    <span style="background: var(--white); border: 1px solid var(--border); color: var(--text); padding: 8px 14px; border-radius: 4px; font-size: 0.9rem; font-weight: 600;">Python (ETL/ML)</span>
                    <span style="background: var(--white); border: 1px solid var(--border); color: var(--text); padding: 8px 14px; border-radius: 4px; font-size: 0.9rem; font-weight: 600;">Lakehouse & DW</span>
                    <span style="background: var(--white); border: 1px solid var(--border); color: var(--text); padding: 8px 14px; border-radius: 4px; font-size: 0.9rem; font-weight: 600;">Azure Data Lake</span>
                    <span style="background: var(--white); border: 1px solid var(--border); color: var(--text); padding: 8px 14px; border-radius: 4px; font-size: 0.9rem; font-weight: 600;">GCP BigQuery</span>
                    <span style="background: var(--white); border: 1px solid var(--border); color: var(--text); padding: 8px 14px; border-radius: 4px; font-size: 0.9rem; font-weight: 600;">SAP & Oracle Retail</span>
                    <span style="background: var(--white); border: 1px solid var(--border); color: var(--text); padding: 8px 14px; border-radius: 4px; font-size: 0.9rem; font-weight: 600;">Alteryx</span>
                </div>
            </div>
        </section>
    </main>
</div>

</body>
</html>
