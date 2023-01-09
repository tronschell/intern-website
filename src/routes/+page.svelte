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

</script>

<style>
  .hero-background{
    opacity: 0.8;
  background-image:  radial-gradient(#638fb4 0.6000000000000001px, transparent 0.6000000000000001px), radial-gradient(#638fb4 0.6000000000000001px, transparent 0.6000000000000001px);
  background-size: 24px 24px;
  background-position: 0 0,12px 12px;
  z-index:9;
  max-width: 100%;
  max-width: 100%;
  }

  .hero-section{
    margin-top:10rem;
    display:flex;
    justify-content:center;
    align-items: center;
    flex-direction: column;
    gap:3rem;

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
</style>
<Header platformName="test" bind:isSideNavOpen>

  <SideNav>
    <SideNavItems>
      <SideNavLink>Test</SideNavLink>
    </SideNavItems>
  </SideNav>
</Header>
<div class="hero-background">
  <div class="hero-section">
    <h1 class="hero-text">Streamline the Internship / Co-op job searching experience.</h1>
    <h4 class="hero-description">Delete those endless Chrome tabs by compiling all aspects of the job search experience into one platform.</h4>
    
    <div class="hero-button-section">
      <Button tooltipAlignment="center">Sign Up</Button>
      <Button kind="tertiary">Learn More</Button>
    </div>
  </div>
</div>

