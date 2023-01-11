<script>
  import {Button,
    Header,
    HeaderUtilities,
    HeaderAction,
    HeaderGlobalAction,
    HeaderPanelLinks,
    HeaderPanelDivider,
    HeaderPanelLink,
    SideNav,
    SideNavItems,
    SideNavMenu,
    SideNavMenuItem,
    SideNavLink,
    SkipToContent,
    Content,
    Grid,
    Row,
    Column} from "carbon-components-svelte";
  import "carbon-components-svelte/css/g90.css";
  
  let isSideNavOpen = false;
  const dashboardImgUrl = new URL('/Users/tronschell/Documents/JS/intern-website/static/business-dashboard-example.png', import.meta.url).href
  const workingImgUrl = new URL('/Users/tronschell/Documents/JS/intern-website/static/man-working-on-desktop-pc-in-office-HN72X1.jpg', import.meta.url).href


</script>

<style>

  .dashboard-image{
    object-fit: contain;
    max-width: 50vw;
    border-color: aliceblue;
    border-width: 2px;
    border-style: solid;
  }

  body{
    background-image:  radial-gradient(#638fb4 0.6000000000000001px, transparent 0.6000000000000001px), radial-gradient(#638fb4 0.6000000000000001px, transparent 0.6000000000000001px);
  background-size: 24px 24px;
  background-position: 0 0,12px 12px;
    z-index: 0;
  }

  .hero-section{
    padding-top: 10rem;
    display:flex;
    justify-content:center;
    align-items: center;
    flex-direction: column;
    gap:3rem;
    
    max-width: 100vw;
  }

  .hero-text{
    text-align: center;
    display:flex;
    font-weight: bold;
    width:75vw;
    height:auto;
    transition: cubic-bezier(0.075, 0.82, 0.165, 1);
  }

  .hero-description{
    text-align: center;
    display:flex;
    width:45rem;
    height:auto;
    font-size: 16px;
    color:gainsboro;
    transition: ease-in 0.7s;
  }

  .hero-button-section{
    display:flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap:1rem;
  }

  .info-section-one{
    background-color: black;
    gap:1rem; 
    width:50vw;
  }

  .info-section-one-textblock{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 75vh;
    gap:5rem;
    
  }

  .info-section-one-text{
    text-align: center;
    display:flex;
    width:75%;
    height:auto;
    font-size: 16px;
    color:gainsboro;
    transition: ease-in 0.7s;
    align-items: center;
    justify-content: center;
    
  }
</style>

  <Header platformName="test" bind:isSideNavOpen>

    <SideNav>
      <SideNavItems>
        <SideNavLink>Test</SideNavLink>
      </SideNavItems>
    </SideNav>
  </Header>
<body>
  <div class="hero-background">
    <div class="hero-section">
      <h1 class="hero-text">Optimize the Internship / Co-op job search experience.</h1>
      <h4 class="hero-description">Delete those endless Chrome tabs by compiling all aspects of the job search experience into one unified platform.</h4>
      
      <div class="hero-button-section">
        <Button tooltipAlignment="center">Sign Up</Button>
        <Button kind="tertiary">Learn More</Button>
      </div>

      <img class="dashboard-image" src={dashboardImgUrl} alt="placeholder-image">
    </div>
  </div>

  <div class="info-section-one">
    <div class="info-section-one-textblock">
      <h4 class="info-section-one-text">Read company reviews with pay statistics from anonymous sources.</h4>
      <h4 class="info-section-one-text">Find jobs from multiple different sources including company websites, Indeed.com, Glassdoor.com, and more.</h4>
      <h4 class="info-section-one-text">Use our job application tracker to manage the status of your applications for different companies without needing to use a spreadsheet.</h4>
    </div>
    <div class="info-section-two">
      <img src={workingImgUrl} alt="placeholder-image-two">
    </div>
    
  </div>
</body>
