Sublime StringTemplate Syntax
=============================

Sublime syntax definition file for StringTemplate. It was designed for HTML templates and requires modification of the HTML syntax file to be fully functional.

Download
--------

Download the [Gist](https://gist.github.com/schmalls/5420869/download) for the compiled files.

Dollar vs. Angle Bracket Delimiters
-----------------------------------

There are 2 options for the delimiters. Angle bracket delimiters have not been tested, but should theoretically work.

HTML Syntax File Modifications
------------------------------

Open the `HTML.tmLanguage` file and update the embedded code section to add your preferred StringTemplate language definition.

```xml
<key>embedded-code</key>
<dict>
    <key>patterns</key>
    <array>
        <dict>
            <key>include</key>
            <string>#ruby</string>
        </dict>
        <dict>
            <key>include</key>
            <string>#php</string>
        </dict>
        <dict>
            <key>include</key>
            <string>#python</string>
        </dict>
        <dict>
            <key>include</key>
            <string>text.stringtemplate.dollar</string>
        </dict>
    </array>
</dict>
```

The `.dollar` can be replaced with `.angle` if you use angle brackets instead of dollar delimiters.

Also add `st` to the `fileTypes` array to open all StringTemplate files in HTML mode automatically.

Theme File Modifications
------------------------

If you want the StringTemplate items to stand out, modify your theme file. The following addition works pretty well for the `Monokai.tmTheme` file.

```xml
<dict>
    <key>scope</key>
    <string>entity.name.function.template.stringtemplate, keyword.control.if.stringtemplate, keyword.control.stringtemplate, punctuation.definition.anonymous.begin.stringtemplate, punctuation.definition.anonymous.end.stringtemplate, punctuation.definition.comma.stringtemplate, punctuation.definition.concatenation.stringtemplate, punctuation.definition.control.begin.stringtemplate, punctuation.definition.control.end.stringtemplate, punctuation.definition.delimiter.begin.stringtemplate, punctuation.definition.delimiter.end.stringtemplate, punctuation.definition.dot.stringtemplate, punctuation.definition.equal.stringtemplate, punctuation.definition.function.begin.stringtemplate, punctuation.definition.function.end.stringtemplate, punctuation.definition.indirect.begin.stringtemplate, punctuation.definition.indirect.end.stringtemplate, punctuation.definition.list.begin.stringtemplate, punctuation.definition.list.end.stringtemplate, punctuation.definition.logical.not.stringtemplate, punctuation.definition.semicolon.stringtemplate, punctuation.definition.string.begin.stringtemplate, punctuation.definition.string.end.stringtemplate, punctuation.definition.template.begin.stringtemplate, punctuation.definition.template.call.stringtemplate, punctuation.definition.template.end.stringtemplate, storage.modifier.option.stringtemplate, string.quoted.double.stringtemplate, support.function.stringtemplate, variable.other.stringtemplate, variable.parameter.stringtemplate</string>
    <key>settings</key>
    <dict>
        <key>background</key>
        <string>#444444</string>
    </dict>
</dict>
```

If someone knows a better way to do any of this, please let me know.
