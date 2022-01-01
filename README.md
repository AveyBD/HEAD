# 🤯 HEAD

> HTML এর `<head>` এলিমেন্টসের একটি সাধারন গাইড

[![Contributors](https://img.shields.io/github/contributors/joshbuchea/head.svg?style=for-the-badge)](https://github.com/joshbuchea/HEAD/graphs/contributors)
[![CC0](https://img.shields.io/badge/license-CC0-green.svg?style=for-the-badge)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Follow @joshbuchea on Twitter](https://img.shields.io/badge/Follow_@joshbuchea-blue?logo=twitter&logoColor=white&style=for-the-badge)](https://twitter.com/joshbuchea)

## সুচিপত্র

- [🤯 HEAD](#-head)
  - [সুচিপত্র](#সুচিপত্র)
  - [যা লাগবেই](#যা-লাগবেই)
  - [এলিমেন্টস](#এলিমেন্টস)
  - [মেটা](#মেটা)
  - [লিংক](#লিংক)
  - [আইকন](#আইকন)
  - [সোশ্যাল](#সোশ্যাল)
    - [ফেসবুক ওপেন গ্রাথ](#ফেসবুক-ওপেন-গ্রাথ)
    - [টুইটার কার্ড](#টুইটার-কার্ড)
    - [টুইটার প্রাইভেসি](#টুইটার-প্রাইভেসি)
    - [Schema.org](#schemaorg)
    - [পিন্টারেস্ট](#পিন্টারেস্ট)
    - [ফেসবুক ইনস্ট্যান্ট আর্টিকেল](#ফেসবুক-ইনস্ট্যান্ট-আর্টিকেল)
    - [ওএমডেড](#ওএমডেড)
    - [QQ/Wechat](#qqwechat)
  - [ব্রাউজার্স / প্লাটফর্ম](#ব্রাউজার্স--প্লাটফর্ম)
    - [এপল আইওস](#এপল-আইওস)
    - [গুগল এন্ড্রয়েড](#গুগল-এন্ড্রয়েড)
    - [গুগল ক্রোম](#গুগল-ক্রোম)
    - [মাইক্রোসফট ইন্টারনেট এক্সপ্লোরার](#মাইক্রোসফট-ইন্টারনেট-এক্সপ্লোরার)
  - [ব্রাউজার (চাইনিজ)](#ব্রাউজার-চাইনিজ)
    - [360 ব্রাউজার](#360-ব্রাউজার)
    - [QQ মোবাইল ব্রাউজার](#qq-মোবাইল-ব্রাউজার)
    - [UC মোবাইল ব্রাউজার](#uc-মোবাইল-ব্রাউজার)
  - [এ্যাপ লিংক](#এ্যাপ-লিংক)
  - [আরো তথ্য](#আরো-তথ্য)
  - [একই ধরনের প্রজেক্ট](#একই-ধরনের-প্রজেক্ট)
  - [পিডিঐফ আকারে নামান](#পিডিঐফ-আকারে-নামান)
  - [🌐 অনুবাূ](#-অনুবাূ)
  - [🤝 Contributing](#-contributing)
    - [Guide](#guide)
      - [1. `master`](#1-master)
      - [2. `gh-pages`](#2-gh-pages)
  - [🌟 Contributors](#-contributors)
  - [👤 Author](#-author)
  - [💛 Support](#-support)
  - [📝 License](#-license)

## যা লাগবেই

নিচের ট্যাগগুলো একটি HTML পেজের জন্য অনেক গুরুত্বপুর্ণ, যা লাগবেই।: 

```html
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--
  উপরের দুইটি মেটা ট্যাগ <head> এর সবার  উপরে থাকা উচিৎ 
  যেন প্রতিটি HTML ফাইল ঠিমভাবে রেন্ডার হয়। বাকি যেকোন হেড 
  এলিমেন্ট এই দুইটি ট্যাগের পরে আসবে।
 -->
<title>পাতার টাইটেল</title>
```

`meta charset` - ওয়েবসাইটের এনকোডিং কি সেটা বলে দেয়, সাধারনত `utf-8` ব্যবহার করা হয়। 

`meta name="viewport"` - মোবাইল ট্যাব ইত্যাদি ভিন্ন ভিন্ন ডিসপ্লে সাইজের জন্য সেটিংস যেন সকল সাইজের স্ক্রিনে ঠিকভাবে দেখা যায়।

`width=device-width` - ডিসপ্লের ফিজিক্যাল প্রশস্তা অনুসারে কনেন্ট ডিজাইনের জন্য ( মোবাইল ডিভাইসগুলোর জন্য ভাল) ।

`initial-scale=1` - সাইটলোড হবার পর প্রথম কেমন জুম থামবে সেটা। ১ থাকা মানে কোন জুম হবেনা।

**[⬆ সুচিপত্রে যান](#সুচিপত্র)**

## এলিমেন্টস

`<head>` এর এলিমেন্টসগুলো হল `meta`, `link`, `title`, `style`, `script`, `noscript`, ও `base` । 

এই এলিমেন্টস গুলো একটি HTML পেজকে কিভাবে রিসিভ করে কিভাবে দেখানো উচিৎ সেই সম্পর্কে ব্রাউজার, সার্র্চ ইঞ্জিণ, বটস  ইত্যাদিকে তথ্য প্রদান করে।

```html
<!--
  নিচের ট্যাগটি ব্রাাউজারকে HTML ডকুমেন্টটির ক্যারেকটার সেট কে UTF-8 হিসাবে চিন্হিত করতে বলে 
  যেন ইমোজি সহ বাকি সব ক্যরেক্টার ঠিকভাবে দেখা যায়।
  আরো জানতে এখানে দেখুন। https://en.wikipedia.org/wiki/Character_encodings_in_HTML
-->
<meta charset="utf-8">

<!-- পেজের টাইটেল সেট করতে -->
<title>Page Title</title>

<!-- এই ডকুমেন্টের যত লিংক আছে তার একটি বেজ লিংক -->
<base href="https://example.com/page.html">

<!-- পেজের সাথে এক্সটার্নাল CSS এর সম্পর্ক স্থাপন করে -->
<link rel="stylesheet" href="styles.css">

<!-- পেজের মধ্যে CSS ডিজাইন এড করার জন্য -->
<style>
  /* ... */
</style>

<!-- পেজে এক্সটার্নাল জাভাস্ক্রিপ্ট ফাইল করতে -->
<script src="script.js"></script>

<!-- পেজে জাভাস্ক্রিপ্ট করতে -->
<script>
  // function(s) go here
</script>

<!-- ব্রাউজার জাভাস্ক্রিপ্ট সাপোর্ট না করলে কি দেখাবে সেটা লেখার জন্য -->
<noscript>
  <!-- No JS alternative -->
</noscript>
```

**[⬆ সুচিপত্র](#সুচিপত্র)**

## মেটা

```html
<!--
  উপরের দুইটি মেটা ট্যাগ <head> এর সবার  উপরে থাকা উচিৎ 
  যেন প্রতিটি HTML ফাইল ঠিমভাবে রেন্ডার হয়। বাকি যেকোন হেড 
  এলিমেন্ট এই দুইটি ট্যাগের পরে আসবে।
-->
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<!--
  পেজের রিসোর্সগুলো কোথা থেকে কন্ট্রোল হবে তা নিয়ন্ত্রণ করার কাজ করে্।
  পেজের <head> এর যত উপরে সম্ভব দেয়া উচিৎ।
-->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- ওয়েব এ্যাপ্লিকেপশেনর নাম (তখনই ব্যবহার করা উচিৎ যখন Application হিসাবে ইউজ করা হয়) -->
<meta name="application-name" content="Application Name">

<!-- ক্রোম, ফায়ারফক্স ও ওপেরা মিনির জন্য থিম কালার -->
<meta name="theme-color" content="#4285f4">

<!-- ১৫০ শব্দের মধ্যে পেজের ছোট একটি ডেসক্রিপশন -->
<!-- এটা সার্চ ইঞ্জিনের মেটা হিসাবেও ব্যবহার হতে পারে -->
<meta name="description" content="A description of the page">

<!-- সার্চ ইঞ্জিন পেজ ক্রাউল করবে কিনা এবং তা সার্চ রেজাল্টে দেখাবে কিনা তা নিয়ন্ত্রণ করে -->
<meta name="robots" content="index,follow"><!-- সকল সার্চ ইঞ্জিনের জন্য -->
<meta name="googlebot" content="index,follow"><!-- শুধুমাত্র গুগলের জন্য -->

<!-- গুগলকে বলে যে সাইটের লিংক সার্চ রেজাল্টে দেখাবে কিনা -->
<meta name="google" content="nositelinkssearchbox">

<!-- গুগলকে সাইট ট্রান্সলেট করতে মানা করে -->
<meta name="google" content="notranslate">

<!-- ওয়েবসাইটের মালিকানা ভেরিফিকেশনের জন্য -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
<meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
<meta name="alexaVerifyID" content="verification_token"><!-- Alexa Console -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Pinterest Console-->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- কি দিয়ে পেজটি বানানো হয়েছে তা বুঝানোর জন্য -->
<meta name="generator" content="program">

<!-- পাতাটি কি বিষয়ে তা বুঝানোর জন্য -->
<meta name="subject" content="your document's subject">

<!-- পাতাটি যে সম্পর্কে তার একটি সাধারন রেটিং -->
<meta name="rating" content="General">

<!-- রেফার কেমন হবে সেই সম্পর্কে-->
<meta name="referrer" content="no-referrer">

<!-- ডকুমেন্টে থাকা নাম্বারকে অটো ডিটেকশন করতে মানা করা -->
<meta name="format-detection" content="telephone=no">

<!-- DNS Prefetch কে সম্পুর্নরুপে বন্ধ করার জন্য -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- ফ্রেমে কেমন হবে সেটা -->
<meta http-equiv="Window-Target" content="_value">

<!-- জিও লোকাল ট্যাগ -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- দেশের কোড (ISO 3166-1): লাগবেই, এলাকার কোড (ISO 3166-2): ইচ্ছাকৃত; যেমন. content="BD" / content="BD-DHK" -->
<meta name="geo.placename" content="city/town"><!-- যেমন. content="Dhaka" -->

<!-- ওয়েব মনোটোনাইজেশন https://webmonetization.org/docs/getting-started -->
<meta name="monetization" content="$paymentpointer.example">
```

- 📖 [গুগল যেসব মেটা ট্যাগ বুঝে](https://support.google.com/webmasters/answer/79812?hl=en)
- 📖 [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- 📖 [ICBM on Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- 📖 [উইকিপেডিতায়ে Geotagging](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

**[⬆ back to top](#সুচিপত্র)**

## লিংক

```html
<!-- এক্সটার্নাল CSS স্টাইলশিট লিংক করার জন্য -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- ডুপ্লিকেট কনটেন্ট রোধ করার জন্য -->
<link rel="canonical" href="https://example.com/article/?page=2">

<!-- বর্তমান ভার্শনের AMP ভার্শনের লিংক বুঝানোর জন্য -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- যদি ওয়েব এপ্লিকেশন হিসাবে ইউঝ করা হয় তবে তার জন্য  ইন্সটালেশন ফাইল -->
<link rel="manifest" href="manifest.json">

<!-- ডকুমেন্টের লেখক সম্পর্কে তথ্য -->
<link rel="author" href="humans.txt">

<!-- ডকুমেন্টের কপিরাইট সম্পর্কিত তথ্যের জন্য -->
<link rel="license" href="copyright.html">

<!-- ডকুমেন্টের অন্য ভাষার একটি ডকুমেন্টের সাথে লিংক দেখানোর জন্য -->
<link rel="alternate" href="https://bn.example.com/" hreflang="bn">

<!-- লেখক সম্পর্কে আরো তথ্য দেয়ার জন্য -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- আর্কাইভ সম্পর্কে তথ্য দিতে -->
<link rel="archives" href="https://example.com/archives/">

<!-- এই ডকুমেন্টের উচ্চতর লেভেলের কোন লিংক দেয়ার জন্য -->
<link rel="index" href="https://example.com/article/">

<!-- সেল্ফ রেফারেন্সের জন্য -->
<link rel="self" type="application/atom+xml" href="https://example.com/atom.xml">

<!-- ঐকই কমেন্টের প্রথম শেষ আগের ও পরের আর্টিকেলের লিংক দেয়ার জন্য -->
<link rel="first" href="https://example.com/article/">
<link rel="last" href="https://example.com/article/?page=42">
<link rel="prev" href="https://example.com/article/?page=1">
<link rel="next" href="https://example.com/article/?page=3">

<!-- Used when a 3rd party service is utilized to maintain a blog -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!--যখন আপনার ওয়ার্ডপ্রেস পোস্ট লিংক অন্য কোন ওয়ার্ডপ্রেসে ইউজ করা হয় তখন তার লিংক পিং করার জন্য -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- আপনি যখন আপনার ডকুমেন্টে এটি যুক্ত করেন তখন যেখানে পিং করবে  -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Enables posting to your own domain using a Micropub client -->
<link rel="micropub" href="https://example.com/micropub">

<!-- ওপেন সার্চ -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- ফিড -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- প্রিফেচিং, প্রিলোডিং, প্রিব্রাউজিং -->
<!-- আরো জানতে: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
```

- 📖 [লিংক রিলেশন](https://www.iana.org/assignments/link-relations/link-relations.xhtml)

**[⬆ সুচিপত্র](#সুচিপত্র)**

## আইকন

```html
<!-- Internet Explorer ১০ বা  এর নিচের জন্য -->
<!-- আপনার সাইটের মুল ফোল্ডারে favicon.ico রাখলেই হবে -->

<!-- আইকনের সর্বোচ্চ রেজুলেশন -->
<link rel="icon" sizes="192x192" href="/path/to/icon.png">

<!-- এপল টাচ আইকন (reuse 192px icon.png) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- সাফারি পিন ট্যাব আইকন -->
<link rel="mask-icon" href="/path/to/icon.svg" color="blue">
```

- 📖 [ফেবিকন সম্পর্কে (সাথে টাচ আইকনও)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [কিভাবে পিন ট্যাব আইকন বানাবেন](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html)
- 📖 [ফ্যাবআইকন চিটশিট](https://github.com/audreyr/favicon-cheat-sheet)
- 📖 [আইকন ও ব্রাউজার কালার সম্পর্কে](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/)

**[⬆ উপরে যান](#সুচিপত্র)**

## সোশ্যাল

### ফেসবুক ওপেন গ্রাথ
> বেশিরভাগ আর্টিকেলই ফেসবুকে শেয়ার হয়, তাই ফেসবুক অপেন গ্রাফকে এমনভাবে আপনার পেজের হেডে ভালভাবে প্রতিস্থাপন করা উচিৎ [More about Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup) 

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:image:alt" content="A description of what is in the image (not a caption)">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

- 📖 [ওপেন গ্রাফ প্রটোকল(http://ogp.me/)
- 🛠 আপনার ডকুমেন্টকে টেস্ট করুন[Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

### টুইটার কার্ড
> টুইটার কার্ড দিয়ে আপনার লিংকের টুইটার শেয়ারের মান উন্নত করতে পারেন। [More about Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
<meta name="twitter:image:alt" content="A text description of the image conveying the essential nature of an image to users who are visually impaired. Maximum 420 characters.">
```

- 📖 [Getting started with cards — Twitter Developers](https://dev.twitter.com/cards/getting-started)
- 🛠 আপনার পেজকে টেস্ট করুন [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### টুইটার প্রাইভেসি
আপনি যদি আপনার সাইটে টুইট ইউজ করেন তাহলে সেখানে টুইটার তার প্রাইভেসি পলিসি এপ্লাই করতে পারে [More about Twitter privacy options](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- আপনার সাইটের তথ্য টুইটারকে ব্যবহার করতে মানা করুন -->
<meta name="twitter:dnt" content="on">
```

### Schema.org

```html
<html lang="" itemscope itemtype="https://schema.org/Article">
    <head>
      <link rel="author" href="">
      <link rel="publisher" href="">
      <meta itemprop="name" content="Content Title">
      <meta itemprop="description" content="Content description less than 200 characters">
      <meta itemprop="image" content="https://example.com/image.jpg">
```

**Note:** এই ট্যাগগুলোর জন্য `itemscope` ও `itemtype` কে `<html>` ট্যাগে য়ুক্ত করতে হবে‌।

- 📖 [Getting Started - schema.org](https://schema.org/docs/gs.html)
- 🛠 আপনার পেজকে টেস্ট করুন [Rich Results Test](https://search.google.com/test/rich-results)

### পিন্টারেস্ট

এই ট্যাগের মাধ্যমে আপনি আপনার সাইটকে পিন্টারেস্টে পিন হওয়া থেকে আটকাতে পারবেন, তাদর[হেল্প সেন্টার অনুসারে](https://help.pinterest.com/en/business/article/prevent-saves-to-pinterest-from-your-site) `description` না দিলেও চলবে।

```html
<meta name="pinterest" content="nopin" description="Sorry, you can't save from my website!">
```

### ফেসবুক ইনস্ট্যান্ট আর্টিকেল

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- আপনার আর্টিকেলের মুল লিংক -->
<link rel="canonical" href="https://example.com/article.html">

<!-- ফেসবুক আর্টিকেলে যে স্টাইল এপ্লাই হবে -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [আরো জানুন- Instant Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Code Samples - Instant Articles](https://developers.facebook.com/docs/instant-articles/reference)

### ওএমডেড

```html
<link rel="alternate" type="application/json+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- 📖 [oEmbed format](https://oembed.com/)

### QQ/Wechat

আপনার লিংক QQ বা WeChat এ শেয়ার করলে তা ফরমেটেটড মেসেজ হিসাবে দেখাবে

```html
<meta itemprop="name" content="share title">
<meta itemprop="image" content="http://imgcache.qq.com/qqshow/ac/v4/global/logo.png">
<meta name="description" itemprop="description" content="share content">
```
- 📖 [Code Format Docs](http://open.mobile.qq.com/api/mqq/index#api:setShareInfo)

**[⬆ back to top](#সুচিপত্র)**

## ব্রাউজার্স / প্লাটফর্ম

### এপল আইওস

```html
<!-- স্মার্ট এ্যাপ ব্যানার -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- ডকুমেন্টে থাকা নাম্বারকে অটো ডিটেকশন করতে মানা করা -->
<meta name="format-detection" content="telephone=no">

<!-- লাঞ্চ আইকন (180x180px বা এর বেশি) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- শুরুর স্ক্রিনের ছবি -->
<link rel="apple-touch-startup-image" href="/path/to/launch.png">

<!-- লাঞ্চ আইকনের টাইটেেল-->
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- ফুল স্ক্রিন মুড চালু করতে -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- স্ট্যাটাসবার দেখাবে কিনা -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- iOS এ্যাপ ডিপ লিংক -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

### গুগল এন্ড্রয়েড

```html
<meta name="theme-color" content="#E64545">

<!-- হোম স্ক্রিনে যুক্ত করার অপশন দেখাতে -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android এ্যাপ ডিপ লিংক -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### গুগল ক্রোম

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- ট্রান্সলেশন বন্ধ করতে -->
<meta name="google" content="notranslate">
```

### মাইক্রোসফট ইন্টারনেট এক্সপ্লোরার

```html
<!-- ইন্টারনেট এক্সপ্লোরার 8/9/10 কে তাদের লেটেস্ট ইঞ্জিন ব্যবহার করতে বলার জন্য -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- স্কাইপি টুলবার ব্যবহার করে ডকুমেন্টে থাকা নাম্বারকে অটো ডিটেকশন করতে মানা করা -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- উইন্ডোজ টাইলস -->
<meta name="msapplication-config" content="/browserconfig.xml">
```

`browserconfig.xml` এর জন্য সর্বনিন্ম XML:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <square150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <square310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

- 📖 [Browser configuration schema reference](https://msdn.microsoft.com/en-us/library/dn320426.aspx)

**[⬆ সুচিপত্র](#সুচিপত্র)**

## ব্রাউজার (চাইনিজ)

### 360 ব্রাউজার

```html
<!-- রেন্ডারিং ইনঞ্জিন কোনটার পরে কোনটা হবো -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ মোবাইল ব্রাউজার

```html
<!-- স্ক্রিনের অরিয়েন্টেশন কিভাবে দেখাবে তা লক করা -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- ডকুমেন্ট ফুল স্ক্রিনে দেখাতে -->
<meta name="x5-fullscreen" content="true">

<!-- ডকুমেন্টকে "application mode" এ দেখাবে (যেমন ফুল স্ক্রিন) -->
<meta name="x5-page-mode" content="app">
```

### UC মোবাইল ব্রাউজার

```html
<!-- স্ক্রিনের অরিয়েন্টেশন কিভাবে দেখাবে তা লক করা -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- ডকুমেন্ট ফুল স্ক্রিনে দেখাতে -->
<meta name="full-screen" content="yes">

<!-- UC ব্রাউজার text only mode এ থাকলেও ছবি দেখাবে -->
<meta name="imagemode" content="force">

<!-- ডকুমেন্টকে "application mode" এ দেখাবে (যেমন ফুল স্ক্রিন) -->
<meta name="browsermode" content="application">

<!-- ব্রাউজারের নাইট মুড বন্ধ করতে -->
<meta name="nightmode" content="disable">

<!-- ডাটা ট্রান্সফার কমাতে -->
<meta name="layoutmode" content="fitscreen">

<!-- "scaling font up when there are many words in this document" ফিচার বন্ধ করতে -->
<meta name="wap-font-scale" content="no">
```

- 📖 [UC Browser Docs](https://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆সুচিপত্র](#সুচিপত্র)**

## এ্যাপ লিংক

```html
<!-- আইফোন -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">

<!-- এন্ড্রয়েড -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">

<!-- ওয়েব ফল ব্যাক -->
<meta property="al:web:url" content="https://applinks.org/documentation">
```

- 📖 [App Links](https://developers.facebook.com/docs/applinks)

**[⬆ সুচিপত্র](#সুচিপত্র)**

## আরো তথ্য

- 📖 [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- 📖 [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

**[⬆ সুচিপত্র](#সুচিপত্র)**

## একই ধরনের প্রজেক্ট

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js

**[⬆ সুচিপত্র](#সুচিপত্র)**

## পিডিঐফ আকারে নামান

- 📄 [পিডিএফ](https://github.com/aveybd/HEAD/blob/master/README.md)

**[⬆ সুচিপত্র](#সুচিপত্র)**

## 🌐 অনুবাূ

- 🇮🇩 [Bahasa](https://github.com/rijdz/HEAD)
- 🇧🇩 [Bengali](https://github.com/AveyBD/HEAD)
- 🇧🇷 [Brazilian Portuguese](https://github.com/Webschool-io/HEAD)
- 🇨🇳 [Chinese (Simplified)](https://github.com/Amery2010/HEAD)
- 🇩🇪 [German](https://github.com/Shidigital/HEAD)
- 🇮🇹 [Italian](https://github.com/Fakkio/HEAD)
- 🇯🇵 [Japanese](https://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- 🇰🇷 [Korean](https://github.com/Lutece/HEAD)
- 🇷🇺 [Russian/Русский](https://github.com/Konfuze/HEAD)
- 🇪🇸 [Spanish](https://github.com/alvaroadlf/HEAD)
- 🇹🇷 [Turkish/Türkçe](https://github.com/mkg0/HEAD)

**[⬆ সুচিপত্র](#সুচিপত্র)**

## 🤝 Contributing

**Open an issue or a pull request to suggest changes or additions.**

### Guide

The **HEAD** repository consists of two branches:

#### 1. `master`

This branch consists of the `README.md` file that is reflected on the [htmlhead.dev](https://htmlhead.dev/) website. All changes to the content of the guide should be made in this file.

Please follow these steps for pull requests:

{:.list-style-default}
- Modify only one tag, or one related set of tags at a time
- Use double quotes on attributes
- Don't include a trailing slash in self-closing elements — the HTML5 spec says they're optional
- Consider including a link to documentation that supports your change

#### 2. `gh-pages`

This branch is responsible for the [htmlhead.dev](https://htmlhead.dev/) website. We use [Jekyll](https://jekyllrb.com/) to deploy the `README.md` markdown file to [GitHub Pages](https://pages.github.com/). All website related modifications should be made in this branch.

You may find it helpful to review the [Jekyll Docs](https://jekyllrb.com/docs/home/) and understand how Jekyll works before working in this branch.

## 🌟 Contributors

Check out all the super awesome [contributors](https://github.com/joshbuchea/HEAD/graphs/contributors) 🤩

## 👤 Author

**Josh Buchea**

- GitHub: [@joshbuchea](https://github.com/joshbuchea)
- Twitter: [@joshbuchea](https://twitter.com/joshbuchea)

## 💛 Support

If this project was helpful for you or your organization, please considering supporting my work directly:

- 💛 [Sponsor me on GitHub](https://github.com/sponsors/joshbuchea)
- ⭐️ [Star this project on GitHub](https://github.com/joshbuchea/HEAD)
- 🐙 [Follow me on GitHub](https://github.com/joshbuchea)
- 🐦 [Follow me on Twitter](https://twitter.com/joshbuchea)

Everything helps, thanks! 🙏

— Josh

## 📝 License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ back to top](#table-of-contents)**
