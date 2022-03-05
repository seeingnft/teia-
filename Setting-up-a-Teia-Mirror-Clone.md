## Apache/Local Webserver/Traditional Web Host

_by Manitcor_

### Using npm
if you use yarn just translate the commands

```bash
git clone https://github.com/teia-community/teia-ui.git
cd teia-ui
npm install
npm run start # to test locally 
npm run build
```
The output build can be found in the `build` directory, copy this output to your web server.

### `.htaccess` for apache

```htaccess
RewriteEngine on

# Don't rewrite files or directories
RewriteCond %{REQUEST_FILENAME} -f [OR]
RewriteCond %{REQUEST_FILENAME} -d
RewriteRule ^ - [L]

# Rewrite everything else to index.html to allow html5 state links
RewriteRule ^ index.html [L]
```

## Netlify or Cloudflare

_by NFTBiker_

I don't know for Digital Ocean, but the most straight forward way is Netlify or Cloudflare page. 
For Netlify it's just:

1. You need a free Github account and a free Netlify account
2. Clone this repository in your own Github account
3. Go to Netlify and use "New site from Git". When linking to your Github account, if you don't allow Netlify to access everything, you will have to follow their instructions to configure access to your cloned repository
4. Follow Netlify deployment instructions, and for the build command use :
CI=false npm run build

Cloudflare page, the process is similar ... have the repo in your own github account, then cloudflare ask to connect to github, select repo, and then it build ... And it run ... Both work great, i've used both


## Vercel

_by mel_

```bash 
git clone https://github.com/teia-community/teia-ui.git
cd teia-ui
pnpm install # or npm install or yarn
npx vercel # follow the instructions
```