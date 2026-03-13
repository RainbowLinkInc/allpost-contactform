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

本プラグインは、任意のHTMLフォームで収集したデータをもとに、「確認画面」と「送信完了画面」を自動生成し、入力内容を指定のメールアドレスに送信します。
また、高頻度スパム（例：1分間に600通以上の連続送信）からメールボックスを保護する対策機能も備えています。

== Description ==
本プラグインは、任意のHTMLフォームで収集したデータをもとに、「確認画面」と「送信完了画面」を自動生成し、入力内容を指定のメールアドレスに送信します。
また、高頻度スパム（例：1分間に600通以上の連続送信）からメールボックスを保護する対策機能も備えています。

▼実物デモをご覧ください。
https://www.secure-formmail.net/?tag=all-post-contact-form%e3%81%ae%e3%83%87%e3%83%a2


【✨ 特長】
●投稿・固定ページ上に自由なHTMLフォームを作成可能
●任意のメールアドレス宛にフォーム内容を送信
●確認画面・送信完了画面の自動表示
●スパム・爆撃対策機能
●ファイル添付・マルチ言語対応（日本語・英語・中国語・アラビア語）
●ショートコード一つで複数のフォーム運用可

【フォーム構成例】
<input type="text" name="お名前">
<input type="text" name="電話番号">


【訪問者が入力した内容は以下の形式で出力されます】
お名前：　和明戸　布麗子
電話番号：　123-4567-8910


【導入方法】
(0)HTMLフォームを投稿・固定ページで作成（※FAQにフォーム作成支援サイトを紹介）
(1)本プラグインをインストール・有効化
(2)管理画面「設定 > コンタクトフォーム」から初期設定を実施
　   参考：/assets/screenshot-7.png（日本語表示にはブラウザの言語設定を日本語にしてください）
(3)ショートコード [rlallpostcontactform] を任意のページに貼り付け
　   参考：/assets/screenshot-8.png
(4)HTMLフォームの <form> タグ冒頭に以下の記述を追加：
　   <pre><code> 
　   <form action="(3)のパーマリンク" method="POST" name="rl_apcf" onsubmit="return checkForm()" enctype="multipart/form-data">
　   </code></pre>
　  参考：/assets/screenshot-9.png


【カスタマイズポイント】
✅ デザイン変更
allpost-contactform.css を編集することで、「確認画面」「送信完了画面」の見た目を調整可能。

✅ 添付ファイル対応
ファイルアップロードの input に name="attachment_file" を指定してください。
<input name="attachment_file" type="file"> 

✅ 添付ファイルの保存（v1.6.2以降）
ファイルは /wp-content/apcf_att に保存。.htaccess によるアクセス制限も付属（Apache 2.2/2.4）。他サーバーをご利用の際は適宜制限設定をお願いいたします。


【件名のカスタマイズ】
▼完全カスタム件名
<input type="hidden" name="custom_apcf_subject" value="独自の件名">

▼デフォルト件名＋サブ件名の追加
<input type="hidden" name="custom_apcf_subject_sub" value="独自の件名">

▼プルダウンなどで件名選択（v1.5.4以降）
<input type="hidden" name="custom_apcf_subject_show" value="件名">
<select name="custom_apcf_subject" id="form_subject">
	<option class="selectoption" value="通常の連絡">通常の連絡</option>
	<option class="selectoption" value="協業の打診">協業の打診</option>
	<option class="selectoption" value="営業">営業</option>
	<option class="selectoption" value="企画の売り込み">企画の売り込み</option>
	<option class="selectoption" value="ログインできない">ログインできない</option>
</select>
　   参考：/assets/screenshot-16.png


【多言語対応】
●表示言語の切り替え
設定画面の特定欄を空白にすると、ユーザーのブラウザ言語に応じて自動的に言語が切り替わります。初期対応言語：日本語、英語、中国語、アラビア語。

●初期文言の編集
以下のファイルを直接編集してください：
rl-apcf-admin.php / rl-apcf-public.php

言語別ファイル（例：rl-apcf-admin-ja.php、rl-apcf-public-ar.php 等）

●言語追加方法：GitHubにて公開
https://github.com/RainbowLinkInc/All-Post-Contact-Form---for-usage-of-multilingual--

【主なカスタマイズ用ファイル一覧】
●allpost-contactform.css：画面デザイン変更用
●allpost-contactform-str_replace.php：表示文言の置換
●言語別ファイル一式
●アップロードファイル設定：allpost-contactform-upload_mime.php
●添付ファイル保存：allpost-contactform-sub12_uploadAttachment.php


【FAQ】
▼全FAQはこちら
https://jp.Rainbow-Link.com/catalogue.htm?&item_no=RLF16ja#faq


【問い合わせ先】
▼不具合・ご質問はWordPress.orgではなく、開発元公式サイトよりご連絡ください。
https://jp.Rainbow-Link.com/catalogue.htm?&item_no=RLF16ja#inquiry


【有料アドオン紹介】
▼自動返信機能
https://jp.Rainbow-Link.com/catalogue.htm?&item_no=RL30ja&link_id=wp

▼カーボンコピー機能
https://jp.Rainbow-Link.com/catalogue.htm?&item_no=RL31ja&link_id=wp

▼受信通知機能
https://jp.Rainbow-Link.com/catalogue.htm?&item_no=RL32ja&link_id=wp

▼自動返信＋カーボンコピー
https://jp.Rainbow-Link.com/catalogue.htm?&item_no=RL33ja&link_id=wp

▼CSV出力対応
https://jp.Rainbow-Link.com/catalogue.htm?&item_no=RL34ja&link_id=wp




== Installation ==
1. WordPress管理画面「プラグイン」から本プラグインをインストール
2. 同画面で有効化
3. 「設定 > コンタクトフォーム」にて初期設定を行ってください
　　詳細は「使い方」セクションをご参照ください


== Frequently Asked Questions ==
= FAQ LIST URL =
https://jp.Rainbow-Link.com/catalogue.htm?&item_no=RLF16ja#faq


== Screenshots ==
= Release =
1. screenshot-1.png: "Settings" > "Contact Form"
2. screenshot-2.png: Pasting this plugin's ShortCode on the "Page" 
3. screenshot-3.png: Completing your html form
4. screenshot-4.png: Contact Form Window
5. screenshot-5.png: Confirmation Window 
6. screenshot-6.png: Submission Window
7. screenshot-7.png: 「設定　＞　コンタクトフォーム」
8. screenshot-8.png: 「固定ページ」のあるページにショートコードを貼り付けた場面
9. screenshot-9.png: htmlフォームを完成させた場面
10. screenshot-10.png: コンタクトフォーム画面
11. screenshot-11.png: 確認画面 
12. screenshot-12.png: 送信完了画面

= Since v1.0.4 =
13. screenshot-13.png: Added a function of receiving an attachment file to screenshot-3.png
14. screenshot-14.png: screenshot-8.pngに添付ファイル受信機能を追加したところ

= Since v1.5.4 =
15. screenshot-15.png: Added the function to add multiple subjects to one form. 
16. screenshot-16.png: 「一つのフォームに複数の件名を付けた」ところ

= Since v1.6.2 =
17. screenshot-17.png: About design of Confirmation-Window & Submission-Window | 確認画面と送信画面のデザインのこと
18. screenshot-18.png: About design of Confirmation-Window & Submission-Window | 確認画面と送信画面のデザインのこと

= Since v1.5.0 =
Added some screenshots
settings_ar.png
settings_en.png
settings_ja.png
settings_zh.png
plugins_list_ar.png
plugins_list_en.png
plugins_list_ja.png
plugins_list_zh.png


== Changelog ==
=1.8.2=
May 5, 2025: タグエラーを解消しました。

=1.8.1=
May 4, 2025: スクリプトキディ対策を強化しました。 

=1.8.0=
Apr 24, 2025: allpost-contactform.phpにStable Tagを追加しました。

=1.7.9=
Apr 24, 2025: SVNサーバーに保存されていたスクリーンショットの一部のpngにエラーがあることが分かったため、再度アップロードしました。
Apr 22, 2025: ChatGPTの支援を得て、readme.txtとreadme_ja.txtを書き換えました。
Jan 21, 2025: Header Parts (Requires at least,Requires PHP,Update URI) を追加しました。

=1.7.8=
Nov 12, 2024: zipのアップロード要件をゆるくしました。PDFをデフォルトで許可しました。

=1.7.7=
Nov 07, 2024: テキストファイルの別名保存についての処理を書き加えました。


=1.7.6=
Nov 07, 2024: allpost-contactform-upload_mime.phpを変更しました。

=1.7.5=
Nov 07, 2024: v1.7.4 が保存エラーになったため、やりなおしました。 

=1.7.4=
Oct 31, 2024: allpost-contactform.jsの利用方法を変更しました。いままでは本プラグインが自動で読み込んでおりましたが、完全にユーザー樣の裁量に置かせていただくことにいたしました。
- 「確認画面」への遷移時に、未入力の項目について、ポップアップアラートを表示することができます。
ポップアップアラートを表示するには、「assets/allpost-contactform.js」を、お使いのテーマに読み込んでください。

=1.7.3=
Oct 30, 2024: v1.7.2のバグを修正しました。

=1.7.2=
Oct 28, 2024: FAQを追加しました：　Mime Typeの管理方法

=1.7.1=
Oct 28, 2024: ショートコードページのセキュリティを強化しました。coreページを分割し、コメントを入れました。

=1.7.0=
Oct 25, 2024: ショートコードページのセキュリティを強化しました。 ( v1.6.9のバグを修正しました )

=1.6.9=
Oct 24, 2024: ショートコードページのセキュリティを強化しました。

=1.6.8=
Oct 22, 2024: .htaccessを変更しました。添付ファイルの名称を一律自動で小文字に変更する仕様に変更しました。

=1.6.7=
Oct 21, 2024: .htaccessの処理を変更しました。attディレクトリを削除しました。

=1.6.6=
Oct 19, 2024: アップロード部分の処理を変更しました。

=1.6.5=
Oct 15, 2024: 1.6.2で、v1.6.2で、「$rl_apcf_admin_sa1_eg」とすべきところを「$rl_apcf_admin_sathahteh1_eg」としていました。寝ぼけてへんな文字を打ち込んだようです。v.1.6.2をWordPress.orgのサーバーにアップロードした時点で外部サイト（ https://plugintests.com/plugins/wporg/allpost-contactform/latest ）に指摘されていましたが、きょうまで気づきませんでした。申し訳ございません。 

=1.6.4=
Oct 11, 2024: アップロード部分のバグを修正しました。「allpost-contactform-upload_mime.php」を追加しました。

=1.6.3=
Oct 11, 2024: WordPress公式チームから注意された部分を修正しました:　text-domain 
Oct 10, 2024: WordPress公式チームから注意された部分を修正しました:　tags (limited: tags to 5 & Shortened: the 'Short Description')  

=1.6.2=
Sep 21, 2024:　仕様を大きく変更いたしました:
(1)添付ファイルをサーバー内に残すかどうかを管理画面で決めることができるようにしました。
(2)確認画面と送信画面のデザインをCSSで簡単にご変更いただけるよう、初期設定のCSS(allpost-contactform.css)に記述を追加しました。
(3)uninstall.phpを変更しました。「完全なアンインストール」に変更いたしました。

=1.6.1=
Sep 10, 2024: アイコンを変更しました。

=1.6.0=
Sep 09, 2024: 差出人のバグを修正しました。エンドユーザーが管理画面で設定した内容で差出人を上書きできないバグを修正しました。

=1.5.9=
Jun 22, 2024: html出力タグのバグを修正しました。一ヶ所、apcf-content-keyとすべきところが、apcf-content-valueになっていました。 

=1.5.8=
May 10, 2024: URL用のフィルタを改造しました( WordPressの専用snitizingを利用することにしました)。 Modified: tableレイアウトからflexに変更したことに伴い、CSSを改造しました。「確認画面」で、最後に表示されていた空行を削除しました。 

=1.5.7=
May 02, 2024: URL用のフィルタを追加しました。 CSSの"apcf_disp_gototop"にもうひとつセンタリング用のタグをデフォルトで追加することにしました。

=1.5.6=
Mar 06, 2024: ２箇所の次の警告に対処しました: 'Undefined array key'. 

=1.5.5=
Nov 14, 2023: 2つの小さなバグを修正いたしました。 

=1.5.4=
Nov 14, 2023:「一つのフォームに複数の件名を付ける」機能を追加いたしました。

=1.5.3=
Nov 13, 2023:v1.5.0から、件名の変更機能が無効になっておりました。いままで一年も気付かず、申し訳ありませんでした。

=1.5.2=
Nov 4, 2022:「爆弾攻撃」を避けるためのクッキーについて、管理者が管理画面で有効にするかどうかを選択することができるようにしました。デフォルトの設定は「無効」です。本バージョンまでは「有効」をデフォルトにしておりました。

=1.5.1=
Oct 30, 2022: 本プラグインが自動でメールに挿入する項目を、デフォルトで非表示にしました。管理画面で表示/非表示を選択することができます。

=1.5.0=
Oct 18, 2022: 今までconfファイルで設定していたオプション設定を、管理画面で設定できるように変更しました。

=1.4.2=
Mar 12, 2022: PHP8に対応しました #2。

=1.4.1=
Dec 6, 2021:  </form> タグを間違って削除していたことに気づいて入れました。 PHP8に対応しました #1。

=1.4.0=
Sep 9, 2019: フォームに応じて独自の件名をつける機能を追加しました。

=1.3.7=
May 12, 2019: allpost-contactform.css の形を整形しました。

=1.3.6=
Mar 29, 2019: allpost-contactform.css を更新しました。 

=1.3.5=
Jan 7, 2019: allpost-contactform-str_replace.php を更新しました。

=1.3.4=
Jan 7, 2019: allpost-contactform-language.php を更新しました。２０１８年１２月１５日に更新していたつもりでいましたが、アップグレードできていませんでした。

=1.3.3=
Jan 3, 2019: クッキー削除処理をプラグイン内で実行する仕様に変更しました。

=1.3.2=
Jan 2, 2019: 確認画面と送信完了画面のデザインを変更しました。偶数行と奇数行にそれぞれクラスを当て、背景色をつけることができるようにしました。

=1.3.1=
Jan 1, 2019: 送信完了画面上に二重認証のチェック部分を表示しないようにしました。

=1.3.0=
Dec 31, 2018: 間違えて作成途中のファイルをアップロードしてしまったので、やり直しました。

=1.2.9=
Dec 31, 2018: 
*二重送信を防止する機能を追加しました。Jqueryで実装されているかたが多いかとは存じますが、プラグイン本体の初期設定として、クッキーで処理することにいたしました。独自設定を維持することを希望されるかたや、クッキー処理を希望されないかたは、v1.2.8をご利用ください。
*assetsフォルダに、header_apcf.phpを追加しました。

=1.2.8=
Dec 15, 2018: 初期設定の言語を追加: 中国語

=1.2.7=
Dec 5, 2018: 送信完了後、フロントページにリダイレクトする機能を付け加えました。

=1.2.6=
Nov 21, 2018: 当社カタログのURLを変更しました。

=1.2.5=
Nov 21, 2018: サニタイズエラーを発見したので修正しました。

=1.2.4=
Nov 21, 2018: リロード抑制のため、ジャバスクリプトを追加しました。

=1.2.3=
Nov 19, 2018: 「送信確認ボタン」のクラスを新設いたしました。「.btn_confirm」です。

=1.2.2=
Oct 05, 2018: ワードプレスのバージョンを、いままで間違えて一つ多くしていたことに気づきました。失礼いたしました。
Aug 21, 2018: 初期設定の言語を追加: アラビア語

=1.2.1=
Jul 23, 2018: Updated: allpost-contactform.css
初期設定でフォームテーブルの罫線（ボーダー）を消すようにする設定の追加処置

=1.2.0=
Jul 23, 2018: Updated: allpost-contactform.css
'apcf_table'クラスにしていたものを 'apcf_table'IDになおしました。
うっかりしていて失礼いたしました。 

=1.1.9=
Jul 15, 2018: Updated: allpost-contactform.css
初期設定でフォームテーブルの罫線（ボーダー）を消すようにしました。

=1.1.8=
Jun 08, 2018: for the add-on 'csv'

=1.1.7=
Feb 13, 2018 Added: 3 files below:
*allpost-contactform-str_replace.php （ 使い方：　https://jp.Rainbow-Link.com/FAQ.htm?&faq_id=247 ）
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
May 14, 2017 Fixed: SVN upload error of v1.1.1.
May 15, 2017: Update: readme.txt & readme_ja.txt of v1.1.1.

=1.1.0=
May 14, 2017 Fixed: SVN upload error of v1.0.9.

=1.0.9=
May 14, 2017 Fixed Activation Error and version code error.

=1.0.8=
May 07, 2017: Update: readme.txt & readme_ja.txt
Apr 26, 2017: Update [ATTENTION] of readme.txt （ readme_ja.txtの「ご注意ください」をアップデートしました。）
Apr 26, 2017: Fixed: Activation Error

=1.0.7=
Apr 20, 2017: Fixed: commit-error of v1.0.6

=1.0.6=
Apr20, 2017: Modified: screenshot-1.png, screenshot-7.png | Added: screenshot-13.png, screenshot-14.png |  Fixed: a bug ( deleting-error of uploaded file )

=1.0.5=
Apr 19, 2017: Update: readme.txt & readme_ja.txt: Added: about 1.0.4 |  Fixed: a bug ( displaying-error of "submit: CONFIRM" )

=1.0.4=
Apr 19, 2017: Added: a function to upload a file ( an attachment file ).
If you use this new function, please update your <form tag. 

=1.0.3=
Apr 18, 2017: Modified: readme.txt & readme_ja.txt | Added: Language-Parts on GitHub
Apr 17, 2017: Modified: readme.txt & readme_ja.txt: DEMO URL
Apr 17, 2017: readme_ja.txtに「ご注意ください」を付け加えました。
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
