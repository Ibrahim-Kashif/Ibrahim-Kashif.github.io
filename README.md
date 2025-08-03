<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ibrahim Kashif | Data Scientist Portfolio</title>
    
    <!-- Google Fonts: Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Icons (Lucide) -->
    <script src="https://unpkg.com/lucide@latest/dist/umd/lucide.min.js"></script>


    <style>
        /* CSS Reset & Base Styles */
        :root {
            --background: #0a0a0a;
            --foreground: #fafafa;
            --card: #1a1a1a;
            --card-foreground: #fafafa;
            --popover: #1a1a1a;
            --popover-foreground: #fafafa;
            --primary: #3b82f6; /* Professional Blue */
            --primary-foreground: #fafafa;
            --secondary: #2a2a2a;
            --secondary-foreground: #fafafa;
            --muted: #2a2a2a;
            --muted-foreground: #a1a1aa;
            --accent: #2a2a2a;
            --accent-foreground: #fafafa;
            --destructive: #ef4444;
            --destructive-foreground: #fafafa;
            --border: #2a2a2a;
            --input: #2a2a2a;
            --ring: var(--primary);
            --radius: 0.5rem;
        }

        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
            background-color: var(--background);
            color: var(--foreground);
            font-family: 'Inter', sans-serif;
        }

        body {
            line-height: 1.6;
            font-size: 16px;
        }

        /* Utility Classes */
        .container {
            width: 100%;
            max-width: 1100px;
            margin-left: auto;
            margin-right: auto;
            padding-left: 1.5rem;
            padding-right: 1.5rem;
        }

        section {
            padding: 6rem 0;
            border-bottom: 1px solid var(--border);
        }
        
        section:last-of-type {
            border-bottom: none;
        }

        h1, h2, h3, h4, h5, h6 {
            color: var(--foreground);
            font-weight: 700;
            line-height: 1.2;
        }

        h2 {
            font-size: 2.25rem;
            margin-bottom: 2rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }
        
        h2 .icon {
            color: var(--primary);
        }

        p {
            color: var(--muted-foreground);
            margin-bottom: 1rem;
        }

        a {
            color: var(--primary);
            text-decoration: none;
            transition: opacity 0.2s ease;
        }

        a:hover {
            opacity: 0.8;
        }
        
        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 0.75rem 1.5rem;
            border-radius: var(--radius);
            font-weight: 600;
            text-align: center;
            cursor: pointer;
            transition: all 0.2s ease;
            border: 1px solid transparent;
        }
        
        .btn-primary {
            background-color: var(--primary);
            color: var(--primary-foreground);
            font-weight: 700;
        }
        
        .btn-primary:hover {
            opacity: 0.9;
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--foreground);
            border-color: var(--border);
        }

        .btn-secondary:hover {
            background-color: var(--accent);
        }

        /* Header & Navigation */
        #main-header {
            position: sticky;
            top: 0;
            width: 100%;
            padding: 1rem 0;
            background-color: rgba(10, 10, 10, 0.8);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            z-index: 50;
            border-bottom: 1px solid var(--border);
        }

        #main-header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        #logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--foreground);
        }
        
        #logo span {
            color: var(--primary);
        }

        #main-nav nav a {
            color: var(--muted-foreground);
            margin-left: 1.5rem;
            font-weight: 500;
            position: relative;
            padding-bottom: 4px;
        }

        #main-nav nav a:hover {
            color: var(--foreground);
            opacity: 1;
        }

        #main-nav nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: width 0.3s ease;
        }

        #main-nav nav a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        #hero {
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            min-height: 80vh;
        }
        
        #hero h1 {
            font-size: 3.75rem;
            margin-bottom: 1rem;
        }

        #hero h1 span {
            color: var(--primary);
        }

        #hero p {
            font-size: 1.25rem;
            max-width: 600px;
            margin: 0 auto 2rem auto;
        }

        #hero .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
        }

        /* About Section */
        #about .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .skill-category {
            background-color: var(--card);
            padding: 2rem;
            border-radius: var(--radius);
            border: 1px solid var(--border);
        }
        
        .skill-category h3 {
            font-size: 1.25rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .skill-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem;
            list-style: none;
        }

        .skill-list li {
            background-color: var(--secondary);
            color: var(--muted-foreground);
            padding: 0.5rem 1rem;
            border-radius: 999px;
            font-size: 0.875rem;
            font-weight: 500;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: var(--card);
            border-radius: var(--radius);
            border: 1px solid var(--border);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(59, 130, 246, 0.1);
        }

        .project-card .card-content {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .project-card h3 {
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
        }
        
        .project-card p {
            font-size: 0.95rem;
            flex-grow: 1;
        }
        
        .project-card .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }
        
        .project-card .tag {
            background-color: var(--secondary);
            color: var(--muted-foreground);
            padding: 0.25rem 0.75rem;
            border-radius: 999px;
            font-size: 0.75rem;
            font-weight: 500;
        }
        
        .project-card .card-footer {
            display: flex;
            gap: 1rem;
            align-items: center;
            margin-top: auto;
        }
        
        .project-card .link {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-weight: 500;
        }
        
        .project-card .link i {
            width: 18px;
            height: 18px;
        }
        
        /* Experience Section */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 3px;
            background-color: var(--border);
            top: 0;
            bottom: 0;
            left: 30px;
        }

        .timeline-item {
            padding: 10px 40px;
            padding-left: 70px;
            position: relative;
        }
        
        .timeline-item:last-child {
            padding-bottom: 0;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: var(--background);
            border: 3px solid var(--primary);
            top: 24px;
            left: 20px;
            z-index: 1;
        }

        .timeline-content h3 {
            font-size: 1.25rem;
        }
        
        .timeline-content span {
            color: var(--primary);
            font-size: 0.9rem;
            font-weight: 500;
            display: block;
            margin: 0.25rem 0 1rem 0;
        }
        
        .timeline-content ul {
            list-style-type: none;
            padding-left: 0;
        }

        .timeline-content ul li {
            margin-bottom: 0.5rem;
            color: var(--muted-foreground);
            position: relative;
            padding-left: 20px;
        }

        .timeline-content ul li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: var(--primary);
            font-weight: 700;
        }

        /* University Modules Section */
        .education-overview {
            background-color: var(--card);
            border: 1px solid var(--border);
            border-radius: var(--radius);
            padding: 2rem;
            margin-bottom: 3rem;
        }
        
        .education-overview h3 {
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .education-header {
             display: flex;
             justify-content: space-between;
             align-items: center;
             margin-bottom: 2rem;
             flex-wrap: wrap;
             gap: 1rem;
        }
        
        .education-header .filter-group {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .education-header select, .modal-body select {
             background-color: var(--input);
             color: var(--foreground);
             border: 1px solid var(--border);
             padding: 0.75rem;
             border-radius: var(--radius);
             font-family: inherit;
             font-size: 1rem;
             width: 100%;
        }
        
        .modules-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.5rem;
        }
        
        .module-card {
            background-color: var(--card);
            border: 1px solid var(--border);
            padding: 1.5rem;
            border-radius: var(--radius);
            display: flex;
            flex-direction: column;
        }
        
        .module-card h4 {
            font-size: 1.1rem;
            margin-bottom: 0.25rem;
        }
        
        .module-card .module-code {
            color: var(--muted-foreground);
            font-size: 0.85rem;
            font-weight: 500;
            margin-bottom: 1rem;
        }

        .module-card .module-desc {
            font-size: 0.9rem;
            color: var(--muted-foreground);
            margin-bottom: 1rem;
            flex-grow: 1;
        }

        .module-details {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.9rem;
            margin-bottom: 0.75rem;
            color: var(--muted-foreground);
        }
        
        .module-details .grade {
            font-weight: 600;
            padding: 0.25rem 0.75rem;
            border-radius: var(--radius);
            font-size: 0.8rem;
        }
        
        .grade-first { background-color: rgba(59, 130, 246, 0.1); color: #3b82f6; }
        .grade-2-1 { background-color: rgba(20, 184, 166, 0.1); color: #14b8a6; }
        .grade-2-2 { background-color: rgba(245, 158, 11, 0.1); color: #f59e0b; }
        .grade-third { background-color: rgba(239, 68, 68, 0.1); color: #ef4444; }
        .grade-fail { background-color: rgba(120, 113, 108, 0.1); color: #78716c; }

        .progress-bar {
            width: 100%;
            height: 8px;
            background-color: var(--secondary);
            border-radius: 999px;
            overflow: hidden;
        }
        
        .progress-bar-fill {
            height: 100%;
            background-color: var(--primary);
            border-radius: 999px;
            transition: width 0.5s ease-in-out;
        }

        /* Contact Section */
        #contact-form {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-group input, .form-group textarea {
            width: 100%;
            background-color: var(--input);
            border: 1px solid var(--border);
            color: var(--foreground);
            padding: 0.75rem;
            border-radius: var(--radius);
            font-family: inherit;
        }
        
        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 2px rgba(59, 130, 246, 0.2);
        }
        
        .contact-info {
            text-align: center;
            margin-top: 4rem;
        }
        
        .contact-info p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
        }
        
        .social-links a {
             color: var(--muted-foreground);
        }
        .social-links a:hover {
            color: var(--primary);
        }

        /* Modal Styles */
        .modal-backdrop {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }
        
        .modal-backdrop.visible {
            opacity: 1;
            visibility: visible;
        }

        .modal-content {
            background-color: var(--card);
            padding: 2rem;
            border-radius: var(--radius);
            border: 1px solid var(--border);
            width: 90%;
            max-width: 500px;
            transform: scale(0.95);
            transition: transform 0.3s ease;
        }
        
        .modal-backdrop.visible .modal-content {
            transform: scale(1);
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .modal-header h3 {
            font-size: 1.5rem;
        }
        
        .close-modal-btn {
            background: none;
            border: none;
            color: var(--muted-foreground);
            cursor: pointer;
        }
        
        .close-modal-btn:hover {
            color: var(--foreground);
        }

        .modal-footer {
            margin-top: 2rem;
            display: flex;
            justify-content: flex-end;
            gap: 1rem;
        }

        /* Footer */
        footer {
            padding: 2rem 0;
            text-align: center;
            color: var(--muted-foreground);
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            h2 { font-size: 2rem; }
            
            #main-header .container { flex-direction: column; gap: 1rem; }
            #main-nav nav { display: flex; flex-wrap: wrap; justify-content: center; gap: 0.5rem; }
            #main-nav nav a { margin: 0 0.75rem; }

            #about .container { grid-template-columns: 1fr; }
            
            .timeline::after { left: 15px; }
            .timeline-item { padding-left: 50px; }
            .timeline-item::before { left: 6px; }
            
            #hero { min-height: 60vh; }
        }
        
        @media (max-width: 480px) {
            .container { padding-left: 1rem; padding-right: 1rem; }
            section { padding: 4rem 0; }
            #hero h1 { font-size: 2.2rem; }
            #hero p { font-size: 1rem; }
            .cta-buttons { flex-direction: column; }
            .education-header { flex-direction: column; align-items: stretch; }
        }

    </style>
</head>
<body>

    <!-- Header -->
    <header id="main-header">
        <div class="container">
            <a href="#" id="logo">Your Name<span>.</span></a>
            <div id="main-nav">
                <nav>
                    <a href="#about">About</a>
                    <a href="#skills">Skills</a>
                    <a href="#projects">Projects</a>
                    <a href="#experience">Experience</a>
                    <a href="#university">University</a>
                    <a href="#contact">Contact</a>
                </nav>
            </div>
        </div>
    </header>

    <main>

        <!-- Hero Section -->
        <section id="hero">
            <div class="container">
                <h1>Hi, I'm a Mathematics Student & <span>Aspiring Data Scientist</span>.</h1>
                <p>I leverage statistical analysis and machine learning to extract insights from complex datasets. Currently seeking data science internships and graduate roles.</p>
                <div class="cta-buttons">
                    <a href="#projects" class="btn btn-primary">View My Projects</a>
                    <a href="mailto:your.email@example.com" class="btn btn-secondary">Get In Touch</a>
                </div>
            </div>
        </section>

        <!-- About Me Section -->
        <section id="about">
            <div class="container">
                <div class="about-text">
                    <h2><i class="icon" data-lucide="user-round"></i>About Me</h2>
                    <p>
                        I've always been fascinated by the power of mathematics to model the world around us. My studies at the University of Manchester have solidified this passion, showing me how abstract concepts can be transformed into powerful tools for understanding complex systems. This analytical mindset is what draws me to data science.
                    </p>
                    <p>
                        I am passionate about the entire data lifecycle, from wrangling and exploring raw data to building predictive models and communicating insights through compelling visualizations. I'm a regular on Kaggle, where I enjoy tackling real-world problems and learning from the community. When I'm not in front of a screen, I enjoy hiking and landscape photography.
                    </p>
                </div>
                 <div class="about-image" style="text-align: center;">
                    <!-- Placeholder for an image of you -->
                    <img src="https://placehold.co/350x350/1a1a1a/3b82f6?text=Me" alt="A professional photo of me" style="border-radius: var(--radius); border: 1px solid var(--border);">
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section id="skills">
            <div class="container">
                <h2><i class="icon" data-lucide="brain-circuit"></i>Data Science Skills</h2>
                <div class="skills-grid">
                    <div class="skill-category">
                        <h3>Languages & Querying</h3>
                        <ul class="skill-list">
                            <li>Python</li>
                            <li>R</li>
                            <li>SQL</li>
                            <li>MATLAB</li>
                            <li>JavaScript (D3.js)</li>
                        </ul>
                    </div>
                    <div class="skill-category">
                        <h3>Libraries & Frameworks</h3>
                        <ul class="skill-list">
                            <li>Pandas</li>
                            <li>NumPy</li>
                            <li>Scikit-learn</li>
                            <li>Matplotlib</li>
                            <li>Seaborn</li>
                            <li>TensorFlow</li>
                            <li>PyTorch</li>
                        </ul>
                    </div>
                    <div class="skill-category">
                        <h3>Tools & Platforms</h3>
                        <ul class="skill-list">
                            <li>Jupyter Notebooks</li>
                            <li>Git & GitHub</li>
                            <li>Docker</li>
                            <li>PostgreSQL</li>
                            <li>Tableau</li>
                            <li>AWS (S3, SageMaker)</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <div class="container">
                <h2><i class="icon" data-lucide="lightbulb"></i>Projects</h2>
                <div class="projects-grid">
                    <!-- Projects will be dynamically inserted here -->
                </div>
            </div>
        </section>
        
        <!-- Experience Section -->
        <section id="experience">
            <div class="container">
                <h2><i class="icon" data-lucide="briefcase"></i>Experience</h2>
                <div class="timeline">
                    <!-- Experience items will be dynamically inserted here -->
                </div>
            </div>
        </section>

        <!-- University Modules Section -->
        <section id="university">
            <div class="container">
                <h2><i class="icon" data-lucide="graduation-cap"></i>University Modules & Grades</h2>
                
                <div class="education-overview">
                    <h3>BSc (Hons) Mathematics @ University of Manchester</h3>
                    <p id="overall-average-display" style="margin-bottom: 0.5rem;"><strong>Overall Average:</strong> Calculating...</p>
                    <p style="margin-bottom: 0;"><strong>Achievements:</strong> Placed in top 5% in the university's annual Kaggle competition.</p>
                </div>
                
                <div class="education-header">
                    <div class="filter-group">
                        <label for="year-filter">Filter by Year:</label>
                        <select id="year-filter">
                            <!-- Year options will be dynamically inserted here -->
                        </select>
                    </div>
                    <button id="add-module-btn" class="btn btn-secondary">
                        <i data-lucide="plus" style="width: 16px; height: 16px; margin-right: 8px;"></i>Add Module
                    </button>
                </div>
                
                <div id="modules-container" class="modules-grid">
                    <!-- Module cards will be dynamically inserted here -->
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <div class="container">
                <h2 style="text-align: center; justify-content: center;"><i class="icon" data-lucide="mail"></i>Get In Touch</h2>
                <p style="text-align: center; max-width: 600px; margin: 0 auto 3rem auto;">
                    I'm currently open to new opportunities and collaborations. Whether you have a question or just want to say hi, feel free to reach out. I'll get back to you as soon as possible!
                </p>

                <form id="contact-form">
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" rows="5" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Send Message</button>
                </form>

                <div class="contact-info">
                     <div class="social-links">
                        <a href="#" aria-label="GitHub"><i data-lucide="github"></i></a>
                        <a href="#" aria-label="LinkedIn"><i data-lucide="linkedin"></i></a>
                        <a href="#" aria-label="Twitter/X"><i data-lucide="x"></i></a>
                    </div>
                </div>

            </div>
        </section>

    </main>
    
    <!-- Add Module Modal -->
    <div id="add-module-modal" class="modal-backdrop">
        <div class="modal-content">
            <div class="modal-header">
                <h3>Add New Module</h3>
                <button class="close-modal-btn" aria-label="Close modal">&times;</button>
            </div>
            <form id="add-module-form">
                <div class="modal-body">
                    <div class="form-group">
                        <label for="module-name">Module Name</label>
                        <input type="text" id="module-name" required>
                    </div>
                    <div class="form-group">
                        <label for="module-code">Module Code (e.g., MATH12345)</label>
                        <input type="text" id="module-code" required>
                    </div>
                     <div class="form-group">
                        <label for="module-year">Academic Year</label>
                        <select id="module-year" required>
                            <option value="1">Year 1</option>
                            <option value="2">Year 2</option>
                            <option value="3">Year 3</option>
                            <option value="4">Year 4 (Masters)</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="module-credits">Credits</label>
                        <input type="number" id="module-credits" min="5" max="40" step="5" required>
                    </div>
                    <div class="form-group">
                        <label for="module-percentage">Percentage (%)</label>
                        <input type="number" id="module-percentage" min="0" max="100" required>
                    </div>
                    <div class="form-group">
                        <label for="module-description">Description</label>
                        <textarea id="module-description" rows="3"></textarea>
                    </div>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary close-modal-btn">Cancel</button>
                    <button type="submit" class="btn btn-primary">Save Module</button>
                </div>
            </form>
        </div>
    </div>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2025 Your Name. Built with passion and data.</p>
        </div>
    </footer>

    <script>
        // --- MOCK DATA ---
        
        const projectsData = [
            {
                title: "Customer Churn Prediction",
                description: "Used logistic regression and random forests to predict customer churn for a subscription service, achieving 88% accuracy. Deployed a simple Flask API for the model.",
                tags: ["Python", "Scikit-learn", "Pandas", "Flask"],
                github: "#",
                live: "#"
            },
            {
                title: "Sentiment Analysis of Movie Reviews",
                description: "Developed an NLP model using TensorFlow and LSTMs to classify the sentiment of IMDb reviews. Visualized word embeddings with t-SNE.",
                tags: ["TensorFlow", "NLP", "Python", "Matplotlib"],
                github: "#",
                live: null
            },
            {
                title: "Sales Forecasting with Time Series",
                description: "Applied ARIMA and Prophet models to forecast monthly sales for a retail dataset, improving forecast accuracy by 20% over baseline.",
                tags: ["R", "Time Series", "Prophet", "ggplot2"],
                github: "#",
                live: "#"
            }
        ];

        const experienceData = [
            {
                role: "Data Analyst Intern",
                company: "Data Insights Inc.",
                duration: "June 2024 - August 2024",
                achievements: [
                    "Cleaned and preprocessed a large dataset of customer transactions, improving data quality for modelling.",
                    "Developed interactive dashboards in Tableau to track key business metrics, providing actionable insights to the marketing team.",
                    "Assisted senior data scientists with feature engineering for a new recommendation engine.",
                    "Presented findings on customer segmentation to stakeholders, leading to a new targeted marketing campaign."
                ]
            },
            {
                role: "Undergraduate Teaching Assistant",
                company: "University of Manchester - Maths Dept.",
                duration: "September 2023 - May 2024",
                achievements: [
                    "Assisted first-year students with Calculus and Linear Algebra problem sets.",
                    "Led weekly tutorials, explaining complex mathematical concepts to groups of up to 20 students.",
                    "Received positive feedback from 95% of students for clarity and helpfulness."
                ]
            }
        ];
        
        // This array is now empty. Use the "Add Module" button to populate it.
        let modulesData = [];
        
        // --- DYNAMIC CONTENT RENDERING & EVENT HANDLING ---
        
        document.addEventListener('DOMContentLoaded', () => {
            // This needs to be called after the script is loaded
            lucide.createIcons();
            
            // Render initial content
            renderProjects();
            renderExperience();
            updateAndRenderModules();

            // Setup event listeners
            document.getElementById('year-filter').addEventListener('change', (e) => {
                renderModules(e.target.value);
            });
            
            // Form submission handler (prevents default for this demo)
            document.getElementById('contact-form').addEventListener('submit', (e) => {
                e.preventDefault();
                alert('Thank you for your message! (Form submission is disabled for this demo)');
            });

            // Modal handling
            const modal = document.getElementById('add-module-modal');
            const openModalBtn = document.getElementById('add-module-btn');
            const closeModalBtns = document.querySelectorAll('.close-modal-btn');
            const addModuleForm = document.getElementById('add-module-form');

            openModalBtn.addEventListener('click', () => modal.classList.add('visible'));
            
            closeModalBtns.forEach(btn => {
                btn.addEventListener('click', () => modal.classList.remove('visible'));
            });

            addModuleForm.addEventListener('submit', handleAddModule);
        });
        
        function handleAddModule(e) {
            e.preventDefault();
            
            const newModule = {
                name: document.getElementById('module-name').value,
                code: document.getElementById('module-code').value,
                year: parseInt(document.getElementById('module-year').value),
                credits: parseInt(document.getElementById('module-credits').value),
                percentage: parseInt(document.getElementById('module-percentage').value),
                description: document.getElementById('module-description').value,
            };

            newModule.grade = calculateGrade(newModule.percentage);
            
            modulesData.push(newModule);
            
            // Sort modules by year then name
            modulesData.sort((a, b) => {
                if (a.year !== b.year) {
                    return a.year - b.year;
                }
                return a.name.localeCompare(b.name);
            });

            updateAndRenderModules();
            
            // Close modal and reset form
            document.getElementById('add-module-modal').classList.remove('visible');
            e.target.reset();
        }

        function updateAndRenderModules() {
            updateYearFilter();
            updateOverallAverage();
            const currentFilter = document.getElementById('year-filter').value;
            renderModules(currentFilter);
        }

        function renderProjects() {
            const container = document.querySelector('.projects-grid');
            if (!container) return;
            container.innerHTML = projectsData.map(project => `
                <div class="project-card">
                    <div class="card-content">
                        <h3>${project.title}</h3>
                        <div class="tags">
                            ${project.tags.map(tag => `<span class="tag">${tag}</span>`).join('')}
                        </div>
                        <p>${project.description}</p>
                        <div class="card-footer">
                            <a href="${project.github}" class="link" target="_blank" rel="noopener noreferrer">
                                <i data-lucide="github"></i> GitHub
                            </a>
                            ${project.live ? `
                            <a href="${project.live}" class="link" target="_blank" rel="noopener noreferrer">
                                <i data-lucide="external-link"></i> Live Demo
                            </a>` : ''}
                        </div>
                    </div>
                </div>
            `).join('');
            lucide.createIcons();
        }

        function renderExperience() {
            const container = document.querySelector('.timeline');
            if (!container) return;
            container.innerHTML = experienceData.map(exp => `
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>${exp.role}</h3>
                        <span>${exp.company} | ${exp.duration}</span>
                        <ul>
                            ${exp.achievements.map(ach => `<li>${ach}</li>`).join('')}
                        </ul>
                    </div>
                </div>
            `).join('');
        }
        
        function calculateGrade(percentage) {
            if (percentage >= 70) return 'First Class';
            if (percentage >= 60) return 'Upper Second';
            if (percentage >= 50) return 'Lower Second';
            if (percentage >= 40) return 'Third Class';
            return 'Fail';
        }

        function getGradeClass(grade) {
            if (grade === 'First Class') return 'grade-first';
            if (grade === 'Upper Second') return 'grade-2-1';
            if (grade === 'Lower Second') return 'grade-2-2';
            if (grade === 'Third Class') return 'grade-third';
            return 'grade-fail';
        }

        function updateYearFilter() {
            const yearFilter = document.getElementById('year-filter');
            const currentSelection = yearFilter.value;
            const years = [...new Set(modulesData.map(m => m.year))].sort((a,b) => a-b);
            
            yearFilter.innerHTML = '<option value="all">All Years</option>';
            
            years.forEach(year => {
                const yearModules = modulesData.filter(m => m.year === year);
                const totalCredits = yearModules.reduce((sum, m) => sum + m.credits, 0);
                const weightedSum = yearModules.reduce((sum, m) => sum + (m.percentage * m.credits), 0);
                const average = totalCredits > 0 ? (weightedSum / totalCredits).toFixed(1) : 0;
                
                const option = document.createElement('option');
                option.value = year;
                option.textContent = `Year ${year} (Avg: ${average}%)`;
                yearFilter.appendChild(option);
            });
            yearFilter.value = currentSelection || 'all';
        }

        function updateOverallAverage() {
            const display = document.getElementById('overall-average-display');
            const totalCredits = modulesData.reduce((sum, m) => sum + m.credits, 0);
            
            if (totalCredits === 0) {
                display.innerHTML = `<strong>Overall Average:</strong> N/A`;
                return;
            }

            const weightedSum = modulesData.reduce((sum, m) => sum + (m.percentage * m.credits), 0);
            const average = (weightedSum / totalCredits).toFixed(1);
            const grade = calculateGrade(average);
            display.innerHTML = `<strong>Overall Average:</strong> ${average}% (${grade})`;
        }

        function renderModules(yearFilter) {
            const container = document.getElementById('modules-container');
            const filteredModules = yearFilter === 'all' 
                ? modulesData 
                : modulesData.filter(m => m.year == yearFilter);

            if (filteredModules.length === 0) {
                container.innerHTML = `<p>No modules added yet. Click 'Add Module' to get started.</p>`;
                return;
            }
            
            container.innerHTML = filteredModules.map(module => `
                <div class="module-card">
                    <h4>${module.name}</h4>
                    <p class="module-code">${module.code} &bull; ${module.credits} Credits</p>
                    <p class="module-desc">${module.description || 'No description available.'}</p>
                    <div class="module-details">
                        <span class="grade ${getGradeClass(module.grade)}">${module.grade}</span>
                        <span class="percentage">${module.percentage}%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-bar-fill" style="width: ${module.percentage}%;"></div>
                    </div>
                </div>
            `).join('');
            // We need to re-run createIcons after rendering new content with data-lucide attributes
            lucide.createIcons();
        }
    </script>
</body>
</html>
