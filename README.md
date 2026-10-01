<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Antonious Adel Samir | The Data Consigliere</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lora:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #f4efe6;         
            --card-bg: #fcfbfa;          
            --text-main: #2b1d14;        
            --text-muted: #594a3e;       
            --accent-red: #721c1c;       
            --border-color: #4a3424;     
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--bg-color);
            background-image: url('https://www.transparenttextures.com/patterns/cream-paper.png'); 
            color: var(--text-main);
            font-family: 'Lora', serif;
            line-height: 1.6;
            padding: 2rem 1rem;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        /* --- HEADER --- */
        header {
            text-align: center;
            padding: 3rem 0;
            border-bottom: 3px double var(--border-color);
            margin-bottom: 2.5rem;
        }

        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            color: var(--text-main);
            margin-bottom: 0.2rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .subtitle {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            color: var(--accent-red);
            font-style: italic;
            margin-bottom: 1rem;
        }

        .quote {
            font-size: 1.1rem;
            color: var(--text-main);
            max-width: 600px;
            margin: 0 auto 1.5rem auto;
            font-weight: 600;
        }

        .quote::before, .quote::after {
            content: '"';
            color: var(--accent-red);
        }

        .badges {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .badge {
            border: 1px solid var(--border-color);
            color: var(--text-main);
            padding: 0.3rem 1rem;
            border-radius: 2px;
            font-size: 0.9rem;
            font-weight: 600;
            background-color: #eae1d1;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        section {
            margin-bottom: 3.5rem;
        }

        h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            color: var(--accent-red);
            text-align: center;
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 0.5rem;
            margin-bottom: 2rem;
            position: relative;
        }

        /* --- SKILLS SECTION --- */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .skill-category {
            background-color: var(--card-bg);
            padding: 1.5rem;
            border: 2px solid var(--border-color);
            box-shadow: 4px 4px 0px rgba(74, 52, 36, 0.1);
        }

        .skill-category h3 {
            font-family: 'Playfair Display', serif;
            color: var(--text-main);
            font-size: 1.3rem;
            margin-bottom: 1rem;
            border-bottom: 1px dashed var(--border-color);
            padding-bottom: 0.5rem;
        }

        .skill-category ul {
            list-style: none;
        }

        .skill-category li {
            color: var(--text-muted);
            margin-bottom: 0.5rem;
            font-size: 1rem;
        }

        .skill-category li::before {
            content: "❖ ";
            color: var(--accent-red);
            font-size: 0.8rem;
        }

        /* --- PROJECTS SECTION --- */
        .project-card {
            background-color: var(--card-bg);
            border: 2px solid var(--border-color);
            padding: 2rem;
            margin-bottom: 1.5rem;
            box-shadow: 4px 4px 0px rgba(74, 52, 36, 0.1);
        }

        .project-card h3 {
            font-family: 'Playfair Display', serif;
            color: var(--accent-red);
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .project-tech {
            font-size: 0.9rem;
            color: var(--text-main);
            margin-bottom: 1rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .project-card p {
            color: var(--text-muted);
            margin-bottom: 1rem;
        }

        .project-card ul {
            list-style-position: inside;
            color: var(--text-muted);
            margin-left: 1rem;
        }

        /* --- SERVICES SECTION --- */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.5rem;
        }

        .service-card {
            background-color: var(--card-bg);
            border: 2px solid var(--border-color);
            padding: 1.5rem;
            text-align: center;
            box-shadow: 4px 4px 0px rgba(74, 52, 36, 0.1);
        }

        .service-card h3 {
            font-family: 'Playfair Display', serif;
            color: var(--text-main);
            margin-bottom: 0.75rem;
            font-size: 1.25rem;
        }

        .service-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* --- CONTACT SECTION --- */
        .contact-box {
            background-color: var(--card-bg);
            border: 3px double var(--border-color);
            padding: 2.5rem;
            text-align: center;
        }

        .contact-box p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        .contact-link {
            font-family: 'Playfair Display', serif;
            color: var(--card-bg);
            background-color: var(--accent-red);
            text-decoration: none;
            font-weight: 700;
            padding: 0.75rem 1.5rem;
            border: 2px solid var(--accent-red);
            border-radius: 2px;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .contact-link:hover {
            background-color: var(--card-bg);
            color: var(--accent-red);
        }

        footer {
            text-align: center;
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-top: 4rem;
            border-top: 1px solid var(--border-color);
            padding-top: 2rem;
            font-family: 'Playfair Display', serif;
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>Antonious Adel Samir</h1>
        <p class="subtitle">The Data Consigliere to the Digital Family</p>
        <p class="quote">I'll make you an offer on automated data pipelines you can't refuse.</p>
        <div class="badges">
            <span class="badge">DEPI Scholar</span>
            <span class="badge">Azure Data Engineer</span>
            <span class="badge">B.Eng. Comm & Electronics</span>
        </div>
    </header>

    <!-- 1. SKILLS SECTION -->
    <section>
        <h2>Skills of the Family</h2>
        <div class="skills-grid">
            <div class="skill-category">
                <h3>Cloud Territory</h3>
                <ul>
                    <li>Microsoft Azure Infrastructure</li>
                    <li>Azure Data Factory (ADF)</li>
                    <li>Azure Synapse Analytics</li>
                    <li>Blob Storage & Data Lakes</li>
                </ul>
            </div>
            <div class="skill-category">
                <h3>The Vault (Databases)</h3>
                <ul>
                    <li>Advanced SQL Querying</li>
                    <li>Relational Database Management</li>
                    <li>Big Data Processing</li>
                    <li>Data Cleaning & Structuring</li>
                </ul>
            </div>
            <div class="skill-category">
                <h3>Operations (DevOps)</h3>
                <ul>
                    <li>Advanced Python Scripts</li>
                    <li>Prompt Engineering (AI)</li>
                    <li>Azure DevOps & Git</li>
                    <li>Automated ETL/ELT Pipelines</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- 2. PROJECTS SECTION -->
    <section>
        <h2>Projects of Respect</h2>

        <div class="project-card">
            <h3>1. End-to-End Automated ETL Pipeline</h3>
            <p class="project-tech">Azure Data Factory | Blob Storage | Azure SQL | Python</p>
            <p>Took control of fragmented business data, orchestrating a fully automated cloud pipeline to clean and consolidate raw sales numbers into a centralized database.</p>
            <ul>
                <li>Automated daily API and legacy file ingestion into the Azure Bronze layer.</li>
                <li>Wrote custom Python scripts to enforce data integrity and eliminate missing values.</li>
                <li>Scheduled nightly triggers that run silently in the background with strict error monitoring.</li>
            </ul>
        </div>

        <div class="project-card">
            <h3>2. Database Optimization & Big Data Processing</h3>
            <p class="project-tech">Advanced SQL | Star Schema | Indexing</p>
            <p>Restructured a bloated, slow-moving database into a highly efficient, streamlined analytics engine, saving the business time and computing resources.</p>
            <ul>
                <li>Re-architected transactional schemas into a reporting-optimized Star Schema.</li>
                <li>Applied strategic indexing on high-traffic queries to drastically reduce read times.</li>
                <li>Cut query response times from 4 minutes to under 15 seconds.</li>
            </ul>
        </div>

        <div class="project-card">
            <h3>3. AI-Enhanced Validation Workflow</h3>
            <p class="project-tech">Python | Prompt Engineering | Azure DevOps</p>
            <p>Brought artificial intelligence into the family business. Built a pre-processing pipeline to automatically read, categorize, and clean unstructured logs.</p>
            <ul>
                <li>Integrated LLM APIs for automated sentiment and category tagging.</li>
                <li>Built quarantine logic to isolate suspicious or low-confidence records for human review.</li>
            </ul>
        </div>
    </section>

    <!-- 3. SERVICES SECTION -->
    <section>
        <h2>Services Offered to the Business World</h2>
        <div class="services-grid">
            <div class="service-card">
                <h3>Pipeline Orchestration</h3>
                <p>Building reliable, scheduled data ingestion pathways (ETL/ELT) that never miss a deadline.</p>
            </div>
            <div class="service-card">
                <h3>Database Optimization</h3>
                <p>Cleaning up slow queries and poorly structured tables to make your data lightning fast.</p>
            </div>
            <div class="service-card">
                <h3>Azure Architecture</h3>
                <p>Setting up your cloud storage, data factories, and analytical environments the right way.</p>
            </div>
        </div>
    </section>

    <!-- 4. CONTACT SECTION -->
    <section>
        <h2>Contacting the Data Consigliere</h2>
        <div class="contact-box">
            <p>Ready to bring order to your raw data? Send a message to arrange a meeting.</p>
            <div class="contact-links">
                <a href="mailto:antoniousadel15@gmail.com" class="contact-link">Send a Wire (Email)</a>
                <a href="https://www.linkedin.com/in/antonious-adel-900975264" target="_blank" class="contact-link">LinkedIn</a>
                <a href="https://github.com/Antonious-Samir" target="_blank" class="contact-link">GitHub</a>
            </div>
        </div>
    </section>

    <footer>
        <p>© 2026 Antonious Adel Samir | Digital Egypt Pioneers Initiative (DEPI)</p>
        <p>Microsoft Azure Data Engineer</p>
    </footer>
</div>

</body>
</html>
