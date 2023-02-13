# Step 4 - Web Chat Channel Configuration

⏱️ 12 minutes + time to update and publish your own website

---

## 4.1 Create the Web Chat Flow in Zoom Contact Center

⏱️ 5 minutes

- Download [accShopifyWebChat.json](../accShopifyWebChat.json) file
- Within **Zoom Contact Center Management**, select **Flows** in the left menu
- First we need to create the web chat flow. To do this, click **Import**, and then within the dialog:
  - Enter the name: `accShopifyWebChat`
  - Enter the description: `Calls Shopify Admin API to retrieve customer/order data and populate Zoom custom variables. Accelerator provided by Acceleraate Ltd - acceleraate.com`
  - Click **Import** and then locate the file **accShopifyWebChat.json** you downloaded
  - Click Add
- After importing, the flow will be in a draft state and will need to be published. To do this, click on **accShopifyWebChat** in the list of flows to edit it and the flow will open in a new browser tab. Within the flow editing screen:
  - Click the **Publish** button located in the top-right of the screen - this can take up to 30 seconds to publish.
  - Once it’s confirmed as published then close the flow tab

## 4.2 Create an Entry ID for Web Chat

⏱️ 3 minutes

Within Zoom Contact Centre, an Entry ID is the mechanism for linking a flow to your website.

- Within the Zoom Admin Portal, in the **Contact Centre Management** section, select **Preferences**
- Click the **Entry ID** tab and then click the **Create** button.
- Enter a display name for the Entry ID, e.g. `shopify-webchat`
- Then click **Create** and the new entry ID will appear on the list

## 4.3 Attach the Entry ID to your Web Chat Flow

⏱️ 2 minutes

Next, you’ll need to attach the new Entry ID to the **accShopifyWebChat** flow you created:

- In the **Contact Centre Management** section, click on **Flows**
- Locate the **accShopifyWebChat** flow in the list, click on the three dots icon on the right of the row and select **Manage Entry Point**
- Click **Add Entry Point**
- Tick the box next the the Entry ID you created earlier, then click **Save**
- Select the **Install SDK** option
- Click the **Copy** button to copy the script tag
- Make a note of the script by pasting it into a safe place - you’ll need this script when updating your website in the next step
- Finally, click **Save** and the dialog will close

## 4.4 Add the script to your website

⏱️ Time depends on your own website publishing process

To test your flow from a web browser, you need install the script you got from the previous step onto your website. It’s likely that you’ll need help from your web development or web publishing teams to make these changes.

- Locate the script that you saved from the previous step. It will look something like the example below - make sure that you use your own script and **DO NOT copy this script** as it won’t work on your website.

```JavaScript
// Don't copy this script to your site
<script
  data-chat-entry-id="XXXyyyZZZaaaBBBccc"
  src="https://xxxxxxxx.zoom.us/zzz/web-sdk/chat-client.js">
</script>
```

- Add the script tag to any pages where you want your chat to be available - the best place for the script is just before the closing body tag `</body>`

## 4.5 Add your website domain to your list of Associated Domains

⏱️ 2 minutes

It’s important that you’ve added your website domain to the list of Associated Domains within Zoom Account Management, Account Profile. If you don’t do this then the chat function will fail as it won’t be able to access your Zoom Contact Centre account.

You can set up Associated Domains for your website staging/test environments in addition to your live environment.

Refer to the Zoom documentation for adding Associated Domains.

## 4.6 Publish your website updates

⏱️ Time depends on your own website publishing process

Finally, publish the changes you made to your website.

---

## Next Step

[Step 5 - Testing the Shopify Accelerator](step-5.md)

---

## Installation Index

[Zoom Contact Center &amp; Shopify Accelerator](../README.md)

[Step 1: Shopify App Installation](step-1.md)

[Step 2: Zoom Contact Center Configuration](step-2.md)

[Step 3: Voice Channel Configuration](step-3.md)

[Step 4: Web Chat Channel Configuration](step-4.md)

[Step 5: Testing](step-5.md)
