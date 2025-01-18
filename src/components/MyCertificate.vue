<template>
  <section class="certifications">
    <h2 class="section-title" style="font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #1e293b;
    padding: 10px
    ;color: whitesmoke;
    
    ">My Certifications</h2>   
    <div class="button-grid">
      <div class="button-wrapper">
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
            {{ certification.title || "Certificate" }}
          </h3>
          <p class="certification-organization">
            {{ certification.organization || "Organization" }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
  name: "MyCertificate",
  data() {
    return {
      certifications: [
        { id: 1, image: require("../assets/Nov-2024.png") },
        { id: 2, image: require("../assets/4-may-24.png") },
        { id: 3, image: require("../assets/8-feb-24.png") },
        { id: 4, image: require("../assets/8-feb-24(2).png") },
        { id: 5, image: require("../assets/18-feb-24.png") },
        { id: 6, image: require("../assets/march-2023.jpg") },
        { id: 7, image: require("../assets/nov-2022.jpg") },
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
  width: 100%;
  height: auto;
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
}
@media (max-width: 480px) {
  .section-title {
    font-size: 1.5rem;
  }

  .certification-title {
    font-size: 0.9rem;
  }

  .gradient-border-button {
    padding: 1rem 2rem;
    font-size: 1rem;
  }
}
</style>
