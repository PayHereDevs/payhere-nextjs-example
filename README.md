This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

This repo contains an example integration of a Next.js project with the [PayHere Javascript SDK](https://support.payhere.lk/api-&-mobile-sdk/payhere-javascript).

## PayHere

######  1. Development and production versions of the `payhere.js` file are available in the "public" folder.

```
- public
 - payhere.js
 - payhere.dev.js
```

###### 2. In `index.js`, the appropriate script is loaded from this method:
```js
function payHereURL(){
    if (process && process.env.NODE_ENV == "production")
      return '/payhere.js';
    else
      return '/payhere.dev.js';
}
```

###### 3. Include the PayHere Script as follows:

```jsx
<script src={payHereURL()}></script>
```

###### 4. Check the `startPayment()` method in `index.js` to see how PayHere is integrated. 

## Run

Run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
