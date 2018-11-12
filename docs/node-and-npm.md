# Node and NPM

We use Node and NPM so much on front-end projects, that it's well worth having it set up correctly. **If you are having to do the following, your set up is not correct:**

❌ Use `sudo` to get anything done  
❌ Uninstall versions of Node if you need to change between them  
❌ Manually point to node and npm binaries  
❌ Run as "Administrator"...  

What we really want:

✅ Be able to willingly switch between Node versions (because your home projects are so cutting edge, right?!)  
✅ Never use `sudo` or admin rights  
✅ Be confident about how Node and NPM are installed  

## Introducing NVM

Node Version Manager (NVM) is a way to manage multiple Node installations on one machine. It also manages all your privileges. It's absolutely brilliant — so we're going to use this.

## Starting fresh

So, if you're up for the challenge, let's uninstall what you currently have and do this thing!  Firstly, pick your path depending on whether you're Mac or Windows:

## Mac
It's worth noting that this can be quite a command line-y thing to do on a Mac. If you're not comfortable with the command line, this is a great way to learn.

#### 1. Uninstall Node

You might know from experience that removing Node can be a bit of a pain. There is a repo that can help with this. Note that this _is_ a destructive operation. We are removing Node from deep folders in your system. Projects you have might break. However, the upshot is that when we have a clean set up, we can truly control our Node setup and fix these bugs properly. So, if you're still up for the challenge:

1. Clone this repo: https://github.com/brock/node-reinstall
2. Open a Terminal and `cd` to the cloned repo's location
3. Run: `./node-reinstall --nvm-latest`

This script will attempt to remove Node, install `nvm`, re-install the latest Node and re-install any global packages you had before.

