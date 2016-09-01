---
layout: page
title: Basic iOS Security 
permalink: /projects/ios-security/
---
iOS is the most secure consumer mobile operating system out of the box. However, regardless the OS, we will always be the weakest link in any security process. Here are my tips for further securing your instance of iOS. 

**Note:** This guide is currently designed for the Settings.app layout in iOS 10. However, most of what follows should be very similar to iOS 9. 

## Glossary

2FA: Two-Factor Authentication. In addition to your password, some services allow you require a time-sensitive code at login, which will be texted to you. 

## Step 1. Lock down the lock screen

The lock screen is the most important part of your security strategy on iOS. Understanding the different ways data and interactions are exposed can help you stay safe. 

### Turn on Touch ID & Passcode

Touch ID and / or a Passcode is your first line of defense with iOS. Turn them on. For your passcode, use at least the six-digit numeric code or a longer alphanumeric code. 

Require Passcode: Immediately 

Scroll down to the services that can be accessed from the lock screen. I’d recommend turning off `Reply to Message`, because this could be used to try and get information out of your loved ones. A quick “Text Mom…” and suddenly you’re divulging security question answers. 

### Disable Siri

“Call Mom” / “Text my brother” 

These are both escorts of attack that someone could use Siri for, in order to conduct some phishing. If you’ve turned off message preview on the lock screen, an attacker couldn’t see the responses, but it’s still an unnecessary risk. You only want Siri operational if you’ve authenticated into your device. 

Settings \> Siri \> Set `Access on Lock Screen` to `Off`

I should note that disabling Siri may be for he extra cautious. Disabling Siri will also render her useless from earbud microphones and while driving, unless you unlock your phone. If you want to keep Siri enabled, then you absolutely must disable Message previews, which are explained next. 

### Hide Message Previews

Go to Notifications, and then open up the settings for Messages. Scroll down to the bottom, and turn `Show Previews` to Off. This prevents anyone from reading your text messages, including those 2FA codes that your bank, email, or other service might send you. 

Additionally, hiding message previews drastically reduces the risk of someone impersonating you via Siri from the lock screen. 

### Health

Inside the Health app, there’s a section called Medical ID. This lets you set up some basic health information that can be displayed on the lock screen. The idea being that should ever be unresponsive, someone could grab your phone and get some quick information about your basic medical profile. 

It’s also a bad idea. Someone could [use your Medical ID to initiate a phishing attack](https://news.ycombinator.com/item?id=12222135). Considering the odds of you losing your iPhone are higher than actually needing Medical ID from the lock screen, let’s turn it off. 

Enter Health app, edit your Medical ID, and then turn Show When Locked to Off. 

### Review App Permissions

Settings \> Privacy

There are a multitude of things here that you should be aware of. Here are a few of the key rows:

**Location Services** — There are three levels of location permissions that an app can request: Always, While Using, or Never. For most apps, While Using should be all you need to allow. The only apps that should always be allowed to access your location, at any time they want, are those that need to send you geo-based notifications. E.g. a weather app that tells you before it's about to rain, or a fitness tracking app. 

**Photos** — Be aware that any app with Photos access have full photo access. Additionally, most, if not all, of your photos will contain metadata that reveal location, date and time of the shot. 