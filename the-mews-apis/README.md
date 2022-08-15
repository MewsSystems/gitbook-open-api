# The Mews APIs

Mews currently supports three separate APIs, each serving a different purpose.

> ### Three individual APIs
>
> * [Mews Connector API](#mews-connector-api)
> * [Mews Channel Manager API](#mews-channel-manager-api)
> * [Mews Booking Engine API](#mews-booking-engine-api)

The documentation for each API is self-contained and consists of two parts:

* A set of guidelines on how to use the API
* A detailed reference for all the API operations

And each API is hosted as a public GitHub repository.

## Mews Connector API

This API is a general-purpose API that gives access to data and services in Mews Operations.
The API supports many use cases, including Kiosk, Point Of Sale, Reservations Data, Upselling and Events Management, to name just a few.
We encourage you to explore the API and innovate new solutions for our customers!

* For the full documentation, see [Mews Connector API](https://mews-systems.gitbook.io/connector-api/)

## Mews Channel Manager API

This API is for Channel Managers and other distribution channels to fetch availability, rates and inventory data, and make reservations.

* For the full documentation, see [Mews Channel Manager API](https://mews-systems.gitbook.io/channel-manager-api/)

## Mews Booking Engine API

This API is for booking engines to enable your customers to create reservations directly in Mews.
Please note that if you want to build a custom booking engine solution, you will need a Mews Enterprise subscription.

* For the full documentation, see [Mews Booking Engine API](https://mews-systems.gitbook.io/booking-engine-guide/)

## Which API to use?

If you are a Channel Manager, or a bulk sales or distribution channel such as an Online Travel Agent, then you will want the [Mews Channel Manager API](https://mews-systems.gitbook.io/channel-manager-api/).
If you are implementing a Booking Engine for your customers to book with you directly, you will want the [Mews Booking Engine API](https://mews-systems.gitbook.io/booking-engine-guide/).
For all other use cases, use the [Mews Connector API](https://mews-systems.gitbook.io/connector-api/).
Please also take a look at [Use Cases](../use-cases/README.md), where you can find more information on individual use cases and links to more details in the documentation for the appropriate API.
