# Web Accessibility (a11y)

It is the inclusive practice of ensuring there are no barriers that prevent interaction with, or access to, websites on the World Wide Web by people with physical disabilities, situational disabilities, and social-economic restrictions on bandwidth and speed. When sites are correctly designed, developed and edited, more users have equal access to information and functionality.

## Why

* To include people with disabilities.
* To improve website usability.
* It is a law in some places **(ADA)**.

[See Dominos's case](https://www.cnbc.com/2019/10/07/dominos-supreme-court.html)

## WCAG (Web Content Accessibility Guidelines)

Guidelines to make websites more accessible. Created by W3C (Also Web standards creators) under the initiative of WAI.

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



## ARIA: dialog role

The dialog role is used to mark up an HTML based application dialog or window that separates content or UI from the rest of the web application or page. Dialogs are generally placed on top of the rest of the page content using an overlay. Dialogs can be either non-modal (it's still possible to interact with content outside of the dialog) or modal (only the content in the dialog can be interacted with).

```html
<div role="dialog" aria-labelledby="dialog1Title" aria-describedby="dialog1Desc">
  <h2 id="dialog1Title">Your personal details were successfully updated</h2>
  <p id="dialog1Desc">You can change your details at any time in the user account section.</p>
  <button>Close</button>
</div>
```
### Description

Marking up a dialog element with the dialog role helps assistive technology identify the dialog's content as being grouped and separated from the rest of the page content. However, adding role="dialog" alone is not sufficient to make a dialog accessible. Additionally, the following needs to be done:

The dialog must be properly labeled
Keyboard focus must be managed correctly 
The sections below describe how these two requirements can be met.

Labeling
Even though it is not required for the dialog itself to be able to receive focus, it still needs to be labeled. The label given to the dialog will provide contextual information for the interactive controls inside the dialog. In other words, the dialog's label acts like a grouping label for the controls inside it (similar to how a <legend> element provides a grouping label for the controls inside a <fieldset> element).

If a dialog already has a visible title bar, the text inside that bar can be used to label the dialog itself. The best way to achieve this is by using the aria-labelledby attribute to the role="dialog" element. Additionally, if the dialog contains additional descriptive text besides the dialog title, this text can be associated with the dialog using the aria-describedby attribute. This approach is shown in the code snippet below:
 
```html
<div role="dialog" aria-labelledby="dialog1Title" aria-describedby="dialog1Desc">
  <h2 id="dialog1Title">Your personal details were successfully updated</h2>
  <p id="dialog1Desc">You can change your details at any time in the user account section.</p>
  <button>Close</button>
</div>
 ```

> :warning: **Keep in mind that a dialog's title and description text do not have to be focusable in order to be perceived by screen readers operating in a non-virtual mode. The combination of the ARIA dialog role and labeling techniques should make the screen reader announce the dialog's information when focus is moved into it.**
