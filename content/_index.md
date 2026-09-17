  # **Maciej Woźniak**  / editor

Welcome to my editing porfolio. <br>


<BR>

<div class="filmstrip-container">
  <!-- Static Edge Vignettes blending continuously into background -->
  <div class="filmstrip-overlay left"></div>
  <div class="filmstrip-overlay right"></div>
  
  <div class="filmstrip-track">
    <img 
      src="https://i.ibb.co/JRTQfB8k/FILMSTRIP-TEST3.png" 
      alt="IMAX Filmstrip" 
      class="filmstrip-image"
    />
    <!-- Duplicate image for seamless infinite looping -->
    <img 
      src="https://i.ibb.co/JRTQfB8k/FILMSTRIP-TEST3.png" 
      alt="" 
      class="filmstrip-image"
      aria-hidden="true"
    />
  </div>
</div>

<style>
  .filmstrip-container {
    position: relative;
    width: 100%;
    height: 300px;
    overflow: hidden;
    background-color: #141414;
    margin: 1rem 0;
  }

  /* Continuous sliding track */
  .filmstrip-track {
    display: flex;
    width: max-content;
    height: 100%;
    will-change: transform;
    /* Adjust '40s' to speed up or slow down the continuous scroll */
    animation: infinite-filmstrip 40s linear infinite;
  }

  .filmstrip-image {
    height: 100% !important;
    width: auto !important;
    max-width: none !important;
    display: block;
    flex-shrink: 0;
  }

  /* Edge Overlays blending into site background */
  .filmstrip-overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 2rem;
    z-index: 2;
    pointer-events: none;
  }

  .filmstrip-overlay.left {
    left: 0;
    background: linear-gradient(to right, #141414 15%, transparent 100%);
  }

  .filmstrip-overlay.right {
    right: 0;
    background: linear-gradient(to left, #141414 15%, transparent 100%);
  }

  /* --- INFINITE LOOP KEYFRAMES --- */
  @keyframes infinite-filmstrip {
    0% {
      transform: translate3d(0, 0, 0);
    }
    100% {
      /* Shifts exactly 50% (the width of 1 image) before seamlessly snapping back to 0% */
      transform: translate3d(-50%, 0, 0);
    }
  }
</style>

