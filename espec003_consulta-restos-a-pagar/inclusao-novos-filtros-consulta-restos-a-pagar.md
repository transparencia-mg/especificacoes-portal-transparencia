      <!DOCTYPE html>
      <html>
        <head>
            <meta charset="utf-8" />
            <title>inclusao-novos-filtros-consulta-restos-a-pagar</title>
            <style>.markdown-preview:not([data-use-github-style]) { padding: 2em; font-size: 1.2em; color: rgb(56, 58, 66); background-color: rgb(250, 250, 250); overflow: auto; }
.markdown-preview:not([data-use-github-style]) > :first-child { margin-top: 0px; }
.markdown-preview:not([data-use-github-style]) h1, .markdown-preview:not([data-use-github-style]) h2, .markdown-preview:not([data-use-github-style]) h3, .markdown-preview:not([data-use-github-style]) h4, .markdown-preview:not([data-use-github-style]) h5, .markdown-preview:not([data-use-github-style]) h6 { line-height: 1.2; margin-top: 1.5em; margin-bottom: 0.5em; color: rgb(0, 0, 0); }
.markdown-preview:not([data-use-github-style]) h1 { font-size: 2.4em; font-weight: 300; }
.markdown-preview:not([data-use-github-style]) h2 { font-size: 1.8em; font-weight: 400; }
.markdown-preview:not([data-use-github-style]) h3 { font-size: 1.5em; font-weight: 500; }
.markdown-preview:not([data-use-github-style]) h4 { font-size: 1.2em; font-weight: 600; }
.markdown-preview:not([data-use-github-style]) h5 { font-size: 1.1em; font-weight: 600; }
.markdown-preview:not([data-use-github-style]) h6 { font-size: 1em; font-weight: 600; }
.markdown-preview:not([data-use-github-style]) strong { color: rgb(0, 0, 0); }
.markdown-preview:not([data-use-github-style]) del { color: rgb(94, 97, 110); }
.markdown-preview:not([data-use-github-style]) a, .markdown-preview:not([data-use-github-style]) a code { color: rgb(82, 111, 255); }
.markdown-preview:not([data-use-github-style]) img { max-width: 100%; }
.markdown-preview:not([data-use-github-style]) > p { margin-top: 0px; margin-bottom: 1.5em; }
.markdown-preview:not([data-use-github-style]) > ul, .markdown-preview:not([data-use-github-style]) > ol { margin-bottom: 1.5em; }
.markdown-preview:not([data-use-github-style]) blockquote { margin: 1.5em 0px; font-size: inherit; color: rgb(94, 97, 110); border-color: rgb(209, 209, 210); border-width: 4px; }
.markdown-preview:not([data-use-github-style]) hr { margin: 3em 0px; border-top: 2px dashed rgb(209, 209, 210); background: none; }
.markdown-preview:not([data-use-github-style]) table { margin: 1.5em 0px; }
.markdown-preview:not([data-use-github-style]) th { color: rgb(0, 0, 0); }
.markdown-preview:not([data-use-github-style]) th, .markdown-preview:not([data-use-github-style]) td { padding: 0.66em 1em; border: 1px solid rgb(209, 209, 210); }
.markdown-preview:not([data-use-github-style]) code { color: rgb(0, 0, 0); background-color: rgb(234, 234, 235); }
.markdown-preview:not([data-use-github-style]) pre.editor-colors { margin: 1.5em 0px; padding: 1em; font-size: 0.92em; border-radius: 3px; background-color: rgb(240, 240, 240); }
.markdown-preview:not([data-use-github-style]) kbd { color: rgb(0, 0, 0); border-width: 1px 1px 2px; border-style: solid; border-color: rgb(209, 209, 210) rgb(209, 209, 210) rgb(193, 193, 194); border-image: initial; background-color: rgb(234, 234, 235); }
.markdown-preview[data-use-github-style] { font-family: "Helvetica Neue", Helvetica, "Segoe UI", Arial, freesans, sans-serif; line-height: 1.6; overflow-wrap: break-word; padding: 30px; font-size: 16px; color: rgb(51, 51, 51); background-color: rgb(255, 255, 255); overflow: scroll; }
.markdown-preview[data-use-github-style] > :first-child { margin-top: 0px !important; }
.markdown-preview[data-use-github-style] > :last-child { margin-bottom: 0px !important; }
.markdown-preview[data-use-github-style] a:not([href]) { color: inherit; text-decoration: none; }
.markdown-preview[data-use-github-style] .absent { color: rgb(204, 0, 0); }
.markdown-preview[data-use-github-style] .anchor { position: absolute; top: 0px; left: 0px; display: block; padding-right: 6px; padding-left: 30px; margin-left: -30px; }
.markdown-preview[data-use-github-style] .anchor:focus { outline: none; }
.markdown-preview[data-use-github-style] h1, .markdown-preview[data-use-github-style] h2, .markdown-preview[data-use-github-style] h3, .markdown-preview[data-use-github-style] h4, .markdown-preview[data-use-github-style] h5, .markdown-preview[data-use-github-style] h6 { position: relative; margin-top: 1em; margin-bottom: 16px; font-weight: bold; line-height: 1.4; }
.markdown-preview[data-use-github-style] h1 .octicon-link, .markdown-preview[data-use-github-style] h2 .octicon-link, .markdown-preview[data-use-github-style] h3 .octicon-link, .markdown-preview[data-use-github-style] h4 .octicon-link, .markdown-preview[data-use-github-style] h5 .octicon-link, .markdown-preview[data-use-github-style] h6 .octicon-link { display: none; color: rgb(0, 0, 0); vertical-align: middle; }
.markdown-preview[data-use-github-style] h1:hover .anchor, .markdown-preview[data-use-github-style] h2:hover .anchor, .markdown-preview[data-use-github-style] h3:hover .anchor, .markdown-preview[data-use-github-style] h4:hover .anchor, .markdown-preview[data-use-github-style] h5:hover .anchor, .markdown-preview[data-use-github-style] h6:hover .anchor { padding-left: 8px; margin-left: -30px; text-decoration: none; }
.markdown-preview[data-use-github-style] h1:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h2:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h3:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h4:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h5:hover .anchor .octicon-link, .markdown-preview[data-use-github-style] h6:hover .anchor .octicon-link { display: inline-block; }
.markdown-preview[data-use-github-style] h1 tt, .markdown-preview[data-use-github-style] h2 tt, .markdown-preview[data-use-github-style] h3 tt, .markdown-preview[data-use-github-style] h4 tt, .markdown-preview[data-use-github-style] h5 tt, .markdown-preview[data-use-github-style] h6 tt, .markdown-preview[data-use-github-style] h1 code, .markdown-preview[data-use-github-style] h2 code, .markdown-preview[data-use-github-style] h3 code, .markdown-preview[data-use-github-style] h4 code, .markdown-preview[data-use-github-style] h5 code, .markdown-preview[data-use-github-style] h6 code { font-size: inherit; }
.markdown-preview[data-use-github-style] h1 { padding-bottom: 0.3em; font-size: 2.25em; line-height: 1.2; border-bottom: 1px solid rgb(238, 238, 238); }
.markdown-preview[data-use-github-style] h1 .anchor { line-height: 1; }
.markdown-preview[data-use-github-style] h2 { padding-bottom: 0.3em; font-size: 1.75em; line-height: 1.225; border-bottom: 1px solid rgb(238, 238, 238); }
.markdown-preview[data-use-github-style] h2 .anchor { line-height: 1; }
.markdown-preview[data-use-github-style] h3 { font-size: 1.5em; line-height: 1.43; }
.markdown-preview[data-use-github-style] h3 .anchor { line-height: 1.2; }
.markdown-preview[data-use-github-style] h4 { font-size: 1.25em; }
.markdown-preview[data-use-github-style] h4 .anchor { line-height: 1.2; }
.markdown-preview[data-use-github-style] h5 { font-size: 1em; }
.markdown-preview[data-use-github-style] h5 .anchor { line-height: 1.1; }
.markdown-preview[data-use-github-style] h6 { font-size: 1em; color: rgb(119, 119, 119); }
.markdown-preview[data-use-github-style] h6 .anchor { line-height: 1.1; }
.markdown-preview[data-use-github-style] p, .markdown-preview[data-use-github-style] blockquote, .markdown-preview[data-use-github-style] ul, .markdown-preview[data-use-github-style] ol, .markdown-preview[data-use-github-style] dl, .markdown-preview[data-use-github-style] table, .markdown-preview[data-use-github-style] pre { margin-top: 0px; margin-bottom: 16px; }
.markdown-preview[data-use-github-style] hr { height: 4px; padding: 0px; margin: 16px 0px; background-color: rgb(231, 231, 231); border: 0px none; }
.markdown-preview[data-use-github-style] ul, .markdown-preview[data-use-github-style] ol { padding-left: 2em; }
.markdown-preview[data-use-github-style] ul.no-list, .markdown-preview[data-use-github-style] ol.no-list { padding: 0px; list-style-type: none; }
.markdown-preview[data-use-github-style] ul ul, .markdown-preview[data-use-github-style] ul ol, .markdown-preview[data-use-github-style] ol ol, .markdown-preview[data-use-github-style] ol ul { margin-top: 0px; margin-bottom: 0px; }
.markdown-preview[data-use-github-style] li > p { margin-top: 16px; }
.markdown-preview[data-use-github-style] dl { padding: 0px; }
.markdown-preview[data-use-github-style] dl dt { padding: 0px; margin-top: 16px; font-size: 1em; font-style: italic; font-weight: bold; }
.markdown-preview[data-use-github-style] dl dd { padding: 0px 16px; margin-bottom: 16px; }
.markdown-preview[data-use-github-style] blockquote { padding: 0px 15px; color: rgb(119, 119, 119); border-left: 4px solid rgb(221, 221, 221); }
.markdown-preview[data-use-github-style] blockquote > :first-child { margin-top: 0px; }
.markdown-preview[data-use-github-style] blockquote > :last-child { margin-bottom: 0px; }
.markdown-preview[data-use-github-style] table { display: block; width: 100%; overflow: auto; word-break: keep-all; }
.markdown-preview[data-use-github-style] table th { font-weight: bold; }
.markdown-preview[data-use-github-style] table th, .markdown-preview[data-use-github-style] table td { padding: 6px 13px; border: 1px solid rgb(221, 221, 221); }
.markdown-preview[data-use-github-style] table tr { background-color: rgb(255, 255, 255); border-top: 1px solid rgb(204, 204, 204); }
.markdown-preview[data-use-github-style] table tr:nth-child(2n) { background-color: rgb(248, 248, 248); }
.markdown-preview[data-use-github-style] img { max-width: 100%; box-sizing: border-box; }
.markdown-preview[data-use-github-style] .emoji { max-width: none; }
.markdown-preview[data-use-github-style] span.frame { display: block; overflow: hidden; }
.markdown-preview[data-use-github-style] span.frame > span { display: block; float: left; width: auto; padding: 7px; margin: 13px 0px 0px; overflow: hidden; border: 1px solid rgb(221, 221, 221); }
.markdown-preview[data-use-github-style] span.frame span img { display: block; float: left; }
.markdown-preview[data-use-github-style] span.frame span span { display: block; padding: 5px 0px 0px; clear: both; color: rgb(51, 51, 51); }
.markdown-preview[data-use-github-style] span.align-center { display: block; overflow: hidden; clear: both; }
.markdown-preview[data-use-github-style] span.align-center > span { display: block; margin: 13px auto 0px; overflow: hidden; text-align: center; }
.markdown-preview[data-use-github-style] span.align-center span img { margin: 0px auto; text-align: center; }
.markdown-preview[data-use-github-style] span.align-right { display: block; overflow: hidden; clear: both; }
.markdown-preview[data-use-github-style] span.align-right > span { display: block; margin: 13px 0px 0px; overflow: hidden; text-align: right; }
.markdown-preview[data-use-github-style] span.align-right span img { margin: 0px; text-align: right; }
.markdown-preview[data-use-github-style] span.float-left { display: block; float: left; margin-right: 13px; overflow: hidden; }
.markdown-preview[data-use-github-style] span.float-left span { margin: 13px 0px 0px; }
.markdown-preview[data-use-github-style] span.float-right { display: block; float: right; margin-left: 13px; overflow: hidden; }
.markdown-preview[data-use-github-style] span.float-right > span { display: block; margin: 13px auto 0px; overflow: hidden; text-align: right; }
.markdown-preview[data-use-github-style] code, .markdown-preview[data-use-github-style] tt { padding: 0.2em 0px; margin: 0px; font-size: 85%; background-color: rgba(0, 0, 0, 0.04); border-radius: 3px; }
.markdown-preview[data-use-github-style] code::before, .markdown-preview[data-use-github-style] tt::before, .markdown-preview[data-use-github-style] code::after, .markdown-preview[data-use-github-style] tt::after { letter-spacing: -0.2em; content: " "; }
.markdown-preview[data-use-github-style] code br, .markdown-preview[data-use-github-style] tt br { display: none; }
.markdown-preview[data-use-github-style] del code { text-decoration: inherit; }
.markdown-preview[data-use-github-style] pre > code { padding: 0px; margin: 0px; font-size: 100%; word-break: normal; white-space: pre; background: transparent; border: 0px; }
.markdown-preview[data-use-github-style] .highlight { margin-bottom: 16px; }
.markdown-preview[data-use-github-style] .highlight pre, .markdown-preview[data-use-github-style] pre { padding: 16px; overflow: auto; font-size: 85%; line-height: 1.45; background-color: rgb(247, 247, 247); border-radius: 3px; }
.markdown-preview[data-use-github-style] .highlight pre { margin-bottom: 0px; word-break: normal; }
.markdown-preview[data-use-github-style] pre { overflow-wrap: normal; }
.markdown-preview[data-use-github-style] pre code, .markdown-preview[data-use-github-style] pre tt { display: inline; max-width: initial; padding: 0px; margin: 0px; overflow: initial; line-height: inherit; overflow-wrap: normal; background-color: transparent; border: 0px; }
.markdown-preview[data-use-github-style] pre code::before, .markdown-preview[data-use-github-style] pre tt::before, .markdown-preview[data-use-github-style] pre code::after, .markdown-preview[data-use-github-style] pre tt::after { content: normal; }
.markdown-preview[data-use-github-style] kbd { display: inline-block; padding: 3px 5px; font-size: 11px; line-height: 10px; color: rgb(85, 85, 85); vertical-align: middle; background-color: rgb(252, 252, 252); border-width: 1px; border-style: solid; border-color: rgb(204, 204, 204) rgb(204, 204, 204) rgb(187, 187, 187); border-image: initial; border-radius: 3px; box-shadow: rgb(187, 187, 187) 0px -1px 0px inset; }
.markdown-preview[data-use-github-style] a { color: rgb(51, 122, 183); }
.markdown-preview[data-use-github-style] code { color: inherit; }
.markdown-preview[data-use-github-style] pre.editor-colors { padding: 0.8em 1em; margin-bottom: 1em; font-size: 0.85em; border-radius: 4px; overflow: auto; }
.markdown-preview pre.editor-colors { user-select: auto; }
.scrollbars-visible-always .markdown-preview pre.editor-colors .vertical-scrollbar, .scrollbars-visible-always .markdown-preview pre.editor-colors .horizontal-scrollbar { visibility: hidden; }
.scrollbars-visible-always .markdown-preview pre.editor-colors:hover .vertical-scrollbar, .scrollbars-visible-always .markdown-preview pre.editor-colors:hover .horizontal-scrollbar { visibility: visible; }
.markdown-preview .task-list-item input[type="checkbox"] { position: absolute; margin: 0.25em 0px 0px -1.4em; }
.markdown-preview .task-list-item { list-style-type: none; }
.bracket-matcher .region {
  border-bottom: 1px dotted lime;
  position: absolute;
}
.line-number.bracket-matcher.bracket-matcher {
  color: #383a42;
  background-color: #e5e5e6;
}

.spell-check-misspelling .region {
  border-bottom: 2px dotted rgba(255, 51, 51, 0.75);
}
.spell-check-corrections {
  width: 25em !important;
}

pre.editor-colors {
  background-color: #fafafa;
  color: #383a42;
}
pre.editor-colors .line.cursor-line {
  background-color: rgba(56, 58, 66, 0.05);
}
pre.editor-colors .invisible {
  color: #383a42;
}
pre.editor-colors .cursor {
  border-left: 2px solid #526fff;
}
pre.editor-colors .selection .region {
  background-color: #e5e5e6;
}
pre.editor-colors .bracket-matcher .region {
  border-bottom: 1px solid #526fff;
  box-sizing: border-box;
}
pre.editor-colors .invisible-character {
  color: rgba(56, 58, 66, 0.2);
}
pre.editor-colors .indent-guide {
  color: rgba(56, 58, 66, 0.2);
}
pre.editor-colors .wrap-guide {
  background-color: rgba(56, 58, 66, 0.2);
}
pre.editor-colors .find-result .region.region.region,
pre.editor-colors .current-result .region.region.region {
  border-radius: 2px;
  background-color: rgba(82, 111, 255, 0.2);
  transition: border-color 0.4s;
}
pre.editor-colors .find-result .region.region.region {
  border: 2px solid transparent;
}
pre.editor-colors .current-result .region.region.region {
  border: 2px solid #526fff;
  transition-duration: .1s;
}
pre.editor-colors .gutter .line-number {
  color: #9d9d9f;
  -webkit-font-smoothing: antialiased;
}
pre.editor-colors .gutter .line-number.cursor-line {
  color: #383a42;
  background-color: #e5e5e6;
}
pre.editor-colors .gutter .line-number.cursor-line-no-selection {
  background-color: transparent;
}
pre.editor-colors .gutter .line-number .icon-right {
  color: #383a42;
}
pre.editor-colors .gutter:not(.git-diff-icon) .line-number.git-line-removed.git-line-removed::before {
  bottom: -3px;
}
pre.editor-colors .gutter:not(.git-diff-icon) .line-number.git-line-removed::after {
  content: "";
  position: absolute;
  left: 0px;
  bottom: 0px;
  width: 25px;
  border-bottom: 1px dotted rgba(255, 20, 20, 0.5);
  pointer-events: none;
}
pre.editor-colors .gutter .line-number.folded,
pre.editor-colors .gutter .line-number:after,
pre.editor-colors .fold-marker:after {
  color: #383a42;
}
.syntax--comment {
  color: #a0a1a7;
  font-style: italic;
}
.syntax--comment .syntax--markup.syntax--link {
  color: #a0a1a7;
}
.syntax--entity.syntax--name.syntax--type {
  color: #c18401;
}
.syntax--entity.syntax--other.syntax--inherited-class {
  color: #c18401;
}
.syntax--keyword {
  color: #a626a4;
}
.syntax--keyword.syntax--control {
  color: #a626a4;
}
.syntax--keyword.syntax--operator {
  color: #383a42;
}
.syntax--keyword.syntax--other.syntax--special-method {
  color: #4078f2;
}
.syntax--keyword.syntax--other.syntax--unit {
  color: #986801;
}
.syntax--storage {
  color: #a626a4;
}
.syntax--storage.syntax--type.syntax--annotation,
.syntax--storage.syntax--type.syntax--primitive {
  color: #a626a4;
}
.syntax--storage.syntax--modifier.syntax--package,
.syntax--storage.syntax--modifier.syntax--import {
  color: #383a42;
}
.syntax--constant {
  color: #986801;
}
.syntax--constant.syntax--variable {
  color: #986801;
}
.syntax--constant.syntax--character.syntax--escape {
  color: #0184bc;
}
.syntax--constant.syntax--numeric {
  color: #986801;
}
.syntax--constant.syntax--other.syntax--color {
  color: #0184bc;
}
.syntax--constant.syntax--other.syntax--symbol {
  color: #0184bc;
}
.syntax--variable {
  color: #e45649;
}
.syntax--variable.syntax--interpolation {
  color: #ca1243;
}
.syntax--variable.syntax--parameter {
  color: #383a42;
}
.syntax--string {
  color: #50a14f;
}
.syntax--string > .syntax--source,
.syntax--string .syntax--embedded {
  color: #383a42;
}
.syntax--string.syntax--regexp {
  color: #0184bc;
}
.syntax--string.syntax--regexp .syntax--source.syntax--ruby.syntax--embedded {
  color: #c18401;
}
.syntax--string.syntax--other.syntax--link {
  color: #e45649;
}
.syntax--punctuation.syntax--definition.syntax--comment {
  color: #a0a1a7;
}
.syntax--punctuation.syntax--definition.syntax--method-parameters,
.syntax--punctuation.syntax--definition.syntax--function-parameters,
.syntax--punctuation.syntax--definition.syntax--parameters,
.syntax--punctuation.syntax--definition.syntax--separator,
.syntax--punctuation.syntax--definition.syntax--seperator,
.syntax--punctuation.syntax--definition.syntax--array {
  color: #383a42;
}
.syntax--punctuation.syntax--definition.syntax--heading,
.syntax--punctuation.syntax--definition.syntax--identity {
  color: #4078f2;
}
.syntax--punctuation.syntax--definition.syntax--bold {
  color: #c18401;
  font-weight: bold;
}
.syntax--punctuation.syntax--definition.syntax--italic {
  color: #a626a4;
  font-style: italic;
}
.syntax--punctuation.syntax--section.syntax--embedded {
  color: #ca1243;
}
.syntax--punctuation.syntax--section.syntax--method,
.syntax--punctuation.syntax--section.syntax--class,
.syntax--punctuation.syntax--section.syntax--inner-class {
  color: #383a42;
}
.syntax--support.syntax--class {
  color: #c18401;
}
.syntax--support.syntax--type {
  color: #0184bc;
}
.syntax--support.syntax--function {
  color: #0184bc;
}
.syntax--support.syntax--function.syntax--any-method {
  color: #4078f2;
}
.syntax--entity.syntax--name.syntax--function {
  color: #4078f2;
}
.syntax--entity.syntax--name.syntax--class,
.syntax--entity.syntax--name.syntax--type.syntax--class {
  color: #c18401;
}
.syntax--entity.syntax--name.syntax--section {
  color: #4078f2;
}
.syntax--entity.syntax--name.syntax--tag {
  color: #e45649;
}
.syntax--entity.syntax--other.syntax--attribute-name {
  color: #986801;
}
.syntax--entity.syntax--other.syntax--attribute-name.syntax--id {
  color: #4078f2;
}
.syntax--meta.syntax--class {
  color: #c18401;
}
.syntax--meta.syntax--class.syntax--body {
  color: #383a42;
}
.syntax--meta.syntax--method-call,
.syntax--meta.syntax--method {
  color: #383a42;
}
.syntax--meta.syntax--definition.syntax--variable {
  color: #e45649;
}
.syntax--meta.syntax--link {
  color: #986801;
}
.syntax--meta.syntax--require {
  color: #4078f2;
}
.syntax--meta.syntax--selector {
  color: #a626a4;
}
.syntax--meta.syntax--separator {
  color: #383a42;
}
.syntax--meta.syntax--tag {
  color: #383a42;
}
.syntax--underline {
  text-decoration: underline;
}
.syntax--none {
  color: #383a42;
}
.syntax--invalid.syntax--deprecated {
  color: #000000 !important;
  background-color: #f2a60d !important;
}
.syntax--invalid.syntax--illegal {
  color: white !important;
  background-color: #ff1414 !important;
}
.syntax--markup.syntax--bold {
  color: #986801;
  font-weight: bold;
}
.syntax--markup.syntax--changed {
  color: #a626a4;
}
.syntax--markup.syntax--deleted {
  color: #e45649;
}
.syntax--markup.syntax--italic {
  color: #a626a4;
  font-style: italic;
}
.syntax--markup.syntax--heading {
  color: #e45649;
}
.syntax--markup.syntax--heading .syntax--punctuation.syntax--definition.syntax--heading {
  color: #4078f2;
}
.syntax--markup.syntax--link {
  color: #0184bc;
}
.syntax--markup.syntax--inserted {
  color: #50a14f;
}
.syntax--markup.syntax--quote {
  color: #986801;
}
.syntax--markup.syntax--raw {
  color: #50a14f;
}
.syntax--source.syntax--c .syntax--keyword.syntax--operator {
  color: #a626a4;
}
.syntax--source.syntax--cpp .syntax--keyword.syntax--operator {
  color: #a626a4;
}
.syntax--source.syntax--cs .syntax--keyword.syntax--operator {
  color: #a626a4;
}
.syntax--source.syntax--css .syntax--property-name,
.syntax--source.syntax--css .syntax--property-value {
  color: #696c77;
}
.syntax--source.syntax--css .syntax--property-name.syntax--support,
.syntax--source.syntax--css .syntax--property-value.syntax--support {
  color: #383a42;
}
.syntax--source.syntax--elixir .syntax--source.syntax--embedded.syntax--source {
  color: #383a42;
}
.syntax--source.syntax--elixir .syntax--constant.syntax--language,
.syntax--source.syntax--elixir .syntax--constant.syntax--numeric,
.syntax--source.syntax--elixir .syntax--constant.syntax--definition {
  color: #4078f2;
}
.syntax--source.syntax--elixir .syntax--variable.syntax--definition,
.syntax--source.syntax--elixir .syntax--variable.syntax--anonymous {
  color: #a626a4;
}
.syntax--source.syntax--elixir .syntax--parameter.syntax--variable.syntax--function {
  color: #986801;
  font-style: italic;
}
.syntax--source.syntax--elixir .syntax--quoted {
  color: #50a14f;
}
.syntax--source.syntax--elixir .syntax--keyword.syntax--special-method,
.syntax--source.syntax--elixir .syntax--embedded.syntax--section,
.syntax--source.syntax--elixir .syntax--embedded.syntax--source.syntax--empty {
  color: #e45649;
}
.syntax--source.syntax--elixir .syntax--readwrite.syntax--module .syntax--punctuation {
  color: #e45649;
}
.syntax--source.syntax--elixir .syntax--regexp.syntax--section,
.syntax--source.syntax--elixir .syntax--regexp.syntax--string {
  color: #ca1243;
}
.syntax--source.syntax--elixir .syntax--separator,
.syntax--source.syntax--elixir .syntax--keyword.syntax--operator {
  color: #986801;
}
.syntax--source.syntax--elixir .syntax--variable.syntax--constant {
  color: #c18401;
}
.syntax--source.syntax--elixir .syntax--array,
.syntax--source.syntax--elixir .syntax--scope,
.syntax--source.syntax--elixir .syntax--section {
  color: #696c77;
}
.syntax--source.syntax--gfm .syntax--markup {
  -webkit-font-smoothing: auto;
}
.syntax--source.syntax--gfm .syntax--link .syntax--entity {
  color: #4078f2;
}
.syntax--source.syntax--go .syntax--storage.syntax--type.syntax--string {
  color: #a626a4;
}
.syntax--source.syntax--ini .syntax--keyword.syntax--other.syntax--definition.syntax--ini {
  color: #e45649;
}
.syntax--source.syntax--java .syntax--storage.syntax--modifier.syntax--import {
  color: #c18401;
}
.syntax--source.syntax--java .syntax--storage.syntax--type {
  color: #c18401;
}
.syntax--source.syntax--java .syntax--keyword.syntax--operator.syntax--instanceof {
  color: #a626a4;
}
.syntax--source.syntax--java-properties .syntax--meta.syntax--key-pair {
  color: #e45649;
}
.syntax--source.syntax--java-properties .syntax--meta.syntax--key-pair > .syntax--punctuation {
  color: #383a42;
}
.syntax--source.syntax--js .syntax--keyword.syntax--operator {
  color: #0184bc;
}
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--delete,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--in,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--of,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--instanceof,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--new,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--typeof,
.syntax--source.syntax--js .syntax--keyword.syntax--operator.syntax--void {
  color: #a626a4;
}
.syntax--source.syntax--ts .syntax--keyword.syntax--operator {
  color: #0184bc;
}
.syntax--source.syntax--flow .syntax--keyword.syntax--operator {
  color: #0184bc;
}
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--string.syntax--quoted.syntax--json {
  color: #e45649;
}
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--string.syntax--quoted.syntax--json > .syntax--punctuation.syntax--string {
  color: #e45649;
}
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--value.syntax--json > .syntax--string.syntax--quoted.syntax--json,
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--array.syntax--json > .syntax--value.syntax--json > .syntax--string.syntax--quoted.syntax--json,
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--value.syntax--json > .syntax--string.syntax--quoted.syntax--json > .syntax--punctuation,
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--array.syntax--json > .syntax--value.syntax--json > .syntax--string.syntax--quoted.syntax--json > .syntax--punctuation {
  color: #50a14f;
}
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--dictionary.syntax--json > .syntax--constant.syntax--language.syntax--json,
.syntax--source.syntax--json .syntax--meta.syntax--structure.syntax--array.syntax--json > .syntax--constant.syntax--language.syntax--json {
  color: #0184bc;
}
.syntax--ng.syntax--interpolation {
  color: #e45649;
}
.syntax--ng.syntax--interpolation.syntax--begin,
.syntax--ng.syntax--interpolation.syntax--end {
  color: #4078f2;
}
.syntax--ng.syntax--interpolation .syntax--function {
  color: #e45649;
}
.syntax--ng.syntax--interpolation .syntax--function.syntax--begin,
.syntax--ng.syntax--interpolation .syntax--function.syntax--end {
  color: #4078f2;
}
.syntax--ng.syntax--interpolation .syntax--bool {
  color: #986801;
}
.syntax--ng.syntax--interpolation .syntax--bracket {
  color: #383a42;
}
.syntax--ng.syntax--pipe,
.syntax--ng.syntax--operator {
  color: #383a42;
}
.syntax--ng.syntax--tag {
  color: #0184bc;
}
.syntax--ng.syntax--attribute-with-value .syntax--attribute-name {
  color: #c18401;
}
.syntax--ng.syntax--attribute-with-value .syntax--string {
  color: #a626a4;
}
.syntax--ng.syntax--attribute-with-value .syntax--string.syntax--begin,
.syntax--ng.syntax--attribute-with-value .syntax--string.syntax--end {
  color: #383a42;
}
.syntax--source.syntax--ruby .syntax--constant.syntax--other.syntax--symbol > .syntax--punctuation {
  color: inherit;
}
.syntax--source.syntax--php .syntax--class.syntax--bracket {
  color: #383a42;
}
.syntax--source.syntax--python .syntax--keyword.syntax--operator.syntax--logical.syntax--python {
  color: #a626a4;
}
.syntax--source.syntax--python .syntax--variable.syntax--parameter {
  color: #986801;
}
</style>
        </head>
        <body class='markdown-preview' data-use-github-style><hr>
<p>titulo: "Nova especificação da Consulta Restos a pagar"
pull_request:<a href="https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/3">https://github.com/transparencia-mg/especificacoes-portal-transparencia/pull/3</a></p>
<h1 id="visão-geral-da-demanda">Visão geral da demanda</h1>
<p>Essa demanda visa acrescentar modos de pesquisa adicionais a <a href="http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar">consulta de Restos a Pagar</a>, nos moldes da <a href="http://www.transparencia.mg.gov.br/despesa-estado/despesa">consulta de Despesa</a>. Devem ser acrescentados os modos de pesquisa:</p>
<ol>
<li>Filtro favorecido por nome;</li>
<li>Filtro favorecido por CPF/CNPJ;</li>
<li>Pesquisa Avançada.</li>
</ol>
<p>Os filtros dos três modos de pesquisa devem possuir funcionalidade de autocompletar (eg. <a href="http://www.transparencia.mg.gov.br/compras-e-patrimonio/compras-e-contratos">consulta compras</a>) com possibilidade de seleção múltipla. O escopo das sugestões deve se restringir aos valores existentes no ano corrente, indicando caso nenhuma correspondência for encontrada.</p>
<h3 id="observações-gerais"><em>Observações gerais:</em></h3>
<ul>
<li><p><strong>Filtro favorecido por CPF/CNPJ</strong>: O filtro por CPF/CNPJ deve realizar autocomplete e buscar com CPFs/CNPJs formatados ou númericos.</p>
</li>
<li><p><strong>Pesquisa Avançada</strong>: A pesquisa avançada deve possuir um botão de marcar/desmarcar todas as colunas. Além disso, o autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias (eg. <a href="http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada">consulta proposta orçamentária</a>)</p>
</li>
</ul>
<h1 id="motivação--contexto-da-demanda">Motivação / contexto da demanda</h1>
<p>As consultas do Portal de Transparência possuem como padrão a possibilidade de pesquisa por meio de filtros (eg. <a href="http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-favorecidos/2019/01-01-2019/31-12-2019/0/LUCIANA%20CASSIA%20NOGUEIRA/0/3"><em>Filtro Favorecido - Consulta Despesas</em></a>) e pesquisa avançada (eg. <a href="http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-pesquisa-avancada"><em>Pesquisa Avançada - Consulta Despesa</em></a>). No entanto, na reestruturação do Portal de Transparência, ocorrida entre 2015 e 2017, a consulta de Restos a Pagar não foi contemplada com essa possibilidade, sendo disponibilizada apenas com o filtro de <a href="http://www.transparencia.mg.gov.br/despesa-estado/restos-a-pagar">pesquisa Órgão</a>.</p>
<p>Atualmente, a Diretoria Central de Transparência Ativa têm recebidos diversos questionamentos por do telefone do Portal quanto a não possibilidade de outras formas de pesquisa na consulta de Restos a Pagar. Nesse sentido, com o objetivo de ofertar mais opções aos usuários essa nova especificação visa acrescentar os filtros de favorecidos por nome e CPF/CNPJ e pesquisa avançada nos moldes da consulta de despesa.</p>
<p>A decisão de acrescentar apenas os filtros mencionados acima se deve ao levantamento realizado no google analytics considerando como parâmetro os filtros da consulta de despesa.</p>
<p>Conforme tabela abaixo os filtros por Programa e função são poucos utilizados.</p>
<table>
<thead>
<tr>
<th>Filtros Consulta Despesa</th>
<th align="right">Acessos</th>
<th align="right">%</th>
</tr>
</thead>
<tbody><tr>
<td>Órgãos</td>
<td align="right">132.412</td>
<td align="right">86,40%</td>
</tr>
<tr>
<td>Programa</td>
<td align="right">429</td>
<td align="right">0,28%</td>
</tr>
<tr>
<td>Função</td>
<td align="right">4.179</td>
<td align="right">2,73%</td>
</tr>
<tr>
<td>Favorecido</td>
<td align="right">16.235</td>
<td align="right">10,59%</td>
</tr>
<tr>
<td><strong><em>Total de sessões</em></strong></td>
<td align="right"><strong><em>153.255</em></strong></td>
<td align="right"></td>
</tr>
</tbody></table>
<p>  <strong>Fonte</strong>: Google Analytics -período jan/2019 a 23/out/2019</p>
<h1 id="especificação">Especificação</h1>
<h2 id="página-inicial">Página Inicial</h2>
<p>Para contemplar a inclusão dos novos filtros a página inicial deverá sofrer alterações conforme abaixo:</p>
<p> O cidadão seleciona a opção Restos a pagar e o Portal exibirá:</p>
<ul>
<li><p><strong>Ano da consulta (aaaa)</strong>: Conforme padrão adotado atualmente.</p>
</li>
<li><p><strong>Consulta</strong>: Órgão, Favorecido por nome, Favorecido por CPF/CNPJ.</p>
</li>
<li><p><strong>Filtro:</strong> Exibir filtro para selecionar uma opção.</p>
</li>
<li><p><strong>Data Ínicio e Fim</strong>: Conforme padrão adotado atualmente</p>
</li>
<li><p><strong>Pesquisar</strong>: Conforme padrão adotado atualmente</p>
</li>
<li><p><strong>Pesquisa Avançada</strong>:</p>
</li>
</ul>
<p>Exemplo:
<img alt="Pagina Inicial" src="C:\Users\m13368964\Documents\Documents\CGE\Projetos-Transparencia-Ativa\especificacoes-portal-transparencia\espec003_consulta-restos-a-pagar\static\pagina-inicial.png"></p>
<table>
<thead>
<tr>
<th>Ano</th>
<th align="left">Consulta</th>
<th>Filtro</th>
<th>Início</th>
<th>Fim</th>
<th>Pesquisa</th>
<th>Pesquisa Avançada</th>
</tr>
</thead>
<tbody><tr>
<td></td>
<td align="left">Órgão (Consulta Principal)</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td align="left">Favorecido nome</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td align="left">Favorecido por CPF/CNPJ</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody></table>
<h3 id="observações-gerais-1">Observações Gerais</h3>
<ul>
<li><p>O filtro favorecido por Nome deve ter a opção de autocomplete;</p>
</li>
<li><p>O filtro favorecido por Nome deve permitir que o cidadão digite qualquer parte do nome e o portal retornará todos os itens que encaixem na pesquisa;</p>
</li>
<li><p>O filtro favorecido por CPF/CNPJ deve realizar a busca com CPFs/CNPJs formatados ou númericos.</p>
</li>
<li><p>A Pesquisa Avançada deve possuir um botão de marcar/desmarcar todas as colunas. Além disso, o autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias (<a href="http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada">eg. consulta proposta orçamentária</a>);</p>
</li>
<li><p>Todas as páginas da consulta devem exibir ícones com links para compartilhar consultas no facebook e twitter e a possibilidade de fazer download da planilha completa em csv, exportar para pdf e imprimir conforme padrão já adotado em outras consultas do Portal;</p>
</li>
<li><p>Todas as páginas devem exibir cabeçalho e legenda da tabela e “migalhas” conforme padrão;</p>
</li>
<li><p>Todos os gráficos da consulta irão buscar a o valor pago no ano e apresentar legenda conforme o já adotado em outras consultas.</p>
</li>
<li><p>Em todos os níveis o cidadão poderá avançar para os próximos níveis tanto clicando no gráfico quanto na tabela.</p>
</li>
</ul>
<h2 id="consulta-favorecido-por-nome">Consulta Favorecido por nome</h2>
<p><strong><em>1º nível (Favorecido)</em></strong></p>
<p>O portal deve exibir a opção de escolher tipo da consulta e ao selecionar o tipo <em>[Favorecido por nome]</em>, permiti que o cidadão escreva o nome completo ou parte do nome do favorecido. O Portal retorna todos os resultados que se encaixem no termo informado do filtro.</p>
<p>O Portal da Transparência irá listar o resultado da consulta em um gráfico treemap e em tabela.</p>
<p>&lt;&lt;Título do gráfico: Favorecidos&gt;&gt;</p>
<p><img alt="modelo-grafico-treemap" src="C:\Users\m13368964\Documents\Documents\CGE\Projetos-Transparencia-Ativa\especificacoes-portal-transparencia\espec003_consulta-restos-a-pagar\static\modelo-grafico-treemap.png"></p>
<table>
<thead>
<tr>
<th>Favorecido</th>
<th>CNPJ/CPF</th>
<th>Valor inscrito processado</th>
<th>Valor não inscrito processado</th>
<th>Valor pago no ano</th>
<th>Valor a pagar</th>
</tr>
</thead>
<tbody><tr>
<td><em>Link para o próximo nível</em></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody></table>
<p><strong>2º nível (Elemento de Despesa)</strong></p>
<p>Ao clicar no nome do <em>[Favorecido]</em> o Portal exibirá um gráfico treemap e uma tabela.</p>
<p>&lt;&lt;Título do gráfico: Nome do favorecido selecionado no nível anterior&gt;&gt;
<img alt="modelo-grafico-treemap" src="C:\Users\m13368964\Documents\Documents\CGE\Projetos-Transparencia-Ativa\especificacoes-portal-transparencia\espec003_consulta-restos-a-pagar\static\modelo-grafico-treemap.png"></p>
<table>
<thead>
<tr>
<th>Categoria Econômica</th>
<th>Grupo de Despesa</th>
<th>Elemento de Despesa</th>
<th>Valor inscrito processado</th>
<th>Valor não inscrito processado</th>
<th>Valor pago no ano</th>
<th>Valor a pagar</th>
</tr>
</thead>
<tbody><tr>
<td></td>
<td></td>
<td><em>Link para o próximo nível</em></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody></table>
<p><strong>3º nível (Item de despesa)</strong></p>
<p>Ao clicar no <em>[Elemento de despesa]</em> o Portal exibirá um gráfico treemap e uma tabela.</p>
<p>&lt;&lt;Título do gráfico: Nome do elemento de despesa selecionado no nível anterior&gt;&gt;
<img alt="modelo-grafico-treemap" src="C:\Users\m13368964\Documents\Documents\CGE\Projetos-Transparencia-Ativa\especificacoes-portal-transparencia\espec003_consulta-restos-a-pagar\static\modelo-grafico-treemap.png"></p>
<table>
<thead>
<tr>
<th>Fonte de Recursos</th>
<th>Modalidade de Aplicação</th>
<th>Item de Despesa</th>
<th>Valor inscrito processado</th>
<th>Valor não inscrito processado</th>
<th>Valor pago no ano</th>
<th>Valor a pagar</th>
</tr>
</thead>
<tbody><tr>
<td></td>
<td></td>
<td><em>Link para o próximo nível</em></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody></table>
<p><strong>4º nível (Órgão)</strong></p>
<p>Ao clicar em <em>[Item de despesa]</em> o Portal exibirá um gráfico treemap e uma tabela.</p>
<p>&lt;&lt;Título do gráfico: Nome do item de despesa selecionado no nível anterior&gt;&gt;
<img alt="modelo-grafico-treemap" src="C:\Users\m13368964\Documents\Documents\CGE\Projetos-Transparencia-Ativa\especificacoes-portal-transparencia\espec003_consulta-restos-a-pagar\static\modelo-grafico-treemap.png"></p>
<table>
<thead>
<tr>
<th>Código</th>
<th>Órgão</th>
<th>Valor inscrito processado</th>
<th>Valor não inscrito processado</th>
<th>Valor pago no ano</th>
<th>Valor a pagar</th>
</tr>
</thead>
<tbody><tr>
<td></td>
<td><em>Link para o próximo nível</em></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody></table>
<p><strong>5º nível (Número de Empenho)</strong></p>
<p>Ao clicar em <em>[órgão]</em> o Portal exibirá e uma tabela.</p>
<table>
<thead>
<tr>
<th>Data</th>
<th>Número do Empenho</th>
<th>Valor inscrito processado</th>
<th>Valor não inscrito processado</th>
<th>Valor pago no ano</th>
<th>Valor a pagar</th>
</tr>
</thead>
<tbody><tr>
<td></td>
<td><em>Link para o próximo nível</em></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody></table>
<p><strong><em>OBS: A data deverá ser a data de registro inicial do empenho</em></strong></p>
<p><strong>6º nível (Formulário de detalhamento)</strong></p>
<p>Ao clicar no <em>[número do empenho]</em> o Portal exibirá o Formulário de detalhamento igual ao utilizado atualmente na consulta por órgão.</p>
<p><img alt="Formulário de detalhamento" src="C:\Users\m13368964\Documents\Documents\CGE\Projetos-Transparencia-Ativa\especificacoes-portal-transparencia\espec003_consulta-restos-a-pagar\static\formulario-detalhamento.png"></p>
<h2 id="consulta-favorecido-por-cpfcnpj">Consulta Favorecido por CPF/CNPJ</h2>
<p><strong><em>1º nível (Favorecido)</em></strong></p>
<p>O portal deve exibir a opção de escolher tipo da consulta e ao selecionar o tipo <em>[Favorecido por CPF/CNPJ]</em>, permiti que o cidadão escreva o número do CPF/CNPJ formatados ou númericos. O Portal retorna todos os resultados que se encaixem no termo informado do filtro.</p>
<p><strong>2º nível (Elemento de Despesa)</strong></p>
<p>Mesma regra do nível favorecido por nome</p>
<p><strong>3º nível (Item de despesa)</strong></p>
<p>Mesma regra do nível favorecido por nome</p>
<p><strong>4º nível (Órgão)</strong></p>
<p>Mesma regra do nível favorecido por nome</p>
<p><strong>5º nível (Número de Empenho)</strong></p>
<p>Mesma regra do nível favorecido por nome</p>
<p><strong>6º nível (Formulário de detalhamento)</strong></p>
<p>Mesma regra do nível favorecido por nome</p>
<h2 id="consulta-avançada">Consulta Avançada</h2>
<p>A consulta avançada terá 12 campos de filtro e parâmetro de ano:</p>
<ol>
<li>Órgão</li>
<li>Função</li>
<li>Subfunção</li>
<li>Programas</li>
<li>ação</li>
<li>Categoria Econômica</li>
<li>Grupo de Despesa</li>
<li>Modalidade de Aplicação</li>
<li>Elemento de despesa</li>
<li>Item de Despesa</li>
<li>Fonte de Recursos</li>
<li>Identificador de Procedência e Uso (IPU)</li>
</ol>
<p>O usuário poderá escolher em exibir ou não a lista dos favorecidos. Como padrão o portal não exibirá os favorecidos.</p>
<p>Favorecidos</p>
<ul>
<li class="task-list-item"><input type="checkbox" disabled=""> Exibir favorecidos   </li>
<li class="task-list-item"><input type="checkbox" disabled="" checked=""> Não exibir Favorecidos</li>
</ul>
<h4 id="observações-gerais-2"><em>Observações Gerais:</em></h4>
<ul>
<li><p>A Pesquisa Avançada deve possuir um botão de marcar/desmarcar todas as colunas.</p>
</li>
<li><p>O autocomplete da pesquisa avançada deve possuir código e descrição das classificações orçamentárias (<a href="http://www.transparencia.mg.gov.br/planejamento-e-resultados/proposta-lei-orcamentaria/proposta-orcamentaria/proposta-pesquisa-avancada">eg. consulta proposta orçamentária</a>);</p>
</li>
<li><p>Ao exibir o favorecido o Portal deverá retornar o nome e CNPJ/CPF do favorecido, conforme já ocorre na <a href="http://www.transparencia.mg.gov.br/despesa-estado/despesa/despesa-resultado-pesquisa-avancada/2019/01-01-2019/31-12-2019/3853/0/3684/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/0/1/0">Consulta de despesa</a>.</p>
</li>
<li><p>O Portalo dever ter a funcionalidade de autocompletar (desde a primeira letra), desconsiderando acentuação, letras maiúsculas/minúsculas e palavras intermediárias (ex.: Ao digitar "gestao pública", um dos resultados será "Gestão da Administração Pública").</p>
</li>
<li><p>O cidadão poderá informar mais de um valor para cada filtro. Ao informar um valor de filtro, listar todas as opções. Se o cidadão não informar um valor para cada filtro, o Portal considerará todos os valores possíveis para cada filtro não informado.</p>
</li>
<li><p>O cidadão poderá escolher os campos que ele quer que apareça no resultado (seguir modelo das demais consultas).</p>
</li>
<li><p>O cidadão deverá escolher o ano da pesquisa.</p>
</li>
<li><p>Ao exibir o resultado na tabela a consulta deverá retornar as colunas valor inscrito processado, valor inscrito não processado, valor pago no ano e valor a pagar.</p>
</li>
</ul>
<h1 id="dependências--integrações">Dependências / Integrações</h1>
<p>A integração será realizada com o armazém do SIAFI (BO) conforme ocorre atualmente.</p>
<h1 id="exemplos">Exemplos</h1>
<p>Seguir o modelo atual da <a href="http://www.transparencia.mg.gov.br/despesa-estado/despesa">consulta de Despesa</a> do Portal de Transparência</p>
<h1 id="dúvidas">Dúvidas</h1></body>
      </html>
