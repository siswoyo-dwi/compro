<template>
    <!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
        <h2>Portfolio</h2>

        <div class="slider">
        <h3>Profil Lulusan</h3>
        <div class="slide-track">
            <div class="card" v-for="(graduate, index) in graduates" :key="index">
            <h4>{{ graduate.name }}</h4>
            <p>Keterampilan: {{ graduate.skills }}</p>
            <p>Status: Lulusan {{ graduate.year }}</p>
            <p>Proyek Terkenal: {{ graduate.project }}</p>
            <a :href="graduate.linkedin">LinkedIn</a>
            </div>
        </div>
        <button class="prev" @click="moveSlide(-1)">&#10094;</button>
        <button class="next" @click="moveSlide(1)">&#10095;</button>
        </div>

        <div class="slider">
        <h3>Profil Proyek</h3>
        <div class="slide-track">
            <div class="card" v-for="(project, index) in projects" :key="index">
            <h4>{{ project.title }}</h4>
            <p>Deskripsi: {{ project.description }}</p>
            <p>Teknologi: {{ project.technology }}</p>
            <p>Tahun: {{ project.year }}</p>
            <a :href="project.github">GitHub</a>
            </div>
        </div>
        <button class="prev" @click="moveSlide(-1)">&#10094;</button>
        <button class="next" @click="moveSlide(1)">&#10095;</button>
        </div>
    </section>
</template>
<script>
export default {
  components: {
  },
  props: [ 'projects','graduates' ],
  data() {
    return {
        autoSlideInterval:null,
        currentIndex:0
    };
  },
  async mounted() {
    // Trigger animations on scroll
const options = { threshold: 0.3 };
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, options);

    const sections = document.querySelectorAll('.section');
    sections.forEach(section => {
      observer.observe(section);
    });

    // Start automatic slide
    this.startAutoSlide();
  },
  beforeUnmount() {
    // Clear the interval when the component is destroyed
    clearInterval(this.autoSlideInterval);
  },
  methods: {
    moveSlide(direction) {
      const slides = document.querySelectorAll('.slide-track');
      let maxChildren =0
        for (let i = 0; i < slides.length; i++) {
            if (slides[i].children.length>maxChildren) {
                maxChildren = slides[i].children.length
            }            
        }
      const totalSlides = Math.ceil(maxChildren/3)
        
      this.currentIndex += direction;
      if (this.currentIndex < 0) this.currentIndex = totalSlides - 1;
      if (this.currentIndex >= totalSlides) this.currentIndex = 0;

      slides.forEach(slide => {
        slide.style.transform = `translateX(-${this.currentIndex * 100}%)`;
      });
    },
    startAutoSlide() {
      this.autoSlideInterval = setInterval(() => {
        this.moveSlide(1);
      }, 3000); // Change slide every 3 second
    }
    
  },
};
</script>
<style>

.portfolio {
    max-width: 1200px;
    margin: auto;
    padding: 20px;
    background: white;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

h2 {
    text-align: center;
    color: #333;
}

h3 {
    margin-top: 20px;
    color: #555;
}

.slider {
    position: relative;
    overflow: hidden;
    margin-bottom: 40px;
}

.slide-track {
    display: flex;
    transition: transform 0.3s ease;
}

.card {
    background: #f9f9f9;
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 15px;
    flex: 0 0 300px;
    margin: 0 10px;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.2);
}

.card h4 {
    margin: 0 0 10px;
    color: #333;
}

.card p {
    margin: 5px 0;
}

.card a {
    text-decoration: none;
    color: #007bff;
    font-weight: bold;
}

.card a:hover {
    text-decoration: underline;
}

button {
    /* position: absolute; */
    top: 50%;
    transform: translateY(-50%);
    background: rgba(255, 255, 255, 0.8);
    border: none;
    padding: 10px;
    cursor: pointer;
    font-size: 18px;
}

.prev {
    left: 10px;
}

.next {
    right: 10px;
}

</style>