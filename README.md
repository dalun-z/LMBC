  Project Plan: Local Business Discovery Platform        body { font-family: 'Inter', sans-serif; background-color: #F9F7F3; /\* Light warm neutral \*/ color: #383838; } .nav-link { transition: all 0.2s ease-in-out; border-bottom: 2px solid transparent; } .nav-link.active, .nav-link:hover { color: #4A90E2; /\* Subtle blue accent \*/ border-bottom-color: #4A90E2; } .tab-button.active { border-color: #4A90E2; background-color: #4A90E2; color: #FFFFFF; } .feature-accordion-header { cursor: pointer; transition: background-color 0.2s ease; } .feature-accordion-header:hover { background-color: #EFEBE5; } .feature-accordion-content { max-height: 0; overflow: hidden; transition: max-height 0.3s ease-out; } .risk-card-inner { transition: transform 0.6s; transform-style: preserve-3d; } .risk-card.flipped .risk-card-inner { transform: rotateY(180deg); } .risk-card-front, .risk-card-back { -webkit-backface-visibility: hidden; backface-visibility: hidden; } .risk-card-back { transform: rotateY(180deg); } .chart-container { position: relative; width: 100%; max-width: 900px; margin-left: auto; margin-right: auto; height: 300px; max-height: 400px; } @media (min-width: 768px) { .chart-container { height: 400px; } }

LMBC Project Plan
=================

[Overview](#overview) [Tech Stack](#tech-stack) [Features](#features) [Architecture](#architecture) [Timeline](#timeline) [Risks](#risks)

Project Overview & Goals
------------------------

This project aims to build a dual-app mobile platform connecting small, mobile businesses with local consumers. This interactive dashboard outlines the full project scope, from technology choices to timeline and risks.

2

### Core Applications

Business Owner App & Consumer App

14 Weeks

### Estimated Duration

From initial setup to deployment

2+

### Core Technologies

React Native & AWS Serverless

Technology Stack
----------------

The platform is built on a modern, scalable stack chosen for cross-platform compatibility, performance, and cost-effectiveness. Each component plays a crucial role in delivering a robust user experience.

MVP Feature Breakdown
---------------------

The Minimum Viable Product focuses on the core user journeys of registration, discovery, and engagement. Explore the features planned for each part of the platform by selecting a tab below.

Business Owner App Consumer App Backend & API

High-Level System Architecture
------------------------------

The system uses a serverless architecture to ensure scalability and maintainability. User requests from the mobile apps are routed through an API Gateway to specific functions that handle business logic and data persistence. Hover over components to learn more.

📱

#### Business Owner App

📱

#### Consumer App

→

↓

#### 🔒 AWS Cognito

#### GATEWAY  
AWS API Gateway

↓

#### ⚙️ AWS Lambda Functions

→

↓

🗄️

#### AWS DynamoDB

🖼️

#### AWS S3 Storage

Hover over a component to see its description.

Development Phases & Timeline
-----------------------------

The project is broken down into five distinct phases, from initial setup to final deployment, over an estimated 14-week period. This phased approach ensures a structured development cycle with clear milestones.

Key Risks & Mitigation
----------------------

Proactively identifying potential risks is crucial for project success. Below are the key challenges anticipated for this project, along with their corresponding mitigation strategies. Click on any card to see the solution.

Interactive Project Plan | LMBC

document.addEventListener('DOMContentLoaded', () => { // --- DATA --- const techStackData = \[ { layer: 'Frontend (Mobile)', tech: 'React Native (Expo)', rationale: 'Cross-platform development (iOS/Android) from a single codebase. Expo simplifies build management.' }, { layer: 'Backend (Cloud)', tech: 'AWS', rationale: 'Provides scalable, secure, and pay-as-you-go cloud infrastructure.' }, { layer: 'Authentication', tech: 'AWS Cognito', rationale: 'Fully managed user directory and authentication for both business owners and consumers.' }, { layer: 'API Layer', tech: 'API Gateway & Lambda', rationale: 'Serverless architecture for scalable, cost-effective execution of business logic.' }, { layer: 'Database', tech: 'AWS DynamoDB (NoSQL)', rationale: 'Ideal for high-volume, low-latency data access, like real-time location updates.' }, { layer: 'Storage', tech: 'AWS S3', rationale: 'Secure storage for static assets like business logos and product images.' }, \]; const featuresData = { boa: \[ { name: 'Onboarding & Auth', desc: 'Registration, Login, Password Reset.', services: 'Cognito, Lambda' }, { name: 'Profile Management', desc: 'Set up business name, type, category, and business hours.', services: 'DynamoDB, S3' }, { name: 'Product Management', desc: 'Add, edit, and delete product listings with images.', services: 'DynamoDB, S3' }, { name: 'Real-Time Location', desc: 'Ability to "Go Live" or "Close Shop," streaming GPS location.', services: 'Lambda, DynamoDB' }, { name: 'Brand Introduction', desc: 'Dedicated section for a detailed brand story.', services: 'DynamoDB' }, { name: 'View Feedback', desc: 'Simple list view of recent ratings and comments.', services: 'DynamoDB' }, \], ca: \[ { name: 'Onboarding & Auth', desc: 'Optional registration/login (including social) via Cognito.', services: 'Cognito' }, { name: 'Location Access', desc: 'Request and use device GPS to find nearby businesses.', services: 'React Native Geolocation' }, { name: 'Business Discovery (Map View)', desc: 'Interactive map showing live locations of open businesses.', services: 'Lambda, DynamoDB' }, { name: 'Search & Filtering', desc: 'Filter businesses by Category, Type, and Rating.', services: 'Lambda, DynamoDB' }, { name: 'Business Detail View', desc: 'View full profile, menu, and reviews.', services: 'DynamoDB, S3' }, { name: 'Rating & Comment', desc: 'Submit a star rating (1-5) and a text review.', services: 'Lambda, DynamoDB' }, \], backend: \[ { name: 'User & Session Mgmt', desc: 'Securely handle authentication tokens and user roles.', services: 'Cognito, API Gateway' }, { name: 'Location Processing', desc: 'Receive and update business coordinates in the database.', services: 'API Gateway, Lambda, DynamoDB' }, { name: 'Geospatial Query', desc: 'Endpoint to query businesses within a specific radius.', services: 'Lambda, DynamoDB' }, { name: 'Image Hosting', desc: 'Secure upload and serving of product and profile images.', services: 'S3' }, { name: 'Rating Aggregation', desc: 'Calculate the average star rating for a business.', services: 'Lambda, DynamoDB' }, \] }; const timelineData = { labels: \['Setup & Design', 'Backend & Auth', 'Business App', 'Consumer App', 'Testing & Deploy'\], datasets: \[{ label: 'Phase Duration (Weeks)', data: \[ \[0, 2\], // Phase 0: Start Week 0, End Week 2 \[2, 5\], // Phase 1: Start Week 2, End Week 5 (3 weeks duration) \[5, 9\], // Phase 2: Start Week 5, End Week 9 (4 weeks duration) \[9, 14\], // Phase 3: Start Week 9, End Week 14 (5 weeks duration) \[14, 16\] // Phase 4: Start Week 14, End Week 16 (2 weeks duration) - Adjusted for visualization \], backgroundColor: \['#34D399', '#38BDF8', '#FBBF24', '#A78BFA', '#F87171'\], borderColor: \['#059669', '#0284C7', '#D97706', '#7C3AED', '#DC2626'\], borderWidth: 1, barPercentage: 0.6, }\] }; const timelineTasks = { 'Setup & Design': 'Tasks: AWS setup, React Native init, UI/UX mockups, DB schema design.', 'Backend & Auth': 'Tasks: Implement Cognito, Setup API Gateway/Lambda, Develop data models.', 'Business App': 'Tasks: Develop BOA Auth, Profile/Product Mgmt, Real-Time Location Streaming.', 'Consumer App': 'Tasks: Develop CA Auth, GPS/Map View, Search/Filter, Review forms.', 'Testing & Deploy': 'Tasks: Feature testing, performance optimization, security audit, App Store prep.', }; const risksData = \[ { risk: 'Battery Drain (BOA)', impact: 'Continuous GPS updates can quickly deplete a business owner\\'s phone battery.', mitigation: 'Implement intelligent location tracking (e.g., only update when moving), and clearly communicate the battery impact to users.' }, { risk: 'Data Synchronization', impact: 'Inconsistent data between the business location and the map view.', mitigation: 'Use DynamoDB\\'s low-latency and implement real-time subscription logic for map updates.' }, { risk: 'App Store Rejection', impact: 'Issues with privacy policies related to location data.', mitigation: 'Ensure clear, compliant privacy policies and request location permissions only when necessary.' }, { risk: 'Cost Overruns', impact: 'Excessive usage of serverless resources under heavy load.', mitigation: 'Implement robust monitoring (CloudWatch) and throttling limits on the API Gateway.' }, \]; // --- RENDER FUNCTIONS --- function renderTechStack() { const container = document.getElementById('tech-stack-container'); container.innerHTML = techStackData.map(item => \` <div class="bg-white p-6 rounded-lg shadow-md border border-gray-200 transform hover:-translate-y-1 transition-transform duration-200"> <h3 class="text-lg font-bold text-gray-800">${item.tech}</h3> <p class="text-sm font-medium text-sky-700 mb-2">${item.layer}</p> <p class="text-gray-600">${item.rationale}</p> </div> \`).join(''); } function renderFeatures(tab = 'boa') { const container = document.getElementById('features-content'); const features = featuresData\[tab\]; container.innerHTML = \` <div id="feature-accordion-container" class="border border-gray-200 rounded-lg bg-white shadow-sm"> ${features.map((feature, index) => \` <div class="border-b last:border-b-0 border-gray-200"> <div class="feature-accordion-header p-4 flex justify-between items-center"> <h4 class="font-semibold text-gray-800">${feature.name}</h4> <span class="text-gray-400 transform transition-transform duration-300">+</span> </div> <div class="feature-accordion-content px-4"> <div class="pb-4"> <p class="text-gray-600 mb-2">${feature.desc}</p> <p class="text-sm text-gray-500"><strong class="font-medium text-gray-600">Services:</strong> ${feature.services}</p> </div> </div> </div> \`).join('')} </div> \`; setupFeatureAccordion(); } function renderRisks() { const container = document.getElementById('risks-container'); container.innerHTML = risksData.map(item => \` <div class="risk-card perspective-1000 h-56"> <div class="risk-card-inner relative w-full h-full text-center"> <div class="risk-card-front absolute w-full h-full bg-white rounded-lg shadow-lg border border-gray-200 p-4 flex flex-col justify-center items-center"> <h4 class="text-lg font-bold text-gray-800">${item.risk}</h4> <p class="mt-2 text-sm text-gray-500">(Click to see mitigation)</p> </div> <div class="risk-card-back absolute w-full h-full bg-slate-700 text-white rounded-lg shadow-lg border border-gray-200 p-4 flex flex-col justify-center"> <h5 class="font-bold mb-2">Mitigation Strategy</h5> <p class="text-sm">${item.mitigation}</p> </div> </div> </div> \`).join(''); setupRiskCards(); } // --- SETUP EVENT LISTENERS --- function setupNavLinks() { const sections = document.querySelectorAll('section'); const navLinks = document.querySelectorAll('.nav-link'); const observerOptions = { root: null, rootMargin: '0px', threshold: 0.3 }; const observer = new IntersectionObserver((entries) => { entries.forEach(entry => { if (entry.isIntersecting) { navLinks.forEach(link => { link.classList.toggle('active', link.getAttribute('href').substring(1) === entry.target.id); }); } }); }, observerOptions); sections.forEach(section => observer.observe(section)); } function setupFeatureTabs() { const tabContainer = document.querySelector('.flex.justify-center.border-b'); const buttons = tabContainer.querySelectorAll('.tab-button'); tabContainer.addEventListener('click', (e) => { if (e.target.classList.contains('tab-button')) { buttons.forEach(btn => btn.classList.remove('active')); e.target.classList.add('active'); renderFeatures(e.target.dataset.tab); } }); // Activate first tab by default buttons\[0\].classList.add('active'); } function setupFeatureAccordion() { const container = document.getElementById('feature-accordion-container'); if (!container) return; container.addEventListener('click', e => { const header = e.target.closest('.feature-accordion-header'); if (header) { const content = header.nextElementSibling; const icon = header.querySelector('span'); // Close all other open accordions const allContent = container.querySelectorAll('.feature-accordion-content'); const allIcons = container.querySelectorAll('.feature-accordion-header span'); allContent.forEach((el, index) => { if (el !== content && el.style.maxHeight) { el.style.maxHeight = null; allIcons\[index\].style.transform = 'rotate(0deg)'; } }); if (content.style.maxHeight) { content.style.maxHeight = null; icon.style.transform = 'rotate(0deg)'; } else { content.style.maxHeight = content.scrollHeight + "px"; icon.style.transform = 'rotate(45deg)'; } } }); } function setupArchitectureDiagram() { const components = document.querySelectorAll('.arch-component'); const tooltip = document.getElementById('arch-tooltip'); const defaultText = tooltip.textContent; components.forEach(component => { component.addEventListener('mouseover', () => { tooltip.textContent = component.dataset.info; tooltip.classList.remove('opacity-0'); }); component.addEventListener('mouseout', () => { tooltip.textContent = defaultText; tooltip.classList.add('opacity-0'); }); }); } function createTimelineChart() { const ctx = document.getElementById('timelineChart').getContext('2d'); new Chart(ctx, { type: 'bar', data: timelineData, options: { indexAxis: 'y', responsive: true, maintainAspectRatio: false, scales: { x: { min: 0, max: 16, title: { display: true, text: 'Timeline in Weeks' } }, y: { grid: { display: false } } }, plugins: { legend: { display: false }, tooltip: { callbacks: { label: function(context) { const phase = context.label; const duration = context.raw\[1\] - context.raw\[0\]; const tasks = timelineTasks\[phase\]; return \`${duration} weeks - ${tasks}\`; } } } } } }); } function setupRiskCards() { const cards = document.querySelectorAll('.risk-card'); cards.forEach(card => { card.addEventListener('click', () => { card.classList.toggle('flipped'); }); }); } // --- INITIALIZATION --- renderTechStack(); renderFeatures(); setupFeatureTabs(); setupArchitectureDiagram(); createTimelineChart(); renderRisks(); setupNavLinks(); });