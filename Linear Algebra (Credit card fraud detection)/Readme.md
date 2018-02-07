<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>EDA and Similarity of Transactions on CreditCardFraudDetection</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Kaggle-Data-Set---Credit-Card-Fraud">Kaggle Data Set - Credit Card Fraud<a class="anchor-link" href="#Kaggle-Data-Set---Credit-Card-Fraud">&#182;</a></h2><h3 id="The-datasets-contains-transactions-made-by-credit-cards-in-September-2013-by-european-cardholders.">The datasets contains transactions made by credit cards in September 2013 by european cardholders.<a class="anchor-link" href="#The-datasets-contains-transactions-made-by-credit-cards-in-September-2013-by-european-cardholders.">&#182;</a></h3><h2 id="Dataset-Information:">Dataset Information:<a class="anchor-link" href="#Dataset-Information:">&#182;</a></h2>
<pre><code>* Number of Instances: 284,807
* Number of Attributes: 31 (including the class attribute)
* Attribute Information:
* Features V1, V2, ... V28 are the principal components obtained with PCA.    
* The only features which have not been transformed with PCA are 'Time' and 'Amount'.
* Feature 'Time' contains the seconds elapsed between each transaction and the first 
  transaction in the   dataset.
</code></pre>
<h3 id="Class-(class-attribute):">Class (class attribute):<a class="anchor-link" href="#Class-(class-attribute):">&#182;</a></h3>
<pre><code>* Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 
  otherwise. 
  1 = Fraud Transaction
  0 = Normal Transaction
</code></pre>
<h3 id="All-the-remaining-details-regarding-the-data-set-can-be-found-in-the-below-link.">All the remaining details regarding the data set can be found in the below link.<a class="anchor-link" href="#All-the-remaining-details-regarding-the-data-set-can-be-found-in-the-below-link.">&#182;</a></h3><h3 id="CreditCardFraud"><a href="https://www.kaggle.com/dalpozz/creditcardfraud/data">CreditCardFraud</a><a class="anchor-link" href="#CreditCardFraud">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics.pairwise</span> <span class="k">import</span> <span class="n">cosine_similarity</span>

<span class="o">%</span><span class="k">matplotlib</span> inline
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[31]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#download the data set from  </span>
<span class="c1">#https://www.kaggle.com/dalpozz/creditcardfraud/data</span>
<span class="c1"># load the data set</span>
<span class="n">data</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s2">&quot;creditcard.csv&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[32]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[32]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(284807, 31)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[33]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[33]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Time</th>
      <th>V1</th>
      <th>V2</th>
      <th>V3</th>
      <th>V4</th>
      <th>V5</th>
      <th>V6</th>
      <th>V7</th>
      <th>V8</th>
      <th>V9</th>
      <th>...</th>
      <th>V21</th>
      <th>V22</th>
      <th>V23</th>
      <th>V24</th>
      <th>V25</th>
      <th>V26</th>
      <th>V27</th>
      <th>V28</th>
      <th>Amount</th>
      <th>Class</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.0</td>
      <td>-1.359807</td>
      <td>-0.072781</td>
      <td>2.536347</td>
      <td>1.378155</td>
      <td>-0.338321</td>
      <td>0.462388</td>
      <td>0.239599</td>
      <td>0.098698</td>
      <td>0.363787</td>
      <td>...</td>
      <td>-0.018307</td>
      <td>0.277838</td>
      <td>-0.110474</td>
      <td>0.066928</td>
      <td>0.128539</td>
      <td>-0.189115</td>
      <td>0.133558</td>
      <td>-0.021053</td>
      <td>149.62</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.0</td>
      <td>1.191857</td>
      <td>0.266151</td>
      <td>0.166480</td>
      <td>0.448154</td>
      <td>0.060018</td>
      <td>-0.082361</td>
      <td>-0.078803</td>
      <td>0.085102</td>
      <td>-0.255425</td>
      <td>...</td>
      <td>-0.225775</td>
      <td>-0.638672</td>
      <td>0.101288</td>
      <td>-0.339846</td>
      <td>0.167170</td>
      <td>0.125895</td>
      <td>-0.008983</td>
      <td>0.014724</td>
      <td>2.69</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1.0</td>
      <td>-1.358354</td>
      <td>-1.340163</td>
      <td>1.773209</td>
      <td>0.379780</td>
      <td>-0.503198</td>
      <td>1.800499</td>
      <td>0.791461</td>
      <td>0.247676</td>
      <td>-1.514654</td>
      <td>...</td>
      <td>0.247998</td>
      <td>0.771679</td>
      <td>0.909412</td>
      <td>-0.689281</td>
      <td>-0.327642</td>
      <td>-0.139097</td>
      <td>-0.055353</td>
      <td>-0.059752</td>
      <td>378.66</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1.0</td>
      <td>-0.966272</td>
      <td>-0.185226</td>
      <td>1.792993</td>
      <td>-0.863291</td>
      <td>-0.010309</td>
      <td>1.247203</td>
      <td>0.237609</td>
      <td>0.377436</td>
      <td>-1.387024</td>
      <td>...</td>
      <td>-0.108300</td>
      <td>0.005274</td>
      <td>-0.190321</td>
      <td>-1.175575</td>
      <td>0.647376</td>
      <td>-0.221929</td>
      <td>0.062723</td>
      <td>0.061458</td>
      <td>123.50</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2.0</td>
      <td>-1.158233</td>
      <td>0.877737</td>
      <td>1.548718</td>
      <td>0.403034</td>
      <td>-0.407193</td>
      <td>0.095921</td>
      <td>0.592941</td>
      <td>-0.270533</td>
      <td>0.817739</td>
      <td>...</td>
      <td>-0.009431</td>
      <td>0.798278</td>
      <td>-0.137458</td>
      <td>0.141267</td>
      <td>-0.206010</td>
      <td>0.502292</td>
      <td>0.219422</td>
      <td>0.215153</td>
      <td>69.99</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 31 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#how many transactions are fraud </span>
<span class="n">data</span><span class="p">[</span><span class="s2">&quot;Class&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[6]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0    284315
1       492
Name: Class, dtype: int64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h5 id="Class-label:"><strong>Class label</strong>:<a class="anchor-link" href="#Class-label:">&#182;</a></h5><ul>
<li>label 0 - <strong>Normal transactions</strong> count is  <strong>284315</strong>.</li>
<li>label 1 - <strong>Fraud transactions</strong> count is <strong>492</strong>.</li>
</ul>
<p>Clearly it is an <strong>imbalanced dataset</strong>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># statistics</span>
<span class="n">data</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[7]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Time</th>
      <th>V1</th>
      <th>V2</th>
      <th>V3</th>
      <th>V4</th>
      <th>V5</th>
      <th>V6</th>
      <th>V7</th>
      <th>V8</th>
      <th>V9</th>
      <th>...</th>
      <th>V21</th>
      <th>V22</th>
      <th>V23</th>
      <th>V24</th>
      <th>V25</th>
      <th>V26</th>
      <th>V27</th>
      <th>V28</th>
      <th>Amount</th>
      <th>Class</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>284807.000000</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>...</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>2.848070e+05</td>
      <td>284807.000000</td>
      <td>284807.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>94813.859575</td>
      <td>3.919560e-15</td>
      <td>5.688174e-16</td>
      <td>-8.769071e-15</td>
      <td>2.782312e-15</td>
      <td>-1.552563e-15</td>
      <td>2.010663e-15</td>
      <td>-1.694249e-15</td>
      <td>-1.927028e-16</td>
      <td>-3.137024e-15</td>
      <td>...</td>
      <td>1.537294e-16</td>
      <td>7.959909e-16</td>
      <td>5.367590e-16</td>
      <td>4.458112e-15</td>
      <td>1.453003e-15</td>
      <td>1.699104e-15</td>
      <td>-3.660161e-16</td>
      <td>-1.206049e-16</td>
      <td>88.349619</td>
      <td>0.001727</td>
    </tr>
    <tr>
      <th>std</th>
      <td>47488.145955</td>
      <td>1.958696e+00</td>
      <td>1.651309e+00</td>
      <td>1.516255e+00</td>
      <td>1.415869e+00</td>
      <td>1.380247e+00</td>
      <td>1.332271e+00</td>
      <td>1.237094e+00</td>
      <td>1.194353e+00</td>
      <td>1.098632e+00</td>
      <td>...</td>
      <td>7.345240e-01</td>
      <td>7.257016e-01</td>
      <td>6.244603e-01</td>
      <td>6.056471e-01</td>
      <td>5.212781e-01</td>
      <td>4.822270e-01</td>
      <td>4.036325e-01</td>
      <td>3.300833e-01</td>
      <td>250.120109</td>
      <td>0.041527</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
      <td>-5.640751e+01</td>
      <td>-7.271573e+01</td>
      <td>-4.832559e+01</td>
      <td>-5.683171e+00</td>
      <td>-1.137433e+02</td>
      <td>-2.616051e+01</td>
      <td>-4.355724e+01</td>
      <td>-7.321672e+01</td>
      <td>-1.343407e+01</td>
      <td>...</td>
      <td>-3.483038e+01</td>
      <td>-1.093314e+01</td>
      <td>-4.480774e+01</td>
      <td>-2.836627e+00</td>
      <td>-1.029540e+01</td>
      <td>-2.604551e+00</td>
      <td>-2.256568e+01</td>
      <td>-1.543008e+01</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>54201.500000</td>
      <td>-9.203734e-01</td>
      <td>-5.985499e-01</td>
      <td>-8.903648e-01</td>
      <td>-8.486401e-01</td>
      <td>-6.915971e-01</td>
      <td>-7.682956e-01</td>
      <td>-5.540759e-01</td>
      <td>-2.086297e-01</td>
      <td>-6.430976e-01</td>
      <td>...</td>
      <td>-2.283949e-01</td>
      <td>-5.423504e-01</td>
      <td>-1.618463e-01</td>
      <td>-3.545861e-01</td>
      <td>-3.171451e-01</td>
      <td>-3.269839e-01</td>
      <td>-7.083953e-02</td>
      <td>-5.295979e-02</td>
      <td>5.600000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>84692.000000</td>
      <td>1.810880e-02</td>
      <td>6.548556e-02</td>
      <td>1.798463e-01</td>
      <td>-1.984653e-02</td>
      <td>-5.433583e-02</td>
      <td>-2.741871e-01</td>
      <td>4.010308e-02</td>
      <td>2.235804e-02</td>
      <td>-5.142873e-02</td>
      <td>...</td>
      <td>-2.945017e-02</td>
      <td>6.781943e-03</td>
      <td>-1.119293e-02</td>
      <td>4.097606e-02</td>
      <td>1.659350e-02</td>
      <td>-5.213911e-02</td>
      <td>1.342146e-03</td>
      <td>1.124383e-02</td>
      <td>22.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>139320.500000</td>
      <td>1.315642e+00</td>
      <td>8.037239e-01</td>
      <td>1.027196e+00</td>
      <td>7.433413e-01</td>
      <td>6.119264e-01</td>
      <td>3.985649e-01</td>
      <td>5.704361e-01</td>
      <td>3.273459e-01</td>
      <td>5.971390e-01</td>
      <td>...</td>
      <td>1.863772e-01</td>
      <td>5.285536e-01</td>
      <td>1.476421e-01</td>
      <td>4.395266e-01</td>
      <td>3.507156e-01</td>
      <td>2.409522e-01</td>
      <td>9.104512e-02</td>
      <td>7.827995e-02</td>
      <td>77.165000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>172792.000000</td>
      <td>2.454930e+00</td>
      <td>2.205773e+01</td>
      <td>9.382558e+00</td>
      <td>1.687534e+01</td>
      <td>3.480167e+01</td>
      <td>7.330163e+01</td>
      <td>1.205895e+02</td>
      <td>2.000721e+01</td>
      <td>1.559499e+01</td>
      <td>...</td>
      <td>2.720284e+01</td>
      <td>1.050309e+01</td>
      <td>2.252841e+01</td>
      <td>4.584549e+00</td>
      <td>7.519589e+00</td>
      <td>3.517346e+00</td>
      <td>3.161220e+01</td>
      <td>3.384781e+01</td>
      <td>25691.160000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
<p>8 rows × 31 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># lets plot plain scatter plot considering Amount and Class</span>
<span class="n">data</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">kind</span><span class="o">=</span><span class="s1">&#39;scatter&#39;</span><span class="p">,</span> <span class="n">x</span><span class="o">=</span><span class="s1">&#39;Amount&#39;</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="s1">&#39;Class&#39;</span><span class="p">,</span><span class="n">title</span> <span class="o">=</span><span class="s1">&#39;Amount verus Transactions type&#39;</span><span class="p">);</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Observation:">Observation:<a class="anchor-link" href="#Observation:">&#182;</a></h3><p>1) We can see from the above Scatter plot that <strong>most of the transaction amounts</strong> are <strong>between 0 to 2500 for both normal and fraud</strong>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Let-us-check-fraud-Amount-versus-normal-Amount-distrubutions">Let us check fraud Amount versus normal Amount distrubutions<a class="anchor-link" href="#Let-us-check-fraud-Amount-versus-normal-Amount-distrubutions">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">g</span><span class="o">=</span><span class="n">sns</span><span class="o">.</span><span class="n">FacetGrid</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s1">&#39;Class&#39;</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="mi">8</span><span class="p">)</span>
<span class="n">plot</span><span class="o">=</span><span class="n">g</span><span class="o">.</span><span class="n">map</span><span class="p">(</span><span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">,</span><span class="s2">&quot;Amount&quot;</span><span class="p">)</span><span class="o">.</span><span class="n">add_legend</span><span class="p">()</span>
<span class="n">g</span> <span class="o">=</span> <span class="n">g</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlim</span><span class="o">=</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="mi">3000</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
md0sv4KmOS0zJvmq6HJeSpKUyA+W7DsAAEC8nn/++fpVq1b1neyaefPmZR9//PFX0um0e+GFF1I3
3HDDmZs2bXrp7rvvnnn55Zd33X777fuz2ay6u7u9X/3qV+l9+/bVbN269UVJOnToUOJkfU8kTCCz
cdrGLpib6Jow94YVqi/n3J2S7pSkc5YsKNnCvlwiCGQ5AhkAANUkk8nYTTfdtHDz5s31nudp586d
KUm66KKLej/2sY8tGhoa8q699tqjF198cf/y5csHd+/enbrxxhsXXHXVVV3ve9/7jkf5zjBTlp2S
Fox6P1/S3omuMbOkpCb505Fh7h3rteGpyODf4U3TovRVMlTIAACoPOedd17/c889lz7ZNbfddtsZ
s2fPHnrppZc2v/DCC5uHhoY8Sbryyit7HnvssS1tbW2ZD33oQ4u/+tWvzmptbc1t2rRp89vf/vbu
O+64Y/a6desWRRlXmED2tKRlZrbYzGrlL9JfP+aa9ZJuDF5fK+lR55wL2tcFT2Eulr8g/6lJvm90
XzdK+vdR7X8UPG15kaSu4anNcsgl6iRJidxAuYYAAAAKdNVVV3VnMhn74he/2DLc9vOf/zzd0dFR
O/y+q6srMXfu3KFEIqE77rhjVi7n7zn6yiuv1La1tQ195jOfOfSHf/iHh37961+n9+3bl8zlcvrQ
hz507G/+5m/2vPDCCycNexOZdMoyWBP2KUkbJCUk3e2ce9HMbpW00Tm3XtJdkr5jZh3yK2Prgntf
NLP7JW2WlJX0Sef8nVTN7LuSLpPUYmadkr7gnLtL0t9Jut/MbpK0S9J1wVAelPQu+Q8G9En6cJQf
HJcsFTIAACqO53lav379tk984hML/uEf/mFOKpVy8+fPH/zKV74ysk79T//0Tw9cc801S37wgx/M
eOtb39pdX1+fl6QNGzY0fvnLX56TTCZdOp3O3XPPPTteffXVmptuumlRPp83Sbr11ls7o4zL/EJW
dTpnyQL3rb/709j73dZ+nVKZo7rmp5do4zm36JVFH4z9O6a6D1zYXu4hAAAgjVpj/txzz726atWq
Q+UcTFjPPfdcy6pVqxYNv2en/oiokAEAgLgQyCLK85QlAACICYEsImcJ5SxJhQwAABSNQFaEXKKO
ChkAACgagawIOS+lRJ5tLwAAQHEIZEXIJVKcZQkAAIpGICtCzkuxMSwAAHidBx54YPqiRYvObW9v
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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Divide the dataset according to the label FraudTransactions and Normal Transactions</span>
<span class="c1"># Fraud means Class=1 and Normal means status =0</span>
<span class="n">fraud</span><span class="o">=</span><span class="n">data</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">data</span><span class="p">[</span><span class="s2">&quot;Class&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span>
<span class="n">normal</span><span class="o">=</span><span class="n">data</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">data</span><span class="p">[</span><span class="s2">&quot;Class&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">5</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">121</span><span class="p">)</span>
<span class="n">fraud</span><span class="o">.</span><span class="n">Amount</span><span class="o">.</span><span class="n">plot</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">title</span><span class="o">=</span><span class="s2">&quot;Histogram of Fraud transactions&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">122</span><span class="p">)</span>
<span class="n">normal</span><span class="o">.</span><span class="n">Amount</span><span class="o">.</span><span class="n">plot</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">title</span><span class="o">=</span><span class="s2">&quot;Histogram of Normal transactions&quot;</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[11]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x10fca2da0&gt;</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Summary Statistics of fraud transactions:&quot;</span><span class="p">)</span>
<span class="n">fraud</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span><span class="o">.</span><span class="n">Amount</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Summary Statistics of fraud transactions:
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt output_prompt">Out[12]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>count     492.000000
mean      122.211321
std       256.683288
min         0.000000
25%         1.000000
50%         9.250000
75%       105.890000
max      2125.870000
Name: Amount, dtype: float64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Summary Statistics of Normal transactions:&quot;</span><span class="p">)</span>
<span class="n">normal</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span><span class="o">.</span><span class="n">Amount</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Summary Statistics of Normal transactions:
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt output_prompt">Out[13]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>count    284315.000000
mean         88.291022
std         250.105092
min           0.000000
25%           5.650000
50%          22.000000
75%          77.050000
max       25691.160000
Name: Amount, dtype: float64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Observation:">Observation:<a class="anchor-link" href="#Observation:">&#182;</a></h3><p>From the above plots and Statistics we can see that  <strong>fraud transactions amount on average is higher than normal transactions amount though absolute amount for normal transactions is high.</strong> Based on this <strong>we cannot simply come up with a condition on amount</strong> to detect a fraud transaction.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Let-us-Analyze-fraud-and-normal-transactions-with-respect-to-time---Though-each-transaction-is-different-just-out-of-curiosity,-am-checking-fraud-transactions-occurence-with-respect-to-time-on-two-days">Let us Analyze fraud and normal transactions with respect to time - Though each transaction is different just out of curiosity, am checking fraud transactions occurence with respect to time on two days<a class="anchor-link" href="#Let-us-Analyze-fraud-and-normal-transactions-with-respect-to-time---Though-each-transaction-is-different-just-out-of-curiosity,-am-checking-fraud-transactions-occurence-with-respect-to-time-on-two-days">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># DataSet contains two days transactions. </span>
<span class="c1"># Feature &#39;Time&#39; contains the seconds elapsed between each transaction and the first </span>
<span class="c1"># transaction in the dataset.let us convert time in seconds to hours of a day</span>
<span class="n">dataSubset</span> <span class="o">=</span> <span class="n">data</span><span class="p">[[</span><span class="s1">&#39;Time&#39;</span><span class="p">,</span> <span class="s1">&#39;Amount&#39;</span><span class="p">,</span> <span class="s1">&#39;Class&#39;</span><span class="p">]]</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get rid of $ and , in the SAL-RATE, then convert it to a float</span>
<span class="k">def</span> <span class="nf">seconds_Hour_Coversion</span><span class="p">(</span><span class="n">seconds</span><span class="p">):</span>
      <span class="n">hours</span> <span class="o">=</span> <span class="n">seconds</span><span class="o">/</span><span class="p">(</span><span class="mi">60</span><span class="o">*</span><span class="mi">60</span><span class="p">)</span> <span class="c1">## for conversion of seconds to hours.</span>
      <span class="k">if</span> <span class="n">hours</span><span class="o">&gt;</span><span class="mi">24</span><span class="p">:</span> 
    <span class="c1">## if it is more than 24 hours then divide it by 2 as max number of hours is 48.</span>
        <span class="n">hours</span><span class="o">=</span> <span class="n">hours</span><span class="o">/</span><span class="mi">2</span> 
        <span class="k">return</span> <span class="nb">int</span><span class="p">(</span><span class="n">hours</span><span class="p">)</span>
      <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="nb">int</span><span class="p">(</span><span class="n">hours</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Save the result in a new column</span>
<span class="n">dataSubset</span><span class="p">[</span><span class="s1">&#39;Hours&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">dataSubset</span><span class="p">[</span><span class="s1">&#39;Time&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="n">seconds_Hour_Coversion</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">g</span><span class="o">=</span><span class="n">sns</span><span class="o">.</span><span class="n">FacetGrid</span><span class="p">(</span><span class="n">dataSubset</span><span class="p">,</span> <span class="n">hue</span><span class="o">=</span><span class="s1">&#39;Class&#39;</span><span class="p">,</span> <span class="n">size</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>
<span class="n">plot</span><span class="o">=</span><span class="n">g</span><span class="o">.</span><span class="n">map</span><span class="p">(</span><span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">,</span><span class="s2">&quot;Hours&quot;</span><span class="p">)</span><span class="o">.</span><span class="n">add_legend</span><span class="p">()</span>
<span class="n">g</span> <span class="o">=</span> <span class="n">g</span><span class="o">.</span><span class="n">set</span><span class="p">(</span><span class="n">xlim</span><span class="o">=</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="mi">24</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#Divide the data set according to the label FraudTransactions and Normal Transactions</span>
<span class="c1"># Fraud means Class=1 and Normal means status =0</span>
<span class="n">frauddata</span><span class="o">=</span><span class="n">dataSubset</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">data</span><span class="p">[</span><span class="s2">&quot;Class&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">1</span><span class="p">]</span>
<span class="n">normaldata</span><span class="o">=</span><span class="n">dataSubset</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="n">data</span><span class="p">[</span><span class="s2">&quot;Class&quot;</span><span class="p">]</span><span class="o">==</span><span class="mi">0</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[19]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">frauddata</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[19]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Time</th>
      <th>Amount</th>
      <th>Class</th>
      <th>Hours</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>492.000000</td>
      <td>492.000000</td>
      <td>492.0</td>
      <td>492.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>80746.806911</td>
      <td>122.211321</td>
      <td>1.0</td>
      <td>14.313008</td>
    </tr>
    <tr>
      <th>std</th>
      <td>47835.365138</td>
      <td>256.683288</td>
      <td>0.0</td>
      <td>5.928253</td>
    </tr>
    <tr>
      <th>min</th>
      <td>406.000000</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>41241.500000</td>
      <td>1.000000</td>
      <td>1.0</td>
      <td>11.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>75568.500000</td>
      <td>9.250000</td>
      <td>1.0</td>
      <td>14.500000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>128483.000000</td>
      <td>105.890000</td>
      <td>1.0</td>
      <td>19.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>170348.000000</td>
      <td>2125.870000</td>
      <td>1.0</td>
      <td>23.000000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Observation:">Observation:<a class="anchor-link" href="#Observation:">&#182;</a></h3><p>1) During the <strong>early hours</strong> i.e at (2 to 3 AM) there are <strong>more fraud transactions when compared with normal transactions</strong> - may be more chance of occuring during that time.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#let us plot a heat map for correlation of the features</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">data</span><span class="o">.</span><span class="n">corr</span><span class="p">())</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[20]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.axes._subplots.AxesSubplot at 0x113c73860&gt;</pre>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
rJS+KH5RNG3EZ7fY/kfDbZP0hKTt07P17Ukizlsda7mkRcAbSE6sh9W1dMd09UTg+YiYAXyDJGNm
SNl0RzfqZtYt0cZ/Jc0FTkofn0RygvwKkqZJ2jh9vAVwMPBgXsHdTHcEWAZcnT6+Btin5PHNzCrV
xayY84AjJC0GjkifI2mGpIvTffYAbpV0N/Bz4IsRcW9ewV1Ld0xdCxyW7v8m4KEix5kUXZrF1szW
061JszfO6QHp1mTW3bp4mk5WdPgQ628HTksf/5QRnABXMY79cuAHvNwlM5DuuJWkk9N1J0fEQpJv
pMsknQmsIa28mVldNOHO066mO6ZDHt9W9phmZp3irBgzs4ZpZ1RMXblhNzPLcGyvmVnDdDErpmPc
sJuZZfiM3cw2eFVNmv3P+3dn0uw8TThj73a64+GS7kyzhX8hybeUmlmtdPHO044pc+dpNk5gwHHA
F4D3RcRrSHJkvixp83T714DjI2I/4HvAp0sc38yscn3RX3ipqzIN+xzg7ZImAgxKd1wMSWgNSbDN
NulrApiSPt4MyI2fNDPrpoj+wktdjbhhT2+HHUh3hGLpjqcB8yQtA04kzUYYiqRZkm6XdPtta4YM
gDQzq1w/UXipq26nO54JvDUipgH/ClwwXMHZdMeZk6eXrKaZWTFdDAHrmK6lO0raBtg3Im5NX3sl
cFDJ45uZVaoJZ+zdTHdcCWwm6VUR8RBJTOUDZY4/4KZY2XL7dY8vzC3jHdvtn7vPMeumtNx+9tpf
5ZZxybidc/fZfc+nWm4/9+GhJmR5pc1z/mifZV1uGdNifO4+eb2M4wr83d+owD7PVTDP8dgCx5mY
s8+Ksfn9qrO2zJ8Y7JYV27bcvjCvIsBq+lpu37k//8/v2TH57ydvkum8VEYoNpTxw3e2HhL5lS4N
h+zrr2/feVFdTXeU9H7gakn9JA39n1dwfDOzytR5GGNR3U53vIbkbN7MrJbq3HdelO88NTPLqHPf
eVFu2M3MMnzGbmbWME3IinHDbmaWUeeogKLUCz87Pr/TCS0ruUJrW77+9S/mD/u6dvzq3H1OeGGT
lttv2Cj/L8RmjM3d58H4bcvtB8Xk3DKWjmk9nPGR/jW5ZZz+Qv5xLpjQeqjpm8ds03I7wDXrfpO7
z9Hjprbcfhurcst45MXWdQU4cOIOLbe/ui//71JfgUmXx+f8s1tTwfDOIs1TkeGoefL/RherS15V
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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Observation:">Observation:<a class="anchor-link" href="#Observation:">&#182;</a></h3><p>1) All most all the features are <strong>uncorrelated</strong>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Cosine-Similarity-of-Transactions:">Cosine Similarity of Transactions:<a class="anchor-link" href="#Cosine-Similarity-of-Transactions:">&#182;</a></h2><h4 id="1)Extract-100-Samples-from-the-dataSet.">1)Extract 100 Samples from the dataSet.<a class="anchor-link" href="#1)Extract-100-Samples-from-the-dataSet.">&#182;</a></h4><h4 id="2)For-every-transaction-in-the-sample--top-10-transactions-in-the-dataset-which-have-the-lowest-similarity(i,j).">2)For every transaction in the sample  top 10 transactions in the dataset which have the lowest similarity(i,j).<a class="anchor-link" href="#2)For-every-transaction-in-the-sample--top-10-transactions-in-the-dataset-which-have-the-lowest-similarity(i,j).">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[34]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## let us take 100 samples from the dataset using train_test_split without missing </span>
<span class="c1"># class distrubution in the original dataset.</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="k">import</span> <span class="n">train_test_split</span>
<span class="n">X_train</span><span class="p">,</span><span class="n">X_test</span><span class="p">,</span><span class="n">y_train</span><span class="p">,</span><span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">data</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span> <span class="n">data</span><span class="o">.</span><span class="n">columns</span> <span class="o">!=</span> <span class="s1">&#39;Class&#39;</span><span class="p">],</span>\
                <span class="n">data</span><span class="p">[</span><span class="s1">&#39;Class&#39;</span><span class="p">],</span> <span class="n">test_size</span><span class="o">=</span><span class="mf">0.00035</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>
<span class="n">sample</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">X_test</span><span class="p">,</span> <span class="n">y_test</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span> 
<span class="n">sample</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[34]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(100, 31)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Computing the Similarity</span>
<span class="n">similarity</span><span class="o">=</span><span class="n">cosine_similarity</span><span class="p">(</span><span class="n">sample</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[36]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># rename the index and name it as TransactionId</span>
<span class="n">sample</span><span class="o">.</span><span class="n">index</span><span class="o">.</span><span class="n">name</span> <span class="o">=</span> <span class="s1">&#39;TransactionId&#39;</span>
<span class="n">sample</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[36]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Time</th>
      <th>V1</th>
      <th>V2</th>
      <th>V3</th>
      <th>V4</th>
      <th>V5</th>
      <th>V6</th>
      <th>V7</th>
      <th>V8</th>
      <th>V9</th>
      <th>...</th>
      <th>V21</th>
      <th>V22</th>
      <th>V23</th>
      <th>V24</th>
      <th>V25</th>
      <th>V26</th>
      <th>V27</th>
      <th>V28</th>
      <th>Amount</th>
      <th>Class</th>
    </tr>
    <tr>
      <th>TransactionId</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>43428</th>
      <td>41505.0</td>
      <td>-16.526507</td>
      <td>8.584972</td>
      <td>-18.649853</td>
      <td>9.505594</td>
      <td>-13.793819</td>
      <td>-2.832404</td>
      <td>-16.701694</td>
      <td>7.517344</td>
      <td>-8.507059</td>
      <td>...</td>
      <td>1.190739</td>
      <td>-1.127670</td>
      <td>-2.358579</td>
      <td>0.673461</td>
      <td>-1.413700</td>
      <td>-0.462762</td>
      <td>-2.018575</td>
      <td>-1.042804</td>
      <td>364.19</td>
      <td>1</td>
    </tr>
    <tr>
      <th>49906</th>
      <td>44261.0</td>
      <td>0.339812</td>
      <td>-2.743745</td>
      <td>-0.134070</td>
      <td>-1.385729</td>
      <td>-1.451413</td>
      <td>1.015887</td>
      <td>-0.524379</td>
      <td>0.224060</td>
      <td>0.899746</td>
      <td>...</td>
      <td>-0.213436</td>
      <td>-0.942525</td>
      <td>-0.526819</td>
      <td>-1.156992</td>
      <td>0.311211</td>
      <td>-0.746647</td>
      <td>0.040996</td>
      <td>0.102038</td>
      <td>520.12</td>
      <td>0</td>
    </tr>
    <tr>
      <th>29474</th>
      <td>35484.0</td>
      <td>1.399590</td>
      <td>-0.590701</td>
      <td>0.168619</td>
      <td>-1.029950</td>
      <td>-0.539806</td>
      <td>0.040444</td>
      <td>-0.712567</td>
      <td>0.002299</td>
      <td>-0.971747</td>
      <td>...</td>
      <td>0.102398</td>
      <td>0.168269</td>
      <td>-0.166639</td>
      <td>-0.810250</td>
      <td>0.505083</td>
      <td>-0.232340</td>
      <td>0.011409</td>
      <td>0.004634</td>
      <td>31.00</td>
      <td>0</td>
    </tr>
    <tr>
      <th>276481</th>
      <td>167123.0</td>
      <td>-0.432071</td>
      <td>1.647895</td>
      <td>-1.669361</td>
      <td>-0.349504</td>
      <td>0.785785</td>
      <td>-0.630647</td>
      <td>0.276990</td>
      <td>0.586025</td>
      <td>-0.484715</td>
      <td>...</td>
      <td>0.358932</td>
      <td>0.873663</td>
      <td>-0.178642</td>
      <td>-0.017171</td>
      <td>-0.207392</td>
      <td>-0.157756</td>
      <td>-0.237386</td>
      <td>0.001934</td>
      <td>1.50</td>
      <td>0</td>
    </tr>
    <tr>
      <th>278846</th>
      <td>168473.0</td>
      <td>2.014160</td>
      <td>-0.137394</td>
      <td>-1.015839</td>
      <td>0.327269</td>
      <td>-0.182179</td>
      <td>-0.956571</td>
      <td>0.043241</td>
      <td>-0.160746</td>
      <td>0.363241</td>
      <td>...</td>
      <td>-0.238644</td>
      <td>-0.616400</td>
      <td>0.347045</td>
      <td>0.061561</td>
      <td>-0.360196</td>
      <td>0.174730</td>
      <td>-0.078043</td>
      <td>-0.070571</td>
      <td>0.89</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 31 columns</p>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[39]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">printResult</span><span class="p">(</span><span class="n">transaction1</span><span class="p">,</span><span class="n">first10pairs</span><span class="p">,</span><span class="n">sample</span><span class="p">,</span><span class="nb">dict</span><span class="p">):</span>
     <span class="n">x</span><span class="o">=</span><span class="n">transaction1</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="mi">30</span><span class="p">]</span>
     <span class="n">y</span><span class="o">=</span><span class="n">transaction1</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
     <span class="n">s1</span><span class="o">=</span><span class="s1">&#39;For the transaction id = &#39;</span><span class="o">+</span> <span class="s1">&#39;</span><span class="si">{:d}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">y</span><span class="p">)</span> <span class="o">+</span> <span class="s1">&#39;, and Class = &#39;</span> <span class="o">+</span> \
        <span class="s1">&#39;</span><span class="si">{0:.5g}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
     <span class="nb">print</span> <span class="p">(</span><span class="n">s1</span> <span class="o">+</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>   
     <span class="nb">print</span> <span class="p">(</span><span class="s1">&#39;Similar transactions are :&#39;</span><span class="o">+</span> <span class="s1">&#39;</span><span class="se">\n</span><span class="s1">&#39;</span><span class="p">)</span>
     <span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="n">first10pairs</span><span class="p">:</span>
        <span class="n">printSimilarity</span><span class="p">(</span><span class="n">k</span><span class="p">,</span><span class="nb">dict</span><span class="p">[</span><span class="n">k</span><span class="p">],</span><span class="n">sample</span><span class="p">)</span>
     <span class="nb">print</span> <span class="p">(</span><span class="s1">&#39;--------------------------------------------------------&#39;</span><span class="o">+</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>   
            
<span class="k">def</span> <span class="nf">printSimilarity</span><span class="p">(</span><span class="n">transactionId</span><span class="p">,</span><span class="n">similarity</span><span class="p">,</span><span class="n">sample</span><span class="p">):</span>
   
     <span class="k">for</span> <span class="n">transaction</span> <span class="ow">in</span> <span class="n">sample</span><span class="o">.</span><span class="n">iterrows</span><span class="p">():</span> 
            <span class="k">if</span> <span class="n">transaction</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">==</span> <span class="n">transactionId</span><span class="p">:</span>
              <span class="n">x</span><span class="o">=</span><span class="n">transaction</span><span class="p">[</span><span class="mi">1</span><span class="p">][</span><span class="mi">30</span><span class="p">]</span>
              <span class="n">s</span><span class="o">=</span><span class="n">similarity</span>
              <span class="n">y</span><span class="o">=</span><span class="n">transactionId</span>  
              <span class="nb">print</span> <span class="p">(</span><span class="s2">&quot;Class = &quot;</span> <span class="o">+</span> <span class="s1">&#39;</span><span class="si">{0:.5g}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">x</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot;, Similarity = &quot;</span><span class="o">+</span>\
                 <span class="s1">&#39;</span><span class="si">{:f}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">s</span><span class="p">)</span><span class="o">+</span> <span class="s2">&quot;, transactionId = &quot;</span><span class="o">+</span><span class="s1">&#39;</span><span class="si">{:d}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">y</span><span class="p">)</span><span class="o">+</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
              
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[38]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">operator</span>
<span class="kn">import</span> <span class="nn">itertools</span>
<span class="n">i</span><span class="o">=-</span><span class="mi">1</span><span class="p">;</span>
<span class="nb">dict</span><span class="o">=</span><span class="p">{}</span>
<span class="k">for</span> <span class="n">transaction1</span> <span class="ow">in</span> <span class="n">sample</span><span class="o">.</span><span class="n">iterrows</span><span class="p">()</span> <span class="p">:</span>
        <span class="n">i</span><span class="o">=</span><span class="n">i</span><span class="o">+</span><span class="mi">1</span>
        <span class="n">j</span><span class="o">=</span><span class="mi">0</span>
        <span class="k">for</span> <span class="n">transaction2</span> <span class="ow">in</span> <span class="n">sample</span><span class="o">.</span><span class="n">iterrows</span><span class="p">():</span>
            <span class="k">if</span> <span class="n">i</span> <span class="ow">is</span> <span class="ow">not</span> <span class="n">j</span><span class="p">:</span>
              <span class="nb">dict</span><span class="p">[</span><span class="n">transaction2</span><span class="p">[</span><span class="mi">0</span><span class="p">]]</span> <span class="o">=</span> <span class="n">similarity</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">j</span><span class="p">]</span>
            <span class="n">j</span><span class="o">=</span><span class="n">j</span><span class="o">+</span><span class="mi">1</span>
                   
        <span class="k">if</span> <span class="nb">dict</span> <span class="p">:</span> 
            <span class="n">sorted_dict</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="nb">dict</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="nb">dict</span><span class="o">.</span><span class="fm">__getitem__</span><span class="p">)[:</span><span class="mi">10</span><span class="p">]</span>
            <span class="n">printResult</span><span class="p">(</span><span class="n">transaction1</span><span class="p">,</span><span class="n">sorted_dict</span><span class="p">,</span><span class="n">sample</span><span class="p">,</span><span class="nb">dict</span><span class="p">)</span>
            <span class="nb">dict</span><span class="o">.</span><span class="n">clear</span><span class="p">()</span>    
        
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>For the transaction id = 43428, and Class = 1

Similar transactions are :

Class = 0, Similarity = 0.999612, transactionId = 21934

Class = 0, Similarity = 0.999872, transactionId = 219257

Class = 0, Similarity = 0.999961, transactionId = 15816

Class = 0, Similarity = 0.999961, transactionId = 278846

Class = 0, Similarity = 0.999961, transactionId = 276741

Class = 0, Similarity = 0.999961, transactionId = 257395

Class = 0, Similarity = 0.999961, transactionId = 209862

Class = 0, Similarity = 0.999961, transactionId = 158290

Class = 0, Similarity = 0.999961, transactionId = 276481

Class = 0, Similarity = 0.999961, transactionId = 149100

-------------------------------------------------------------------------

For the transaction id = 49906, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999691, transactionId = 21934

Class = 0, Similarity = 0.999916, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 15816

Class = 0, Similarity = 0.999931, transactionId = 276741

Class = 0, Similarity = 0.999931, transactionId = 278846

Class = 0, Similarity = 0.999931, transactionId = 257395

Class = 0, Similarity = 0.999931, transactionId = 209862

Class = 0, Similarity = 0.999931, transactionId = 158290

Class = 0, Similarity = 0.999931, transactionId = 276481

Class = 0, Similarity = 0.999931, transactionId = 149100

-------------------------------------------------------------------------

For the transaction id = 29474, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999361, transactionId = 21934

Class = 0, Similarity = 0.999716, transactionId = 219257

Class = 0, Similarity = 0.999941, transactionId = 49906

Class = 0, Similarity = 0.999959, transactionId = 35730

Class = 1, Similarity = 0.999968, transactionId = 43428

Class = 0, Similarity = 0.999980, transactionId = 38442

Class = 0, Similarity = 0.999985, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 276481, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999979, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 278846, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999979, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 101565, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999383, transactionId = 21934

Class = 0, Similarity = 0.999730, transactionId = 219257

Class = 0, Similarity = 0.999947, transactionId = 49906

Class = 0, Similarity = 0.999964, transactionId = 35730

Class = 1, Similarity = 0.999973, transactionId = 43428

Class = 0, Similarity = 0.999984, transactionId = 38442

Class = 0, Similarity = 0.999988, transactionId = 105030

Class = 0, Similarity = 0.999997, transactionId = 80419

Class = 0, Similarity = 0.999997, transactionId = 36749

Class = 0, Similarity = 0.999999, transactionId = 15816

-------------------------------------------------------------------------

For the transaction id = 260880, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999334, transactionId = 21934

Class = 0, Similarity = 0.999697, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 214337, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999332, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 201575, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999333, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 81055, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999392, transactionId = 21934

Class = 0, Similarity = 0.999736, transactionId = 219257

Class = 0, Similarity = 0.999950, transactionId = 49906

Class = 0, Similarity = 0.999966, transactionId = 35730

Class = 1, Similarity = 0.999974, transactionId = 43428

Class = 0, Similarity = 0.999985, transactionId = 38442

Class = 0, Similarity = 0.999989, transactionId = 105030

Class = 0, Similarity = 0.999998, transactionId = 80419

Class = 0, Similarity = 0.999998, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 15816

-------------------------------------------------------------------------

For the transaction id = 134976, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999349, transactionId = 21934

Class = 0, Similarity = 0.999708, transactionId = 219257

Class = 0, Similarity = 0.999937, transactionId = 49906

Class = 0, Similarity = 0.999956, transactionId = 35730

Class = 1, Similarity = 0.999965, transactionId = 43428

Class = 0, Similarity = 0.999978, transactionId = 38442

Class = 0, Similarity = 0.999983, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 237701, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999335, transactionId = 21934

Class = 0, Similarity = 0.999698, transactionId = 219257

Class = 0, Similarity = 0.999933, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 256836, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999366, transactionId = 21934

Class = 0, Similarity = 0.999718, transactionId = 219257

Class = 0, Similarity = 0.999942, transactionId = 49906

Class = 0, Similarity = 0.999960, transactionId = 35730

Class = 1, Similarity = 0.999969, transactionId = 43428

Class = 0, Similarity = 0.999981, transactionId = 38442

Class = 0, Similarity = 0.999985, transactionId = 105030

Class = 0, Similarity = 0.999996, transactionId = 80419

Class = 0, Similarity = 0.999996, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 97650, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999353, transactionId = 21934

Class = 0, Similarity = 0.999710, transactionId = 219257

Class = 0, Similarity = 0.999938, transactionId = 49906

Class = 0, Similarity = 0.999957, transactionId = 35730

Class = 1, Similarity = 0.999966, transactionId = 43428

Class = 0, Similarity = 0.999979, transactionId = 38442

Class = 0, Similarity = 0.999983, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 158290, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999979, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 246697, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999332, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 68279, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 267585, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999336, transactionId = 21934

Class = 0, Similarity = 0.999698, transactionId = 219257

Class = 0, Similarity = 0.999933, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 26525, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999409, transactionId = 21934

Class = 0, Similarity = 0.999747, transactionId = 219257

Class = 0, Similarity = 0.999955, transactionId = 49906

Class = 0, Similarity = 0.999970, transactionId = 35730

Class = 1, Similarity = 0.999978, transactionId = 43428

Class = 0, Similarity = 0.999988, transactionId = 38442

Class = 0, Similarity = 0.999991, transactionId = 105030

Class = 0, Similarity = 0.999998, transactionId = 15816

Class = 0, Similarity = 0.999998, transactionId = 276741

Class = 0, Similarity = 0.999998, transactionId = 278846

-------------------------------------------------------------------------

For the transaction id = 74422, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999345, transactionId = 21934

Class = 0, Similarity = 0.999704, transactionId = 219257

Class = 0, Similarity = 0.999936, transactionId = 49906

Class = 0, Similarity = 0.999955, transactionId = 35730

Class = 1, Similarity = 0.999964, transactionId = 43428

Class = 0, Similarity = 0.999977, transactionId = 38442

Class = 0, Similarity = 0.999982, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 206357, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999342, transactionId = 21934

Class = 0, Similarity = 0.999703, transactionId = 219257

Class = 0, Similarity = 0.999935, transactionId = 49906

Class = 0, Similarity = 0.999954, transactionId = 35730

Class = 1, Similarity = 0.999964, transactionId = 43428

Class = 0, Similarity = 0.999977, transactionId = 38442

Class = 0, Similarity = 0.999982, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 257395, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999979, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 283656, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999331, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 231156, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999336, transactionId = 21934

Class = 0, Similarity = 0.999698, transactionId = 219257

Class = 0, Similarity = 0.999933, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 38442, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999566, transactionId = 21934

Class = 0, Similarity = 0.999846, transactionId = 219257

Class = 0, Similarity = 0.999974, transactionId = 15816

Class = 0, Similarity = 0.999974, transactionId = 278846

Class = 0, Similarity = 0.999974, transactionId = 276741

Class = 0, Similarity = 0.999974, transactionId = 257395

Class = 0, Similarity = 0.999974, transactionId = 209862

Class = 0, Similarity = 0.999974, transactionId = 276481

Class = 0, Similarity = 0.999974, transactionId = 158290

Class = 0, Similarity = 0.999974, transactionId = 149100

-------------------------------------------------------------------------

For the transaction id = 225485, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999357, transactionId = 21934

Class = 0, Similarity = 0.999713, transactionId = 219257

Class = 0, Similarity = 0.999940, transactionId = 49906

Class = 0, Similarity = 0.999958, transactionId = 35730

Class = 1, Similarity = 0.999967, transactionId = 43428

Class = 0, Similarity = 0.999979, transactionId = 38442

Class = 0, Similarity = 0.999984, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 92410, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999379, transactionId = 21934

Class = 0, Similarity = 0.999727, transactionId = 219257

Class = 0, Similarity = 0.999946, transactionId = 49906

Class = 0, Similarity = 0.999963, transactionId = 35730

Class = 1, Similarity = 0.999972, transactionId = 43428

Class = 0, Similarity = 0.999983, transactionId = 38442

Class = 0, Similarity = 0.999987, transactionId = 105030

Class = 0, Similarity = 0.999997, transactionId = 80419

Class = 0, Similarity = 0.999997, transactionId = 36749

Class = 0, Similarity = 0.999999, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 10828, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999373, transactionId = 21934

Class = 0, Similarity = 0.999723, transactionId = 219257

Class = 0, Similarity = 0.999944, transactionId = 49906

Class = 0, Similarity = 0.999962, transactionId = 35730

Class = 1, Similarity = 0.999970, transactionId = 43428

Class = 0, Similarity = 0.999982, transactionId = 38442

Class = 0, Similarity = 0.999986, transactionId = 105030

Class = 0, Similarity = 0.999996, transactionId = 80419

Class = 0, Similarity = 0.999996, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 61461, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999346, transactionId = 21934

Class = 0, Similarity = 0.999705, transactionId = 219257

Class = 0, Similarity = 0.999936, transactionId = 49906

Class = 0, Similarity = 0.999955, transactionId = 35730

Class = 1, Similarity = 0.999965, transactionId = 43428

Class = 0, Similarity = 0.999977, transactionId = 38442

Class = 0, Similarity = 0.999982, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 134354, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999372, transactionId = 21934

Class = 0, Similarity = 0.999723, transactionId = 219257

Class = 0, Similarity = 0.999944, transactionId = 49906

Class = 0, Similarity = 0.999961, transactionId = 35730

Class = 1, Similarity = 0.999970, transactionId = 43428

Class = 0, Similarity = 0.999982, transactionId = 38442

Class = 0, Similarity = 0.999986, transactionId = 105030

Class = 0, Similarity = 0.999996, transactionId = 80419

Class = 0, Similarity = 0.999996, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 45265, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999362, transactionId = 21934

Class = 0, Similarity = 0.999716, transactionId = 219257

Class = 0, Similarity = 0.999941, transactionId = 49906

Class = 0, Similarity = 0.999959, transactionId = 35730

Class = 1, Similarity = 0.999968, transactionId = 43428

Class = 0, Similarity = 0.999980, transactionId = 38442

Class = 0, Similarity = 0.999985, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 151374, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999331, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 219257, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999694, transactionId = 15816

Class = 0, Similarity = 0.999695, transactionId = 278846

Class = 0, Similarity = 0.999695, transactionId = 276741

Class = 0, Similarity = 0.999695, transactionId = 257395

Class = 0, Similarity = 0.999695, transactionId = 209862

Class = 0, Similarity = 0.999695, transactionId = 158290

Class = 0, Similarity = 0.999695, transactionId = 276481

Class = 0, Similarity = 0.999695, transactionId = 149100

Class = 0, Similarity = 0.999695, transactionId = 233533

Class = 0, Similarity = 0.999695, transactionId = 71345

-------------------------------------------------------------------------

For the transaction id = 49275, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999411, transactionId = 21934

Class = 0, Similarity = 0.999749, transactionId = 219257

Class = 0, Similarity = 0.999955, transactionId = 49906

Class = 0, Similarity = 0.999971, transactionId = 35730

Class = 1, Similarity = 0.999978, transactionId = 43428

Class = 0, Similarity = 0.999988, transactionId = 38442

Class = 0, Similarity = 0.999992, transactionId = 105030

Class = 0, Similarity = 0.999997, transactionId = 15816

Class = 0, Similarity = 0.999997, transactionId = 278846

Class = 0, Similarity = 0.999997, transactionId = 276741

-------------------------------------------------------------------------

For the transaction id = 113769, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999350, transactionId = 21934

Class = 0, Similarity = 0.999708, transactionId = 219257

Class = 0, Similarity = 0.999937, transactionId = 49906

Class = 0, Similarity = 0.999956, transactionId = 35730

Class = 1, Similarity = 0.999965, transactionId = 43428

Class = 0, Similarity = 0.999978, transactionId = 38442

Class = 0, Similarity = 0.999983, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 205650, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999333, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 250467, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999357, transactionId = 21934

Class = 0, Similarity = 0.999712, transactionId = 219257

Class = 0, Similarity = 0.999939, transactionId = 49906

Class = 0, Similarity = 0.999958, transactionId = 35730

Class = 1, Similarity = 0.999967, transactionId = 43428

Class = 0, Similarity = 0.999979, transactionId = 38442

Class = 0, Similarity = 0.999984, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 194599, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999340, transactionId = 21934

Class = 0, Similarity = 0.999701, transactionId = 219257

Class = 0, Similarity = 0.999934, transactionId = 49906

Class = 0, Similarity = 0.999953, transactionId = 35730

Class = 1, Similarity = 0.999963, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 266912, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999337, transactionId = 21934

Class = 0, Similarity = 0.999699, transactionId = 219257

Class = 0, Similarity = 0.999933, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 228215, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999350, transactionId = 21934

Class = 0, Similarity = 0.999708, transactionId = 219257

Class = 0, Similarity = 0.999937, transactionId = 49906

Class = 0, Similarity = 0.999956, transactionId = 35730

Class = 1, Similarity = 0.999966, transactionId = 43428

Class = 0, Similarity = 0.999978, transactionId = 38442

Class = 0, Similarity = 0.999983, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 259706, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999332, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 149066, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999334, transactionId = 21934

Class = 0, Similarity = 0.999697, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 68119, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999377, transactionId = 21934

Class = 0, Similarity = 0.999726, transactionId = 219257

Class = 0, Similarity = 0.999945, transactionId = 49906

Class = 0, Similarity = 0.999963, transactionId = 35730

Class = 1, Similarity = 0.999971, transactionId = 43428

Class = 0, Similarity = 0.999983, transactionId = 38442

Class = 0, Similarity = 0.999987, transactionId = 105030

Class = 0, Similarity = 0.999997, transactionId = 80419

Class = 0, Similarity = 0.999997, transactionId = 36749

Class = 0, Similarity = 0.999999, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 225255, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999391, transactionId = 21934

Class = 0, Similarity = 0.999735, transactionId = 219257

Class = 0, Similarity = 0.999950, transactionId = 49906

Class = 0, Similarity = 0.999966, transactionId = 35730

Class = 1, Similarity = 0.999974, transactionId = 43428

Class = 0, Similarity = 0.999985, transactionId = 38442

Class = 0, Similarity = 0.999989, transactionId = 105030

Class = 0, Similarity = 0.999998, transactionId = 80419

Class = 0, Similarity = 0.999998, transactionId = 36749

Class = 0, Similarity = 0.999999, transactionId = 15816

-------------------------------------------------------------------------

For the transaction id = 21934, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 15816

Class = 0, Similarity = 0.999330, transactionId = 278846

Class = 0, Similarity = 0.999330, transactionId = 276741

Class = 0, Similarity = 0.999330, transactionId = 257395

Class = 0, Similarity = 0.999330, transactionId = 209862

Class = 0, Similarity = 0.999330, transactionId = 276481

Class = 0, Similarity = 0.999330, transactionId = 158290

Class = 0, Similarity = 0.999330, transactionId = 149100

Class = 0, Similarity = 0.999330, transactionId = 233533

Class = 0, Similarity = 0.999330, transactionId = 71345

-------------------------------------------------------------------------

For the transaction id = 105030, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999544, transactionId = 21934

Class = 0, Similarity = 0.999832, transactionId = 219257

Class = 0, Similarity = 0.999979, transactionId = 15816

Class = 0, Similarity = 0.999979, transactionId = 278846

Class = 0, Similarity = 0.999979, transactionId = 276741

Class = 0, Similarity = 0.999979, transactionId = 257395

Class = 0, Similarity = 0.999979, transactionId = 209862

Class = 0, Similarity = 0.999979, transactionId = 158290

Class = 0, Similarity = 0.999979, transactionId = 276481

Class = 0, Similarity = 0.999979, transactionId = 149100

-------------------------------------------------------------------------

For the transaction id = 114027, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999335, transactionId = 21934

Class = 0, Similarity = 0.999698, transactionId = 219257

Class = 0, Similarity = 0.999933, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 178329, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999333, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 109526, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999336, transactionId = 21934

Class = 0, Similarity = 0.999698, transactionId = 219257

Class = 0, Similarity = 0.999933, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 32278, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999342, transactionId = 21934

Class = 0, Similarity = 0.999703, transactionId = 219257

Class = 0, Similarity = 0.999935, transactionId = 49906

Class = 0, Similarity = 0.999954, transactionId = 35730

Class = 1, Similarity = 0.999964, transactionId = 43428

Class = 0, Similarity = 0.999977, transactionId = 38442

Class = 0, Similarity = 0.999982, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 233533, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 76922, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999331, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 187045, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999433, transactionId = 21934

Class = 0, Similarity = 0.999763, transactionId = 219257

Class = 0, Similarity = 0.999961, transactionId = 49906

Class = 0, Similarity = 0.999976, transactionId = 35730

Class = 1, Similarity = 0.999982, transactionId = 43428

Class = 0, Similarity = 0.999991, transactionId = 38442

Class = 0, Similarity = 0.999994, transactionId = 105030

Class = 0, Similarity = 0.999996, transactionId = 15816

Class = 0, Similarity = 0.999996, transactionId = 276741

Class = 0, Similarity = 0.999996, transactionId = 278846

-------------------------------------------------------------------------

For the transaction id = 149100, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999979, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 133186, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999331, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 89165, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999340, transactionId = 21934

Class = 0, Similarity = 0.999701, transactionId = 219257

Class = 0, Similarity = 0.999934, transactionId = 49906

Class = 0, Similarity = 0.999953, transactionId = 35730

Class = 1, Similarity = 0.999963, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 138728, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999427, transactionId = 21934

Class = 0, Similarity = 0.999759, transactionId = 219257

Class = 0, Similarity = 0.999960, transactionId = 49906

Class = 0, Similarity = 0.999974, transactionId = 35730

Class = 1, Similarity = 0.999981, transactionId = 43428

Class = 0, Similarity = 0.999990, transactionId = 38442

Class = 0, Similarity = 0.999993, transactionId = 105030

Class = 0, Similarity = 0.999996, transactionId = 15816

Class = 0, Similarity = 0.999996, transactionId = 276741

Class = 0, Similarity = 0.999996, transactionId = 278846

-------------------------------------------------------------------------

For the transaction id = 161808, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 15816, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999694, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999979, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 150994, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999335, transactionId = 21934

Class = 0, Similarity = 0.999698, transactionId = 219257

Class = 0, Similarity = 0.999933, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 79591, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999352, transactionId = 21934

Class = 0, Similarity = 0.999709, transactionId = 219257

Class = 0, Similarity = 0.999938, transactionId = 49906

Class = 0, Similarity = 0.999956, transactionId = 35730

Class = 1, Similarity = 0.999966, transactionId = 43428

Class = 0, Similarity = 0.999979, transactionId = 38442

Class = 0, Similarity = 0.999983, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 36749, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999465, transactionId = 21934

Class = 0, Similarity = 0.999783, transactionId = 219257

Class = 0, Similarity = 0.999969, transactionId = 49906

Class = 0, Similarity = 0.999982, transactionId = 35730

Class = 1, Similarity = 0.999987, transactionId = 43428

Class = 0, Similarity = 0.999992, transactionId = 15816

Class = 0, Similarity = 0.999992, transactionId = 276741

Class = 0, Similarity = 0.999992, transactionId = 278846

Class = 0, Similarity = 0.999992, transactionId = 257395

Class = 0, Similarity = 0.999992, transactionId = 209862

-------------------------------------------------------------------------

For the transaction id = 28828, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999331, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 232448, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999376, transactionId = 21934

Class = 0, Similarity = 0.999725, transactionId = 219257

Class = 0, Similarity = 0.999945, transactionId = 49906

Class = 0, Similarity = 0.999962, transactionId = 35730

Class = 1, Similarity = 0.999971, transactionId = 43428

Class = 0, Similarity = 0.999983, transactionId = 38442

Class = 0, Similarity = 0.999987, transactionId = 105030

Class = 0, Similarity = 0.999997, transactionId = 80419

Class = 0, Similarity = 0.999997, transactionId = 36749

Class = 0, Similarity = 0.999999, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 28195, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999338, transactionId = 21934

Class = 0, Similarity = 0.999700, transactionId = 219257

Class = 0, Similarity = 0.999934, transactionId = 49906

Class = 0, Similarity = 0.999953, transactionId = 35730

Class = 1, Similarity = 0.999963, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 240146, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999419, transactionId = 21934

Class = 0, Similarity = 0.999753, transactionId = 219257

Class = 0, Similarity = 0.999957, transactionId = 49906

Class = 0, Similarity = 0.999972, transactionId = 35730

Class = 1, Similarity = 0.999980, transactionId = 43428

Class = 0, Similarity = 0.999989, transactionId = 38442

Class = 0, Similarity = 0.999992, transactionId = 105030

Class = 0, Similarity = 0.999997, transactionId = 15816

Class = 0, Similarity = 0.999997, transactionId = 278846

Class = 0, Similarity = 0.999997, transactionId = 276741

-------------------------------------------------------------------------

For the transaction id = 240449, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999332, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 49296, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999374, transactionId = 21934

Class = 0, Similarity = 0.999724, transactionId = 219257

Class = 0, Similarity = 0.999944, transactionId = 49906

Class = 0, Similarity = 0.999962, transactionId = 35730

Class = 1, Similarity = 0.999971, transactionId = 43428

Class = 0, Similarity = 0.999982, transactionId = 38442

Class = 0, Similarity = 0.999986, transactionId = 105030

Class = 0, Similarity = 0.999996, transactionId = 80419

Class = 0, Similarity = 0.999996, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 14176, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999340, transactionId = 21934

Class = 0, Similarity = 0.999702, transactionId = 219257

Class = 0, Similarity = 0.999934, transactionId = 49906

Class = 0, Similarity = 0.999953, transactionId = 35730

Class = 1, Similarity = 0.999963, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 80419, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999465, transactionId = 21934

Class = 0, Similarity = 0.999783, transactionId = 219257

Class = 0, Similarity = 0.999969, transactionId = 49906

Class = 0, Similarity = 0.999982, transactionId = 35730

Class = 1, Similarity = 0.999987, transactionId = 43428

Class = 0, Similarity = 0.999992, transactionId = 15816

Class = 0, Similarity = 0.999992, transactionId = 276741

Class = 0, Similarity = 0.999992, transactionId = 278846

Class = 0, Similarity = 0.999992, transactionId = 257395

Class = 0, Similarity = 0.999992, transactionId = 209862

-------------------------------------------------------------------------

For the transaction id = 210194, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999362, transactionId = 21934

Class = 0, Similarity = 0.999716, transactionId = 219257

Class = 0, Similarity = 0.999941, transactionId = 49906

Class = 0, Similarity = 0.999959, transactionId = 35730

Class = 1, Similarity = 0.999968, transactionId = 43428

Class = 0, Similarity = 0.999980, transactionId = 38442

Class = 0, Similarity = 0.999985, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 177473, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999333, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 81436, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 104674, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999331, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 102058, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999341, transactionId = 21934

Class = 0, Similarity = 0.999702, transactionId = 219257

Class = 0, Similarity = 0.999935, transactionId = 49906

Class = 0, Similarity = 0.999954, transactionId = 35730

Class = 1, Similarity = 0.999963, transactionId = 43428

Class = 0, Similarity = 0.999977, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 237523, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999377, transactionId = 21934

Class = 0, Similarity = 0.999726, transactionId = 219257

Class = 0, Similarity = 0.999946, transactionId = 49906

Class = 0, Similarity = 0.999963, transactionId = 35730

Class = 1, Similarity = 0.999972, transactionId = 43428

Class = 0, Similarity = 0.999983, transactionId = 38442

Class = 0, Similarity = 0.999987, transactionId = 105030

Class = 0, Similarity = 0.999997, transactionId = 80419

Class = 0, Similarity = 0.999997, transactionId = 36749

Class = 0, Similarity = 0.999999, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 51750, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999352, transactionId = 21934

Class = 0, Similarity = 0.999709, transactionId = 219257

Class = 0, Similarity = 0.999938, transactionId = 49906

Class = 0, Similarity = 0.999956, transactionId = 35730

Class = 1, Similarity = 0.999966, transactionId = 43428

Class = 0, Similarity = 0.999978, transactionId = 38442

Class = 0, Similarity = 0.999983, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 93581, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999333, transactionId = 21934

Class = 0, Similarity = 0.999697, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 228491, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999331, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 217792, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999373, transactionId = 21934

Class = 0, Similarity = 0.999723, transactionId = 219257

Class = 0, Similarity = 0.999944, transactionId = 49906

Class = 0, Similarity = 0.999962, transactionId = 35730

Class = 1, Similarity = 0.999971, transactionId = 43428

Class = 0, Similarity = 0.999982, transactionId = 38442

Class = 0, Similarity = 0.999986, transactionId = 105030

Class = 0, Similarity = 0.999996, transactionId = 80419

Class = 0, Similarity = 0.999996, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 276741, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999979, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 71345, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 234744, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999333, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 7730, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999357, transactionId = 21934

Class = 0, Similarity = 0.999712, transactionId = 219257

Class = 0, Similarity = 0.999939, transactionId = 49906

Class = 0, Similarity = 0.999958, transactionId = 35730

Class = 1, Similarity = 0.999967, transactionId = 43428

Class = 0, Similarity = 0.999979, transactionId = 38442

Class = 0, Similarity = 0.999984, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 35730, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999644, transactionId = 21934

Class = 0, Similarity = 0.999891, transactionId = 219257

Class = 0, Similarity = 0.999951, transactionId = 15816

Class = 0, Similarity = 0.999951, transactionId = 278846

Class = 0, Similarity = 0.999951, transactionId = 276741

Class = 0, Similarity = 0.999951, transactionId = 257395

Class = 0, Similarity = 0.999951, transactionId = 209862

Class = 0, Similarity = 0.999951, transactionId = 158290

Class = 0, Similarity = 0.999951, transactionId = 276481

Class = 0, Similarity = 0.999951, transactionId = 149100

-------------------------------------------------------------------------

For the transaction id = 24338, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999347, transactionId = 21934

Class = 0, Similarity = 0.999706, transactionId = 219257

Class = 0, Similarity = 0.999936, transactionId = 49906

Class = 0, Similarity = 0.999955, transactionId = 35730

Class = 1, Similarity = 0.999965, transactionId = 43428

Class = 0, Similarity = 0.999978, transactionId = 38442

Class = 0, Similarity = 0.999982, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 44942, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999345, transactionId = 21934

Class = 0, Similarity = 0.999705, transactionId = 219257

Class = 0, Similarity = 0.999936, transactionId = 49906

Class = 0, Similarity = 0.999955, transactionId = 35730

Class = 1, Similarity = 0.999964, transactionId = 43428

Class = 0, Similarity = 0.999977, transactionId = 38442

Class = 0, Similarity = 0.999982, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 80953, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999345, transactionId = 21934

Class = 0, Similarity = 0.999705, transactionId = 219257

Class = 0, Similarity = 0.999936, transactionId = 49906

Class = 0, Similarity = 0.999955, transactionId = 35730

Class = 1, Similarity = 0.999964, transactionId = 43428

Class = 0, Similarity = 0.999977, transactionId = 38442

Class = 0, Similarity = 0.999982, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 212975, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999361, transactionId = 21934

Class = 0, Similarity = 0.999715, transactionId = 219257

Class = 0, Similarity = 0.999941, transactionId = 49906

Class = 0, Similarity = 0.999959, transactionId = 35730

Class = 1, Similarity = 0.999968, transactionId = 43428

Class = 0, Similarity = 0.999980, transactionId = 38442

Class = 0, Similarity = 0.999985, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 209862, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999979, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 91821, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999330, transactionId = 21934

Class = 0, Similarity = 0.999695, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999974, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999992, transactionId = 80419

Class = 0, Similarity = 0.999992, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 208257, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999357, transactionId = 21934

Class = 0, Similarity = 0.999712, transactionId = 219257

Class = 0, Similarity = 0.999939, transactionId = 49906

Class = 0, Similarity = 0.999958, transactionId = 35730

Class = 1, Similarity = 0.999967, transactionId = 43428

Class = 0, Similarity = 0.999979, transactionId = 38442

Class = 0, Similarity = 0.999984, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999998, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 185213, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999338, transactionId = 21934

Class = 0, Similarity = 0.999700, transactionId = 219257

Class = 0, Similarity = 0.999934, transactionId = 49906

Class = 0, Similarity = 0.999953, transactionId = 35730

Class = 1, Similarity = 0.999963, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 265204, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999354, transactionId = 21934

Class = 0, Similarity = 0.999711, transactionId = 219257

Class = 0, Similarity = 0.999939, transactionId = 49906

Class = 0, Similarity = 0.999957, transactionId = 35730

Class = 1, Similarity = 0.999966, transactionId = 43428

Class = 0, Similarity = 0.999979, transactionId = 38442

Class = 0, Similarity = 0.999983, transactionId = 105030

Class = 0, Similarity = 0.999995, transactionId = 80419

Class = 0, Similarity = 0.999995, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 188412, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999340, transactionId = 21934

Class = 0, Similarity = 0.999701, transactionId = 219257

Class = 0, Similarity = 0.999934, transactionId = 49906

Class = 0, Similarity = 0.999953, transactionId = 35730

Class = 1, Similarity = 0.999963, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 11648, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999339, transactionId = 21934

Class = 0, Similarity = 0.999701, transactionId = 219257

Class = 0, Similarity = 0.999934, transactionId = 49906

Class = 0, Similarity = 0.999953, transactionId = 35730

Class = 1, Similarity = 0.999963, transactionId = 43428

Class = 0, Similarity = 0.999976, transactionId = 38442

Class = 0, Similarity = 0.999981, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 252178, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999332, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999931, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 162203, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999343, transactionId = 21934

Class = 0, Similarity = 0.999703, transactionId = 219257

Class = 0, Similarity = 0.999935, transactionId = 49906

Class = 0, Similarity = 0.999954, transactionId = 35730

Class = 1, Similarity = 0.999964, transactionId = 43428

Class = 0, Similarity = 0.999977, transactionId = 38442

Class = 0, Similarity = 0.999982, transactionId = 105030

Class = 0, Similarity = 0.999994, transactionId = 80419

Class = 0, Similarity = 0.999994, transactionId = 36749

Class = 0, Similarity = 0.999997, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 221033, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999332, transactionId = 21934

Class = 0, Similarity = 0.999696, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999951, transactionId = 35730

Class = 1, Similarity = 0.999961, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

For the transaction id = 147106, and Class = 0

Similar transactions are :

Class = 0, Similarity = 0.999334, transactionId = 21934

Class = 0, Similarity = 0.999697, transactionId = 219257

Class = 0, Similarity = 0.999932, transactionId = 49906

Class = 0, Similarity = 0.999952, transactionId = 35730

Class = 1, Similarity = 0.999962, transactionId = 43428

Class = 0, Similarity = 0.999975, transactionId = 38442

Class = 0, Similarity = 0.999980, transactionId = 105030

Class = 0, Similarity = 0.999993, transactionId = 80419

Class = 0, Similarity = 0.999993, transactionId = 36749

Class = 0, Similarity = 0.999996, transactionId = 187045

-------------------------------------------------------------------------

</pre>
</div>
</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
