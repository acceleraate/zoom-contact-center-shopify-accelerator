# Step 5 - Testing

## 5.1 Testing Overview

To test the Shopify Accelerator you’ll need some customer/order details from your Shopify account. You’ll need one or more of the following:

- Customer email address
- Customer phone number
- Order number

## 5.1 Testing the Voice Channel

_Coming soon_

## 5.2 Testing the Web Chat Channel

- Open up your website and navigate to page where the script tag has been added from the previous step
- The Zoom web chat icon will appear
- Click the icon to start the web chat and enter your details
  Once the chat starts then the accShopifyWebChat flow will run and you can test the Shopify integration. First you’ll be asked how you’d like to search. Simply follow the steps and provide the information requested. If everything is working properly, the information gathered from your Shopify account will be displayed to you in the chat window. If there are any errors, then these will be displayed along with the error codes listed below in the Troubleshooting section.

## Troubleshooting

If errors are encountered during the processing of the flow, then use the code returned in the error message and the list below to check for troubleshooting steps.

Error: `1001` - No API Key defined

- The API key is the security mechanism used by Shopify to authorise calls to their API to retrieve your customer and order details.
- Check that you’ve taken the API key from Step 1 and entered it as a linked value against the apiKey Zoom Contact Centre Global Variable you created in Step 2.
- If you didn’t make a note of your API Key then you will need to Uninstall the Custom App in Shopify and repeat Step 1.

Error: `1002` - No Store Name defined

- The Store Name value is what’s used to uniquely identify your Shopify store in the URL:
  - URL format: `https://[store-name].myshopify.com`
  - Example URL: `https://test-store.myshopify.com`
- In the above example, the value needed would be test-store however the value needed will be specific to your own store.
- Check that you’ve got the correct store name and entered it as a linked value against the storeName Zoom Contact Centre Global Variable you created in Step 2.

Error: `1003` - No variables set

- None of the required pre-execution Global Variables were set. The test flow provided will prompt the end-user for one of the following values:
  - Customer email
  - Customer phone
  - Order number
- If you’ve modified the flows to include your own logic, then make sure that you’ve set one of the following variables in your flow:
  - `global_custom.accShopify.customerEmail`
  - `global_custom.accShopify.customerPhone`
  - `global_custom.accShopify.orderNumber`
- Refer to the Zoom documentation on how to set global variables within the Script widget.

Error: `1004` - Supplied email address not valid

- The value provided as an email address to the `customerEmail` variable wasn’t valid

Error: `1005` - Supplied phone number not valid

- The value provided to the customerPhone variable wasn’t valid. Phone numbers must be in the E164 standard e.g. For example:
  - UK number `0161 123 4567` in E164 format is `441611234567`
  - UK mobile number `07777 123 456` in E164 format is `447777123456`
  - USA number `555-513-0514` in E164 format is `15555130514`
  - Please note that the `+` is not needed when carrying out a search, however the script below accepts it but will strip it from the return value

Error: `2001` - Authentication failed

Error: `2002` - Timeout

Error: `3001` - Customer not found using email address

- Check that the email address matches a customer in your Shopify account
- Use the Shopify admin portal to search for a customer using the same value
- Double-check that the `apiKey` and `storeName` Zoom Global Variables are set to the correct values for the same Shopify store.
- If using your own flow logic then consider implementing the function in a script block detailed in Error `1004` to make sure that the email is in the expected format.

Error: `3002` - Customer not found using phone number

- Check that the phone number entered matches a customer in your Shopify account
- Use the Shopify admin portal to search for a customer using the same value
- Double-check that the `apiKey` and `storeName` Zoom Global Variables are set to the correct values for the same Shopify store.
- If using your own flow logic then consider implementing the function in a script block detailed in Error `1005` to make sure that the phone number is in E164 format.

Error: `3003` - Order not found

- Check that the order number entered matches a customer in your Shopify account
- Use the Shopify order number to search and not the order ID - the order number can be either with or without the leading # character
- Use the Shopify admin portal to search for a customer using the same value
- Double-check that the `apiKey` and `storeName` Zoom Global Variables are set to the correct values for the same Shopify store.

Error: `9000` - Unexpected error

- A script block resulted in an unexpected error
- The error message will include a description of the error, the name of the flow and the name of the block where the error occured

## Next Step

Do you need more help customising your flows? Contact us at [support@acceleraate.com](mailto:support@acceleraate.com)

---

## Installation Index

[Zoom Contact Center &amp; Shopify Accelerator](../README.md)

[Step 1: Shopify App Installation](step-1.md)

[Step 2: Zoom Contact Center Configuration](step-2.md)

[Step 3: Voice Channel Configuration](step-3.md)

[Step 4: Web Chat Channel Configuration](step-4.md)

[Step 5: Testing](step-5.md)
