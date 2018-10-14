# Prerequisites

1. First, check that you can run `node -v` and `npm -v` from a command line. Your 'node' version should be v6 or higher.
2. If you can't run `node -v`, you'll need to install it ([below](#1-installing-node)).
3. Once you can run `node` and `npm`, make sure you can load packages:
   
	  `npm install -g create-react-app`
4. If errors occur, you'll need to configure npm to load packages from an npm "Registry" ([below](#2-configure-npm-to-use-a-registry)).


## 1. Installing node

### Windows

On Windows, install node from https://nodejs.org/

### Mac

On Mac, I use _nvm_ as it doesn't require installing node as root, and we can manage multiple node versions.

1. Install nvm from https://github.com/creationix/nvm
2. Run `nvm install node`
	
(To list available versions: `nvm ls-remote`)

### Linux

On Linux, install node using your distribution's [package manager](https://nodejs.org/en/download/package-manager/).



## 2. Configure npm to use a Registry

> If you're not behind a corporate firewall, skip this section.

Does your company have an internal registry (sometimes called a binary repository or Artifactory)? If so, try Option 1 [below](#option-1-use-internal-artifactory). Otherwise, use Option 2 [below](#option-2-use-proxies-to-access-npmjs-registry).

### Option 1: Use internal Artifactory

Use `npm config` to set npm to use your company's internal Artifactory. For example:

- `npm config set registry https://artprod.dev.`mycompany`.com/artifactory/api/npm/npm-repos`

  > Don't forget to replace "mycompany" with your company's name, or find your company's Artifactory URL from a colleague.

### Option 2: Use proxies to access NPMJS registry

If you can't access an Artifactory, try accessing the main npm registry, for example like this:

- `npm config set strict-ssl false`
- `npm install -g --registry http://registry.npmjs.org/
--proxy       http://proxy.`mycompany`.com:81/
--https-proxy https://proxy.`mycompany`.com:81/
--verbose --always-auth=false create-react-app`

  > Don't forget to replace "mycompany" with your company's name.

This second command will install `create-react-app` using the settings you provide. (You can also provide the same settings using `npm config` if you prefer.)
