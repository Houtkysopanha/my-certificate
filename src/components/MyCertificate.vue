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
            <span>My-Portfolio</span>
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
.certifications {
  color: #333;
  text-align: center;
  padding: 2rem 1rem;
}

.section-title {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 2rem;
  color: #000;
}

.certification-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 2fr));
  gap: 1.5rem;
}

.certification-card {
  background: #ffffff;
  /* border-radius: 15px; */
  overflow: hidden;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}

.certification-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3);
}

.certification-image-container {
  width: 100%;
  overflow: hidden;
}

.certification-image {
  width: auto;
  height: 330px;
  object-fit: cover;
  transition: transform 0.4s ease;
}

.certification-card:hover .certification-image {
  transform: scale(1.1);
}

.certification-content {
  /* padding: 1.5rem; */
  text-align: center;
}

.certification-title {
  font-size: 1.25rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
  color: #333;
}

.certification-organization {
  font-size: 1rem;
  color: #777;
  margin-bottom: 0.5rem;
}

.certification-date {
  font-size: 0.9rem;
  color: #555;
}

.view-certificate-link {
  display: inline-block;
  margin-top: 1rem;
  color: #007bff;
  font-size: 0.9rem;
  text-decoration: none;
  border: 1px solid #007bff;
  padding: 0.5rem 1rem;
  border-radius: 5px;
  transition: all 0.3s ease;
}

.view-certificate-link:hover {
  background: #007bff;
  color: #fff;
}

.button-grid {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 2rem;
}

.button-wrapper {
  display: inline-flex;
}

/* Gradient Border Button */
.gradient-border-button {
  position: relative;
  padding: 1.2rem 2.4rem;
  font-size: 1.1rem;
  color: white;
  /* background: #1e293b; */
  color: #1e293b;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.gradient-border-button::before {
  content: "";
  position: absolute;
  inset: -3px;
  background: linear-gradient(45deg, #60a5fa, #a78bfa, #60a5fa);
  border-radius: 10px;
  z-index: -1;
  transition: opacity 0.3s ease;
  animation: borderRotate 4s linear infinite;
}
ul li{
  list-style-type: none;
}
ul li a{
  margin-top: 10px;
  text-decoration: none;
  list-style-type: none;
  color: whitesmoke;
  padding: 0.5rem;
}

@keyframes borderRotate {
  0% {
    filter: hue-rotate(0deg);
  }
  100% {
    filter: hue-rotate(360deg);
  }
}

.gradient-border-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(96, 165, 250, 0.4);
}

/* Media Queries */
@media (max-width: 1200px) {
  .section-title {
    font-size: 2rem;
  }

  .certification-grid {
    grid-template-columns: repeat(auto-fit, minmax(400px, 2fr));
  }

  .certification-title {
    font-size: 1rem;
  }
  .certification-image {
  width: 100%;
  height: auto;
  object-fit: cover;
  transition: transform 0.4s ease;
}
}
@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }

  .certification-grid {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  }

  .certification-title {
    font-size: 1rem;
  }
  .certification-image {
  width: 100%;
  height: auto;
  object-fit: cover;
  transition: transform 0.4s ease;
}
.copyright p{
  font-size: 10px;
}
ul li a{
  font-size: 10px;
}
}
@media (max-width: 480px) {
  .section-title {
    font-size: 1.5rem;
  }

  .certification-title {
    font-size: 0.9rem;
  }

  .gradient-border-button {
    /* padding: 1rem 2rem; */
    font-size: 1rem;
  }
  .certification-image {
  width: 100%;
  height: auto;
  object-fit: cover;
  transition: transform 0.4s ease;
}
.copyright p{
  font-size: 10px;
}
ul li a{
  font-size: 10px;
}
}


</style>
