All Podcasts Dataset
====================

This is a free dataset of (almost) all publicly available podcasts - at least
the ones that I could find that were actually working and at least relatively
well formatted.

This dataset consists of ~135,000 podcasts. Each entry was generated
by getting the RSS or Atom feed for a podcast, crawling it and then
capturing whatever information was available. The data was captured in
August 2014.

The data is in tab-separated (.tsv) files that should be easy to import
into pretty much any system. Each file contains all the podcasts that start
with that letter. In the .tsv files, fields containing quotes in the data
are quote delimited. Empty fields are represented as "". Pretty simple stuff.

## Why?

I was doing an experimental project where I needed a database of all podcasts.
Since someone else may be looking for the same thing, I thought I'd share.

Things you could do:

* Build a podcast directory for your podcast player app
* Do some machine learning with the data
* Revel in how many RSS feed urls you now know
* (Please don't) spam all the email addresses of every podcast owner

## Restrictions and Limitations

All this data comes from RSS / Atom feeds published by the podcast authors, so
I don't own any of that content. Do whatever you want. But if you do something
cool, sent me a tweet at [@ageitgey](https://twitter.com/ageitgey) or drop me an
[email](mailto:ageitgey@gmail.com) and show me what you built.

Since this data was built for a quick hack, I make no warranty that it is
complete, accurate or anything else.  There's probably some amount of bad data.
But it worked well for my needs.

## Data elements

Each row in the .tsv represents one podcast.

Each row contains the following fields (in this order):

#### slug
A computer-generated short name or "permalink" for the feed (you can ignore
this).

#### name
The name of the podcast, as reported in the RSS feed.

#### image_url
A url to a cover image for the podcast.

#### feed_url
The url of the RSS / Atom feed itself that was crawled.

#### website_url
The homepage of the podcast, as reported in the RSS feed.

#### itunes_owner_name
The podcast owner's name, as reported via <itunes:owner> tags in the RSS feed.

#### itunes_owner_email
The podcast owner's email address, as reported via <itunes:owner> tags in the
RSS feed.

#### managing_editor_name
The managing owner of the podcast, as reported in the RSS feed (often missing).

#### managing_editor_email
The email address of the managing owner of the podcast, as reported in the RSS
feed.

#### explicit
Whether or not the feed claims to contain explicit content as reported in an
<itunes:explicit> tag.

#### description
The description of the podcast, as reported in the RSS feed.

#### itunes_summary
The iTunes-specific description of the podcast, as reported in a
<itunes:summary> tag in the feed.

## Example entry

Here's one podcast as it appears in the data set:

| slug | name | image_url | feed_url | website_url | itunes_owner_name | itunes_owner_email | managing_editor_name | managing_editor_email | explicit | description | itunes_summary |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| my-brother-my-brother-and-me | My Brother, My Brother And Me | http://assets.libsyn.com/content/7416218.jpg | http://mbmbam.libsyn.com/rss | http://www.mbmbam.com | Justin McElroy | mbmbam@gmail.com | mbmbam@gmail.com | mbmbam@gmail.com | true | Free advice, from three of the world's most qualified experts. | My Brother, My Brother and Me is an advice show for the modern age. |
