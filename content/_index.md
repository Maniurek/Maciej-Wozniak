  # **Maciej Woźniak**  / editor

Welcome to my editing porfolio.

<br>

<div class="filmstrip-container">
  <div class="filmstrip-overlay left"></div>
  <div class="filmstrip-overlay right"></div>
  <img 
    src="https://i.ibb.co/tTfFC1rG/FILMSTRIP-TEST1.png" 
    alt="IMAX Filmstrip" 
    class="filmstrip-image"
  />
</div>

<style>
  .filmstrip-container {
    position: relative;
    width: 100%;
    height: 300px; /* Adjust height to control the filmstrip scale */
    overflow: hidden;
    background-color: #141414;
    container-type: inline-size; /* Auto-calculates exact right edge stop */
    margin: 1rem 0;
  }

  .filmstrip-image {
    height: 100% !important;
    width: auto !important;
    max-width: none !important; /* Prevents theme from squishing the image width */
    display: block;
    will-change: transform, filter;
    animation: filmstrip-pan 40s cubic-bezier(0.3, 0, 0.2, 1) infinite;
  }

  /* Smooth Edge Overlays matching site background */
  .filmstrip-overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 1rem;
    z-index: 2;
    pointer-events: none;
    will-change: opacity;
  }

  .filmstrip-overlay.left {
    left: 0;
    background: linear-gradient(to right, #141414 10%, transparent 100%);
    animation: fade-left-edge 40s cubic-bezier(0.3, 0, 0.2, 1) infinite;
  }

  .filmstrip-overlay.right {
    right: 0;
    background: linear-gradient(to left, #141414 10%, transparent 100%);
    animation: fade-right-edge 40s cubic-bezier(0.2, 0, 0.2, 1) infinite;
  }

  /* --- ANIMATIONS --- */

  @keyframes filmstrip-pan {
    0% {
      transform: translateX(0);
      filter: blur(0px);
    }
    /* Pans across the strip until the far-right edge aligns with container */
    80% {
      transform: translateX(calc(-100% + 100cqi));
      filter: blur(0px);
    }
    /* Brief pause on the last frame */
    81% {
      transform: translateX(calc(-100% + 100cqi));
      filter: blur(0px);
    }
    /* Motion-blurred high-speed rewind back to start */
    82% {
      filter: blur(5px);
      transform: translateX(calc(-100% + 100cqi));
    }
    92% {
      filter: blur(0px);
      transform: translateX(0);
    }
    /* Clean reset for the loop */
    100% {
      transform: translateX(0);
      filter: blur(0px);
    }
  }

  /* Dynamic Left Edge Fade */
  @keyframes fade-left-edge {
    0% { opacity: 0; }
    5% { opacity: 1; }
    83% { opacity: 1; }
    86% { opacity: 0; }
    100% { opacity: 0; }
  }

  /* Dynamic Right Edge Fade */
  @keyframes fade-right-edge {
    0% { opacity: 1; }
    60% { opacity: 1; } /* Starts fading out smoothly while still scrolling */
    78% { opacity: 0; } /* Completely clear right before the pan stops at 80% */
    95% { opacity: 0; } /* Stays transparent through the pause and rewind */
    100% { opacity: 1; } /* Resets for the start of the next loop */
  }
</style>

  <!---

{{< latest_post >}}



  
  {{< figure src="https://i.ibb.co/8nBqHFG6/20270610-DSC09396-2.jpg" >}}
<!---

// [`filmpolski`](https://filmpolski.pl/fp/index.php?osoba=11227907) </br>
&nbsp;&nbsp;&nbsp;&nbsp; polish film archive

This is my editing portfolio. Click the  / projects tab to see what I've worked on. 



  
   >	