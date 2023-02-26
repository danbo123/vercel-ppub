### We hang Pingpub in the cloud for static

- Fork/sync [Pingpub repo](https://github.com/ping-pub/explorer)

- Register on [Vercel](https://vercel.com/signup) (preferably immediately via GitHub)

- Create a new project
  ![223740](assets/223740.png)
  
- Import the project (our fork)

  ![224442](assets/224442.png)

- Authorize Netlify access to GitHub account

- Choose our fork

  ![224803](assets/224803.png)

- Vercel automatically detects deployment environment (Vue.js). Leave the import settings as default

  ![224851](assets/224851.png)

- Deployment

The assembly process takes 4-5 minutes. You can see the deploy log

  ![225441](assets/225441.png)

We are waiting for this:

  ![225923](assets/225923.png)

- We return to the overview and see that the explorer is deployed. Let's follow the link

  ![230108](assets/230108.png)

- Done

  ![230231](assets/230231.png)

### We hatch

![230354](assets/230354.png)

- Getting a human link

  ![230516](assets/230516.png)

- Or, if there is a domain, we connect it

  ![230626](assets/230626.png)

- We make the required changes to the DNS

  ![230734](assets/230734.png)

### Cosmetics and more

It should be noted here that Vercel will automatically rebuild every commit in your fork, which is not always advisable, especially during initial setup. As a result, all manipulations to remove / add networks, replace the logo, links, and other things are best done locally. I am using [GitHub Desktop](https://desktop.github.com/). We clone the fork and finish everything we need. Links are given to the main repository, we correlate with our fork:

- Logo loading [here](https://github.com/ping-pub/explorer/tree/master/public)

- Changing the title of the page [Here](https://github.com/ping-pub/explorer/blob/master/public/index.html#L16)

- Change title in navigation [Here](https://github.com/ping-pub/explorer/blob/master/themeConfig.js#L12). Здесь же смотрим остальные параметры, скин, анимацию и т.д.

- Changing the title of the main page [Here](https://github.com/ping-pub/explorer/blob/master/src/views/Home.vue#L10)

- We put our [social media links](https://github.com/ping-pub/explorer/blob/master/src/navigation/vertical/index.js)

- We clean the `src/chains/mainnet` and `src/chains/testnet` directories and load our network configs there.

- We commit all the changes on the desktop at once, Netlify will automatically rebuild the commit, no additional steps. no movement required

  

