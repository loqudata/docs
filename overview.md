# Overview

## Problem

Open datasets are published in different open data portals. However, it’s still too difficult to search across data portals or visualize data in the same tool.

We won’t consider commercial solutions as they are not publicly available. Other solutions like general search engines or “dataset search engines” are either too broad or have other limitations that result in poor quality results. Public datasets often refer to real-world entities or concepts, like geographic locations or types of economic activity, that already have well-defined semantic schemas. However, existing solutions are not able to analyze the semantic meaning of the fields in such datasets, which leads to a less effective search or exploration experience.

Once the user has located a few datasets of interest, they often need to download the data and load it into other tools to visualize it and make a decision on whether to use it. Some data portals have new features for visualization, but these vary based on the data portal used.

## Solution

Loqu is an open (open source, open data, and free to use) platform that aggregates dataset metadata from data portals and other statistical data providers, and allows users to search, explore, and visualize those datasets in a single tool. We hope to keep Loqu available for a while, so we only store metadata to limit costs.

The platform will allow users to:

- use powerful faceted search features on datasets (e.g. search by properties like license, date published, etc)
- explore datasets based on linked entities. For example, a user could search for a county in the US, and then view the datasets that are linked to that entity, such as data on unemployment or crime.
- create geographic or chart-based visualizations using a graphical user interface
- share and re-use visualizations for different datasets
- add metadata to datasets like links to entities, semantic annotation of table fields, or additional descriptions
- easily export to spreadsheets or other tools

## Current Status

The first version of the platform is available at [loqudata.org](https://loqudata.org/), with over 700 million data series from 81 providers. We have not yet integrated the data set of over 250 data portals. We’ve implemented the basics for the first three key features above: search, exploration, and visualization, but want to do a lot more. Some of our short-term goals are outlined in the **What's up next?** section of the [FAQ](./faq.md).

## Vision

We can imagine Loqu as a “Wikipedia for datasets,” where users contribute new data portals, enrich dataset metadata, and share visualizations, and a community of developers add new features and data pipelines. Hopefully, the platform would increase the accessibility and ease of use of public data and have positive impacts on civic engagement, advocacy, education, and journalism.
