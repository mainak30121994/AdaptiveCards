---
title: Host config - iOS SDK
author: matthidinger
ms.author: mahiding
ms.date: 06/26/2017
ms.topic: article
---

# Host config - iOS

Host can be configured through HostConfig which can be generated by JSON string

```objective-c
ACOParseResult *hostconfigParseResult = [ACOHostConfig FromJson:self.hostconfig];
```

Default HostConfig can be instantiated

```objective-c
ACOHostConfig *defaultConfig = [[ACHostConfig alloc] init];
```

## Render a card using host config

Rederer takes adaptive card and host config. HostConfig can be nil, and if nil, default value will be used.

```objective-c
ACRRenderResult *renderResult;
renderResult = [ACRRenderer render:cardParseResult.card
                            config:hostconfigParseResult.config
                   widthConstraint:300.0];
```