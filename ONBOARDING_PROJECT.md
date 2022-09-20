# Onboarding project

Welcome to the FINN apps team. We have a project prepared for you to get used to some of the decisions we've taken as well to get feedback on them.

Some of the topics that you'll cover here are:
- Code style
- Architecture
- Folder naming and structure
- Networking
- Persistency
- Animations and transitions
- How to create a new feature module
- How we do dependency injection
- How we do navigation
- The current view abstractions we use
- What utils are available
- What fonts, colors and dimensions to use in order to make it fit in the app.
- Light and Dark mode support.

The project consists in adding the Wishlist feature to the FINN app: You should be able to navigate to an ad in FINN and add it and remove it to your Wishlist. You should also be able to access all your wishlist entries from your "Min FINN" page.
Another requirement is that you should be able to access the items in your Wishlist offline.

The Wishlist item in the user wishlist should include:
- Picture of the item
- Price of the item
- Status Ribbon (active, sold, deactivated...)
- Last updated time
- Place
- Title

## Normal approach
Use the favorite ads backend as a wishlist backend (perhaps a "wishlist"-favorite list 🤷) and be inspired by the existing favorite ads API code.

### Optional task
If you decide to try the normal approach and want to know more about our backends. Clone the [Native Apps Proxy](https://github.schibsted.io/finn/finn_native_app_proxy) and [Apps Gateway](https://github.schibsted.io/finn/apps-gw-poc) repositories and try to start the services locally on your machine. You can then also connect the app running in simulator/emulator to the locally running backends.

## Advanced (optional) approach
Add a simple endpoint for storing and retrieving your wishlist to the [apps-platform-service](https://github.schibsted.io/finn/apps-platform-service) backend service, and make it available through the [Apps Gateway](https://github.schibsted.io/finn/apps-gw-poc). It's recommended to just briefly deploy to dev and then roll back once you've verified it works. Adding actual database storage is also unnecessary, a static list is enough.

## History of FINN app backends
A brief history lesson related to the app backends. Our app was originally designed to contact a single backend-for-frontend known as the *Native Apps Proxy*. The proxy contacted other services through various protocols, and merged and transformed results for an app-specific response.
As requirements and strategies have changed, we have moved to instead use domain specific services, maintained by other teams at FINN, but offered through the *Apps Gateway* to give a single root URL and a uniform way of accessing backend services.

## Design suggestions
Below you can see designs for how the feature _could_ look.
You are encouraged to experiment with animations and creative UX concepts to test the possibilities and limitations of our app architecture.
If you have any questions get in touch with your assigned buddy and/or TDE.

We don't expect you to spend too long on the task, anything between 1 and 3 weeks is considered reasonable.
We are thankful for having you on the team and we can't wait to see all the things we'll do together!

Wishlist button:
|Light not added|Dark not added|Light added|Dark added|
|----|----|----|----|
|![Screenshot_1653303017](https://user-images.githubusercontent.com/15628235/169805675-507a86ac-f249-4e09-8c1a-eb92d147ebcf.png)|![Screenshot_1653303024](https://user-images.githubusercontent.com/15628235/169805701-f4a1bcd2-c82f-443c-9c43-4ac22f0f4b17.png)|![Screenshot_1653303033](https://user-images.githubusercontent.com/15628235/169806063-6bcec6de-fe7b-47b9-9b5e-6afa21bae303.png)|![Screenshot_1653303028](https://user-images.githubusercontent.com/15628235/169806044-bb209877-f8c3-47e0-879b-d6b47378f4e3.png)|

The wishlist entry:
|Light|Dark |
|----|----|
|![Screenshot_1653303484](https://user-images.githubusercontent.com/15628235/169804978-3150815a-611f-4069-b133-01d13d0b4e47.png)|![Screenshot_1653302886](https://user-images.githubusercontent.com/15628235/169805078-bb9d54eb-836d-4a7d-a4e4-40563998ba1b.png)|

Empty state of the wishlist:
|Light|Dark |
|----|----|
|![Screenshot_1653302916](https://user-images.githubusercontent.com/15628235/169805460-9cd0d192-fcd5-40a6-aab9-133fa167ad18.png)|![Screenshot_1653302904](https://user-images.githubusercontent.com/15628235/169805537-50592ecf-d9a6-464e-ab83-d40b66125119.png)|
