<div class="ssr_variant">
  <div class="framer_aqk693">
    <h1 class="framer_text">
      <span class="framer_text_normal">A Solana based AI code</span>
      <span
        class="framer_text_colored"
        style="background-image: linear-gradient(0deg, rgb(148, 62, 0) 0%, rgb(255, 255, 255) 54.3008%)"
      >
        Assistant
      </span>
    </h1>
  </div>
</div>

<slot/>

<div class="max-w-3xl w-full mx-auto px-4 sm:px-6 lg:px-8 s-CjiUenwQamYl kike">
  <div class="bg-sora-neutral/95 backdrop-blur-md rounded-lg p-8 s-CjiUenwQamYl about_section">
    <h2 class="about_h2">What is KotoneAI?</h2>
    <p class="text_about">
      <span class="text_accent_pink">KotoneAI</span>
      is a
      <span class="text_accent_pink">solana-based</span>
      ai code assistant. Written in rust, it could generate code, provide real time debug information. KotoneAI virtually supports almost all programming languages. <br class="br">Our native 
      <span class="text_accent_pink">$KOTONE</span>
      token provides an unique experience to the users.
    </p>
  </div>
</div>

<style>
   .ssr_variant {
     display: flex;
     align-items: center;
     justify-content: center;
     min-width: 100%;
     min-height: 100%;
     text-align: center;
     padding: 0 0 1rem;
     box-sizing: border-box;
   }

   .framer_aqk693 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
  }

  .framer_text {
    font-family: "Geist Variable", sans-serif;
    font-size: 58px;
    font-weight: 600;
    letter-spacing: -0.03em;
    line-height: 62px;
    text-align: center; /* Ensures the text is horizontally centered */
  }

  .framer_text_normal {
    display: block;
  }

  .framer_text_colored {
    display: block;
    background-image: linear-gradient(0deg, rgb(148, 62, 0) 0%, rgb(255, 255, 255) 54.3008%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  /* Responsive design for smaller screens */
  @media screen and (max-width: 768px) {
    .framer_text {
      font-size: 39px;
      line-height: 41px;
    }
  }

  @media screen and (max-width: 580px) {
    .framer_text {
      margin-top: 43px;
    }
  }

  @media screen and (max-width: 480px) {
    .framer_text {
      font-size: 26px;
      line-height: 31px;
    }
  }

  .kike {
    margin-top: 6px;
    color: #b9aaaa;
  }

  @media (min-width: 1280px) {
    .kike {
      padding: 4rem;
    }
  }

  @media (min-width: 1280px) {
    .kike {
      gap: 2.5rem;
    }
  }

  @media (min-width: 768px) {
    .kike {
      padding: 2rem;
    }
  }

  @media (max-width: 767px) {
    .kike {
      margin-top: 31px;
    }
  }

  .about_h2 {
    font-weight: 700;
    margin: 0;
  }

  .text_about {
    font-weight: 500;
    margin-top: 16px;
  }

  @media (min-width: 1280px) {
    .about_h2 {
      font-size: 4.5rem;
      line-height: 1;
    }

    .text_about {
      font-size: 1.5rem;
      line-height: 2rem;
    }
  }

  @media (min-width: 768px) {
    .about_h2 {
      font-size: 3.55rem;
      line-height: 1;
    }

    .text_about {
      font-size: 1.25rem;
      line-height: 1.75rem;
    }
  }

  .text_accent_pink {
    background-image: linear-gradient(0deg, rgb(148, 62, 0) 0%, rgb(255, 255, 255) 54.3008%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .br {
    display: none; 
  }
  @media (max-width: 768px) {
   .br {
    display: block; 
    }
  }

</style>

