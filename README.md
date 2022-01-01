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
  - [Icons](#icons)
  - [Social](#social)
    - [Facebook Open Graph](#facebook-open-graph)
    - [Twitter Card](#twitter-card)
    - [Twitter Privacy](#twitter-privacy)
    - [Schema.org](#schemaorg)
    - [Pinterest](#pinterest)
    - [Facebook Instant Articles](#facebook-instant-articles)
    - [OEmbed](#oembed)
    - [QQ/Wechat](#qqwechat)
  - [Browsers / Platforms](#browsers--platforms)
    - [Apple iOS](#apple-ios)
    - [Google Android](#google-android)
    - [Google Chrome](#google-chrome)
    - [Microsoft Internet Explorer](#microsoft-internet-explorer)
  - [Browsers (Chinese)](#browsers-chinese)
    - [360 Browser](#360-browser)
    - [QQ Mobile Browser](#qq-mobile-browser)
    - [UC Mobile Browser](#uc-mobile-browser)
  - [App Links](#app-links)
  - [Other Resources](#other-resources)
  - [Related Projects](#related-projects)
  - [Other Formats](#other-formats)
  - [🌐 Translations](#-translations)
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

**[⬆ back to top](#table-of-contents)**

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

**[⬆ back to top](#table-of-contents)**

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

<!-- Provides information about an author or another person -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Links to a document that describes a collection of records, documents, or other materials of historical interest -->
<link rel="archives" href="https://example.com/archives/">

<!-- Links to top level resource in an hierarchical structure -->
<link rel="index" href="https://example.com/article/">

<!-- Provides a self reference - useful when the document has multiple possible references -->
<link rel="self" type="application/atom+xml" href="https://example.com/atom.xml">

<!-- The first, last, previous, and next documents in a series of documents, respectively -->
<link rel="first" href="https://example.com/article/">
<link rel="last" href="https://example.com/article/?page=42">
<link rel="prev" href="https://example.com/article/?page=1">
<link rel="next" href="https://example.com/article/?page=3">

<!-- Used when a 3rd party service is utilized to maintain a blog -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Forms an automated comment when another WordPress blog links to your WordPress blog or post -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Notifies a URL when you link to it on your document -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Enables posting to your own domain using a Micropub client -->
<link rel="micropub" href="https://example.com/micropub">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, preloading, prebrowsing -->
<!-- More info: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
```

- 📖 [Link Relations](https://www.iana.org/assignments/link-relations/link-relations.xhtml)

**[⬆ back to top](#table-of-contents)**

## Icons

```html
<!-- For IE 10 and below -->
<!-- Place favicon.ico in the root directory - no tag necessary -->

<!-- Icon in the highest resolution we need it for -->
<link rel="icon" sizes="192x192" href="/path/to/icon.png">

<!-- Apple Touch Icon (reuse 192px icon.png) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Safari Pinned Tab Icon -->
<link rel="mask-icon" href="/path/to/icon.svg" color="blue">
```

- 📖 [All About Favicons (And Touch Icons)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [Creating Pinned Tab Icons](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html)
- 📖 [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)
- 📖 [Icons & Browser Colors](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/)

**[⬆ back to top](#table-of-contents)**

## Social

### Facebook Open Graph
> Most content is shared to Facebook as a URL, so it's important that you mark up your website with Open Graph tags to take control over how your content appears on Facebook. [More about Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup) 

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

- 📖 [Open Graph protocol](http://ogp.me/)
- 🛠 Test your page with the [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

### Twitter Card
> With Twitter Cards, you can attach rich photos, videos and media experiences to Tweets, helping to drive traffic to your website. [More about Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)

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
- 🛠 Test your page with the [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### Twitter Privacy
If you embed tweets in your website, Twitter can use information from your site to tailor content and suggestions to Twitter users. [More about Twitter privacy options](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- disallow Twitter from using your site's info for personalization purposes -->
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

**Note:** These meta tags require the `itemscope` and `itemtype` attributes to be added to the `<html>` tag.

- 📖 [Getting Started - schema.org](https://schema.org/docs/gs.html)
- 🛠 Test your page with the [Rich Results Test](https://search.google.com/test/rich-results)

### Pinterest

Pinterest lets you prevent people from saving things from your website, according [to their help center](https://help.pinterest.com/en/business/article/prevent-saves-to-pinterest-from-your-site). The `description` is optional.

```html
<meta name="pinterest" content="nopin" description="Sorry, you can't save from my website!">
```

### Facebook Instant Articles

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- The URL of the web version of your article -->
<link rel="canonical" href="https://example.com/article.html">

<!-- The style to be used for this article -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Creating Articles - Instant Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Code Samples - Instant Articles](https://developers.facebook.com/docs/instant-articles/reference)

### OEmbed

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

Users share web pages to qq wechat will have a formatted message

```html
<meta itemprop="name" content="share title">
<meta itemprop="image" content="http://imgcache.qq.com/qqshow/ac/v4/global/logo.png">
<meta name="description" itemprop="description" content="share content">
```
- 📖 [Code Format Docs](http://open.mobile.qq.com/api/mqq/index#api:setShareInfo)

**[⬆ back to top](#table-of-contents)**

## Browsers / Platforms

### Apple iOS

```html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Disable automatic detection and formatting of possible phone numbers -->
<meta name="format-detection" content="telephone=no">

<!-- Launch Icon (180x180px or larger) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Launch Screen Image -->
<link rel="apple-touch-startup-image" href="/path/to/launch.png">

<!-- Launch Icon Title -->
<meta name="apple-mobile-web-app-title" content="App Title">

<!-- Enable standalone (full-screen) mode -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Status bar appearance (has no effect unless standalone mode is enabled) -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Configuring Web Applications](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

### Google Android

```html
<meta name="theme-color" content="#E64545">

<!-- Add to home screen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Disable translation prompt -->
<meta name="google" content="notranslate">
```

### Microsoft Internet Explorer

```html
<!-- Force IE 8/9/10 to use its latest rendering engine -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- Disable automatic detection and formatting of possible phone numbers by Skype Toolbar browser extension -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Windows Tiles -->
<meta name="msapplication-config" content="/browserconfig.xml">
```

Minimum required xml markup for `browserconfig.xml`:

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

**[⬆ back to top](#table-of-contents)**

## Browsers (Chinese)

### 360 Browser

```html
<!-- Select rendering engine order -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

```html
<!-- Locks the screen into the specified orientation -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- Display this document in fullscreen -->
<meta name="x5-fullscreen" content="true">

<!-- Document will be displayed in "application mode" (fullscreen, etc.) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

```html
<!-- Locks the screen into the specified orientation -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Display this document in fullscreen -->
<meta name="full-screen" content="yes">

<!-- UC browser will display images even if in "text mode" -->
<meta name="imagemode" content="force">

<!-- Document will be displayed in "application mode"(fullscreen, forbidding gesture, etc.) -->
<meta name="browsermode" content="application">

<!-- Disabled the UC browser's "night mode" for this document -->
<meta name="nightmode" content="disable">

<!-- Simplify the document to reduce data transfer -->
<meta name="layoutmode" content="fitscreen">

<!-- Disable the UC browser's feature of "scaling font up when there are many words in this document" -->
<meta name="wap-font-scale" content="no">
```

- 📖 [UC Browser Docs](https://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ back to top](#table-of-contents)**

## App Links

```html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">

<!-- Web fall back -->
<meta property="al:web:url" content="https://applinks.org/documentation">
```

- 📖 [App Links](https://developers.facebook.com/docs/applinks)

**[⬆ back to top](#table-of-contents)**

## Other Resources

- 📖 [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- 📖 [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

**[⬆ back to top](#table-of-contents)**

## Related Projects

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js

**[⬆ back to top](#table-of-contents)**

## Other Formats

- 📄 [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

**[⬆ back to top](#table-of-contents)**

## 🌐 Translations

- 🇮🇩 [Bahasa](https://github.com/rijdz/HEAD)
- 🇧🇷 [Brazilian Portuguese](https://github.com/Webschool-io/HEAD)
- 🇨🇳 [Chinese (Simplified)](https://github.com/Amery2010/HEAD)
- 🇩🇪 [German](https://github.com/Shidigital/HEAD)
- 🇮🇹 [Italian](https://github.com/Fakkio/HEAD)
- 🇯🇵 [Japanese](https://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- 🇰🇷 [Korean](https://github.com/Lutece/HEAD)
- 🇷🇺 [Russian/Русский](https://github.com/Konfuze/HEAD)
- 🇪🇸 [Spanish](https://github.com/alvaroadlf/HEAD)
- 🇹🇷 [Turkish/Türkçe](https://github.com/mkg0/HEAD)

**[⬆ back to top](#table-of-contents)**

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
