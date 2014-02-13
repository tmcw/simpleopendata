---
layout: default
---

# Simple Open Data

So you want to publish some open data? Cheers! - you're awesome. Here are some
helpful hints to make it simple and effective.

## Goals

Why should you publish open data?

* **Using open methods of sharing can make your organization more efficient internally.** When you pay attention to how data is published, packaged, and managed, it's easier to point other departments to good resources, and easier for them to use those resources.
* **A wider audience means having more creativity and types of talent invested in understanding your data.** The most interesting uses can be unexpected - like cross-referenced studies or visualization projects that bring public attention to the details.

## Use Open Formats

Having a wider audience means changing your expectations for how they'll use data. You use a particular operating system and software, and even have a site license for software - but others don't, and software can be prohibitively expensive. Why bother making data free if it costs thousands of dollars to open the file?

Luckily there are many simple, open formats that are supported widely, by commercial and free products and across operating systems.

### Text

**Avoid publishing text as Microsoft Word files.** There are multiple incompatible versions of the format and they are read inconsistently outside Microsoft's products.

**Publishing text as PDF is okay.** But remember that some of the purported benefits of PDF are myths: it is easily possible to edit any PDF file, so the files aren't any more tamper-proof than any other format.

If your text is minimally styled, prefer a simple format. **.txt** files are the simplest format possible, and easy to read in any system.

### Tables

**Never publish tabular data as PDF.** It's nearly impossible to read this data with a computer, and so potential users need to do a lot of manual work to parse or re-type the data.

**The most effective format for publishing table data is [CSV](http://en.wikipedia.org/wiki/Comma-separated_values)**. CSV stands for 'Comma-separated values', and is an option for Microsoft Excel's exports.

### Geographical Information

Geospatial data formats are different for vector versus raster data, and different formats are better for different sizes of data.

**For small vector data, use [GeoJSON](http://geojson.org/) or [KML](http://developers.google.com/kml/documentation/)**. These are simple, widely-adopted standards. Remember that these formats expect geographic coordinates in the [WGS84](http://en.wikipedia.org/wiki/World_Geodetic_System) datum, which is easier to use for data consumers: so reproject before publishing.

**For larger vector data, publish as Shapefiles.**

**A good, simple format for distributing raster data is [GeoTIFF](http://en.wikipedia.org/wiki/GeoTIFF).** It's an open standard with many implementations.

Certain Esri data types like FileGDB, `.lyr`, and `.zlas` are intentionally encrypted and only supported by expensive Esri products, so they aren't recommended for open data distribution. Likewise, GeoPDF is not recommended because it's rarely implemented and also has legal restrictions.

## Use Open Licenses

Specifying a license is essential for any kind of distribution: without clear legal terms, nobody can feel safe enough to use data. Which license you choose depends on a number of factors:

If the data is [a work of a US Federal government employee as part of their job, it's Public Domain](http://en.wikipedia.org/wiki/Work_of_the_United_States_Government) in the US, so there's no choice. Similarly [US laws and other edicts of government](http://en.wikipedia.org/wiki/Edict_of_government) can't be copyrighted in the US.

If your data doesn't fall into one of those conditions, you probably have copyright over it, which means that the rights you grant and those you keep are your choice.

The most liberal option if you are not a US Federal employee is to license the data under [CC0](http://creativecommons.org/publicdomain/zero/1.0/), an open license that replicates Public Domain status. This gives away most rights, like the right to demand attribution or prevent commercial usage, but it means that users are less likely to have legal doubts and more likely to use the data.

Even if you are a US federal employee, applying CC0 to your work in non-US contexts while emphasizing its public domain status in the US can eliminate confusion and maximize worldwide reuse. This is very simple to do, as seen in two examples of federal agencies doing this: [Health and Human Services](https://github.com/HHS/ckanext-datajson#credit--copying), and the [Consumer Financial Protection Bureau](https://github.com/cfpb/qu/blob/master/CONTRIBUTING.md).

If you want to require attribution, you can use the [ODC-BY](http://opendatacommons.org/licenses/by/summary/) license, which lets people use your data as long as they credit you as the original source.

There's another type of license with the property of being 'share-alike': this means that combinations of your data with other data need to be shared under the same license as your data. While this alleviates some fears of freeloading on other people's work, it makes it hard or impossible to mix your data with other data that is not published under compatible licenses. Thus it's not recommended to use share-alike licenses like [ODbL](http://opendatacommons.org/licenses/odbl/) for any new projects.

## Publishing

Once you have open data, it's time to publish!

It's best to start simple: don't build a portal or set up a server when all that you need is a simple download page. If you've just got a bit of data, try publishing & linking it in your existing CMS.

The most important element of any publishing strategy is URLs: as a basic rule, try to make data accessible by reliable, easy-to-remember URLs that don't change over time.

For many organizations, it's important that delivering open data is reliable & inexpensive. Budgeting a portal only aggravates this concern. An easy way to avoid these problems is by using an existing service like [Amazon S3](http://aws.amazon.com/s3/) that handles downloads and storage.

Do you need an API? Create one if:

* You have the staff, time, and funding to maintain the API once it has users.
* You have more data than anyone would want to download at one time, and there's some clear distinction between types that people would want to use as a filter.

Otherwise, you will want to simply publish the data as a raw download to avoid the complexity & responsibility of APIs.

## Promotion

You've published your data - congrats! You are enabling new, awesome ways to think. But how do you get people interested in it, and using it?

**Find your peers and talk.** Now that you're working in the open, you'll find that other folks are doing similar stuff - the state over from yours has the same kind of dataset. Talk to them, link to them, and figure out how you can learn from one another.

**Show how the data is awesome:** create a basic visualization or analysis that uses your data and links to your site. Mention it through your normal channels and the places where analysts hang out, like twitter & GitHub.
