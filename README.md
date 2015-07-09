WordPress Development Recommendations
=====================

## Table of contents

- [Performance](#performance)
- [Security](#security)
- [Social Media Butons](#social-media-buttons)

## Performance
*Work in progress*

## Security
*Work in progress*

## Social Media Buttons
Social media buttons are blamed for their poor performance and privacy offending nature. Based on our [test of 10 popular social media buttons solutions](https://xhtmlized.com/blog/social-media-buttons-test-performance-privacy-features/) the following are recommendations what to use and what not to use in WordPress projects.

### Recommended solutions

#### 1) Custom buttons
- Excellent performance (9/10), flexibility, no privacy concerns
- Custom design can match overall UX/UI
- Create buttons, icons or links using [Social Share URLs](https://github.com/bradvin/social-share-urls)
- Query [SharedCount](http://www.sharedcount.com/) API for [number of shares](https://docs.sharedcount.com/)
- Alternatively, implement counters with [Barebones Share Buttons](https://github.com/finderau/share-buttons) or a similar library

#### 2) [Jetpack](http://jetpack.me/)
- Good performance (6.2/10), no cookies set
- Brings functionality of Wordpress.com to self-hosted websites
- The share functionality is one of [35 different features](http://jetpack.me/)
- Neccessary to connect website to wordpress.com
- 2 button styles, hidden zeroes
- Counts shares correctly
- Easy to use WP admin

#### 3) [Share by Sumome](https://sumome.com/app/share)
- Fair performance (5.9/10), 1 cookie set
- Needs sign up
- A collection of tools for growing website traffic (List Builder, Heat Maps, etc.)
- Allows separate Facebook Share and Like buttons in one set
- Optimized for mobile, hides zeroes
- Easy to use admin interface

#### 4) [Simple Share Buttons](https://wordpress.org/plugins/simple-share-buttons-adder/)
- Good performance (6.8/10), no cookies set
- Longer time loading first byte due to how the plugin is coded (no JS asynchronous loading, buttons and counts are generated in WP)
- Easy to use WP admin interface
- [Additional features](https://simplesharebuttons.com/plus/features/) in the Plus version (10 USD per site) which hides zeroes and improves performance by caching share counts

#### 5) [Flare by Filament](http://filament.io/flare)
- Good performance (6.8/10), no cookies set
- Needs sign up
- WP plugin just redirects to Flare account
- Doesn’t display on mobile at all which makes it really usable only with [Pro version](https://app.filament.io/product_licenses/4/yearly) ($89 / year)
- Slightly cumbersome setup

### Not recommended as solutions
The following solutions are not recommended due to low performance, privacy issues, inconsistent displaying or other reasons.

#### [AddThis](https://wordpress.org/plugins/addthis/)
- Good performance (6.8/10)
- 9 cookies set (7 3rd party cookies)
- Only shows aggregated count, doesn’t count shares correctly
- Easy to use WP admin
- **Not recommended due to privacy concerns**

#### [AddToAny](https://wordpress.org/plugins/add-to-any/)
- Poor performance (3.3/10)
- Buttons are not loaded asynchronously - 16 requests made and 400kB loaded on document complete
- Doesn’t hide zeroes, only displays standard Google+ button
- 3 cookies set
- Easy to use WP admin
- **Not recommended due to low performance**

#### [Shareaholic](https://wordpress.org/plugins/shareaholic/)
- Poor performance (3.5/10)
- 53 requests made on fully loaded page
- 12 3rd party cookies set
- Requests to almost 30 different domains
- **Not recommended due to low performance and privacy concerns**

#### Official Buttons
- Very poor performance (1.3/10)
- 2 cookies set
- Inconsistent look and feel
- Inflexible setup and updates
- **Not recommended due to low performance, inflexible setup and inconsistent look & feel**

#### [Sharethis](https://wordpress.org/plugins/share-this/)
- Very poor performance (1.1/10)
- 36 requests made and 469kB loaded on document complete event
- Buttons with counters not displaying correctly
- Inconvenient WP admin interface
- Sets a lot of cookies and makes requests to many 3rd party domains
- **Not recommended due to low performance and privacy concerns**

For the full test and results check out [A Big Test of Social Media Buttons – Performance, Privacy, Features](https://xhtmlized.com/blog/social-media-buttons-test-performance-privacy-features/).

For the full performance results check [performance results spreadsheet](https://docs.google.com/spreadsheets/d/1J67PBugyoD3SsJQnLJu8s7xDsaTqP8xyz0UbPFJsw48/edit#gid=0) with links to the Webpagetest tests.
