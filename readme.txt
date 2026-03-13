=== All Post Contact Form ===
Contributors: rainbowlinkinc
Donate link: https://www.Rainbow-Link.com/catalogue.htm?&item_no=RLF16&link_id=wp
Tags: contact form, email form, inquiry form
Requires at least: 4.7.3
Tested up to: 6.9
Stable tag: 1.8.2
Requires PHP: 8.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

This plugin adds confirmation and completion screens to any HTML form and sends submitted data via email.


== Description ==

This plugin enhances your custom HTML forms by adding a confirmation screen (= "Confirmation Window") and a submission success screen (= "Submission Window"). It collects the submitted data, presents it to the user for verification, and upon confirmation, sends it to a specified email address. This process is fully compatible with any HTML form structure.

【✨ Key Features】
- Works with any custom HTML form on Pages or Posts
- Automatically generates a confirmation and submission screen
- Sends submitted data to any email address of your choice
- Protects your inbox from spam and rapid-fire submission attacks
- Supports file attachments and multilingual forms (Japanese, English, Arabic, Chinese)
- Use a single shortcode to manage multiple forms site-wide

▼Live Demo
https://www.secure-formmail.net/?tag=demo-of-all-post-contact-form


【How to Use】
(0) Create your HTML form using input, textarea, etc.
  (If you're unfamiliar with HTML, check our FAQ for form generator tools.)
(1) Install and activate this plugin.
(2) Go to Settings > Contact Form in your WordPress admin and complete the plugin setup.
  See: /assets/screenshot-1.png
(3) Copy and paste the shortcode [rlallpostcontactform] into your target Page or Post.
  See: /assets/screenshot-2.png
(4) At the top of your HTML form, insert the following:
<pre><code>
<form action="{Permalink from (3)}" method="POST" name="rl_apcf" onsubmit="return checkForm()" enctype="multipart/form-data">
</code></pre>
  See: /assets/screenshot-3.png


【Customization】
●Design
Customize the confirmation and submission windows via allpost-contactform.css.

●Attachments
To accept file uploads, use:
<pre><code>
<input name="attachment_file" type="file">
</code></pre>

●Attachment Storage (v1.6.2+)
Attachments are saved in /wp-content/apcf_att.
.htaccess rules included for Apache 2.2/2.4. Configure access restrictions for other servers as needed.


【Email Subject Customization】
●Full override:
<pre><code>
<input type="hidden" name="custom_apcf_subject" value="Custom Subject">
</code></pre>

●Add subtitle to default:
<pre><code>
<input type="hidden" name="custom_apcf_subject_sub" value="Your Subtitle">
</code></pre>

●Dropdown selector (v1.5.4+):
<pre><code>
<input type="hidden" name="custom_apcf_subject_show" value="Subject">
<select name="custom_apcf_subject" id="form_subject">
 <option value="General Inquiry">General Inquiry</option>
 <option value="Partnership Proposal">Partnership Proposal</option>
 <option value="Sales">Sales</option>
 <option value="Project Pitch">Project Pitch</option>
 <option value="Login Issues">Login Issues</option>
</select>
</code></pre>


【Multilingual Support】
●Language Switching
Leaving the top 5 config fields blank enables automatic language switching based on browser settings. Defaults: Japanese, English, Arabic, Chinese.

✏️ Modify Default Labels
Edit the following files directly:
- rl-apcf-admin.php / rl-apcf-public.php
- rl-apcf-admin-{lang}.php / rl-apcf-public-{lang}.php

✏️ Add New Languages
https://github.com/RainbowLinkInc/All-Post-Contact-Form---for-usage-of-multilingual--


【Customizable Files】
- allpost-contactform.css
- allpost-contactform.js
- allpost-contactform-str_replace.php
- allpost-contactform-language.php
- allpost-contactform-upload_mime.php
- allpost-contactform-sub12_uploadAttachment.php
- Language files:
 * rl-apcf-admin.php / rl-apcf-public.php
 * rl-apcf-admin-ja.php / rl-apcf-public-ja.php
 * rl-apcf-admin-ar.php / rl-apcf-public-ar.php
 * rl-apcf-admin-zh.php / rl-apcf-public-zh.php


【FAQ】
▼For a full list of FAQs, visit:
https://www.Rainbow-Link.com/catalogue.htm?&item_no=RLF16#faq


【Support】
▼Please contact the official developer site for support:
https://www.Rainbow-Link.com/catalogue.htm?&item_no=RLF16#inquiry


【Paid Add-Ons】
- Auto Responder: https://www.Rainbow-Link.com/catalogue.htm?&item_no=RL30&link_id=wp
- Carbon Copy: https://www.Rainbow-Link.com/catalogue.htm?&item_no=RL31&link_id=wp
- Submission Notifications: https://www.Rainbow-Link.com/catalogue.htm?&item_no=RL32&link_id=wp
- Auto Responder + CC: https://www.Rainbow-Link.com/catalogue.htm?&item_no=RL33&link_id=wp
- CSV Export: https://www.Rainbow-Link.com/catalogue.htm?&item_no=RL34&link_id=wp


== Installation ==
1. Upload and install the plugin via WordPress Plugin Manager.
2. Activate the plugin in your dashboard.
3. Configure it under Settings > Contact Form.



== Screenshots ==
1. Settings Contact Form
2. ShortCode on the Page
3. Completing your html form
4. Contact Form Window
5. Confirmation Window
6. Submission Window
7. 1-ja
8. 2-ja
9. 3-ja
10. 4-ja
11. 5-ja
12. 6-ja
13. Added a function of receiving an attachment file to screenshot3
14. 13-ja
15. Added the function to add multiple subjects to one form
16. 15-ja
17. About design of Confirmation&Submission-Window
18. About design of Confirmation&Submission-Window



== Frequently Asked Questions ==
= FAQ LIST URL =
https://www.Rainbow-Link.com/catalogue.htm?&item_no=RLF16#faq



== Changelog ==
=1.8.2=
May 5, 2025: Fixed: Tag Errors

=1.8.1=
May 4, 2025: Strengthened protection against script kiddies. 

=1.8.0=
Apr 24, 2025: Added: Stable Tag into allpost-contactform.php.

=1.7.9=
Apr 24, 2025: Fixed: Error of screenshots ( Re-uploaded them )
Apr 22, 2025: Rewritten in collaboration with ChatGPT: readme.txt & readme_ja.txt
Jan 21, 2025: Added: Header Parts (Requires at least,Requires PHP,Update URI)

=1.7.8=
Nov 12, 2024: Added: filter of zip: Weakened the zip upload requirements. Allowed PDF by default.

=1.7.7=
Nov 07, 2024 Added processing for saving text files under a different name.

=1.7.6=
Nov 07, 2024 Modified: allpost-contactform-upload_mime.php

=1.7.5=
Nov 07, 2024 Re-try of v1.7.4. v1.7.4 was "version-updating-error" due to my mistake.

=1.7.4=
Oct 30, 2024: Changed: usage of allpost-contactform.js. Until now, this plugin was automatically loaded it into user's theme-header, but from today, this plugin leaves it completely at the user's discretion.
- When transitioning to the "Confirmation Window", a pop-up alert can be displayed for unfilled items.
To display pop-up alerts, use "assets/allpost-contactform.js" into your theme.

=1.7.3=
Oct 30, 2024: Fixed: bug of 1.7.2

=1.7.2=
Oct 28, 2024: Added: about FAQ: How to manage Mime Type

=1.7.1=
Oct 28, 2024: Strengthened: the security of the shortcode page. Divided: the core page and added comments.

=1.7.0=
Oct 25, 2024: Strengthened: the security of the shortcode page ( Fixed: bug of v1.6.9 )

=1.6.9=
Oct 24, 2024: Strengthened: the security of the shortcode page

=1.6.8=
Oct 22, 2024: Changed: Content of .htaccess., Automatically changing the names of attached files to lowercase letters.

=1.6.7=
Oct 21, 2024: Changed: .htaccess Process

=1.6.6=
Oct 19, 2024: Changed: Uploading Process

=1.6.5=
Oct 15, 2024: In v1.6.2, instead of "$rl_apcf_admin_sa1_eg", RL wrote as "$rl_apcf_admin_sathahteh1_eg". It seems like RL was half asleep and typed some strange characters. It was pointed out by an external site ( https://plugintests.com/plugins/wporg/allpost-contactform/latest ) when RL SVNed this plugin to WordPress.org, but RL didn't notice it until today. Sorry.

=1.6.4=
Oct 11, 2024: Fixed: upload parts. Added: allpost-contactform-upload_mime.php

=1.6.3=
Oct 11, 2024: Corrected: the part that WordPress Team instructed us to correct. : text-domain
Oct 10, 2024: Corrected: the parts that WordPress Team instructed us to correct. : tags ( limited: tags to 5 & Shortened: the 'Short Description' )

=1.6.2=
Sep 21, 2024: Major changes to the specifications. There are three main changes:
(1) You can now decide whether or not to leave attachments on the server on the Admin-Window.
(2) Descriptions have been added to the default CSS settings so that you can easily change the design of the Confirmation Window and Submission Window using CSS.
(3) Changed uninstall.php. Changed to "Complete uninstall".

=1.6.1=
Sep 10, 2024: Changed: icons.

=1.6.0=
Sep 09, 2024: Fixed: bug at "sender" section. Fixed a bug that prevented end-users from overwriting the "sender" with settings configured on the Admin-Window.

=1.5.9=
Jun 22, 2024: Fixed: html-output-tag. One of the parts that should have been shown "apcf-content-key" was shown apcf-content-value.

=1.5.8=
May 10, 2024: Modified: the filter for URL ( changed to the wordpress-snitizing ). Modified: CSS ( changed from table-typle to flex-type ). Bug-Fixed: Delete the empty-column at the "Confirmation-Window".

=1.5.7=
May 02, 2024: Added: 1 filter for URL. Modified: CSS ( one more centering-tags for "apcf_disp_gototop" )

=1.5.6=
Mar 06, 2024: Fixed the 2 warnings: 'Undefined array key'.

=1.5.5=
Nov 14, 2023: 2 putit bugs fixed.

=1.5.4=
Nov 14, 2023: Added the function to add multiple subjects to one form.

=1.5.3=
Nov 13, 2023:
From v1.5.0, the function to change the subject has been disabled. We're sorry that we didn't notice this bug for a year.

=1.5.2=
Nov 4, 2022:
Admin can now select whether or not to enable cookies to prevent "bomb attacks" on the management screen. It used to be enabled by default. Disabled by default since this version.

=1.5.1=
Oct 30, 2022: The items automatically inserted by this plugin in the mail are hidden by default. You can select to show/hide on the management screen.

=1.5.0=
Oct 18, 2022: The option settings that have been set in the conf file have been changed so that they can be set on the management screen.

=1.4.2=
Mar 12, 2022: Fixed: Upgrade for PHP8 #2.

=1.4.1=
Dec 6, 2021: Fixed: </form> tag missing. Upgrade for PHP8 #1.

=1.4.0=
Sep 9, 2019: Added: a new function: Creating your own Subjects

=1.3.7=
May 12, 2019: Update (tidied up the shape): allpost-contactform.css

=1.3.6=
Mar 29, 2019: Upgrade: allpost-contactform.css

=1.3.5=
Jan 7, 2019: Upgrade: allpost-contactform-str_replace.php.

=1.3.4=
Jan 7, 2019: Upgrade: allpost-contactform-language.php. We had intended to upgrade it on Dec 15, 2018, but, we found we couldn't have upgraded it today.

=1.3.3=
Jan 3, 2019: Changed: the cookie removal process to run in the plug-in.

=1.3.2=
Jan 2, 2019: Changed: default design of the Confirmation Window and the Submission Window. We've made it possible to put a class and a background color on the even and odd rows of the table.

=1.3.1=
Jan 1, 2019: Stopped: displaying the check part to 'prevent double submission' on the Submission Window.

=1.3.0=
Dec 31, 2018: Because we had uploaded a file in the middle of making by mistake, we uploaded this version.

=1.2.9=
Dec 31, 2018:
* Added: the function to prevent double submission. We think a lot of people would have implemented this function by using jquery. But we decided to process it with a cookie as the initial setting of this plug-in.
If you'd like to maintain your own settings, or if you do not wish to process cookies, please use v1.2.8.
* Added: assets/header_apcf.php.

=1.2.8=
Dec 15, 2018: Added a default language: Chinese

=1.2.7=
Dec 5, 2018: Added: the function to redirect to the front page after completion of submission.

=1.2.6=
Nov 21, 2018: Changed: URL of our Catalogue

=1.2.5=
Nov 21, 2018: Fixed: Sanitizing Error

=1.2.4=
Nov 21, 2018: Added: javascript in order to control reloading

=1.2.3=
Nov 19, 2018: We added a new class of the submit-button for the "Confirmation Window". The name of class = "btn_confirm".

=1.2.2=
Oct 05, 2018: We noticed today that we had mistaken the version of Wordpress. Sorry.
Aug 21, 2018: Added a default language: Arabic

=1.2.1=
Jul 23, 2018: Updated: allpost-contactform.css
added tag: To delete borders of the form-table by the initial setting

=1.2.0=
Jul 23, 2018: Updated: allpost-contactform.css
the class of 'apcf_table' to id of 'apcf_table'
sorry!

=1.1.9=
Jul 15, 2018: Updated: allpost-contactform.css
Deleting borders of the form-table by the initial setting

=1.1.8=
Jun 08, 2018: for the add-on 'csv'

=1.1.7=
Feb 13, 2018 Added: 3 files below:
* allpost-contactform-str_replace.php ( How to Use: https://www.Rainbow-Link.com/FAQ.htm?&faq_id=246 )
*/assets/apcf_template.php
*/assets/apcf_template_ja.php

=1.1.6=
Sep 23, 2017 Fixed: 1.1.5 Update Error

=1.1.5=
Sep 23, 2017 Added: 4 new functions: for Add-Ons. We are going to sell 4 add-ons for this plugin soon.

=1.1.4=
Sep 11, 2017 Fixed a bug: html5 validation error of the Confirmation Window.

=1.1.3=
May 17, 2017 Fixed a bug: on v 1.1.2, by mistake, we deleted creating-a-new-line-function of emailing. we revived it on this version.

=1.1.2=
May 15, 2017 Fixed: SVN upload error of v1.1.1.

=1.1.1=
May 14, 2017: Fixed: SVN upload error of v1.1.1.
May 15, 2017: Update: readme.txt & readme_ja.txt of v1.1.1.

=1.1.0=
May 14, 2017: Fixed: SVN upload error of v1.0.9.

=1.0.9=
May 14, 2017: Fixed Activation Error and version code error.

=1.0.8=
May 07, 2017: Update: readme.txt & readme_ja.txt
Apr 26, 2017: Update [ATTENTION] of readme.txt
Apr 26, 2017: Fixed: Activation Error

=1.0.7=
Apr 20, 2017: Fixed: commit-error of v1.0.6

=1.0.6=
Apr 20, 2017: Modified: screenshot-1.png, screenshot-7.png | Added: screenshot-13.png, screenshot-14.png | Fixed: a bug ( deleting-error of uploaded file )

=1.0.5=
Apr 19, 2017: Update: readme.txt & readme_ja.txt: Added: about 1.0.4 | Fixed: a bug ( displaying-error of "submit: CONFIRM" )

=1.0.4=
Apr 19, 2017: Added: a function to upload a file ( an attachment file ).
If you use this new function, please update your <form tag.

=1.0.3=
Apr 18, 2017: Modified: readme.txt & readme_ja.txt | Added: Language-Parts on GitHub
Apr 17, 2017: Modified: readme.txt & readme_ja.txt: DEMO URL
Apr 17, 2017: Update: readme.txt & readme_ja.txt: Added: ATTENTION
Apr 17, 2017: Fixed: a bug. now all ok!

=1.0.2=
Apr 17, 2017: Fixed: a bug

=1.0.1=
Apr 17, 2017: Update: readme.txt & readme_ja.txt: Added: LIVE DEMO URL
Apr 17, 2017: Update: readme.txt & readme_ja.txt: How To Activate

=1.0.0=
Apr 16, 2017: Update: readme.txt, Fixed: some bugs
Apr 15, 2017: Release


== Upgrade Notice ==

=1.0.3=
Apr 17, 2017: Fixed: a bug. now all ok!

=1.0.2=
Apr 17, 2017: Fixed: a bug

=1.0.0=
Release
