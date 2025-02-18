# Tools for Data Analysis

This is a starting point for making sense of the tools used for analyzing Mozilla data. There are different tools available, each with their own strengths, tailored to a variety of use cases and skill sets.

<!-- toc -->

## High-level tools

These web-based tools do not require specialized technical knowledge (e.g. how to write an SQL query, deep knowledge of BigQuery). This is where you should start.

### Looker

In 2020, Mozilla chose [Looker](https://looker.com/) as its primary tool for analyzing data.
It allows data exploration and visualization by experts and non-experts alike.

As of this writing, [Mozilla's Looker deployment](https://mozilla.cloud.looker.com/) is an active work in progress.
You can see the current status on the [Looker Deploy Working Group](https://mana.mozilla.org/wiki/display/DATA/Looker+Deploy+Working+Group) on Mana (LDAP access required).

### Mozilla Growth & Usage Dashboard (GUD)

The [Mozilla Growth & Usage Dashboard](https://gud.telemetry.mozilla.org/) (GUD) is a tool to visualize growth metrics in a standard way across Mozilla’s products. This is the first place you should look if you have a question like "how many people are using X?".

### Glean Aggregated Metrics Dashboard (GLAM)

The [Glean Aggregated Metrics Dashboard](https://glam.telemetry.mozilla.org/) (GLAM) is an interactive dashboard that is Mozilla’s primary self-service tool for examining the distributions of values of specific individual telemetry metrics, over time and across different user populations. It is similar to GUD in that it is meant to be usable by everyone; no specific data analysis or coding skills are needed. But while GUD is focused on a relatively small number of high level, derived product metrics about user engagement (e.g. MAU, DAU, retention, etc) GLAM is focused on a diverse and plentiful set of probes and data points that engineers capture in code and transmit back from Firefox and other Mozilla products.

For more information on how to use GLAM, see [Introduction to GLAM](../cookbooks/glam.md).

## Lower-level tools

These tools require more specialized knowledge to use.

### sql.telemetry.mozilla.org (STMO)

The [`sql.telemetry.mozilla.org`](https://sql.telemetry.mozilla.org) (STMO) site
is an instance of the very fine [Redash](https://redash.io/) software, allowing
for SQL-based exploratory analysis and visualization / dashboard
construction.
Requires (surprise!) familiarity with SQL, and for your data to be explicitly exposed as an STMO data source.
You can learn more about how to use it in [Introduction to STMO](../tools/stmo.md).

Note that while STMO is not yet considered deprecated, Looker is the preferred solution for producing data visualizations and dashboards at Mozilla (where possible).

## Deprecated tools

These tools are still available, but are generally not recommended.

### Telemetry Measurement Dashboard

The [Telemetry Measurement Dashboard](https://telemetry.mozilla.org/new-pipeline/dist.html) (TMO) site is the 'venerable standby' of Firefox telemetry analysis tools.
It is the predecessor to GLAM (see above) and is still lightly maintained until we are sure that GLAM covers all of its use cases.
