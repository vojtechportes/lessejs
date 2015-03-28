# lessejs
Combination of LESS CSS preprocessor and EJS

##Syntax

#EJS

Use syntax from https://github.com/tj/ejs.

Embed JS code with {{ }} tags

You can use emulation of ES6 template strings by writing between `` quotes.
To embed JS, use this syntax {$...}. This is transformed to concatenaded JS string.

Eg:

return `@media ({$type}: {$size}) { 
  font-size: {$v.type.baseSize}px;
  line-height: {$Math.round(v.type.lineHeight * v.lineHeightSmaller)}em;
  font-family: {$ (g.useFontFace ?  g.type.fontFamily : t.type.fontFamily)};
}`;

is transformed to

return "@media (" + type + ":" + size "px) { font-size: " + v.type.baseSize + ") { font-size: " + v.type.baseSize + "px; line-height: " + Math.round(v.type.lineHeight * v.typeLineHeightSmaller) + "em; font-family: " + (g.useFontFace ?  g.type.fontFamily : t.type.fontFamily) + " }";

#LESS

Use syntax from http://lesscss.org/
