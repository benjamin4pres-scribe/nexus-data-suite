# 🚀 Advanced Setup: Google OAuth & Billing Configuration

**Who is this for?**
The default "API Key" method (via Google AI Studio) is free and recommended for 95% of users. However, if you are a power user processing massive amounts of data, running up against standard rate limits, or operating in an enterprise environment, you can use the **Advanced Setup (Google Login)**. 

This method authenticates your Google account directly. **However, it will only work if your Google account has an active Google Cloud Project (GCP) with billing enabled.**

If you select this option without a billing profile, Google will block the connection with a `403 Permission Denied` error. 

Follow these steps to configure your Google account for Advanced Setup.

### Step 1: Create a Google Cloud Project
1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Sign in with the Google Account you intend to use with Nexus Data Suite.
3. In the top navigation bar, click the **Project Dropdown** (next to the Google Cloud logo).
4. Click **New Project** in the top right of the popup window.
5. Name your project (e.g., `Nexus-Data-Suite-Billing`) and click **Create**.
6. Once created, make sure that project is selected in the top dropdown.

### Step 2: Enable Cloud Billing
*Note: Google offers a $300 free trial for new Cloud users, and Gemini 1.5 Flash is incredibly cheap, but a credit card is required to verify identity and cover overages.*
1. In the left-hand sidebar of the Cloud Console, click on **Billing**.
2. Click **Link a billing account** or **Manage billing accounts**.
3. Follow the prompts to create a new billing account and enter your payment details.
4. Ensure your new billing account is successfully linked to the project you created in Step 1.

### Step 3: Enable the Generative Language API
For Nexus to route its requests through your billing account, the specific AI API must be turned on inside your project.
1. In the left-hand sidebar, go to **APIs & Services** > **Library**.
2. In the search bar, type **Generative Language API**.
3. Click on the result, and click the blue **Enable** button.

### Step 4: Locate Your Project ID (Important)
When you log into Nexus Data Suite via the Advanced Setup, the app may ask for your **Project ID** to ensure the API traffic is correctly routed to your billing profile.
1. Go to the [Cloud Console Dashboard](https://console.cloud.google.com/home/dashboard).
2. Look at the **Project Info** card in the top left.
3. Copy the **Project ID** (it usually looks like `nexus-data-suite-123456`). Keep this handy for the Nexus interface.

### Step 5: Log in to Nexus
You are all set! 
1. Open Nexus Data Suite.
2. Open **AI Settings** and select **Advanced Setup (Google Login)** from the dropdown.
3. Click **Sign in with Google**, select the account you just configured, and accept the permission prompts. 
4. If prompted, paste your Project ID. You now have high-capacity, rate-limit-free access to the suite!
