# my-web-app-2
Get Access token client side – Facebook

Need to change the CLIENT_ID in the "index.html"
function makeRequest() {
// TODO: Make authorization request
            // Define properties
            var AUTH_ENDPOINT = "https://www.facebook.com/dialog/oauth";
            var RESPONSE_TYPE = "token";
            var CLIENT_ID = "<your registered fb app id/clent id>";
            var REDIRECT_URI = "http://localhost:8080/my-web-app-2/callback.html";
            var SCOPE = "public_profile user_posts";
// Build authorization request endpoint
            var requestEndpoint = AUTH_ENDPOINT + "?" +
                "response_type=" + encodeURIComponent(RESPONSE_TYPE) + "&" +
                "client_id=" + encodeURIComponent(CLIENT_ID) + "&" +
                "redirect_uri=" + encodeURIComponent(REDIRECT_URI) + "&" +
                "scope=" + encodeURIComponent(SCOPE);
// Send to authorization request endpoint
            window.location.href = requestEndpoint;
        }
