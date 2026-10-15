<script setup>
import { ref } from 'vue'

const showAllPartners = ref(false)
</script>

<template>
  <div class="main-container">
    
    <section id="hero" class="hero-section">
      <div class="hero-overlay"></div>
      
      <div class="hero-content-wrapper">
        <div class="hero-center-emblem">
          <img src="/images/cpu_seal.png" alt="CPU Seal" class="center-seal-img" />
        </div>
        
        <div class="hero-text-block">
          <p class="hero-subtitle">the CCS core practices that build bridges between gaps</p>
          <h1 class="hero-title">
            REMEMBER<br>
            CONNECT<br>
            ENGAGE<br>
            BUILD<br>
            SHARE
          </h1>
          <p class="hero-tagline">different PEOPLE, ONE goal</p>
          <RouterLink to="/#programs" class="cta-btn">Your FUTURE begins HERE</RouterLink>
        </div>
      </div>
    </section>

<section id="programs" class="programs-section">
  <div class="section-header">
    <h2>Academic Programs</h2>
    <p>Shaping future tech professionals through rigorous computing education.</p>
  </div>
  <div class="programs-grid">
    
    <div class="program-card">
      <div class="card-top-row">
        <span class="program-badge">BSIT</span>
        <img src="/images/cpu_itso.png" alt="ITSO Logo" class="program-logo" />
      </div>
      <h3>Information Technology</h3>
      <p>Focuses on enterprise system administration, networking, web technologies, and software deployment.</p>
    </div>

    <div class="program-card">
      <div class="card-top-row">
        <span class="program-badge">BSCS</span>
        <img src="/images/cpu_css.png" alt="CSS Logo" class="program-logo" />
      </div>
      <h3>Computer Science</h3>
      <p>Centers on advanced algorithms, software engineering theory, data structures, and intelligent systems.</p>
    </div>

    <div class="program-card">
      <div class="card-top-row">
        <span class="program-badge">BSDMIA</span>
        <img src="/images/cpu_midas.png" alt="MIDAS Logo" class="program-logo" />
      </div>
      <h3>Digital Media & Interactive Arts</h3>
      <p>Equips students with cutting-edge skills in 3D modeling, game development, and multimedia animation.</p>
    </div>

    <div class="program-card">
      <div class="card-top-row">
        <span class="program-badge">BLIS</span>
        <img src="/images/cpu_lisso.png" alt="LISSO Logo" class="program-logo" />
      </div>
      <h3>Library & Information Science</h3>
      <p>Focuses on modern information architecture, digital libraries, and knowledge management systems.</p>
    </div>

  </div>
</section>

    <section id="faculty" class="faculty-section">
      <div class="section-header">
        <h2>Faculty & Staff</h2>
        <p>The esteemed mentors guiding the College of Computer Studies.</p>
      </div>

      <div class="department-group">
        <h3>Computer Science Department</h3>
        <div class="faculty-grid">
          <div class="faculty-card">
            <div class="faculty-img-box">
              <img src="/images/dean_spiderman.jpg" alt="Faculty Member" />
            </div>
            <h4>Prof. Ma. Christina A. Quijano</h4>
            <p class="faculty-qual">M.S. Computer Science</p>
            <span class="faculty-role">Dean</span>
          </div>
        </div>
      </div>

      <div class="department-group">
        <h3>Information Technology Department</h3>
        <div class="faculty-grid">
          <div class="faculty-card">
            <div class="faculty-img-box">
              <img src="/images/dean_spiderman.jpg" alt="Faculty Member" />
            </div>
            <h4>Prof. Rea P. Balontong</h4>
            <p class="faculty-qual">M.S. Business Administration</p>
            <span class="faculty-role">Department Head</span>
          </div>
        </div>
      </div>
    </section>

    <section id="partnerships" class="partnerships-section">
      <div class="section-header">
        <h2>Partnerships & Memberships</h2>
        <p>Collaborating with student organizations and industry leaders.</p>
      </div>
      <div class="partners-wrapper">
        <div class="partner-card">
          <img src="/images/cpu_ccs_council.png" alt="CCS Provincial Council Seal" class="council-logo" />
          <div class="partner-info">
            <h3>CCS Provincial Council</h3>
            <p>The official student governing body of the College of Computer Studies, uniting students through academic events, tech symposiums, and community outreach.</p>
          </div>
        </div>

        <div class="logos-container">
      <div class="logos-grid">
        <div class="logo-box">
          <img src="/images/partner_oracle.png" alt="Oracle Academy" />
        </div>
        <div class="logo-box">
          <img src="/images/partner_cisco.webp" alt="Cisco Networking Academy" />
        </div>
        <div class="logo-box">
          <img src="/images/partner_huawei.png" alt="Huawei ICT Academy" />
        </div>
      </div>
      <div v-if="showAllPartners" class="logos-grid expanded-grid">
        <div class="logo-box">
          <img src="/images/partner_psite.png" alt="PSITE" />
        </div>
        <div class="logo-box">
          <img src="/images/partner_govesmart.webp" alt="Govesmart" />
        </div>
        <div class="logo-box">
          <img src="/images/partner_mayad.png" alt="Mayad" />
        </div>
        <div class="logo-box">
          <img src="/images/partner_lasortech.avif" alt="Lasortech" />
        </div>
      </div>

      <div class="toggle-btn-container">
        <button @click="showAllPartners = !showAllPartners" class="view-more-btn">
          {{ showAllPartners ? 'VIEW LESS' : 'VIEW MORE' }}
        </button>
      </div>
    </div>
    </div>
  </section>
  </div>
</template>

<style scoped>
.main-container {
  padding-top: 60px;
  background-color: #001a33;
  color: #f1f5f9;
}
section {
  padding: 6rem 2rem;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
section:nth-child(odd) {
  background-color: #001a33;
}
section:nth-child(even) {
  background-color: #002244;
}
.hero-section {
  position: relative;
  width: 100%;
  background: url('/images/cpu_ccs_council.png') no-repeat center center/cover;
  text-align: left;
  display: flex;
  align-items: center;
}
.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, rgba(0, 34, 68, 0.95) 40%, rgba(0, 26, 51, 0.88) 100%);
  z-index: 1;
}
.hero-content-wrapper {
  position: relative;
  z-index: 2;
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}
.hero-center-emblem {
  display: flex;
  justify-content: flex-start;
}
.center-seal-img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid #ffcc00;
  box-shadow: 0 4px 15px rgba(0,0,0,0.4);
}

.hero-text-block {
  max-width: 650px;
}
.hero-subtitle {
  font-size: 0.9rem;
  color: #ffcc00;
  margin-bottom: 1rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: 600;
}
.hero-title {
  font-size: 2.8rem;
  font-weight: 900;
  line-height: 1.15;
  color: #ffffff;
  margin-bottom: 1rem;
  letter-spacing: 0.5px;
}
.hero-tagline {
  font-size: 1.25rem;
  color: #ffcc00;
  font-weight: 600;
  margin-bottom: 2rem;
}
.cta-btn {
  display: inline-block;
  background-color: #ffcc00;
  color: #002244;
  padding: 0.85rem 2rem;
  font-weight: 700;
  border-radius: 4px;
  text-decoration: none;
  transition: background-color 0.2s, transform 0.2s;
}
.cta-btn:hover {
  background-color: #e6b800;
  transform: translateY(-2px);
}

.section-header {
  text-align: center;
  max-width: 700px;
  margin-bottom: 3.5rem;
}
.section-header h2 {
  font-size: 2.2rem;
  color: #ffffff;
  margin-bottom: 0.5rem;
}
.section-header p {
  color: #cbd5e1;
  font-size: 1rem;
}

.programs-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 2rem;
  max-width: 1100px;
  width: 100%;
}
.program-card {
  background: #002b5c;
  border-top: 4px solid #ffcc00;
  padding: 2rem 1.8rem;
  border-radius: 8px;
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.25);
  transition: transform 0.3s ease, border-color 0.3s ease;
  display: flex;
  flex-direction: column;
}
.program-card:hover {
  transform: translateY(-5px);
}
.card-top-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1.2rem;
}
.program-badge {
  display: inline-block;
  background-color: rgba(255, 204, 0, 0.15);
  color: #ffcc00;
  font-weight: bold;
  padding: 0.35rem 0.8rem;
  border-radius: 4px;
  font-size: 0.85rem;
}
.program-logo {
  width: 115px;
  height: 115px;
  object-fit: contain;
  filter: drop-shadow(0 2px 4px rgba(0,0,0,0.3));
}
.program-card h3 {
  font-size: 1.2rem;
  color: #ffffff;
  margin-bottom: 0.75rem;
}
.program-card p {
  color: #cbd5e1;
  font-size: 0.9rem;
  line-height: 1.5;
}

.department-group {
  width: 100%;
  max-width: 1100px;
  margin-bottom: 3rem;
}
.department-group h3 {
  font-size: 1.3rem;
  color: #ffcc00;
  border-bottom: 2px solid rgba(255, 204, 0, 0.3);
  padding-bottom: 0.5rem;
  margin-bottom: 1.5rem;
}
.faculty-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}
.faculty-card {
  background: #002b5c;
  border: 1px solid rgba(255, 204, 0, 0.2);
  padding: 1.8rem 1.5rem;
  border-radius: 8px;
  text-align: center;
}
.faculty-img-box {
  width: 100px;
  height: 100px;
  margin: 0 auto 1rem auto;
  border-radius: 50%;
  overflow: hidden;
  border: 2px solid #ffcc00;
}
.faculty-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.faculty-card h4 {
  font-size: 1rem;
  color: #ffffff;
  margin-bottom: 0.3rem;
}
.faculty-qual {
  font-size: 0.82rem;
  color: #cbd5e1;
  margin-bottom: 0.75rem;
}
.faculty-role {
  background: rgba(255, 204, 0, 0.15);
  color: #ffcc00;
  padding: 0.2rem 0.6rem;
  border-radius: 10px;
  font-size: 0.75rem;
  font-weight: 600;
}
.partnerships-section {
  text-align: center;
  width: 100%;
}
.partners-wrapper {
  max-width: 1100px;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 2.5rem;
}
.partners-container {
  max-width: 750px;
  width: 100%;
}
.partner-card {
  background: #002b5c;
  border-left: 4px solid #ffcc00;
  padding: 2rem 2.5rem;
  border-radius: 8px;
  display: flex;
  align-items: center;
  gap: 2rem;
  text-align: left;
  box-shadow: 0 4px 15px rgba(0,0,0,0.25);
}
.council-logo {
  width: 90px;
  height: 90px;
  object-fit: contain;
  flex-shrink: 0;
}
.partner-info h3 {
  color: #ffffff;
  margin-bottom: 0.5rem;
  font-size: 1.25rem;
}
.partner-info p {
  color: #cbd5e1;
  font-size: 0.92rem;
  line-height: 1.5;
  margin: 0;
}
.logos-container {
  background: #002b5c; 
  border-left: 4px solid #ffcc00; 
  padding: 3rem 2rem 2.5rem 2rem;
  border-radius: 8px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.25);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2.5rem;
}
.logos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
  width: 100%;
  align-items: center;
  justify-items: center;
}
.expanded-grid {
  animation: fadeIn 0.4s ease-in-out;
}
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}
.logo-box {
  background: #ffffff;
  border-radius: 8px;
  padding: 1.2rem;
  width: 100%;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.logo-box:hover {
  transform: translateY(-4px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.3);
}
.logo-box img {
  max-width: 180px;
  max-height: 80px;
  width: 100%;
  object-fit: contain;
}
.logo-box img:hover {
  transform: scale(1.05);
}
.toggle-btn-container {
  margin-top: 0.5rem;
}
.view-more-btn {
  background-color: #ff9f0a; 
  color: #ffffff;
  border: none;
  padding: 0.75rem 2.5rem;
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.5px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s ease, transform 0.2s ease;
  text-transform: uppercase;
}
.view-more-btn:hover {
  background-color: #e08b00;
  transform: translateY(-2px);
}
@media (max-width: 768px) {
.partner-card {
    flex-direction: column;
    text-align: center;
  }
  .logos-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>



