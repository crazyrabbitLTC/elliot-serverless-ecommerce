# Elliot's ZEIT Next.js Ecommerce Boilerplate

![ELLIOT X ZEIT](elliot-zeit.jpg)

## Features

- Deploy, sell and fulfill in seconds
- Fully localized: multi-currency and language, duties and taxes (DDP - Delivered Duty Paid)
- Native cross border fulfillment: packing, shipping and return labels, commercial invoices and custom declarations forms
- Instant global payments: Apple, Google, Ali and WeChat Pay, plus all major credit cards and leading payment options (Klarna, iDEAL)
- Static SSR for collections, products and all simple pages, in 100+ languages
- Fast and high performing (90%+ across a11y, Performance, and SEO)
- Fully customizable
- Mobile-first and fully responsive
- Cutting-edge project structure and architecture (GraphQL, Next.js and serverless)
- Continuous deployment with [ZEIT Now](https://zeit.co)

## Core Team

If you're new and need some guidance feel free reach out to any of our core team members:

- [Franco Arza](https://github.com/arzafran): `@arzafran`
- [Ismail Ghallou](https://github.com/smakosh): `@smakosh`
- [Omoefe Dukuye](https://github.com/un-tethered): `@un-tethered`

## Structure

```bash
.
├── src
│   ├── components          # Components
│   │   │── cart              # Components used on the cart page
│   │   │── checkout          # Components used on the checkout page
│   │   │── common            # Common components
│   │   │── listing           # Components used on the landing page
│   │   │── product           # Components used on the product page
│   │   └── theme             # Header, Footer, global style and theme config
│   ├── config              # Config variables
│   ├── helpers             # Helpers functions
│   ├── hoc                 # Higher order components
│   ├── lang                # i18n json files
│   ├── pages               # Pages
│   ├── providers           # Providers
│   ├── queries             # GraphQL queries we run during build time
│   ├── reducers            # Reducers
│   ├── scripts             # Scripts meant to be executed before building the website
│   └── pages               # Pages
└── public/.well-known/    # Where you'd put the Apple verification file
```

## Prerequisites

[Create an Elliot account](https://admin.elliot.store/)

> Start by creating a store and adding a few products to it!

[Yarn](https://yarnpkg.com/en/) or [NPM](https://nodejs.org/)

### Locally

1. Clone the repository
2. Create dev environment file from template `./.env.development.tempate` by running `cp .env.development.template .env.development`
3. Use the [Elliot CLI](https://github.com/helloiamelliot/elliot-cli) to fetch your account's single env variable containing:

   ```bash
   ELLIOT_DOMAIN_ID|ELLIOT_STORE_FRONT_ID|ELLIOT_STORE_FRONT_NAME|ELLIOT_API_KEY
   ```

4. Or get them via the [Elliot Dashboard](https://admin.elliot.store/) by clicking on "Get Headless"
5. To enable Apple Pay, you will have to get the Apple verification file and place it under `/public/.well-known/`

   > Follow this [Guide](https://github.com/helloiamelliot/elliot-serverless-ecommerce#Apple) to get the Apple verification file

6. Run the following commands to start the server locally:

   ```bash
   npm i && npm run dev
   ```

7. When deploying to [ZEIT Now](https://zeit.co), you will have to set the [Now secrets](https://zeit.co/docs/v2/build-step#adding-secrets), so ensure that they've been added:

   ```bash
   now secrets add base_url <your domain name>
   now secrets add elliot_env_variables <your Elliot env variable>
   now --prod // Or by pushing to your GitHub repository
   ```

### Production

1. Go to your Domain space
2. Click on "Get Headless"
3. Follow the on boarding and you will be good to go!

> To enable Apple Pay, you will have to get the Apple verification file and place it under `/public/.well-known/`

> Follow this [Guide](https://github.com/helloiamelliot/elliot-serverless-ecommerce#Apple) to get the Apple verification file

## Built with

- Next.js
- React
- VSCode
- And these useful of JavaScript libraries [package.json](package.json)

## Want to contribute?

Want to invest some time in building the future of global commerce? Email us at devs@elliot.store.

If you have discovered a 🐜 or have a feature suggestion, feel free to create an issue on Github.