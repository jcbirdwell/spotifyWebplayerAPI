# spotifyWebplayerAPI

While using the spotify api to create an app in python, I discovered that three extremely useful endpoints were missing from the offical API.
These being a way to get friend activity seen currently in the Spotify desktop app and previously in the Spotify webapp, the followers of a 
user, and the users followed by a user. I figured finding a workaround would be both a fun exercise and a useful tool for development. So, 
here it is. Included in main.py are five functions, four of which give access to these various hidden or exclusive spotify endpoints.
As these endpoints are exclusive to the web player api, a special access token is required to obtain a valid reponse from the spotify servers.
The first function get_web_access_token() assists in obtaining this token.
With this token, the three other non-standard endpoints get_friend_activity(), get_followers(), and get_following() can be used to obtain
their respective response data.
Additionally, a standard api endpoint is used within the get_username() function. This function is used to obtain the username associated with 
the access token for use within the previous follower related functions. 
