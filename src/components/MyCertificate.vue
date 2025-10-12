<template>
  <section class="certifications">
   <header>
    <h2 class="section-title" style="font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #1e293b;
    padding: 10px
    ;color: whitesmoke;
    
    ">My Certificates <i class="fa-solid fa-certificate" style="color: #ffffff;"></i> </h2>   
   </header>
    <div class="button-grid">
      <div class="button-wrapper" style=" z-index: 100;">
        <button class="gradient-border-button">
          <a
          style="text-decoration: none;font-size: large ; font-weight: bold; color: #1e293b;"
            href="https://www.panha.pro"
            target="_blank"
            rel="noopener noreferrer"
          >
            <span style="color: aliceblue;">My-Portfolio</span>
          </a>
        </button>
      </div>
    </div>
    <div class="certification-grid">
      <div
        v-for="certification in certifications"
        :key="certification.id"
        class="certification-card"
      >
        <div class="certification-image-container">
          <img
            :src="certification.image"
            :alt="certification.title || 'Certificate Image'"
            class="certification-image"
          />
        </div>
        <div class="certification-content">
          <h3 class="certification-title">
            {{ certification.title  }}
          </h3>
          <p class="certification-organization">
            {{ certification.organization }}
          </p>
        </div>
      </div>
    </div>
    <footer style="margin-top: 30px; position:relative; bottom: 0;">
      <div class="conten-footer" style="background-color: #1e293b; padding: 10px; color: whitesmoke;">
        <div class="copyright">
          <p>Copyright @houtkysopanha | houtkysopanha@gmail.com |  Contact Me via:</p>
         <div class="link" style="display: flex; text-align: center; justify-content: center; margin-top: 5px;">
          <ul style="text-align: center; display: flex;">
            <li><a href="https://t.me/houtKysopanha" target="blank">Telegram</a></li>|
            <li><a href="https://www.linkedin.com/in/hout-ky-sopanha-8597852ba/" target="blank">Linkedin</a></li>|
            <li><a href="tel: +855 99 654 752" target="blank">Phone</a></li>|
            <li><a href="https://www.facebook.com/houtkyso.panha.9/" target="blank">Facebook</a></li>
          </ul>
         </div>
        </div>
      </div>
    </footer>
  </section>
</template>

<script>

export default {
  name: "MyCertificate",
  data() {
    return {
      certifications: [
        { id: 12, image: require("../assets/ai_camtect.jpg"), title: "Build Your AI App | 05, July 2025", organization: "Paragon" },
        { id: 11, image: require("../assets/paragon.jpg"), title: "Website UX/UI Design (Bootcamp) | May 31, June 1,7 and 8 2025", organization: "Paragon" },
        { id: 10, image: require("../assets/Screenshot 2025-03-09 at 9.56.19 in the morning.png"), title: "EdTech Summit Cambodia(Volunteer) | February 17-18, 2025", organization: "MoEYS" },
        { id: 3, image: require("../assets/Nov-2024.png"), title: "Time Management | November 19, 2024", organization: "Linkedin Learning" },
        { id: 1, image: require("../assets/Dev-nov-3-24.jpeg"), title: "DevSecops Bootcamp | November 03, 2024", organization: "Instinct Institute"},
        { id: 2, image: require("../assets/13-july-24-web.jpeg"), title: "Basic Web Development | July 13, 2024", organization: "Instinct Institute"},
        { id: 4, image: require("../assets/4-may-24.png"), title: "Humanitarian Websites and Portals for Nutrition information Management | May 04, 2024", organization: "Unicef Agora" },
        { id: 5, image: require("../assets/8-feb-24.png"),title: "Developing and Maintaining data and management system | Febuary 08, 2024", organization: "Unicef Agora" },
        { id: 6, image: require("../assets/8-feb-24(2).png"), title: "Developing and IM Work Plan | Febuary 08, 2024", organization: "Unicef Agora" },
        { id: 7, image: require("../assets/18-feb-24.png"),title: "Web Accessibility Training | Febuary 18, 2024", organization: "Unicef Agora" },
        { id: 8, image: require("../assets/march-2023.jpg"), title: "Mathematic PCH | March 12, 2023", organization: "MPCH" },
        { id: 9, image: require("../assets/nov-2022.jpg"),title: "Physics and Astronomy| October 29, 2022", organization: "COPERNICOS" },
      ],
    };
  },
};
</script>

<style scoped>
/* Root variables for consistent theming */
:root {
  --primary-color: #1e293b;
  --primary-light: #334155;
  --accent-color: #60a5fa;
  --accent-secondary: #a78bfa;
  --accent-tertiary: #f472b6;
  --text-primary: #1f2937;
  --text-secondary: #6b7280;
  --text-muted: #9ca3af;
  --white: #ffffff;
  --glass-bg: rgba(255, 255, 255, 0.9);
  --glass-border: rgba(255, 255, 255, 0.2);
  --shadow-light: 0 2px 8px rgba(0, 0, 0, 0.08);
  --shadow-medium: 0 8px 25px rgba(0, 0, 0, 0.12);
  --shadow-heavy: 0 20px 40px rgba(0, 0, 0, 0.15);
  --shadow-glow: 0 0 30px rgba(96, 165, 250, 0.2);
  --border-radius: 16px;
  --border-radius-sm: 8px;
  --transition-fast: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
  --transition-smooth: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  --transition-bounce: all 0.6s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.certifications {
  color: var(--text-primary);
  text-align: center;
  padding: clamp(1rem, 4vw, 3rem) clamp(0.5rem, 2vw, 2rem);
  min-height: 100vh;
  background: 
    radial-gradient(circle at 20% 80%, rgba(96, 165, 250, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(167, 139, 250, 0.1) 0%, transparent 50%),
    linear-gradient(135deg, #f8fafc 0%, #f1f5f9 50%, #e2e8f0 100%);
  position: relative;
  overflow-x: hidden;
}

.certifications::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 200px;
  background: linear-gradient(180deg, rgba(248, 250, 252, 0.8) 0%, transparent 100%);
  pointer-events: none;
  z-index: 1;
}

.section-title {
  font-size: clamp(1.8rem, 4vw, 2.5rem);
  font-weight: 700;
  margin-bottom: clamp(1.5rem, 3vw, 2.5rem);
  color: var(--text-primary);
  line-height: 1.2;
  position: relative;
  z-index: 2;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  animation: fadeInUp 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.certification-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(100%, 350px), 1fr));
  gap: clamp(1rem, 2.5vw, 2rem);
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 clamp(0.5rem, 2vw, 1rem);
  position: relative;
  z-index: 2;
}

.certification-grid > * {
  animation: fadeInScale 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94) forwards;
  opacity: 0;
  transform: translateY(30px) scale(0.95);
}

.certification-grid > *:nth-child(1) { animation-delay: 0.1s; }
.certification-grid > *:nth-child(2) { animation-delay: 0.2s; }
.certification-grid > *:nth-child(3) { animation-delay: 0.3s; }
.certification-grid > *:nth-child(4) { animation-delay: 0.4s; }
.certification-grid > *:nth-child(5) { animation-delay: 0.5s; }
.certification-grid > *:nth-child(6) { animation-delay: 0.6s; }
.certification-grid > *:nth-child(n+7) { animation-delay: 0.7s; }

.certification-card {
  background: var(--glass-bg);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border-radius: var(--border-radius);
  overflow: hidden;
  box-shadow: var(--shadow-light);
  transition: var(--transition-smooth);
  position: relative;
  height: fit-content;
  border: 1px solid var(--glass-border);
  cursor: pointer;
}

.certification-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
  transition: left 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  z-index: 1;
}

.certification-card:hover::before {
  left: 100%;
}

.certification-card:hover {
  transform: translateY(-12px) scale(1.03) rotateX(5deg);
  box-shadow: var(--shadow-heavy), var(--shadow-glow);
  border-color: var(--accent-color);
  background: rgba(255, 255, 255, 0.95);
}

.certification-image-container {
  width: 100%;
  position: relative;
  overflow: hidden;
  background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
  aspect-ratio: 16 / 9;
  display: flex;
  align-items: center;
  justify-content: center;
}

.certification-image-container::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, rgba(96, 165, 250, 0.1) 0%, rgba(167, 139, 250, 0.1) 100%);
  opacity: 0;
  transition: var(--transition-smooth);
  z-index: 1;
}

.certification-card:hover .certification-image-container::after {
  opacity: 1;
}

.certification-image {
  width: 100%;
  height: 100%;
  object-fit: contain;
  object-position: center;
  transition: var(--transition-smooth);
  border-radius: 0;
  background: var(--white);
  filter: brightness(1) saturate(1);
  position: relative;
  z-index: 0;
}

.certification-card:hover .certification-image {
  transform: scale(1.08) rotate(1deg);
  filter: brightness(1.1) saturate(1.2);
}

.certification-content {
  padding: clamp(1rem, 2.5vw, 1.5rem);
  text-align: left;
  background: transparent;
  position: relative;
  z-index: 2;
  transition: var(--transition-smooth);
}

.certification-card:hover .certification-content {
  transform: translateY(-2px);
}

.certification-title {
  font-size: clamp(0.95rem, 2vw, 1.1rem);
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: var(--text-primary);
  line-height: 1.4;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  transition: var(--transition-fast);
  position: relative;
}

.certification-title::after {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, var(--accent-color), var(--accent-secondary));
  transition: var(--transition-smooth);
}

.certification-card:hover .certification-title::after {
  width: 100%;
}

.certification-card:hover .certification-title {
  color: var(--primary-color);
}

.certification-organization {
  font-size: clamp(0.85rem, 1.8vw, 0.95rem);
  color: var(--text-secondary);
  font-weight: 500;
  margin-bottom: 0.25rem;
  transition: var(--transition-fast);
  position: relative;
}

.certification-card:hover .certification-organization {
  color: var(--accent-color);
  transform: translateX(4px);
}

.certification-date {
  font-size: clamp(0.8rem, 1.6vw, 0.9rem);
  color: var(--text-muted);
  font-weight: 400;
}

.view-certificate-link {
  display: inline-block;
  margin-top: 1rem;
  color: var(--accent-color);
  font-size: 0.9rem;
  text-decoration: none;
  border: 2px solid var(--accent-color);
  padding: 0.5rem 1rem;
  border-radius: 6px;
  transition: var(--transition);
  font-weight: 500;
}

.view-certificate-link:hover {
  background: var(--accent-color);
  color: var(--white);
  transform: translateY(-1px);
}

.button-grid {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: clamp(1.5rem, 3vw, 2.5rem);
}

.button-wrapper {
  display: inline-flex;
  position: relative;
}

/* Enhanced Gradient Border Button */
.gradient-border-button {
  position: relative;
  padding: clamp(0.8rem, 2vw, 1.2rem) clamp(1.5rem, 3vw, 2.4rem);
  font-size: clamp(0.95rem, 2vw, 1.1rem);
  color: var(--primary-color);
  background: var(--glass-bg);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  border: none;
  border-radius: 12px;
  cursor: pointer;
  transition: var(--transition-bounce);
  font-weight: 600;
  letter-spacing: 0.025em;
  overflow: hidden;
  animation: pulse 3s ease-in-out infinite;
}

.gradient-border-button::before {
  content: "";
  position: absolute;
  inset: -3px;
  background: linear-gradient(45deg, var(--accent-color), var(--accent-secondary), var(--accent-tertiary), var(--accent-color));
  border-radius: 15px;
  z-index: -1;
  transition: var(--transition-smooth);
  animation: borderRotate 6s linear infinite;
  filter: blur(0.5px);
}

.gradient-border-button::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  background: radial-gradient(circle, rgba(255, 255, 255, 0.3) 0%, transparent 70%);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: var(--transition-smooth);
  z-index: 1;
}

.gradient-border-button:hover::after {
  width: 200px;
  height: 200px;
}

.gradient-border-button:hover {
  transform: translateY(-5px) scale(1.05);
  box-shadow: 
    0 15px 35px rgba(96, 165, 250, 0.4),
    0 5px 15px rgba(167, 139, 250, 0.3);
  background: rgba(255, 255, 255, 0.95);
}

@keyframes borderRotate {
  0% { 
    filter: hue-rotate(0deg);
    transform: rotate(0deg);
  }
  100% { 
    filter: hue-rotate(360deg);
    transform: rotate(360deg);
  }
}

@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInScale {
  0% {
    opacity: 0;
    transform: translateY(30px) scale(0.95);
  }
  100% {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

@keyframes pulse {
  0%, 100% {
    box-shadow: 0 0 20px rgba(96, 165, 250, 0.2);
  }
  50% {
    box-shadow: 0 0 30px rgba(96, 165, 250, 0.4);
  }
}

@keyframes shimmer {
  0% {
    background-position: -200% 0;
  }
  100% {
    background-position: 200% 0;
  }
}

/* Footer Styles */
ul {
  margin: 0;
  padding: 0;
}

ul li {
  list-style-type: none;
  display: inline-block;
}

ul li a {
  text-decoration: none;
  color: whitesmoke;
  padding: 0.4rem 0.8rem;
  font-size: clamp(0.8rem, 1.8vw, 0.9rem);
  transition: var(--transition-smooth);
  border-radius: var(--border-radius-sm);
  position: relative;
  overflow: hidden;
  font-weight: 500;
}

ul li a::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.5s ease;
}

ul li a:hover::before {
  left: 100%;
}

ul li a:hover {
  background: rgba(255, 255, 255, 0.15);
  transform: translateY(-2px) scale(1.05);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  color: var(--accent-color);
}

.copyright p {
  font-size: clamp(0.8rem, 1.6vw, 0.9rem);
  margin: 0.5rem 0;
  line-height: 1.4;
}

.link {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 0.5rem;
  flex-wrap: wrap;
  gap: 0.2rem;
}

/* Responsive Media Queries */
@media (max-width: 1200px) {
  .certification-grid {
    grid-template-columns: repeat(auto-fill, minmax(min(100%, 320px), 1fr));
    gap: 1.5rem;
  }
}

@media (max-width: 768px) {
  .certifications {
    padding: 1.5rem 0.75rem;
  }
  
  .certification-grid {
    grid-template-columns: repeat(auto-fill, minmax(min(100%, 280px), 1fr));
    gap: 1.25rem;
  }
  
  .certification-content {
    text-align: center;
  }
  
  .link {
    flex-direction: column;
    gap: 0.5rem;
  }
  
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.25rem;
  }
}

@media (max-width: 480px) {
  .certifications {
    padding: 1rem 0.5rem;
  }
  
  .certification-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
  
  .certification-card {
    margin: 0 auto;
    max-width: 100%;
  }
  
  .gradient-border-button {
    padding: 0.75rem 1.5rem;
    font-size: 0.95rem;
  }
  
  ul li a {
    font-size: 0.75rem;
    padding: 0.25rem 0.4rem;
  }
  
  .copyright p {
    font-size: 0.75rem;
  }
}

@media (max-width: 320px) {
  .certification-image-container {
    aspect-ratio: 4 / 3;
  }
  
  .certification-title {
    font-size: 0.9rem;
  }
  
  .certification-organization {
    font-size: 0.8rem;
  }
}

/* High-resolution display optimization */
@media (min-resolution: 2dppx) {
  .certification-image {
    image-rendering: -webkit-optimize-contrast;
    image-rendering: crisp-edges;
  }
}

/* Dark mode support (optional) */
@media (prefers-color-scheme: dark) {
  .certifications {
    background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
    color: #f8fafc;
  }
  
  .certification-card {
    background: #1e293b;
    border-color: #334155;
  }
  
  .certification-title {
    color: #f8fafc;
  }
  
  .certification-organization {
    color: #cbd5e1;
  }
  
  .certification-date {
    color: #94a3b8;
  }
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Loading state */
.certification-card.loading {
  background: linear-gradient(90deg, #f0f0f0 25%, #e0e0e0 50%, #f0f0f0 75%);
  background-size: 200% 100%;
  animation: shimmer 2s infinite;
}

/* Focus states for accessibility */
.certification-card:focus-within,
.gradient-border-button:focus,
ul li a:focus {
  outline: 2px solid var(--accent-color);
  outline-offset: 2px;
  border-radius: var(--border-radius-sm);
}

/* Reduced motion preferences */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
  
  .certification-card:hover {
    transform: none;
  }
  
  .gradient-border-button:hover {
    transform: none;
  }
}

/* High contrast mode */
@media (prefers-contrast: high) {
  .certification-card {
    border: 2px solid var(--text-primary);
  }
  
  .certification-title {
    font-weight: 700;
  }
}

/* Print styles */
@media print {
  .certification-card {
    break-inside: avoid;
    box-shadow: none;
    border: 1px solid #ccc;
    background: white !important;
  }
  
  .gradient-border-button {
    display: none;
  }
  
  .certifications::before {
    display: none;
  }
}
</style>
