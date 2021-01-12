# Onboarding project

Welcome to the FINN apps team. We have a project prepared for you to get used to some of the decisions we've taken as well to get feedback on them.

Some of the topics that you'll cover here are:
- Code style
- Architecture
- Folder naming and structure
- Networking
- Persistency
- Animations and transitions

The project consists in adding the Wishlist feature to the FINN app: You should be able to navigate to an ad in FINN and add it and remove it to your Wishlist. You should also be able to access all your wishlist entries from your "Min FINN" page.
Another requirement is that you should be able to access the items in your Wishlist offline.

Bonus task, optional but recommended: Our app was originally designed to contact a single backend-for-frontend known as the *Native Apps Proxy*. The proxy contacted other services through various protocols, and merged and transformed results for an app-specific response. 
As requirements and strategies have changed, we have moved to instead use generic services, mostly maintained by other teams at FINN, but offered through the *Apps Gateway* to give a single root URL and a uniform way of accessing backend services. 

The bonus part of the onboarding task is therefore: Add a simple endpoint for storing and retrieving your wishlist to the [apps-platform-service](https://github.schibsted.io/finn/apps-platform-service) backend service, and make it available through the [Apps Gateway](https://github.schibsted.io/finn/apps-gw-poc). It's OK to just deploy to dev and then roll back once you've verified it works.

Here we are attaching the design for how the feature could look. You are encouraged to experiment with animations and creative UX concepts to test the possibilities and limitations of our app architecture. If you have any questions get in touch with your TDE.

We're thankful for having you on the team, and we can't wait to see all the things we'll do together!

![Wishlist](/Images/wishlist-v1.png)
