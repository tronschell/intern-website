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
  const imgUrl = new URL('/Users/tronschell/Documents/JS/intern-website/static/business-dashboard-example.png', import.meta.url).href

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
    opacity: 0.8;
    background-image:  radial-gradient(#638fb4 0.6000000000000001px, transparent 0.6000000000000001px), radial-gradient(#638fb4 0.6000000000000001px, transparent 0.6000000000000001px);
  background-size: 24px 24px;
  background-position: 0 0,12px 12px;
    
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
    width:45rem;
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
    flex-direction: row;
    
  }

  .info-section-one-text{
    text-align: center;
    display:flex;
    width:45rem;
    height:auto;
    font-size: 16px;
    color:gainsboro;
    transition: ease-in 0.7s;
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

      <img class="dashboard-image" src={imgUrl} alt="placeholder-image">
    </div>
  </div>

  <div class="info-section-one">
    <div class="info-section-one-textblock">
      <h4 class="info-section-one-text">Find jobs from multiple different sources including company websites, Indeed.com, Glassdoor.com, and more.</h4>
    </div>
    
  </div>
</body>
