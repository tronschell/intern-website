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
    import { initializeApp } from "firebase/app";
    import { getAnalytics } from "firebase/analytics";
    import { GoogleAuthProvider } from "firebase/auth";
    // TODO: Add SDKs for Firebase products that you want to use
    // https://firebase.google.com/docs/web/setup#available-libraries

    // Your web app's Firebase configuration
    // For Firebase JS SDK v7.20.0 and later, measurementId is optional
    const firebaseConfig = {
    apiKey: "AIzaSyCtMwSlTBs6jXI6kyqquMlv-PHWavnXldc",
    authDomain: "intern-website-ad5eb.firebaseapp.com",
    projectId: "intern-website-ad5eb",
    storageBucket: "intern-website-ad5eb.appspot.com",
    messagingSenderId: "962106609899",
    appId: "1:962106609899:web:e644d996032e938afdaeae",
    measurementId: "G-XWHG3N1ZJ8"
    };

    // Initialize Firebase
    const app = initializeApp(firebaseConfig);
    const analytics = getAnalytics(app);
    const auth = getAuth(app)


    const provider = new GoogleAuthProvider();

    import { getAuth, signInWithPopup, signInWithRedirect } from "firebase/auth";

    export const googleLogin = () => {
        
        signInWithPopup(auth, provider);
    };

    
</script>

<Button on:click={googleLogin}>Sign up with Google</Button>
    