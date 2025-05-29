# Your journey with Mews

We aim to make your integration journey with Mews efficient and self-service, minimizing dependencies on our support team. Just follow these five steps:

* [Step 1: Explore the APIs](#step-1-exploration)
* [Step 2: Let us know what you plan to do](#step-2-registration)
* [Step 3: Develop and test your integration](#step-3-development)
* [Step 4: Get certified](#step-4-certification)
* [Step 5: Go live with your solution](#step-5-go-live)

If you have questions about the process, reach out to [partnersuccess@mews.com](mailto:partnersuccess@mews.com).

> ### Booking Engine integrations
> Booking Engine integrations are an exception: they do not need to be certified, do not need a pilot property, and will not normally be listed in the Mews Marketplace. See [Booking Engine integrations](booking-engine-integrations.md).

## Step 1: Exploration

> Check out our public documentation.

All Mews API documentation is publicly accessible, allowing you to explore without barriers. Start by identifying [which API to use](../the-mews-apis/README.md). If you're unsure, take a look at our [use cases](../use-cases/README.md) for guidance. Each API has its own documentation—review the operations and guidelines relevant to your integration.

## Step 2: Registration

> Register your application integration with Mews (all except Booking Engine integrations).

### Partner registration
Before you begin development, register to [Become a Mews Partner](https://www.mews.com/en/partners/new-partnerships). This step is required for both public and private integrations (except Booking Engine integrations). Once approved:

* You may be invited to the [Partner Portal](https://partnerportal.mews.com), where you can manage your integrations and access support resources.
* If not, you will receive a `Partner ID` for email-based communication.

### Application registration
After your partner registration is complete, register your specific application.

**If you have access to the Partner Portal**:

* Log in to the [Partner Portal](https://partnerportal.mews.com).
* Navigate to __Integrations__ and select __Start New Application__.

**If you received a Partner ID instead**:

You will be prompted by email to provide basic details:
* Which API(s) will your integration use?
* Is this a private integration (for a specific enterprise) or a public integration (listed in the Mews Marketplace)?
* If public, what is the pilot property?
* What is your estimated timeline for development?

## Step 3: Development

> Go develop your integration!

Once registered, you can begin development and testing in our sandbox environments. In most cases, public Demo credentials are provided in the documentation. In some cases, such as the Channel Manager API, you’ll need to request a `Client Token` from Mews to access the Demo environment. See the specific API documentation for details:

* [Mews Connector API: Demo environment access](https://mews-systems.gitbook.io/connector-api/guidelines/environments)
* [Mews Channel Manager API: Demo environment access](https://mews-systems.gitbook.io/channel-manager-api/your-journey)

## Step 4: Certification

> Let's check your integration is fit for production.

Before you can connect to live properties, public integrations must go through a Certification process to ensure compatibility and performance. The process differs depending on your access method.

**If using the Partner Portal**:

* Log in to the [Partner Portal](https://partnerportal.mews.com).
* Navigate to __Integrations__ and select __Certify Existing Applications__.

**If using a Partner ID**:

* Complete the [Certification Form](https://mews.typeform.com/to/ehTUz7).
* Instructions will follow via email.

You’ll be asked for details such as:
* Endpoints you will call
* Estimated message volume
* Retry or error handling strategy

You can find more information about certification in the documentation for individual APIs:
* [Mews Connector API Certification](https://mews-systems.gitbook.io/connector-api/guidelines/certification)
* [Mews Channel Manager API Certification](https://mews-systems.gitbook.io/channel-manager-api/certification)

> If your integration does not meet the certification criteria, we will provide feedback and ask you to address specific issues before reapplying.

## Step 5: Go live

> Let's roll out your solution to live customer sites.

### Pilot (monitoring)

We start by enabling the integration on a single property to monitor stability and performance — even for private integrations.

After a successful Certification step, you will receive a `Client Token` for connection to production sites; this token is unique to your application. To connect to a specific customer property, you will also need a second token, dependent on the API:

* `Access Token` (for the Mews Connector API) – property-specific
* `Connection Token` (for the Mews Channel Manager API) – property-specific

> **Security reminder:** Tokens grant access to sensitive customer data. Treat them like passwords: store them securely, never share them, and never send them via email.

**Public integration**:

If your integration is intended to be listed publicly in the Mews Marketplace, Mews will add the integration to the agreed pilot property and you will be automatically sent the relevant token for that property (either `Access Token` for a Connector API integration, or `Connection Token` for a Channel Manager API integration). The integration will need to run successfully for a period of time(\*1) on the pilot site before you can progress to full [Publication](#publication).

**Private integration**:

If this is a private integration to a single enterprise or chain, Mews will add the integration to the relevant properties and you will automatically be sent the relevant token or tokens (`Access Tokens` for Connector API integrations, or `Connection Tokens` for Channel Manager API integrations). Although there is no pilot site, we will still monitor the performance of the integration for a period of time\(*1\) just to confirm everything is ok.

### Publication

After a successful pilot or monitoring stage, your integration will be declared fit for general publication. Unless it's a private integration, you will automatically be notified by email with final instructions, and your application will be listed in the [Mews Marketplace](../mews-marketplace/README.md) and on the [Mews website](https://www.mews.com/en/products/marketplace), and you can roll it out to all properties that want to integrate.

For additional resources, search the [Mews Help Center](https://help.mews.com).

> \*1 The monitoring period will depend on circumstances, but typically this will be 2 weeks for a Connector API integration or 4 weeks for a Channel Manager API integration.
