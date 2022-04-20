# Adtrak NextJs Boilerplate with WordPress headless CMS
A [Next.js](https://nextjs.org/) & WordPress starter kit with [Framer Motion](https://www.framer.com/motion/) and [TailwindCSS](https://tailwindcss.com/) plugged in

The WordPress install can be found at [adtrak-next.adtrak.agency](https://adtrak-next.adtrak.agency/). The logins can be found in Salesforce [here](https://adtrak.lightning.force.com/lightning/r/Password__c/a0J08000018LHt5EAG/view)

There is a working React version of ALD that uses ```localStorage``` (via Store.js) to store the query values for 30 days. After 30 days, the storage items will be destroyed when the user next visits the page.

## Global Data
```app.js``` generates a ```globalData``` object containing:
- Global Options (site title etc from WordPress)
- Site Options (ACF Fields from custom options page)
- Marketing (ACF Fields from custom options page)
- Primary and Secondary menus 

The ```globalData``` object is passed around using Context so we don't have to query it on every page. 

## Routes
- Page routes have been configured for parent & child pages, and should work out of the box. 
- Location page routes will be generated from the Locations custom post type
- News pages will be configured from the Posts post-type (standard Posts in WordPress).
-  - News items will revalidate every 60 seconds, meaning new posts will have routes generated automatically without the need for a project rebuild.

## Learn More

To learn more about Next.js, take a look at the following resources:

-  [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.

-  [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!
