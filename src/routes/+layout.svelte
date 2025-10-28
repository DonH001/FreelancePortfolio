<script>
  import "../app.css";
</script>

<style>
  /* Custom navigation link styles */
  .nav-link {
    outline: none;
    border: none;
  }
  
  /* Remove default focus outline and add custom underline effect */
  .nav-link:focus {
    outline: none;
    border: none;
  }
  
  /* Underline effect on hover and focus */
  .nav-link::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background-color: #ef4444; /* red-500 */
    transition: width 0.3s ease-in-out;
  }
  
  .nav-link:hover::after,
  .nav-link:focus::after {
    width: 100%;
  }
  
  /* Remove any browser default focus styles */
  .nav-link:focus-visible {
    outline: none;
    box-shadow: none;
    border: none;
  }
</style>

<nav class="fixed top-0 w-full z-50 bg-white/95 backdrop-blur-md border-b border-gray-200">
  <div class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
    <a href="#home" class="font-bold text-xl text-gray-900 hover:text-red-500 transition-colors">
      HEC <span class="text-red-500">SAN</span>
    </a>
    <div class="hidden md:flex space-x-8 items-center">
      <a href="#home" class="nav-link text-gray-700 hover:text-red-500 transition-all duration-300 font-medium relative py-2">Home</a>
      <a href="#about" class="nav-link text-gray-700 hover:text-red-500 transition-all duration-300 font-medium relative py-2">About</a>
      <a href="#technologies" class="nav-link text-gray-700 hover:text-red-500 transition-all duration-300 font-medium relative py-2">Technologies</a>
      <a href="#experience" class="nav-link text-gray-700 hover:text-red-500 transition-all duration-300 font-medium relative py-2">Experience</a>
      <a href="#projects" class="nav-link text-gray-700 hover:text-red-500 transition-all duration-300 font-medium relative py-2">Projects</a>
      <a href="#certificates" class="nav-link text-gray-700 hover:text-red-500 transition-all duration-300 font-medium relative py-2">Certificates</a>
      <a href="#contact" class="nav-link text-gray-700 hover:text-red-500 transition-all duration-300 font-medium relative py-2">Contact</a>
      
      <!-- Social Icons -->
      <div class="flex items-center space-x-4 ml-4 pl-4 border-l border-gray-300">
        <a 
          href="https://github.com/DonH001" 
          target="_blank" 
          rel="noopener noreferrer"
          class="text-gray-600 hover:text-red-500 transition-all duration-300 hover:scale-110"
          aria-label="GitHub Profile"
        >
          <i class="fab fa-github text-xl"></i>
        </a>
        <a 
          href="https://www.linkedin.com/in/hector-sanchez-969b37236" 
          target="_blank" 
          rel="noopener noreferrer"
          class="text-gray-600 hover:text-red-500 transition-all duration-300 hover:scale-110"
          aria-label="LinkedIn Profile"
        >
          <i class="fab fa-linkedin text-xl"></i>
        </a>
        <a 
          href="https://web.facebook.com/hector.sanchez.621907" 
          target="_blank" 
          rel="noopener noreferrer"
          class="text-gray-600 hover:text-red-500 transition-all duration-300 hover:scale-110"
          aria-label="Facebook Profile"
        >
          <i class="fab fa-facebook text-xl"></i>
        </a>
      </div>
    </div>
  </div>
</nav>

<!-- Add top padding to account for fixed navbar -->
<div class="pt-20">
  <slot />
</div>
