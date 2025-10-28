<script>
  import ExperienceTimeline from '$lib/components/ExperienceTimeline.svelte';
  import ProjectCard from '$lib/components/ProjectCard.svelte';

  const about = `A Cum Laude graduate in Computer Science, I am a dedicated Full Stack Developer with proven expertise in MERN (React, Node.js), PHP (Laravel/CakePHP) and database management. I specialize in building and deploying efficient web solutions, including extensive experience as a CMS Developer, primarily utilizing WordPress for complex, versatile website projects. I contributed to real-world projects at My Creative Panda Inc. and offer technical versatility gained through PC support, graphic design, and managing printing operations. I am a collaborative problem-solver who continuously seeks to learn new technologies and deliver high-quality professional results.`;

  const experiences = [
    {
      role: 'Freelance Web Developer',
      company: 'Self-employed',
      dates: '2025 - Present',
      summary: 'I designed, developed, and deployed Full Stack web applications, including complex systems like Property Management System, utilizing Node.js, PHP, Laravel, and CakePHP with databases such as MySQL and PostgreSQL. I also developed and maintained corporate websites, including real estate platform, leveraging WordPress and PHP.'
    },
    {
      role: 'DG Computer Services',
      company: 'Managed IT Support',
      dates: '2025 - Present',
      summary: 'Managed all printing operations, including large-format output, while also functioning as a Graphic Designer for print and digital projects. Provided comprehensive customer support through troubleshooting hardware and software problems, and performing device reformatting and optimization to ensure client satisfaction and device functionality.'
    },
    {
      role: 'Full Stack Developer',
      company: 'My Creative Panda Inc.',
      dates: '2025',
      summary: 'Assisted in developing websites using the CakePHP framework and WordPress. Applied technical and functional web solutions. Utilized computer skills to work with various development tools and software. Collaborated with senior developers and project teams to complete client-based projects efficiently.'
    },
    {
      role: 'Full Stack Developer Intern',
      company: 'IPhiTech IT and Digital Solutions Corporation',
      dates: '2023',
      summary: 'Utilized technical skills and problem solving skills on developing websites. Utilized computer skills on software used on developing websites. Collaborated with fellow interns and mentors throughout the internship to create projects.'
    }
  ];

  const projects = [
    {
      title: 'RLC Residences Website',
      description: 'Developed and managed a professional, lead-generating website for an Accredited Senior International Property Specialist promoting RLC Residences (Richmond Land Corp).',
      tech: ['HTML', 'CSS', 'JavaScript', 'PHP', 'WordPress'],
      year: '2024',
      url: 'https://rlcpropertiesdv.com/',
      image: 'https://images.unsplash.com/photo-1560472354-b33ff0c44a43?w=800&h=500&fit=crop&crop=entropy&auto=format&q=80',
      preview: 'https://via.placeholder.com/400x250/ef4444/ffffff?text=RLC+Properties+Preview'
    },
    {
      title: 'Umap-it Website',
      description: 'An interactive learning website with a map-inspired flowchart design for U-substitution in calculus, providing an engaging educational experience.',
      tech: ['HTML', 'CSS', 'JavaScript', 'WordPress'],
      year: '2023',
      url: 'http://umapit.it.com/',
      image: 'https://images.unsplash.com/photo-1509228468518-180dd4864904?w=800&h=500&fit=crop&crop=entropy&auto=format&q=80',
      preview: 'https://via.placeholder.com/400x250/3b82f6/ffffff?text=Umap-it+Learning+Platform'
    }
  ];

  const certificates = [
    {
      title: 'Work Ethics and Safe Spaces ACT',
      issuer: 'WESSA 2023',
      date: 'March 10, 2023',
      category: 'Professional Development',
      icon: 'fas fa-briefcase',
      iconColor: 'text-blue-500',
      bgColor: 'bg-blue-100'
    },
    {
      title: 'Personality Development Seminar entitled "ME Version 2.0"',
      issuer: 'IPhiTech IT and Digital Solutions Corporation',
      date: 'April 7th, 2023',
      category: 'Personal Development',
      icon: 'fas fa-user-graduate',
      iconColor: 'text-purple-500',
      bgColor: 'bg-purple-100'
    },
    {
      title: 'Data Visualization using Chart.Js on Web Applications',
      issuer: 'IPhiTech IT and Digital Solutions Corporation',
      date: 'September 9, 2023',
      category: 'Technical Skills',
      icon: 'fas fa-chart-bar',
      iconColor: 'text-green-500',
      bgColor: 'bg-green-100'
    },
    {
      title: '"Choosing The Right Programming Language"',
      issuer: 'IPhiTech IT and Digital Solutions Corporation',
      date: 'August 12, 2023',
      category: 'Programming',
      icon: 'fas fa-code',
      iconColor: 'text-orange-500',
      bgColor: 'bg-orange-100'
    }
  ];

  const technologies = {
    'Programming Languages': [
      { name: 'PHP', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg' },
      { name: 'JavaScript', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg' },
      { name: 'Python', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg' },
      { name: 'Java', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg' }
    ],
    'Frontend': [
      { name: 'React', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg' },
      { name: 'SvelteKit', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/svelte/svelte-original.svg' },
      { name: 'HTML5', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg' },
      { name: 'CSS3', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg' },
      { name: 'Quasar Vue.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/quasar/quasar-original.svg' },
      { name: 'Tailwind CSS', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg' }
    ],
    'Backend': [
      { name: 'Laravel', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-original.svg' },
      { name: 'CakePHP', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cakephp/cakephp-original.svg' },
      { name: 'Node.js', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg' },
    
    ],
    'Database': [
      { name: 'MySQL', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg' },
      { name: 'PostgreSQL', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg' },
      { name: 'Supabase', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/supabase/supabase-original.svg' }
    ],
    'Tools & Others': [
      { name: 'Git', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg' },
      { name: 'WordPress', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/wordpress/wordpress-original.svg' },
      { name: 'Figma', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg' },
      { name: 'Canva', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/canva/canva-original.svg' },
      { name: 'Adobe Creative Suite', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/photoshop/photoshop-plain.svg' }
    ]
  };

  // Form handling
  let formData = {
    name: '',
    email: '',
    message: ''
  };
  
  let isSubmitting = false;
  let submitMessage = '';

  const handleSubmit = async (event) => {
    event.preventDefault();
    isSubmitting = true;
    submitMessage = '';

    try {
      // Option 1: Send to Formspree (free email service)
      const response = await fetch('https://formspree.io/f/movpenbe', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify({
          name: formData.name,
          email: formData.email,
          message: formData.message
        })
      });

      if (response.ok) {
        submitMessage = 'Message sent successfully! I\'ll get back to you soon.';
        // Reset form
        formData = { name: '', email: '', message: '' };
      } else {
        throw new Error('Failed to send message');
      }
      
    } catch (error) {
      // Fallback: mailto link (opens email client)
      const subject = encodeURIComponent('Portfolio Contact from ' + formData.name);
      const body = encodeURIComponent(`Name: ${formData.name}\nEmail: ${formData.email}\n\nMessage:\n${formData.message}`);
      window.location.href = `mailto:donhsanchez001@gmail.com?subject=${subject}&body=${body}`;
      submitMessage = 'Opening your email client...';
    } finally {
      isSubmitting = false;
      // Clear message after 5 seconds
      setTimeout(() => {
        submitMessage = '';
      }, 5000);
    }
  };

  // Scroll to top functionality
  let showScrollTop = false;

  const handleScroll = () => {
    showScrollTop = window.scrollY > 300;
  };

  const scrollToTop = () => {
    window.scrollTo({
      top: 0,
      behavior: 'smooth'
    });
  };

  // Add scroll event listener
  if (typeof window !== 'undefined') {
    window.addEventListener('scroll', handleScroll);
  }

  // Sparkle effects
  let sparkles = [];
  
  const createSparkle = () => {
    if (typeof window !== 'undefined') {
      const sparkle = {
        id: Math.random(),
        x: Math.random() * window.innerWidth,
        y: Math.random() * window.innerHeight,
        size: Math.random() * 4 + 2,
        opacity: Math.random() * 0.5 + 0.3,
        duration: Math.random() * 3000 + 2000
      };
      
      sparkles = [...sparkles.slice(-20), sparkle]; // Keep only last 20 sparkles
      
      setTimeout(() => {
        sparkles = sparkles.filter(s => s.id !== sparkle.id);
      }, sparkle.duration);
    }
  };

  // Create sparkles periodically (reduced frequency for better performance)
  if (typeof window !== 'undefined') {
    setInterval(createSparkle, 2000);
  }

  // Lightbox functionality
  let showLightbox = false;
  let currentProject = null;

  const openLightbox = (project) => {
    currentProject = project;
    showLightbox = true;
    // Prevent body scroll
    if (typeof document !== 'undefined') {
      document.body.style.overflow = 'hidden';
    }
  };

  const closeLightbox = () => {
    showLightbox = false;
    currentProject = null;
    // Restore body scroll
    if (typeof document !== 'undefined') {
      document.body.style.overflow = 'auto';
    }
  };

  // Close lightbox on escape key
  const handleKeydown = (event) => {
    if (event.key === 'Escape' && showLightbox) {
      closeLightbox();
    }
  };

  if (typeof window !== 'undefined') {
    window.addEventListener('keydown', handleKeydown);
  }

  // Lazy loading for project iframes
  let loadedProjects = new Set();
  
  const loadProjectPreview = (projectIndex) => {
    loadedProjects.add(projectIndex);
    loadedProjects = loadedProjects; // Trigger reactivity
  };

  // Intersection Observer for lazy loading
  let projectElements = [];
  
  const setupIntersectionObserver = () => {
    if (typeof window === 'undefined' || !window.IntersectionObserver) return;
    
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const index = parseInt(entry.target.dataset.projectIndex);
          if (!loadedProjects.has(index)) {
            loadProjectPreview(index);
          }
        }
      });
    }, {
      rootMargin: '100px',
      threshold: 0.1
    });

    projectElements.forEach((el, index) => {
      if (el) {
        el.dataset.projectIndex = index;
        observer.observe(el);
      }
    });
  };

  // Setup observer after component mounts
  if (typeof window !== 'undefined') {
    setTimeout(setupIntersectionObserver, 100);
  }


</script>

<section id="home" class="pt-20 pb-32 relative overflow-hidden">
  <!-- Floating geometric elements -->
  <div class="absolute inset-0 pointer-events-none">
    <div class="floating-shape floating-shape-1"></div>
    <div class="floating-shape floating-shape-2"></div>
    <div class="floating-shape floating-shape-3"></div>
    <div class="floating-shape floating-shape-4"></div>
    <div class="floating-shape floating-shape-5"></div>
  </div>
  
  <!-- Dynamic sparkles -->
  <div class="absolute inset-0 pointer-events-none overflow-hidden">
    {#each sparkles as sparkle (sparkle.id)}
      <div 
        class="sparkle"
        style="left: {sparkle.x}px; top: {sparkle.y}px; width: {sparkle.size}px; height: {sparkle.size}px; opacity: {sparkle.opacity};"
      ></div>
    {/each}
  </div>
  
  <div class="max-w-4xl mx-auto px-6 relative z-10">
    <div class="grid md:grid-cols-3 gap-12 items-center">
      <div class="md:col-span-2">
        <h1 class="text-6xl md:text-7xl font-bold text-gray-900 leading-tight">Hector<br><span class="text-red-500">Sanchez</span></h1>
        <div class="text-xl text-red-500 font-semibold mt-4 mb-6">Software/Web Developer</div>
        <p class="text-lg text-gray-600 leading-relaxed max-w-2xl">As a dedicated software developer, I transform ideas into impactful digital solutions. I'm committed to crafting intuitive, high-performance web applications while embracing emerging technologies to deliver exceptional user experiences that drive real results.</p>
        <div class="mt-10 flex flex-col sm:flex-row gap-4 sm:gap-6">
          <a href="#contact" class="px-8 py-4 bg-red-500 text-white font-semibold rounded-lg hover:bg-red-600 transition-all duration-300 text-center">Contact Me</a>
          <a href="#projects" class="px-8 py-4 border-2 border-red-500 text-red-500 font-semibold rounded-lg hover:bg-red-500 hover:text-white transition-all duration-300 text-center">View Projects</a>
        </div>
      </div>
      <div class="hidden md:flex justify-center">
        <div class="relative group profile-container">
          <img 
            src="/hector-sanchez-profile.png" 
            alt="Hector Sanchez - Full Stack Developer" 
            class="w-64 h-64 rounded-full object-cover shadow-2xl transition-all duration-500 group-hover:scale-110 group-hover:shadow-3xl relative z-10"
          />
          <!-- Animated gradient border effect on hover -->
          <div class="absolute inset-0 rounded-full bg-gradient-to-r from-red-500 via-blue-500 to-green-500 opacity-0 group-hover:opacity-30 transition-opacity duration-500 blur-sm"></div>
          
          <!-- Professional badge overlay -->
          <div class="absolute -bottom-4 -right-4 bg-red-500 text-white px-4 py-2 rounded-full text-sm font-bold shadow-lg profile-badge transform transition-all duration-300 z-20">
            <i class="fas fa-code mr-1"></i>
            Developer
          </div>
          
          <!-- Floating skill indicators -->
          <div class="absolute -top-2 -left-2 w-8 h-8 bg-blue-500 rounded-full flex items-center justify-center text-white text-xs font-bold opacity-0 group-hover:opacity-100 transition-all duration-500 delay-100 transform group-hover:scale-110">
            JS
          </div>
          <div class="absolute top-1/2 -right-6 w-8 h-8 bg-green-500 rounded-full flex items-center justify-center text-white text-xs font-bold opacity-0 group-hover:opacity-100 transition-all duration-500 delay-200 transform group-hover:scale-110">
            ⚡
          </div>
          <div class="absolute -bottom-2 left-1/8 w-8 h-8 bg-purple-500 rounded-full flex items-center justify-center text-white text-xs font-bold opacity-0 group-hover:opacity-100 transition-all duration-500 delay-300 transform group-hover:scale-110">
            🚀
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="about" class="py-20 border-t border-gray-700 relative overflow-hidden">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none">
    <div class="floating-shape floating-shape-1 opacity-30"></div>
    <div class="floating-shape floating-shape-3 opacity-20"></div>
  </div>
  
  <div class="max-w-4xl mx-auto px-6 relative z-10">
    <h2 class="text-4xl font-bold text-gray-900 mb-12">About <span class="text-red-500">Me</span></h2>
    <div class="grid md:grid-cols-3 gap-8 mb-12">
      <div class="bg-white rounded-xl p-6 text-center hover:scale-[1.02] transition-all duration-300 border border-gray-200 shadow-sm">
        <div class="w-16 h-16 bg-red-100 rounded-full flex items-center justify-center mx-auto mb-4">
          <span class="text-2xl">💻</span>
        </div>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Web Development</h3>
        <p class="text-gray-600 text-sm">Specializing in creating responsive and user-friendly web applications</p>
      </div>
      <div class="bg-white rounded-xl p-6 text-center hover:scale-[1.02] transition-all duration-300 border border-gray-200 shadow-sm">
        <div class="w-16 h-16 bg-red-100 rounded-full flex items-center justify-center mx-auto mb-4">
          <span class="text-2xl">🎓</span>
        </div>
        <h3 class="text-xl font-bold text-gray-900 mb-2">CS Graduate</h3>
        <p class="text-gray-600 text-sm">Bachelor of Science in Computer Science from Tarlac State University</p>
      </div>
      <div class="bg-white rounded-xl p-6 text-center hover:scale-[1.02] transition-all duration-300 border border-gray-200 shadow-sm">
        <div class="w-16 h-16 bg-red-100 rounded-full flex items-center justify-center mx-auto mb-4">
          <span class="text-2xl">🚀</span>
        </div>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Modern Technologies</h3>
        <p class="text-gray-600 text-sm">Proficient in using the latest web development technologies and frameworks</p>
      </div>
    </div>
    <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
      <p class="text-lg text-gray-700 leading-relaxed">{about}</p>
    </div>
  </div>
</section>

<section id="technologies" class="py-20 border-t border-gray-700 relative overflow-hidden">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none">
    <div class="floating-shape floating-shape-2 opacity-25"></div>
    <div class="floating-shape floating-shape-4 opacity-20"></div>
  </div>
  
  <div class="max-w-4xl mx-auto px-6 relative z-10">
    <h2 class="text-4xl font-bold text-gray-900 mb-12 text-center">Technologies</h2>
    <div class="grid gap-8">
      {#each Object.entries(technologies) as [category, techs], categoryIndex}
        <div class="tech-card bg-white rounded-xl p-6 hover:shadow-lg transition-all duration-300 border border-gray-200">
          <h3 class="text-xl font-bold text-red-500 mb-6 text-center">
            {category}
          </h3>
          <div class="flex flex-wrap gap-4 justify-center">
            {#each techs as tech, techIndex}
              <div class="flex flex-col items-center p-4 bg-gray-50 hover:bg-red-50 rounded-lg transition-all duration-300 cursor-pointer min-w-[80px] group">
                <img 
                  src={tech.icon} 
                  alt={tech.name}
                  class="w-8 h-8 mb-2 transform group-hover:scale-125 transition-transform duration-300 ease-in-out"
                  loading="lazy"
                />
                <span class="text-xs text-gray-700 text-center font-medium">{tech.name}</span>
              </div>
            {/each}
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  @keyframes slideInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes float {
    0%, 100% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-5px);
    }
  }
  
  /* Apply animation to tech cards */
  #technologies .tech-card {
    animation: slideInUp 0.6s ease-out forwards;
    opacity: 1; /* Keep them visible by default */
  }
  
  /* Individual tech items should be visible */
  #technologies .group {
    opacity: 1;
  }
  
  /* Custom scrollbar for the section */
  #technologies::-webkit-scrollbar {
    width: 6px;
  }
  
  #technologies::-webkit-scrollbar-thumb {
    background: #2dd4bf;
    border-radius: 3px;
  }

  /* Scroll to top button animations */
  .scroll-top-btn {
    animation: fadeInUp 0.3s ease-out;
  }

  .scroll-top-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 25px rgba(239, 68, 68, 0.3);
  }

  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  /* Floating geometric shapes */
  .floating-shape {
    position: absolute;
    opacity: 0.6;
    animation-timing-function: ease-in-out;
    animation-iteration-count: infinite;
    animation-direction: alternate;
  }

  .floating-shape-1 {
    width: 80px;
    height: 80px;
    background: linear-gradient(45deg, rgba(239, 68, 68, 0.1), rgba(239, 68, 68, 0.2));
    border-radius: 20px;
    top: 10%;
    left: 10%;
    animation: floatShape1 8s ease-in-out infinite;
  }

  .floating-shape-2 {
    width: 60px;
    height: 60px;
    background: linear-gradient(45deg, rgba(59, 130, 246, 0.1), rgba(59, 130, 246, 0.2));
    border-radius: 50%;
    top: 20%;
    right: 15%;
    animation: floatShape2 6s ease-in-out infinite;
  }

  .floating-shape-3 {
    width: 40px;
    height: 40px;
    background: linear-gradient(45deg, rgba(16, 185, 129, 0.1), rgba(16, 185, 129, 0.2));
    transform: rotate(45deg);
    bottom: 30%;
    left: 5%;
    animation: floatShape3 10s ease-in-out infinite;
  }

  .floating-shape-4 {
    width: 70px;
    height: 70px;
    background: linear-gradient(45deg, rgba(245, 101, 101, 0.1), rgba(245, 101, 101, 0.2));
    border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
    bottom: 15%;
    right: 20%;
    animation: floatShape4 7s ease-in-out infinite;
  }

  .floating-shape-5 {
    width: 50px;
    height: 50px;
    background: linear-gradient(45deg, rgba(139, 92, 246, 0.1), rgba(139, 92, 246, 0.2));
    border-radius: 10px;
    top: 60%;
    right: 5%;
    animation: floatShape5 9s ease-in-out infinite;
  }

  @keyframes floatShape1 {
    0%, 100% { transform: translateY(0px) translateX(0px) rotate(0deg); }
    50% { transform: translateY(-20px) translateX(10px) rotate(5deg); }
  }

  @keyframes floatShape2 {
    0%, 100% { transform: translateY(0px) translateX(0px) scale(1); }
    50% { transform: translateY(-15px) translateX(-10px) scale(1.1); }
  }

  @keyframes floatShape3 {
    0%, 100% { transform: translateY(0px) translateX(0px) rotate(45deg); }
    50% { transform: translateY(-25px) translateX(15px) rotate(50deg); }
  }

  @keyframes floatShape4 {
    0%, 100% { transform: translateY(0px) translateX(0px) rotate(0deg); }
    50% { transform: translateY(-18px) translateX(-12px) rotate(-5deg); }
  }

  @keyframes floatShape5 {
    0%, 100% { transform: translateY(0px) translateX(0px) rotate(0deg); }
    50% { transform: translateY(-22px) translateX(8px) rotate(10deg); }
  }

  /* Enhanced card hover effects with background interaction */
  .tech-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(239, 68, 68, 0.1);
  }

  /* Subtle animation for sections on scroll */
  section {
    position: relative;
  }

  section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(135deg, rgba(255, 255, 255, 0.8) 0%, rgba(248, 250, 252, 0.9) 100%);
    pointer-events: none;
    z-index: 1;
  }

  section > * {
    position: relative;
    z-index: 2;
  }

  /* Sparkle effects */
  .sparkle {
    position: absolute;
    background: radial-gradient(circle, rgba(239, 68, 68, 0.8) 0%, rgba(239, 68, 68, 0.4) 30%, transparent 70%);
    border-radius: 50%;
    animation: sparkleAnimation 2s ease-in-out infinite;
    pointer-events: none;
  }

  @keyframes sparkleAnimation {
    0%, 100% {
      transform: scale(0) rotate(0deg);
      opacity: 0;
    }
    50% {
      transform: scale(1) rotate(180deg);
      opacity: 1;
    }
  }

  /* Enhanced section backgrounds */
  #about, #technologies, #experience, #projects, #certificates, #contact {
    background: rgba(255, 255, 255, 0.7);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.2);
    position: relative;
  }

  /* Subtle gradient overlays for depth */
  #about::after, #technologies::after, #experience::after, #projects::after, #certificates::after, #contact::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(135deg, rgba(239, 68, 68, 0.01) 0%, rgba(59, 130, 246, 0.01) 50%, rgba(16, 185, 129, 0.01) 100%);
    pointer-events: none;
    z-index: 1;
  }

  /* Desktop mockup styles */
  .desktop-mockup {
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
  }

  .desktop-mockup:hover {
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
    transform: translateY(-5px);
  }

  /* Lightbox styles */
  .lightbox-modal {
    backdrop-filter: blur(4px);
  }

  /* Custom scrollbar for lightbox */
  .lightbox-modal ::-webkit-scrollbar {
    width: 8px;
  }

  .lightbox-modal ::-webkit-scrollbar-track {
    background: #f1f1f1;
    border-radius: 4px;
  }

  .lightbox-modal ::-webkit-scrollbar-thumb {
    background: #ef4444;
    border-radius: 4px;
  }

  .lightbox-modal ::-webkit-scrollbar-thumb:hover {
    background: #dc2626;
  }

  /* Responsive iframe sizing */
  @media (max-width: 768px) {
    .desktop-mockup iframe {
      height: 200px;
    }
  }

  /* Animation for modal appearance */
  @keyframes modalSlideIn {
    from {
      opacity: 0;
      transform: scale(0.9) translateY(20px);
    }
    to {
      opacity: 1;
      transform: scale(1) translateY(0);
    }
  }

  .fixed.inset-0 > div {
    animation: modalSlideIn 0.3s ease-out;
  }

  /* Profile picture hover effects */
  .profile-container {
    perspective: 1000px;
  }

  .profile-container:hover .profile-badge {
    transform: scale(1.1) rotate(5deg);
  }

  .profile-badge {
    backdrop-filter: blur(10px);
    border: 2px solid rgba(255, 255, 255, 0.2);
  }

  /* Additional shadow effects */
  .shadow-3xl {
    box-shadow: 0 35px 60px -12px rgba(0, 0, 0, 0.25);
  }

  /* Gradient animation */
  @keyframes gradient-rotate {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }

  .profile-container .group:hover .absolute.inset-0 {
    animation: gradient-rotate 3s linear infinite;
  }
</style>

<section id="experience" class="py-20 border-t border-gray-700 relative overflow-hidden">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none">
    <div class="floating-shape floating-shape-1 opacity-25"></div>
    <div class="floating-shape floating-shape-5 opacity-15"></div>
  </div>
  
  <div class="max-w-4xl mx-auto px-6 relative z-10">
    <h2 class="text-4xl font-bold text-gray-900 mb-12">Experience</h2>
    <div class="space-y-8">
      {#each experiences as entry, index}
        <div class="bg-white rounded-xl p-8 shadow-sm hover:shadow-md transition-all duration-300 border border-gray-200">
          <div class="flex flex-col md:flex-row md:items-start md:justify-between mb-4">
            <div>
              <h3 class="text-xl font-bold text-gray-900">{entry.role}</h3>
              <div class="text-red-500 font-semibold">{entry.company}</div>
            </div>
            <div class="text-sm text-gray-500 mt-2 md:mt-0 bg-gray-100 px-3 py-1 rounded-full">{entry.dates}</div>
          </div>
          <p class="text-gray-700 leading-relaxed">{entry.summary}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<section id="projects" class="py-20 border-t border-gray-700 relative overflow-hidden">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none">
    <div class="floating-shape floating-shape-2 opacity-20"></div>
    <div class="floating-shape floating-shape-3 opacity-25"></div>
  </div>
  
  <div class="max-w-4xl mx-auto px-6 relative z-10">
    <h2 class="text-4xl font-bold text-gray-900 mb-12">Projects</h2>
    <div class="grid md:grid-cols-2 gap-8">
      {#each projects as project, index}
        <div class="bg-white rounded-xl p-8 shadow-sm hover:shadow-md transition-all duration-300 border border-gray-200" bind:this={projectElements[index]}>
          <!-- Desktop-style preview with browser chrome -->
          <div class="w-full bg-gray-100 rounded-lg mb-6 overflow-hidden desktop-mockup">
            <!-- Browser chrome/header -->
            <div class="bg-gray-200 px-4 py-3 flex items-center gap-2">
              <div class="flex gap-2">
                <div class="w-3 h-3 bg-red-400 rounded-full"></div>
                <div class="w-3 h-3 bg-yellow-400 rounded-full"></div>
                <div class="w-3 h-3 bg-green-400 rounded-full"></div>
              </div>
              <div class="flex-1 mx-4">
                <div class="bg-white rounded px-3 py-1 text-xs text-gray-600 truncate">
                  {project.url}
                </div>
              </div>
            </div>
            <!-- Fast loading image preview -->
            <div class="relative h-64 bg-white cursor-pointer" on:click={() => openLightbox(project)}>
              <img 
                src={project.image} 
                alt="{project.title} Preview"
                class="w-full h-full object-cover"
                loading="lazy"
              />
              <!-- Overlay for click interaction -->
              <div class="absolute inset-0 bg-transparent hover:bg-black hover:bg-opacity-5 transition-all duration-300 flex items-center justify-center">
                <div class="opacity-0 hover:opacity-100 transition-opacity duration-300 bg-black bg-opacity-70 text-white px-4 py-2 rounded-lg">
                  <i class="fas fa-expand mr-2"></i>
                  Click to view live site
                </div>
              </div>
            </div>
          </div>
          
          <h3 class="text-2xl font-bold text-gray-900 mb-4">{project.title}</h3>
          <p class="text-gray-700 leading-relaxed mb-6">{project.description}</p>
          <div class="flex flex-wrap gap-2 mb-4">
            {#each project.tech as tech}
              <span class="px-3 py-1 bg-red-100 text-red-600 text-sm font-medium rounded-full">
                {tech}
              </span>
            {/each}
          </div>
          <div class="flex gap-4">
            <!-- <button 
              on:click={() => openLightbox(project)}
              class="inline-flex items-center px-4 py-2 bg-blue-500 text-white font-semibold rounded-lg hover:bg-blue-600 transition-all duration-300"
            >
              <i class="fas fa-expand mr-2"></i>
              View Full Size
            </button> -->
            <a 
              href={project.url} 
              target="_blank" 
              rel="noopener noreferrer"
              class="inline-flex items-center px-4 py-2 bg-red-500 text-white font-semibold rounded-lg hover:bg-red-600 transition-all duration-300"
            >
              <i class="fas fa-external-link-alt mr-2"></i>
              Visit Website
            </a>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- Lightbox Modal -->
{#if showLightbox && currentProject}
  <div 
    class="fixed inset-0 bg-black bg-opacity-80 z-50 flex items-center justify-center p-4"
    on:click={closeLightbox}
  >
    <div 
      class="bg-white rounded-xl shadow-2xl max-w-6xl w-full max-h-full overflow-hidden"
      on:click|stopPropagation
    >
      <!-- Modal Header -->
      <div class="bg-gray-100 px-6 py-4 flex items-center justify-between border-b">
        <div class="flex items-center gap-4">
          <h3 class="text-xl font-bold text-gray-900">{currentProject.title}</h3>
          <div class="flex gap-2">
            {#each currentProject.tech as tech}
              <span class="px-2 py-1 bg-red-100 text-red-600 text-xs font-medium rounded">
                {tech}
              </span>
            {/each}
          </div>
        </div>
        <button 
          on:click={closeLightbox}
          class="p-2 hover:bg-gray-200 rounded-full transition-colors"
        >
          <i class="fas fa-times text-gray-600"></i>
        </button>
      </div>
      
      <!-- Modal Body -->
      <div class="p-6">
        <!-- Desktop mockup in modal -->
        <div class="bg-gray-100 rounded-lg overflow-hidden desktop-mockup mb-6">
          <!-- Browser chrome -->
          <div class="bg-gray-200 px-4 py-3 flex items-center gap-2">
            <div class="flex gap-2">
              <div class="w-3 h-3 bg-red-400 rounded-full"></div>
              <div class="w-3 h-3 bg-yellow-400 rounded-full"></div>
              <div class="w-3 h-3 bg-green-400 rounded-full"></div>
            </div>
            <div class="flex-1 mx-4">
              <div class="bg-white rounded px-3 py-1 text-sm text-gray-600">
                {currentProject.url}
              </div>
            </div>
            <div class="flex gap-2 text-gray-500">
              <i class="fas fa-shield-alt"></i>
              <i class="fas fa-star"></i>
            </div>
          </div>
          <!-- Large website preview -->
          <div class="h-96 bg-white relative">
            <div class="absolute inset-0 flex items-center justify-center bg-gray-100">
              <div class="text-center">
                <div class="animate-spin w-8 h-8 border-4 border-red-500 border-t-transparent rounded-full mx-auto mb-2"></div>
                <p class="text-gray-600 text-sm">Loading website...</p>
              </div>
            </div>
            <iframe 
              src={currentProject.url} 
              class="w-full h-full border-0 relative z-10"
              title="{currentProject.title} Full Preview"
              loading="lazy"
              sandbox="allow-same-origin allow-scripts"
              on:load={() => {
                // Hide loading spinner when iframe loads
                const loadingDiv = document.querySelector('.absolute.inset-0.flex');
                if (loadingDiv) loadingDiv.style.display = 'none';
              }}
            ></iframe>
          </div>
        </div>
        
        <!-- Project details -->
        <div class="grid md:grid-cols-2 gap-6">
          <div>
            <h4 class="text-lg font-semibold text-gray-900 mb-3">About This Project</h4>
            <p class="text-gray-700 leading-relaxed">{currentProject.description}</p>
          </div>
          <div>
            <h4 class="text-lg font-semibold text-gray-900 mb-3">Technologies Used</h4>
            <div class="flex flex-wrap gap-2 mb-4">
              {#each currentProject.tech as tech}
                <span class="px-3 py-2 bg-red-100 text-red-600 font-medium rounded-lg">
                  {tech}
                </span>
              {/each}
            </div>
            <a 
              href={currentProject.url} 
              target="_blank" 
              rel="noopener noreferrer"
              class="inline-flex items-center px-6 py-3 bg-red-500 text-white font-semibold rounded-lg hover:bg-red-600 transition-all duration-300"
            >
              <i class="fas fa-external-link-alt mr-2"></i>
              Open Website
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
{/if}

<section id="education" class="py-20 border-t border-gray-700 relative overflow-hidden">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none">
    <div class="floating-shape floating-shape-4 opacity-20"></div>
    <div class="floating-shape floating-shape-1 opacity-15"></div>
  </div>
  
  <div class="max-w-4xl mx-auto px-6 relative z-10">
    <h2 class="text-4xl font-bold text-gray-900 mb-12">Education</h2>
    <div class="space-y-6">
      <div class="bg-white rounded-xl p-8 shadow-sm border border-gray-200 hover:shadow-md transition-all duration-300">
        <div class="flex flex-col md:flex-row md:items-start justify-between">
          <div class="flex items-start space-x-4">
            <div class="w-12 h-12 bg-red-100 rounded-lg flex items-center justify-center flex-shrink-0">
              <i class="fas fa-university text-red-500 text-xl"></i>
            </div>
            <div>
              <h3 class="text-2xl font-bold text-gray-900">Tarlac State University</h3>
              <div class="text-lg text-red-500 font-semibold mt-2">Bachelor of Science in Computer Science</div>
              <div class="text-gray-600 mt-1">2020-2024</div>
            </div>
          </div>
          <div class="bg-red-100 text-red-600 px-4 py-2 rounded-full font-semibold mt-4 md:mt-0 flex items-center">
            <i class="fas fa-graduation-cap mr-2"></i>
            Cum Laude
          </div>
        </div>
      </div>
      <div class="bg-white rounded-xl p-6 shadow-sm border border-gray-200 hover:shadow-md transition-all duration-300">
        <div class="flex items-start space-x-4">
          <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <i class="fas fa-school text-blue-500"></i>
          </div>
          <div>
            <h4 class="text-lg font-bold text-gray-900 mb-2">Victoria National High School (Senior High)</h4>
            <div class="text-red-500 font-semibold flex items-center">
              <i class="fas fa-medal mr-2"></i>
              With Honors
            </div>
            <div class="text-gray-600 text-sm">2018-2020</div>
          </div>
        </div>
      </div>
      <div class="bg-white rounded-xl p-6 shadow-sm border border-gray-200 hover:shadow-md transition-all duration-300">
        <div class="flex items-start space-x-4">
          <div class="w-10 h-10 bg-green-100 rounded-lg flex items-center justify-center flex-shrink-0">
            <i class="fas fa-school text-green-500"></i>
          </div>
          <div>
            <h4 class="text-lg font-bold text-gray-900 mb-2">Victoria National High School (Junior High)</h4>
            <div class="text-red-500 font-semibold flex items-center">
              <i class="fas fa-medal mr-2"></i>
              With Honors
            </div>
            <div class="text-gray-600 text-sm">2014-2018</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="certificates" class="py-20 border-t border-gray-700 relative overflow-hidden">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none">
    <div class="floating-shape floating-shape-5 opacity-25"></div>
    <div class="floating-shape floating-shape-2 opacity-15"></div>
  </div>
  
  <div class="max-w-4xl mx-auto px-6 relative z-10">
    <h2 class="text-4xl font-bold text-gray-900 mb-12">Certificates</h2>
    <div class="grid md:grid-cols-2 gap-6">
      {#each certificates as cert}
        <div class="bg-white rounded-xl p-6 shadow-sm hover:shadow-md transition-all duration-300 border border-gray-200 hover:border-red-200">
          <div class="flex items-start space-x-4 mb-4">
            <div class="w-12 h-12 {cert.bgColor} rounded-lg flex items-center justify-center flex-shrink-0">
              <i class="{cert.icon} {cert.iconColor} text-xl"></i>
            </div>
            <div class="flex-1">
              <div class="flex justify-between items-start mb-2">
                <div class="bg-red-100 text-red-600 px-3 py-1 rounded-full text-xs font-semibold">
                  {cert.category}
                </div>
                <div class="text-gray-500 text-sm">{cert.date}</div>
              </div>
            </div>
          </div>
          <h3 class="text-lg font-bold text-gray-900 mb-2">{cert.title}</h3>
          <div class="text-red-500 font-semibold text-sm flex items-center">
            <i class="fas fa-certificate mr-2"></i>
            {cert.issuer}
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<section id="contact" class="py-20 border-t border-gray-700 relative overflow-hidden">
  <!-- Background texture -->
  <div class="absolute inset-0 pointer-events-none">
    <div class="floating-shape floating-shape-3 opacity-20"></div>
    <div class="floating-shape floating-shape-4 opacity-15"></div>
  </div>
  
  <div class="max-w-4xl mx-auto px-6 relative z-10">
    <h2 class="text-4xl font-bold text-gray-900 mb-12">Let's Connect</h2>
    <div class="grid md:grid-cols-2 gap-8">
      <div class="bg-white rounded-xl p-8 shadow-sm border border-gray-200">
        <h3 class="text-xl font-bold text-gray-900 mb-6">Contact Information</h3>
        <div class="space-y-4">
          <div class="flex items-center">
            <div class="w-10 h-10 bg-red-100 rounded-lg flex items-center justify-center mr-4">
              <span class="text-red-500">�</span>
            </div>
            <div>
              <div class="text-gray-500 text-sm">Location</div>
              <div class="text-gray-900 font-semibold">Cabuluan, Victoria, Tarlac</div>
            </div>
          </div>
          <div class="flex items-center">
            <div class="w-10 h-10 bg-red-100 rounded-lg flex items-center justify-center mr-4">
              <span class="text-red-500">�</span>
            </div>
            <div>
              <div class="text-gray-500 text-sm">Phone</div>
              <div class="text-gray-900 font-semibold">+63970-936-7505</div>
            </div>
          </div>
          <div class="flex items-center">
            <div class="w-10 h-10 bg-red-100 rounded-lg flex items-center justify-center mr-4">
              <i class="fas fa-envelope text-red-500"></i>
            </div>
            <div>
              <div class="text-gray-500 text-sm">Email</div>
              <div class="text-gray-900 font-semibold">donhsanchez001@gmail.com</div>
            </div>
          </div>
        </div>
        <div class="mt-8 flex gap-4">
          <a href="https://github.com/DonH001" target="_blank" rel="noopener noreferrer" class="flex items-center px-4 py-2 bg-red-100 text-red-600 rounded-lg hover:bg-red-200 transition-colors font-semibold">
            GitHub
          </a>
          <a href="https://www.linkedin.com/in/hector-sanchez-969b37236" target="_blank" rel="noopener noreferrer" class="flex items-center px-4 py-2 bg-red-100 text-red-600 rounded-lg hover:bg-red-200 transition-colors font-semibold">
            LinkedIn
          </a>
        </div>
      </div>
      <div class="bg-white rounded-xl p-8 shadow-sm border border-gray-200">
        <h3 class="text-xl font-bold text-gray-900 mb-6">Send Message</h3>
        <form on:submit={handleSubmit} class="space-y-4">
          <div>
            <input 
              type="text" 
              placeholder="Name" 
              bind:value={formData.name}
              required
              class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-red-500 focus:border-transparent"
            >
          </div>
          <div>
            <input 
              type="email" 
              placeholder="Email" 
              bind:value={formData.email}
              required
              class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-red-500 focus:border-transparent"
            >
          </div>
          <div>
            <textarea 
              placeholder="Message" 
              rows="4" 
              bind:value={formData.message}
              required
              class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-red-500 focus:border-transparent resize-none"
            ></textarea>
          </div>
          {#if submitMessage}
            <div class="p-3 rounded-lg {submitMessage.includes('success') ? 'bg-green-100 text-green-700' : 'bg-red-100 text-red-700'}">
              {submitMessage}
            </div>
          {/if}
          <button 
            type="submit" 
            disabled={isSubmitting}
            class="w-full px-6 py-3 bg-red-500 text-white font-semibold rounded-lg hover:bg-red-600 transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed"
          >
            {isSubmitting ? 'Sending...' : 'Send Message'}
          </button>
        </form>
      </div>
    </div>
  </div>
</section>

<footer class="bg-gray-900 text-white py-16">
  <div class="max-w-6xl mx-auto px-6">
    <div class="grid md:grid-cols-4 gap-8">
      <!-- About Section -->
      <div class="md:col-span-2">
        <h3 class="text-2xl font-bold text-white mb-4">
          Hector <span class="text-red-500">Sanchez</span>
        </h3>
        <p class="text-gray-300 leading-relaxed mb-6 max-w-md">
          Full Stack Developer passionate about creating innovative web solutions. 
          Specializing in modern technologies and delivering exceptional user experiences.
        </p>
        <div class="flex space-x-6">
          <a 
            href="https://github.com/DonH001" 
            target="_blank" 
            rel="noopener noreferrer"
            class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-red-500 transition-all duration-300 hover:scale-110"
            aria-label="GitHub"
          >
            <i class="fab fa-github"></i>
          </a>
          <a 
            href="https://www.linkedin.com/in/hector-sanchez-969b37236" 
            target="_blank" 
            rel="noopener noreferrer"
            class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-red-500 transition-all duration-300 hover:scale-110"
            aria-label="LinkedIn"
          >
            <i class="fab fa-linkedin"></i>
          </a>
          <a 
            href="https://web.facebook.com/hector.sanchez.621907" 
            target="_blank" 
            rel="noopener noreferrer"
            class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-red-500 transition-all duration-300 hover:scale-110"
            aria-label="Facebook"
          >
            <i class="fab fa-facebook"></i>
          </a>
          <a 
            href="mailto:donhsanchez001@gmail.com"
            class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-red-500 transition-all duration-300 hover:scale-110"
            aria-label="Email"
          >
            <i class="fas fa-envelope"></i>
          </a>
          <a 
            href="tel:+639709367505"
            class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-red-500 transition-all duration-300 hover:scale-110"
            aria-label="Phone"
          >
            <i class="fas fa-phone"></i>
          </a>
        </div>
      </div>

      <!-- Quick Links -->
      <div>
        <h4 class="text-lg font-semibold text-white mb-4">Quick Links</h4>
        <ul class="space-y-3">
          <li><a href="#home" class="text-gray-300 hover:text-red-500 transition-colors">Home</a></li>
          <li><a href="#about" class="text-gray-300 hover:text-red-500 transition-colors">About</a></li>
          <li><a href="#technologies" class="text-gray-300 hover:text-red-500 transition-colors">Technologies</a></li>
          <li><a href="#experience" class="text-gray-300 hover:text-red-500 transition-colors">Experience</a></li>
          <li><a href="#projects" class="text-gray-300 hover:text-red-500 transition-colors">Projects</a></li>
          <li><a href="#contact" class="text-gray-300 hover:text-red-500 transition-colors">Contact</a></li>
        </ul>
      </div>

      <!-- Contact Info -->
      <div>
        <h4 class="text-lg font-semibold text-white mb-4">Get in Touch</h4>
        <div class="space-y-3">
          <div class="flex items-center text-gray-300">
            <i class="fas fa-map-marker-alt w-5 text-red-500 mr-3"></i>
            <span class="text-sm">Cabuluan, Victoria, Tarlac</span>
          </div>
          <div class="flex items-center text-gray-300">
            <i class="fas fa-phone w-5 text-red-500 mr-3"></i>
            <span class="text-sm">+63970-936-7505</span>
          </div>
          <div class="flex items-center text-gray-300">
            <i class="fas fa-envelope w-5 text-red-500 mr-3"></i>
            <span class="text-sm">donhsanchez001@gmail.com</span>
          </div>
          <div class="flex items-center text-gray-300">
            <i class="fas fa-briefcase w-5 text-red-500 mr-3"></i>
            <span class="text-sm">Available for freelance</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom Section -->
    <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
      <div class="text-gray-400 text-sm mb-4 md:mb-0">
        © {new Date().getFullYear()} Hector Sanchez. All rights reserved.
      </div>
      <div class="flex items-center space-x-6 text-gray-400 text-sm">
        <span>Built with using SvelteKit & Tailwind CSS</span>
      </div>
    </div>
  </div>
</footer>

<!-- Scroll to Top Button -->
{#if showScrollTop}
  <button 
    on:click={scrollToTop}
    class="fixed bottom-8 right-8 w-12 h-12 bg-red-500 text-white rounded-full shadow-lg hover:bg-red-600 transition-all duration-300 z-50 flex items-center justify-center scroll-top-btn"
    aria-label="Scroll to top"
  >
    <i class="fas fa-chevron-up"></i>
  </button>
{/if}
