ARIA: dialog role
The dialog role is used to mark up an HTML based application dialog or window that separates content or UI from the rest of the web application or page. Dialogs are generally placed on top of the rest of the page content using an overlay. Dialogs can be either non-modal (it's still possible to interact with content outside of the dialog) or modal (only the content in the dialog can be interacted with).

<div role="dialog" aria-labelledby="dialog1Title" aria-describedby="dialog1Desc">
  <h2 id="dialog1Title">Your personal details were successfully updated</h2>
  <p id="dialog1Desc">You can change your details at any time in the user account section.</p>
  <button>Close</button>
</div>
Copy to Clipboard
Description
Marking up a dialog element with the dialog role helps assistive technology identify the dialog's content as being grouped and separated from the rest of the page content. However, adding role="dialog" alone is not sufficient to make a dialog accessible. Additionally, the following needs to be done:

The dialog must be properly labeled
Keyboard focus must be managed correctly 
The sections below describe how these two requirements can be met.

Labeling
Even though it is not required for the dialog itself to be able to receive focus, it still needs to be labeled. The label given to the dialog will provide contextual information for the interactive controls inside the dialog. In other words, the dialog's label acts like a grouping label for the controls inside it (similar to how a <legend> element provides a grouping label for the controls inside a <fieldset> element).

If a dialog already has a visible title bar, the text inside that bar can be used to label the dialog itself. The best way to achieve this is by using the aria-labelledby attribute to the role="dialog" element. Additionally, if the dialog contains additional descriptive text besides the dialog title, this text can be associated with the dialog using the aria-describedby attribute. This approach is shown in the code snippet below:

<div role="dialog" aria-labelledby="dialog1Title" aria-describedby="dialog1Desc">
  <h2 id="dialog1Title">Your personal details were successfully updated</h2>
  <p id="dialog1Desc">You can change your details at any time in the user account section.</p>
  <button>Close</button>
</div>
Copy to Clipboard
Keep in mind that a dialog's title and description text do not have to be focusable in order to be perceived by screen readers operating in a non-virtual mode. The combination of the ARIA dialog role and labeling techniques should make the screen reader announce the dialog's information when focus is moved into it.
