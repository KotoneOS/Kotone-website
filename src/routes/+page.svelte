<script>
   import { onMount } from "svelte";
   import Modal from "$lib/Modal.svelte";
   import Roadmap from "$lib/Roadmap.svelte";
   import { showModal1, showModal2, showModal3 } from "../store";
   import { fade } from "svelte/transition"
   import { copy } from 'svelte-copy';
   import toast from "svelte-french-toast";
   import Content1 from "$lib/content/Content1.svelte";
   import Content2 from "$lib/content/Content2.svelte"
   import Content3 from "$lib/content/Content3.svelte"

   let documentLoaded = false;

   onMount(() => {
    setTimeout(() => {
      documentLoaded = true;
    }, 350);
  });
</script>
<svelte:head>
  <title>kotoneAI - Your coding assistant</title>
</svelte:head>

{#if documentLoaded}
<div class="framer-fu4ahv-container">
  <div class="dark_overlay"></div>
   <img src="https://ik.imagekit.io/1yoj1x4rw/your-name-shooting-3840x2160-14938.jpg?updatedAt=1737737953913" fetchpriority="high" decoding="async" alt="background_img" class="background_video">
</div>

<!-- change the address here with the actual token address -->
<div class="content">
  <h1 class="title">
    <span class="framer-text">Kotone</span><span class="blinking_cursor"></span>
  </h1>
    <p class="sub">Your first Solana-based AI code assistant</p>
    <div class="data-box">
    <span class="data-text"></span>
    <button class="copy-button no_select" aria-label="icon" use:copy={''}
      on:svelte-copy={(event) => {
          toast.success("Copied!", {
            style: `
            background-color: black; 
            color: white;
            display: flex;
            text-align: left;  
            padding: 10px;
            font-family: 'Geist Variable', sans-serif;
            font-weight: 500;
            `,
            iconTheme: {
              primary: "black",
              secondary: "white",
            },
            position: "top-left",
          });
        }
      }>
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide-copy">
        <rect width="14" height="14" x="8" y="8" rx="2" ry="2"></rect>
        <path d="M4 16c-1.1 0-2-.9-2-2V4c0-1.1.9-2 2-2h10c1.1 0 2 .9 2 2"></path>
      </svg>
    </button>
  </div>
</div>


<section class="bottom-content no_select">
  <div class="cards-container">
    <!-- Card 1 -->
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-missing-attribute -->
    <a on:click={() => { showModal1.set(true) }} tabindex= "0" role="button" class="content-card">
      <div class="card-content">
        <img
          fetchpriority="high"
          decoding="async"
          src="https://ik.imagekit.io/i5kg9s8re/1737744779333.jpg?updatedAt=1737745783053"
          alt="Kotone"
          class="card-image"
        />
        <p class="card-text">Kotone</p>
      </div>
    </a>
    <!-- Card 2 -->
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-missing-attribute -->
    <a on:click={() => { showModal2.set(true) }} tabindex="0" role="button" class="content-card">
      <div class="card-content">
        <img
          fetchpriority="high"
          decoding="async"
          src="https://ik.imagekit.io/i5kg9s8re/kotone2?updatedAt=1737746182843"
          alt="Tokenomics"
          class="card-image change_width"
        />
        <p class="card-text" style="padding: 9px;">Premium</p>
      </div>
    </a>
    <!-- Card 3 -->
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-missing-attribute -->
    <a on:click={() => { showModal3.set(true) }} tabindex="0" role="button" class="content-card">
      <div class="card-content">
        <img
          fetchpriority="high"
          decoding="async"
          src="https://ik.imagekit.io/i5kg9s8re/pS8Ex7cgKSZPQEgBQM8v4FwLw.png?updatedAt=1737883503451"
          alt="Partners"
          class="card-image"
        />
        <p class="card-text">Backers</p>
      </div>
    </a>
    <!-- Card 4 -->
    <a href="https://github.com/KotoneOS/Kotone" target="_blank" data-sveltekit-reload rel="noopener noreferrer" class="content-card">
      <div class="card-content">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="card-image">
          <rect width="24" height="24" fill="url(#paint0_linear_302_4642)"></rect>
          <path fill="#fff" d="M11.9972 4.00001C10.0986 3.99821 8.26146 4.67259 6.81492 5.90226C5.36836 7.13194 4.40699 8.83655 4.10306 10.7106C3.79913 12.5847 4.1725 14.5058 5.15628 16.1296C6.14007 17.7535 7.66995 18.9739 9.47178 19.5722C9.87057 19.6417 9.99702 19.4076 9.99702 19.1964C9.99702 19.0052 10.0012 18.4759 9.99702 17.8068C7.77381 18.289 7.31457 16.7543 7.31457 16.7543C7.168 16.2714 6.85356 15.8569 6.42807 15.5857C5.70275 15.0897 6.48226 15.0993 6.48226 15.0993C6.73551 15.1341 6.97745 15.2263 7.18961 15.3689C7.40177 15.5114 7.57855 15.7007 7.70641 15.922C7.81458 16.1191 7.96076 16.2927 8.13648 16.433C8.3122 16.5732 8.51399 16.6772 8.73017 16.7391C8.94635 16.8008 9.17263 16.8191 9.39593 16.7929C9.61921 16.7666 9.83509 16.6964 10.0311 16.5861C10.0679 16.1823 10.2478 15.8048 10.5382 15.5218C8.76452 15.3189 6.89911 14.6339 6.89911 11.5714C6.88785 10.7775 7.18267 10.0097 7.72239 9.42741C7.47783 8.73856 7.50567 7.98229 7.80021 7.31328C7.80021 7.31328 8.47204 7.09861 9.99702 8.13309C11.3068 7.77368 12.6891 7.77368 13.9988 8.13309C15.5273 7.0993 16.1935 7.31328 16.1935 7.31328C16.4881 7.9822 16.5165 8.73833 16.2727 9.42741C16.8126 10.0101 17.107 10.7785 17.0946 11.5728C17.0946 14.6436 15.2264 15.3183 13.4465 15.5148C13.6377 15.7069 13.7854 15.9378 13.8797 16.1919C13.974 16.446 14.0127 16.7174 13.9932 16.9877V19.1998C13.9932 19.4131 14.1225 19.6493 14.5282 19.5722C16.3305 18.9737 17.8607 17.7529 18.8444 16.1284C19.8281 14.5041 20.2012 12.5823 19.8965 10.7079C19.5919 8.83343 18.6295 7.12877 17.1819 5.89954C15.7343 4.67032 13.8963 3.99689 11.9972 4.00001Z"></path>
          <defs>
            <linearGradient id="paint0_linear_302_4642" x1="0" x2="24" y1="12" y2="12" gradientUnits="userSpaceOnUse">
              <stop stop-color="#ED6D6B"></stop>
              <stop offset="1" stop-color="#F0B076"></stop>
            </linearGradient>
          </defs>
        </svg>
        <p class="card-text">Github</p>
      </div>
    </a>
  </div>
</section>

<div class="overlay no_select">
  {#if $showModal1 == true}
    <Modal showModal={showModal1}>
       <Content1>
         <Roadmap />
       </Content1>
    </Modal>
  {/if}

  {#if $showModal2 == true}
    <Modal showModal={showModal2}>
      <Content2 />
    </Modal>
  {/if}
  {#if $showModal3 == true}
    <Modal showModal={showModal3}>
      <Content3 />
    </Modal>
  {/if}
</div>
{:else}
   <div class="fullscreen" style="color: white;">
     <div class="loading_pic">
       <img src="https://ik.imagekit.io/faggot/1736775553348.png?updatedAt=1736775633166" decoding="async" alt="Loader" style="max-width: 209px;" transition:fade={{ duration: 500 }}>
     </div>
   </div>
{/if}

<style>
    .no_select {
      -webkit-tap-highlight-color: transparent;
      -webkit-touch-callout: none;
      -webkit-user-select: none;
      -khtml-user-select: none;
      -moz-user-select: none;
      -ms-user-select: none;
      user-select: none;
     }

     .no_select:focus {
      outline: none !important;
     }

    .fullscreen {
      display: flex;
      flex: none;
      flex-direction: row;
      flex-wrap: nowrap;
      gap: 48px;
      justify-content: center;
      inset: 0;
      overflow: hidden;
      position: fixed;
      z-index: 10;
      color: white;
      background-color: rgb(0, 0, 0);
      font-family: "Open Sans", sans-serif;
      min-height: 100%;
      min-width: 100%;
      margin: 0;
      border: none;
    }
    .content {    
       position: relative;    
       z-index: 1; /* Ensures the content is above the video */ 
       text-align: center;    
       margin-top: 6%;
       flex-direction: column;
       display: flex;
       justify-content: center;
       align-items: center;
    }

    /* bar flicker after logo */
    .title {
       font-size: 3rem; /* Adjust the title size */
       font-weight: 500;
       color: white; /* Title color */
       display: inline-flex;
       align-items: center; /* Ensures vertical alignment with the cursor */
       font-family: 'Geist Variable', sans-serif;
       margin-bottom: 0;
    }

    .framer-text {
       background-image: linear-gradient(0deg, rgb(110, 0, 0) 0%, rgb(255, 255, 255) 52.3%);;
       background-clip: text;
       -webkit-background-clip: text;
       color: transparent; /* Makes gradient visible */
       display: inline-block;
       text-align: center;
    }

    .blinking_cursor {
       font-weight: 100;
       font-size: 30px;
       display: inline-block; /* Allows precise control */
       width: 10px; /* Adjust thickness */
       height: 1em; /* Matches text height */
       background-color: #3F1317; /* Bar color */
       vertical-align: bottom;
       animation: 0.9s blink step-end infinite;
       margin-left: 7px;
       margin-top: 6px;
    }

    .sub {
      font-size: 1.5rem; /* Adjust font size for the subtitle */
      font-weight: 400; /* Slightly lighter than the title */
      color: rgba(255, 255, 255, 0.8); /* Subtle text color for contrast */
      text-align: center; /* Center-aligns the subtitle */
      margin-top: 10px; /* Space between title and subtitle */
      font-family: 'Geist Variable', sans-serif; /* Matches the font style */
    }

    .data-box {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      padding: 15px;
      margin-top: 15px; /* Space between subtitle and data box */
      background-color: rgba(255, 255, 255, 0.1); /* Subtle background */
      border: 1px solid rgba(255, 255, 255, 0.2); /* Light border */
      border-radius: 8px;
      font-family: 'Geist Variable', sans-serif; /* Matches the font style */
      font-weight: 500;
      min-width: 974px;
    }

    .data-text {
      font-size: 17px;
      color: rgba(255, 255, 255, 0.9);
      flex-grow: 1;
    }
    
    .copy-button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 40px;
      height: 40px;
      background: rgba(255, 255, 255, 0.1); /* Button background */
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    
    @media(hover: hover) {
      .copy-button:hover {
        background-color: rgba(255, 255, 255, 0.2); /* Hover effect */
      }
    }
   
    .lucide-copy {
      stroke: rgba(255, 255, 255, 0.8); /* Icon color */
    }

    @media (max-width: 1168px) {
      .data-box {
        min-width: 86%; /* Make the box take 70% of the screen on smaller devices */
      }
    }
    
    @media (max-width: 966px) {
      .data-box {
        min-width: 90%; /* Make the box take 70% of the screen on smaller devices */
      }
    }

    @media (max-width: 806px) {
      .data-text {
        font-size: 15px;
      }
    }

    @media (max-width: 806px) {
      .data-text {
        word-break: break-all; /* Make the box take 70% of the screen on smaller devices */
      }
    }

    @media (max-width: 694px) {
      .copy-button {
        background-color: transparent;
      }

      .lucide-copy {
        width: 20px;
        height: 20px; /* Make the box take 70% of the screen on smaller devices */
      }
    }


    @keyframes blink {
      50% {
        opacity: 0;
      }
    }
    /* end */
    
    .framer-fu4ahv-container {
      opacity: 0.9;
      flex: none;    
      inset: -3px -7px 0 0;    
      top: 0;    
      left: 0;    
      right: 0;    
      bottom: 0;    
      position: absolute;    
      z-index: 1;    
      height: 100vh;
   }

  .background_video {
      cursor: auto;
      border-radius: 0px;
      width: 100%;
      height: 100%;
      display: block;
      object-fit: cover;
      background-color: rgba(0, 0, 0, 0);
      object-position: 50% 50%;
  }

  .dark_overlay {
     position: absolute;
     top: 0;
     left: 0;
     width: 100%;
     height: 100%;
     background: black;
     opacity: 0.5;
     z-index: 2; 
     pointer-events: none;
  }

  .loading_pic {
    display: flex;
    justify-content: center;
    align-items: center;
    height: auto;
  }

  /* start from here */
  .bottom-content {
    width: 100%;
    position: relative;
    padding: 0px;
    height: min-content;
    align-items: center;
    place-content: center;
    gap: 24px;
    flex-flow: column;
    flex: 0 0 auto;
    display: flex;
    overflow: visible;
    margin-top: 7rem;
  }

  .cards-container {
    margin: 0 auto;
    opacity: 1;
    will-change: transform;
    transform: none;
    place-content: center;
    align-items: center;
    display: flex;
    gap: 26px;
    height: min-content;
    max-width: 500px;
    overflow: visible;
    padding: 0px;
    width: 100%;
    flex-flow: row;
    flex: 0 0 auto;
    position: relative;
    z-index: 1;
  }

  .content-card {
    cursor: pointer;
    text-decoration: none;
    color: inherit;
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 150px;
    background: linear-gradient(
      rgba(255, 255, 255, 0.07),
      rgba(255, 255, 255, 0)
    );
    border-radius: 16px;
    box-shadow: rgba(255, 255, 255, 0.25) 2px 2px 5px inset;
    overflow: hidden;
    transition: transform 0.3s, box-shadow 0.3s;
   }

   .content-card:hover {
     transform: translateY(-5px);
     box-shadow: rgba(0, 0, 0, 0.3) 0px 5px 15px;
   }

   .card-content {
     text-align: center;
   }

   .card-image {
     border-radius: inherit;
     width: 100%;
     height: auto;
     max-width: 150px;
     object-fit: cover;
     aspect-ratio: 1 / 1;
   }
   
   .card-text {
     padding: 10px;
     font-family: 'Inter', sans-serif;
     font-weight: 600;
     font-size: 14px;
     color: #fff;
   }
  
   @media (max-width: 760px) {
     .cards-container {
        flex-wrap: wrap;
        gap: 37px;
     }

     .bottom-content {
        margin-top: 30px;
     }

     .content-card {
        width: 79px
     }

     .change_width {
       width: 81px;
     }
   }

   @media (max-width: 446px) {
     .content-card {
        width: 79px
      }

      .change_width {
         max-width: 82px;
      }
   }
</style>
