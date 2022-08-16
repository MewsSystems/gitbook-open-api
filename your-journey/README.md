# Your journey with Mews

> ### Partner ID
> You will be given a Partner ID at the start of the process, please keep this safe as you will need this ID when it is time to certify your integration.

We want your experience working with Mews to be quick and simple, so we make the process as automated and self-service as possible and minimise touchpoints with the Mews team.
You just need to follow these steps:

* [Step 1: Explore the APIs](#step-1-exploration)
* [Step 2: Let us known what you plan to do](#step-2-qualification)
* [Step 3: Develop and test your solution](#step-3-development)
* [Step 4: Get certified](#step-4-certification)
* [Step 5: Go live with a pilot](#step-5-pilot)
* [Step 6: Go into full production!](#step-6-production)

If you have questions about the process, drop us a line to [partnersuccess@mews.com](mailto:partnersuccess@mews.com).

## Step 1: Exploration

First find out [which of our APIs you should be using](../the-mews-apis/README.md).
If you're not sure, take a look at the [use cases](../use-cases/README.md) for suggestions.
Each API has its own body of documentation, so you'll want to familiarize yourself with the guidelines and operations for the API you'll be using.

## Step 2: Qualification

Once you've had a chance to familiarize yourself with the APIs and the process, you will be asked to complete a short Qualification step to answer some basic questions:

* Which API or APIs will you be developing against?
* Is this a private integration (for just one enterprise customer) or a public integration (available through the Mews Marketplace)?
* If this is a public integration, then what will be the pilot site?
* What is your estimated timescale for development?

## Step 3: Development

When you've decided which API operations to use and how, you'll see each API has its own demo credentials for you to try them out, connecting to our demo servers.
All of the information you need to start developing and testing is in the documentation.
For example, if you're working with the Mews Connector API, the [guidelines](https://mews-systems.gitbook.io/connector-api/guidelines) include details of the [URLs and access credentials](https://mews-systems.gitbook.io/connector-api/guidelines/environments).

## Step 4: Certification

When you are finished developing and testing, it's time to get certified! Complete the [certification form](https://mews.typeform.com/to/ehTUz7) and you'll be able to select a date for certification.
As part of the certification process, you will be asked for some details about your integration, such as the endpoints you will be using and the request message frequency.
For more information about the process, see [Connector API Certification: What to expect](https://help.mews.com/s/article/connector-api-certification-what-to-expect?language=en_US) and [Channel API Certification: What to expect](https://help.mews.com/s/article/channel-api-certification-what-to-expect?language=en_US).

## Step 5: Pilot

After successful certification, you will be sent a unique `Client Token` for connection to production sites.
To connect to a customer property, you will also need an `Access Token` or `Connection Token` unique to the property.

* __Private integration__<br>
If this is a private integration to a single enterprise, Mews will add the integration to the relevant properties and you will automatically be sent the relevant connection tokens.
* __Public integration__<br>
If your integration is intended to be listed publicly in the Mews Marketplace, Mews will add the integration to the agreed pilot property and you will be automatically sent the relevant connection token for that property.

## Step 6: Production

If your integration is intended to be listed publicly in the Mews Marketplace, then after an agreed period(\*1) of successful operation at the pilot site, you will automatically be notified by email with final instructions.
Your solution will be listed in the Mews Marketplace and on the [Mews website](https://www.mews.com/en/products/marketplace), and you can roll it out to all properties that want to integrate.
For further information, see the [Connector API onboarding guide](https://help.mews.com/s/article/connector-api-integrations-onboarding-mutual-customers?language=en_US) and the [Channel Manager API onboarding guide](https://help.mews.com/s/article/channel-manager-onboarding-guide?language=en_US).

> \*1 The pilot period will depend on circumstances, but typically this will be 2 weeks for a Connector API integration, 4 weeks for a Channel Manager API integration, or 0 weeks for a Booking Engine API integration.
