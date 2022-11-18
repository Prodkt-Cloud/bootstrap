---
layout: docs
title: Event Activity
description:
group: extend
toc: true
lx-head: true
lx-sideNav: true
---
## In Review

- Designer: Bryan Funk
- Product Owner: John Meindersee

- Maximum width of devices supported by design is 320px
  You might notice with padding inside the container query for our documentation that we more or less go down to 280px. Though we will most always support our own components and designs at that width we are not bound to accdomidate that low of viewport and most notible here is we can't guarantee any brought over components from client libraries. Clients would support their own libraries at this width if they truly have a need for it.

- Design has a decision to make regarding scrollbars
  I will create a ticket to think through how scrollbars need to interact with content on tablet width and below devices. For now Design is using a stable 2-edge scrollbar gutter. Although there is clear content shifting especially with components like modals. Inside web/ios/android there are also differing behaviors (tested iOS 16/Android).

<!-- markdownlint-disable -->
{{< example >}}
{{< tovuti/global/lessonActivity-event >}}
{{< /example >}}
<!-- markdownlint-restore -->
