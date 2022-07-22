# spotifyWebplayerAPI

While using the Spotify API to create an app in Python, I discovered that three extremely useful endpoints were missing from the offical API.
These being a way to get friend activity (seen currently in the Spotify desktop app and previously in the Spotify webapp), the followers of a 
user, and the users followed by a user. I figured finding a workaround would be both a fun exercise and a useful tool for development. So, 
here it is. Included in main.py are five functions, four of which give access to these various hidden or exclusive Spotify endpoints.
As these endpoints are "exclusive" to the web player API, a special access token is required to obtain a valid reponse from the Spotify servers.
The first function get_web_access_token() assists in obtaining this token.
With this token, the three other non-standard endpoints get_friend_activity(), get_followers(), and get_following() can be used to obtain
their respective response data.
Additionally, a standard api endpoint is used within the get_username() function. This function is used to obtain the username associated with 
the access token for use within the previous follower related functions. 

USAGE: The primary hurdle for using these functions will most likely be obtaining the access token. Getting this access token requires the 
user to have logged into the Spotify web player prior to use. The get_web_access_token() function's request requires the "sp_dc" token that 
is stored as a browser cookie upon login to the web player. The token retrieval has been automated using the browser_cookie3 library, but can
also be manually retrieved from the browser via F12 -> Application -> Storage -> Cookies -> https://open.spotify.com -> the value for "sp_dc".
This token can be provided to the function as an optional parameter thus bypassing the browser_cookie3 dependancy and its access requests etc. 
