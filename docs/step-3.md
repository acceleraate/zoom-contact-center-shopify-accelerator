# Step 3 - Voice Channel Configuration

## 3.1 Create the Voice Flow in Zoom Contact Center

⏱️ 5 minutes

- Download [accShopifyVoice.json](../accShopifyVoice.json) file - if you're not cloning the repo then right-click the file link and select **Save link as...**
- Within **Zoom Contact Center Management**, select **Flows** in the left menu
- First we need to create the voice flow. To do this, click **Import**, and then within the dialog:
  - Enter the name: `accShopifyVoice`
  - Enter the description: `Calls Shopify Admin API to retrieve customer/order data and populate Zoom custom variables. Accelerator provided by Acceleraate Ltd - acceleraate.com`
  - Click **Import** and then locate the file **accShopifyVoice.json** you downloaded
  - Click Add
- After importing, the flow will be in a draft state and will need to be published. To do this, click on **accShopifyVoice** in the list of flows to edit it and the flow will open in a new browser tab. Within the flow editing screen:

  - Click the **Publish** button located in the top-right of the screen - this can take up to 30 seconds to publish.

## 3.2 Attach a Phone Number to the Flow

⏱️ 2 minutes

Next, you’ll need to attach an entry point to the **accShopifyVoice** flow you created:

- In the **Contact Centre Management** section, click on **Flows**
- Locate the **accShopifyVoice** flow in the list, click on the three dots icon on the right of the row and select **Manage Entry Point**
- Click **Add Entry Point**
- Tick the box next the the phone number you want to use - if you need a new phone number then click the **Get Number** button.
- Then click **Save**
- On the **Manage Entry Point for Voice** dialog, optionally set a language, then click Save.

## Next Step

[Step 4 - Web Chat Channel Configuration](step-4.md)

[Step 5 - Testing the Shopify Accelerator](step-5.md)

---

## Installation Index

[Zoom Contact Center &amp; Shopify Accelerator](../README.md)

[Step 1 - Shopify App Installation](step-1.md)

[Step 2 - Zoom Contact Center Configuration](step-2.md)

[Step 3 - Voice Channel Configuration](step-3.md)

[Step 4 - Web Chat Channel Configuration](step-4.md)

[Step 5 - Testing the Shopify Accelerator](step-5.md)

[Step 6 - Customising the Flows](step-6.md)
