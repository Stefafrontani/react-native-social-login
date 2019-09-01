react-native-google-signin
  Project
    yarn add react-native-google-signin // npm did not work
  podfile:
    pod 'GoogleSignIn', '~> 4.4.0'
  Run pod install

  GoogleSignin.configure({
    scopes: ['email'],
    webClientId: '',
    iosClientId: '',
    offlineAccess: true, // if you want to access Google API on behalf of the user FROM YOUR SERVER
    hostedDomain: '', // specifies a hosted domain restriction
    loginHint: '', // [iOS] The user's ID, or email address, to be prefilled in the authentication UI if possible. [See docs here](https://developers.google.com/identity/sign-in/ios/api/interface_g_i_d_sign_in.html#a0a68c7504c31ab0b728432565f6e33fd)
    forceConsentPrompt: true, // [Android] if you want to show the authorization prompt at each login.
    accountName: '', // [Android] specifies an account name on the device that should be used
  });

  Made a project with firebase:
    https://console.firebase.google.com/u/0/project/logintestingnewproject/settings/general/ios:org.reactjs.native.example.GoogleLoginTestingNewProjectDinosaurio
    This creates automatically a webClientId in projecy console.cloud.google.com project apis credentiales section
      https://console.cloud.google.com/apis/credentials?project=logintestingnewproject
    
  Get iosClientId for the .configure({}) method
    Go to: https://console.cloud.google.com/apis/credentials?project=logintestingnewproject
      Create credentiales
        Choose ios
          id package === bundle id