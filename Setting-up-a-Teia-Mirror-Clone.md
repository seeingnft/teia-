## Apache/Local Webserver/Traditional Web Host

_by Manitcor_

this was done on NPM 7.24.1 and NODE.js 15.14.0 on windows 10 using WSL2 with ubuntu 20.04 but should work with many different setups. Try yours first before changing anything. 

**using npm **
if you use yarn just translate the commands
1. Pull down site
2. npm install
3. npm run build
4. to test local - npm run start
5. Output of build command can be found in the build directory, copy this output to your web server

**For Local webserver use after build**
1. npm install serve -g  (only do this once)
2. navigate to build directory
3. serve
4. Prompt will tell you port and URI (usually http://localhost:3000/)

**.htaccess for apache**

`RewriteEngine on`

`# Don't rewrite files or directories`

`RewriteCond %{REQUEST_FILENAME} -f [OR]`

`RewriteCond %{REQUEST_FILENAME} -d`

`RewriteRule ^ - [L]`

`# Rewrite everything else to index.html to allow html5 state links`

`RewriteRule ^ index.html [L]`

## netlify or Cloudflare

_by NFTBiker_

I don't know for digital ocean, but the most straight forward way is netlify or cloudflare page. For netlify it's just:
1. You need a free Github account and a free Netlify account
2. Clone this repository in your own Github account
3. Go to Netlify and use "New site from Git". When linking to your Github account, if you don't allow Netlify to access everything, you will have to follow their instructions to configure access to your cloned repository
4. Follow Netlify deployment instructions, and for the build command use :
CI=false npm run build

Cloudflare page, the process is similar ... have the repo in your own github account, then cloudflare ask to connect to github, select repo, and then it build ... And it run ... Both work great, i've used both


## vercel

_by mel_

npm install -g vercel 
git clone https://github.com/hicetnunc2000/hicetnunc.git
cd hicetnunc
npm install 
vercel 
