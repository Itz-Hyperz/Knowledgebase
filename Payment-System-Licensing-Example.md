# Payment System Licensing

You need to make a GET request to `https://domain.ext/api/v1/license/check/YOUR_LICENSE_KEY`

MAKE SURE TO REPLACE `domain.ext` with YOUR DOMAIN!

Here is a code example in JavaScript. Make sure to provide the productid header in the `GET` request.

```js
const axios = require('axios');
licenseCheck("YOUR_PRODUCT_UNIQUE_ID", "YOUR_LICENSE_KEY");

async function licenseCheck(productId, licenseKey) {
  let request = await axios({
    method: 'get',
    url: 'https://domain.ext/api/v1/license/check/' + licenseKey,
    headers: {
      'Content-Type': 'application/json',
      'productid': productId
    },
  });

  if(request.data.authorized) {
    return console.log('License Authorized!');
  } else {
    console.log('License Failed!');
    if(request.data.reason != 'success.') console.log(request.data.reason);
    return process.exit(1);
  };
};
```
