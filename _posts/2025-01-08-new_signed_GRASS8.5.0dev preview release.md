---
title: "Signed GRASS 8.4.0 and GRASS 8.5.0dev preview versions now available"
layout: "single"
class: wide
excerpt_separator: "<!--more-->"
categories:
  - Announcement
tags:
  - Information
---
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-9NBX5KDKM0"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-9NBX5KDKM0');
</script>

"Official" Mac apps are "signed" and "notarized" by Apple to help users avoid problem software or malware. This requires a paid signing key, and using this key is complicated outside of Apple's XCode development environment. OSGEO has a signing key, but because GRASS is not compiled in the XCode environment, we have not been able to apply it (or at least I was unable to find a way to do so). This did not present serious problems in the past, though it sometimes made initially launching GRASS a bit of a pain.

However, with the new Mac OS 15 (Sequoia) upgrade the lack of signing the GRASS app became a more serious problem, generating a bogus error that the app is damaged for any new or upgraded installation. Fortunately, Nicklas Larsson found a workaround terminal command, which I added to the GRASS installation instructions in December 2024. Then he has worked out a way to officially sign and notarize the GRASS Mac apps so we no longer will have problems arising from an unsigned app. Regularizing this protocol is still a little ad hoc, but Nicklas is working on refactoring Mac compiling within the GRASS Github repo to make it easier for all. In the meantime, we'll work together to continue to make the most up to date versions of GRASS available for Mac users.

I've posted the new signed apps that Nicklas generated for you to enjoy. Happy GRASSing!
