# Web Accessibility (a11y)

It is the inclusive practice of ensuring there are no barriers that prevent interaction with, or access to, websites on the World Wide Web by people with physical disabilities, situational disabilities, and social-economic restrictions on bandwidth and speed. When sites are correctly designed, developed and edited, more users have equal access to information and functionality.

## Why

* To include people with disabilities.
* To improve website usability.
* It is a law in some places **(ADA)**.

[See Dominos's case](https://www.cnbc.com/2019/10/07/dominos-supreme-court.html)

## ADA

The Americans with Disabilities Act was instituted in 1990 in an effort to end discrimination based on differing abilities.
This was a fairly revolutionary addition that led to the widespread adoption of wheelchair access ramps, accessible restroom facilities, and many other equal-access accommodations that have become a regular part of most American workplaces.  

The WCAG is an internationally recognized set of guidelines for digital accessibility. It was established and is managed by the international web standards group, the W3C. The de facto standard in the US - recognized (yet not set) by the DOJ (Department of Justice), the courts, and advocates is the WCAG A, AA.

[See more](https://www.accessibility.works/blog/2021-ada-wcag-website-accessibility-standards-requirements/)

## WCAG (Web Content Accessibility Guidelines)

Guidelines to make websites more accessible. Created by W3C (Also Web standards creators) under the initiative of WAI.

WCAG 2.0 and WCAG 2.1 are stable, referenceable technical standards. They have 12-13 guidelines that are organized under 4 principles: perceivable, operable, understandable, and robust. For each guideline, there are testable success criteria, which are at three levels: A, AA, and AAA.

Current version of WCAG is 2.1 released on June 5, 2018.

### Conformance levels

WCAG 2.1 guidelines are categorized into three different conformance levels (Level A, Level AA, and Level AAA) based on the impact they have on design or visual presentation of the pages in order to meet the needs of different individuals and different situations. Conformance levels must be met in full and conformance at higher levels indicates conformance at lower levels:

* **Level A** — The lowest and easiest level of conformance to obtain. Level A sets a minimum level of accessibility and does not achieve broad accessibility for many situations.
* **Level AA** — The mid-range and most common level of conformance to obtain. Level AA is the recommended conformance for all web-based information.
* **Level AAA** — The highest and hardest level of conformance to obtain. It’s not recommended to strive for full AAA compliance as it is not possible to satisfy all Level AAA Success Criteria for some content.

### Categories

* **Perceivable**: All users must be able to perceive your content. If there is audio or video content, you should provide text alternatives. If there is text content, you should provide audio alternatives or a way that assistive technology such as screen readers can consume it for the end-user.

Ask yourself: Is there anything on my site that a deaf, colorblind, low vision or blind user would not be able to perceive?

* **Operable**: All users must be able to operate your site. Most users with disabilities use a keyboard to surf the web using character key shortcuts along the way to navigate, interact with, and access content. Your site should be forgiving to your users if they make a mistake, offering ways to retract, correct, and confirm information.

Ask yourself: Can my site be navigated and operated solely through a keyboard? Do users have control of interactive elements on my site? Are tasks on my site able to be easily and successfully completed?

* **Understandable**: Just because your users can perceive and operate your site doesn’t necessarily mean that they can understand it. Interactive elements on a site including menus, icons, and links should all give an insight to their destination.

Ask yourself: Are all my site’s interactions easy to understand? Is the content on my site presented clearly and meaningfully?

* **Robust**: Users should be able to access your site from any device, platform, or browser. Adopt best development practices to support different operating systems and browsers. To guarantee a functional site for a diverse set of audiences, avoid any mishaps and ensure that your code is clean.

Ask yourself: Is our site developed with best practices in mind? Can our site or application support a variety of devices and browsers? Is the code to our site clean?

## Assistive Technology

People with certain disabilities use display and input technologies to access online resources. There are several software and hardware solutions that have been adopted, commonly referred to as assistive technologies.

* **Screen readers** – used to listen to the content of a webpage.
* **Screen magnification software** - used to enlarge screen content to make it easier to read for users with a partial sight impairment.
* **Alternative Input Devices**- an alternative to the typical mouse and keyboard interaction for users with physical or cognitive impairment (head pointers, motion tracking or eye tracking, single switch entry devices, large-print and tactile keyboards, speech input software...).

## Tools for testing web accessibility

* Lighthouse.
* Disability simulators:
  * NoCoffee
  * Web Disability Simulator.
* Manual testing (keyboard interaction).
* Screen readers.
  * NVDA - Firefox.
  * JAWS - Internet Explorer.
  * VoiceOver - Safari.
  * ChromeVox - Google Chrome.
* Accessibility tree browser.
