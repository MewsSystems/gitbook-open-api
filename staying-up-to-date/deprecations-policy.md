# Deprecations Policy

2nd November 2022

## Contents

This policy addresses the following:

* [Why we have this policy](#why-we-have-this-policy)
* [What do we mean by deprecated?](#what-do-we-mean-by-deprecated)
* [What we deprecate and why](#what-we-deprecate-and-why)
* [When we deprecate](#when-we-deprecate)
* [How we deprecate](#how-we-deprecate)
* [How long is the stoppage notice period?](#how-long-is-the-stoppage-notice-period)
* [How deprecations are communicated](#how-deprecations-are-communicated)
* [As a user, what should I do?](#as-a-user-what-should-i-do)
* [Deprecations & Versioning](#deprecations--versioning)
* [Questions & feedback](#questions--feedback)

## Why we have this policy

Changes to the APIs are necessary and inevitable as part of continuous improvement to our products and services. We try to make those changes in such a way that there is only positive impact on users, not negative impact.
For example, we announce new features and other changes, we encourage you to take advantage of them, and we actively try to avoid making breaking changes, i.e. changes that would impact your current implementation.

Sometimes, however, breaking changes are unavoidable. So the question becomes, how can we manage these changes in a way that has the least negative impact on users?
The answer is not to simply stop a feature or make a breaking change without plenty of notice. Making a feature `deprecated` is us giving notice that this feature will be stopped in the future.

## What do we mean by deprecated?

* **Deprecated**<br>A feature which is `deprecated` is considered an old feature that users should migrate away from; it is no longer up to date; the implication is that there is a better way to do something, or else this something should no longer be done at all; a `deprecated` feature is still supported, it still works, but this is likely to be only for a limited period of time to allow users to migrate away to the preferred alternative. For most deprecations then, you will want to know:
  * What is deprecated
  * When the deprecation occurred
  * What the replacement feature is
  * When the deprecated feature will be discontinued altogether

* **Discontinued**<br>A feature which is `discontinued` no longer exists, it is no longer supported, it is withdrawn, gone, kaput, dead; we might also use `stopped` to mean the same thing.

* **Breaking changes**<br>`Breaking changes` are changes that could potentially impact your current implementation, assuming you use the changed feature.

* **Non-breaking changes**<br>`Non-breaking changes` are changes that should _not_ impact your current implementation, regardless of what features you use.

* **Stoppage notice period**<br>The `stoppage notice period` is the notice period between a feature being deprecated and it being discontinued.

## What we deprecate and why

In the context of our APIs, _feature_ could mean any of these things:

* An entire API endpoint or operation
* A part of the functionality of an API operation
* A data field or property of an API operation
* A URL or part of a URL
* A way of communicating or some other aspect, e.g. method of authentication, use of webhooks or WebSockets

As to the why, we deprecate features because we need to make breaking changes and this is a way to let you know that you should change your implementation, and to give you time to do so - see [Why we have this policy](#why-we-have-this-policy).

## When we deprecate

Most changes to the API do not in fact involve deprecation. For example:

* Adding a new endpoint
* Adding fields to an existing endpoint

These are non-breaking changes, in other words changes that do not require any change to legacy implementations for their continued working.
Deprecations are planned breaking changes, i.e. a statement that we intend to make a breaking change.
We plan it so that any such change does not produce unexpected behaviour \(see [As a user, what should I do?](#as-a-user-what-should-i-do)\) and we follow a clear deprecation process \(see [How we deprecate](#how-we-deprecate)\) to keep you informed and allow you to implement the necessary changes to your implementation.

## How we deprecate

This is the process or life cycle for a deprecated feature:

1. **Announcement** - We announce in the Changelog what feature is deprecated and add it to the Deprecations table; a discontinuation or stoppage date will be set.

2. **Optional push back** - (Optional) The discontinuation or stoppage date may be pushed back, according to circumstances; it will never be brought forward.

3. **Reminder** - (Optional) We may remind users of pending stoppages prior to the stoppage occurring, typically we expect this to be about a month before, but we reserve the right to adjust that based on what produces the best outcome, or to vary it in specific circumstances.

4. **Stoppage** - We permanently stop support for the feature.

What we won't do:

* We won't just discontinue any feature of the API without first going through a deprecation process.
* We won't bring forward the discontinuation or stoppage date.
* We won't plan a change that could cause unexpected behaviour if a user continues to try and use a discontinued feature.

## How long is the stoppage notice period?

The stoppage notice period is the notice period between a feature being deprecated and it being discontinued.
We reserve the right to change the duration of this period in order to optimise the process, but as it stands today our guideline is:

* ONE YEAR for a major change
* SIX MONTHS for a minor change

## How deprecations are communicated

The documentation for each individual API should include a Deprecations page which summarises all deprecations in the API. It provides the necessary information in these table columns:

* **Feature** - What is deprecated
* **Comments** - Additional information, such as the reason for the deprecation and what the replacement feature is
* **Deprecated** - The date when the deprecation occurred, i.e. was announced in the Changelog
* **Discontinued** - The date when the deprecated feature will be discontinued altogether (or _was_ discontinued if the date has passed), or '-' if no date has been set

This is in addition to the Changelog which tracks individual changes to the API, including deprecations.

The policy for documenting deprecations within the API Reference sections of the documentation currently varies between our APIs, as follows:

* **Connectivity API**<br>Deprecated features are removed entirely from the documentation; deprecated features are, however, visible in the OpenAPI definition (linked from the home page), marked as `deprecated` as per the OpenAPI specification.

* **Channel Manager API**<br>Deprecated features are shown in the documentation with strikethrough (e.g. ~~channel~~), followed by the word `Deprecated`. There is currently no Deprecations page summarising all deprecations (historically, deprecations have been very rare in this API), however we plan to add a Deprecations page for consistency across all the APIs.

* **Booking Engine API**<br>Deprecated features are shown in the documentation with strikethrough (e.g. ~~TaxValues~~), followed by the word `Deprecated`.

## As a user, what should I do?

Check the Changelog periodically, but not less often than once a month; optionally, you can set up a notification alert on the GitHub repository for our API Docs to be informed whenever there is an update to the published branch.
Where a deprecation is announced, check your implementation and, if relevant, plan a change to your implementation. This change must be completed within the deprecation period (stoppage notice period).
If you are stuck for any reason, get in touch! \(see [Questions & feedback](#questions--feedback)\).

> ### What will be the impact if I fail to change my implementation in time?
>
> If you try to use a `deprecated` feature after its discontinuation / stoppage date, then the functionality will simply not work.
> We plan that all discontinued features will not produce unexpected behaviour, but will fail in a safe manner. For example, if you call a discontinued endpoint, then you will simply get a response back to the effect that "this endpoint does not exist".
> What should never happen is that you use some feature and it works, but works differently to how it did before. Discontinued features should always fail outright.

## Deprecations & Versioning

The deprecations policy remains the same if versioning is implemented within an API. For example, if an endpoint or operation moves from v1 to v2, then v1 will be a deprecated feature and subject to the normal policy and process.

## Questions & feedback

If you have any questions that are not answered by this policy, or you think that a change is needed to this policy, you require further information, or have any other reason as an API user to communicate about this policy, please as always just get in touch through any available channels, including email to [partnersuccess@mews.com](mailto:partnersuccess@mews.com). 
