# DNS Configuration: backstageinteractive.com

To point your domain to the new **Mission Control** monorepo on Netlify, please update your GoDaddy DNS settings:

## Nameservers (Recommended)
If you want Netlify to handle your SSL and DNS automatically (easiest way to get "Clean URLs"):
1. Log in to GoDaddy.
2. Go to **DNS Management** for `backstageinteractive.com`.
3. Change **Nameservers** to "Custom".
4. Enter the Netlify nameservers (usually look like `dns1.p01.nsone.net`, etc.). 
   *Note: I'll need you to check your Netlify dashboard for the exact four addresses they've assigned to this site.*

## A Record (Alternative)
If you'd rather keep DNS at GoDaddy:
1. **Type**: A
2. **Name**: @
3. **Value**: 75.101.163.88 (Netlify's Load Balancer IP)
4. **Type**: CNAME
5. **Name**: www
6. **Value**: [your-netlify-subdomain].netlify.app

Let me know which path you prefer!
