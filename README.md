What’s in the zip
asveda-landing/
├── index.html      ← the full landing page (HTML + CSS)
├── images/         ← banner and product photos
├── CNAME           ← your custom domain (edit this)
├── .nojekyll
└── README.md

The page is a single index.html. It has a sticky header, a banner and 3 product tiles, a “why As Veda” section and one section each for KaanUpchar, G.V Piles and Fat Cut Pro. Below those are a how-to-order section, a Google Form embed for leads, an FAQ, a footer, and a sticky WhatsApp and call-back bar.

Step 1: Put it on GitHub
Create a free account at github.com, then click New repository.
Name it asveda-landing and set it to Public.
Unzip the folder, then on the repo page click Add file → Upload files. Drag in everything, including the images folder, and click Commit changes.

Or with the command line:

bash
cd asveda-landing
git init
git add .
git commit -m "First landing page"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/asveda-landing.git
git push -u origin main
Step 2: Turn on GitHub Pages
In the repo, go to Settings → Pages.
Under Source, choose Deploy from a branch, then branch main and folder / (root), and click Save.
After 1–2 minutes the site is live at https://YOUR-USERNAME.github.io/asveda-landing/.
Step 3: Connect your domain

Your main site asvedaindia.com is already in use. Pointing it at GitHub would replace your current website. I’d use a subdomain such as offer.asvedaindia.com, which is why the CNAME file contains that. Edit the file if you want a different name.

At your domain registrar (GoDaddy, Hostinger, Namecheap and so on), open DNS settings and add this record:

Type	Name	Value
CNAME	offer	YOUR-USERNAME.github.io

Then:

In GitHub go to Settings → Pages → Custom domain, enter offer.asvedaindia.com and click Save.
Wait 10 minutes to a few hours for DNS to update, then tick Enforce HTTPS. The free SSL certificate is issued automatically.

If you buy a new domain and want it at the root (for example asvedaoffers.in), add these four A records with name @, plus a www CNAME to YOUR-USERNAME.github.io:

185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153

Put that domain in the CNAME file instead.

Things to check before going live
The herb lists carry the comment EDIT: keep only the herbs that are on your product label. Make sure they match your actual labels and ingredients.
Health-benefit wording on Ayurvedic products can draw attention from Indian regulators. Your disclaimer is a good start, so keep the language modest.
To change the WhatsApp number, search 919266040184 in index.html.
