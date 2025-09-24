<script>
export default {
  name: 'FooterContact'
}
</script>

<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="social-links">
        <a href="https://github.com" target="_blank" class="social-link">
          <img src="/public/topos.png" alt="GitHub" class="social-icon">
        </a>
        <a href="https://linkedin.com" target="_blank" class="social-link">
          <img src="/public/catch.png" alt="LinkedIn" class="social-icon">
        </a>
        <a href="https://twitter.com" target="_blank" class="social-link">
          <img src="/public/pinpong.png" alt="Twitter" class="social-icon">
        </a>
        <a href="https://instagram.com" target="_blank" class="social-link">
          <img src="/public/vite.svg" alt="Instagram" class="social-icon">
        </a>
      </div>
      <div class="footer-text">
        <p>&copy; 2025 PagGame. Todos los derechos reservados.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  width: 100vw;
  background-color: var(--footer-bg-color);
  padding: 2rem 0;
  margin-left: calc(-50vw + 50%);
  position: relative;
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 2rem;
  flex-wrap: wrap;
}

.social-link {
  display: inline-block;
  transition: transform 0.3s ease, opacity 0.3s ease;
  border-radius: 50%;
  padding: 0.5rem;
  background-color: var(--social-link-bg);
  border: 2px solid var(--social-link-border);
}

.social-link:hover {
  transform: translateY(-5px) scale(1.1);
  opacity: 0.8;
  background-color: var(--social-link-hover-bg);
}

.social-icon {
  width: 40px;
  height: 40px;
  object-fit: contain;
  filter: brightness(0) saturate(100%) invert(1);
}

.social-link:hover .social-icon {
  filter: brightness(0) saturate(100%) invert(0.8);
}

.footer-text {
  text-align: center;
  color: var(--footer-text-color);
  font-size: 0.9rem;
}

.footer-text p {
  margin: 0;
}

/* Responsive design */
@media (max-width: 768px) {
  .footer-content {
    padding: 0 1rem;
  }
  
  .social-links {
    gap: 1rem;
  }
  
  .social-icon {
    width: 35px;
    height: 35px;
  }
}

@media (max-width: 480px) {
  .social-links {
    gap: 0.8rem;
  }
  
  .social-icon {
    width: 30px;
    height: 30px;
  }
  
  .footer-text {
    font-size: 0.8rem;
  }
}
</style>
