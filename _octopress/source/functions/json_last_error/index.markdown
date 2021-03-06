---
layout: page
title: "JavaScript json_last_error function"
comments: true
sharing: true
footer: true
alias:
- /functions/view/json_last_error:878
- /functions/view/json_last_error
- /functions/view/878
- /functions/json_last_error:878
- /functions/878
---
<!-- Generated by Rakefile:build -->
A JavaScript equivalent of PHP's json_last_error

{% codeblock json/json_last_error.js lang:js https://raw.github.com/kvz/phpjs/master/functions/json/json_last_error.js raw on github %}
function json_last_error () {
  // http://kevin.vanzonneveld.net
  // +   original by: Brett Zamir (http://brett-zamir.me)
  // *     example 1: json_last_error();
  // *     returns 1: 0
/*
  JSON_ERROR_NONE = 0
  JSON_ERROR_DEPTH = 1 // max depth limit to be removed per PHP comments in json.c (not possible in JS?)
  JSON_ERROR_STATE_MISMATCH = 2 // internal use? also not documented
  JSON_ERROR_CTRL_CHAR = 3 // [\u0000-\u0008\u000B-\u000C\u000E-\u001F] if used directly within json_decode(),
                                  // but JSON functions auto-escape these, so error not possible in JavaScript
  JSON_ERROR_SYNTAX = 4
  */
  return this.php_js && this.php_js.last_error_json ? this.php_js.last_error_json : 0;
}
{% endcodeblock %}

 - [view on github](https://github.com/kvz/phpjs/blob/master/functions/json/json_last_error.js)
 - [edit on github](https://github.com/kvz/phpjs/edit/master/functions/json/json_last_error.js)

### Example 1
This code
{% codeblock lang:js example %}
json_last_error();
{% endcodeblock %}

Should return
{% codeblock lang:js returns %}
0
{% endcodeblock %}


### Other PHP functions in the json extension
{% render_partial _includes/custom/json.html %}
