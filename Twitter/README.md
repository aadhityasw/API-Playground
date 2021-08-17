# Twitter API

Here we will use the **`Tweepy`** library of python to link with and utilize the twitter developer tools.


In order to proceed, you would need a twitter developer account. Head on to the [Twitter Developer Portal](https://developer.twitter.com/) and apply for a developer account. You would be asked to fill a form and mail them stating how you will be using their Developer API's. After you do so, twitter's support team will clear you and create a new developer account for you to use. Once you get this done, you would have to 
create a new standalone app from the dashboard, and save the credentials -- `Consumer Keys` (`API Key`, `API Secret`) and the `Authorization Tokens` (`Bearer Token`, `Access Token`, `Access Secret`). Make sure that the access tokens have both `Read, Write, and Direct Message` permissions. These credentials will be useful when we would integrate these features with our application.


Once we have obtained the twitter credentials, we use the `Tweepy` library to interact with their API's. We can bypass this and make direct HTTP requests to the Twitter API's, but the process of setting this up with the authourizations is more complicated. So we use this tweepy library to handle all the low level implementations and use this to interact with the twitter API's. We will have to key in all the credentials saved in the previous stage here.

The Tweepy has the following lines of code as their setup procedure and to send a direct message to any twitter user :

```python

# Authenticate access
auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(key, secret)

# Create API handler
api = tweepy.API(auth)

# Get the userid of the reciever
user = api.get_user("user_name of recipient")
recipient_id = user.id_str

# Send a DM
api.send_direct_message(recipient_id, "Hello")

```




**References**
* Twitter Developer Portal : [developer.twitter.com](https://developer.twitter.com)
