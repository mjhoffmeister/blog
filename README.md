# Local setup

## Windows

### Environment setup

1. Install [Ruby+Devkit](https://rubyinstaller.org/downloads/)
2. Run the `ridk install` step when prompted in the last stage of the installer
3. Choose `MSYS2 and MINGW development toolchain` in the command prompt that opens (option 3 as of
this writing)
4. Open a new command prompt to get PATH updates
5. Execute `gem install jekyll bundler`
6. In the project root folder, run `bundle update github-pages`
7. If you get a message about an error occurring while installing `wdm`, run `gem install wdm:0.1.1 
-- --with-cflags=-Wno-implicit-function-declaration`
8. Execute `bundle exec jekyll -v` to verify your Jekyll installation

### Running locally

After your environment is configured, execute the following command to run locally.

`bundle exec jekyll serve`

# VS Code utilities

## Markdown snippets

The following snippets are helpful for Bible blog posts.

``` json
"Biblia Link": {
    "prefix": ["biblia"],
    "body": [
        "[${1|Genesis,Exodus,Leviticus,Numbers,Deuteronomy,Joshua,Judges,Ruth,1 Samuel,2 Samuel,1 Kings,2 Kings,1 Chronicles,2 Chronicles,Ezra,Nehemiah,Esther,Job,Psalms,Proverbs,Ecclesiastes,Song of Solomon,Isaiah,Jeremiah,Lamentations,Ezekiel,Daniel,Hosea,Joel,Amos,Obadiah,Jonah,Micah,Nahum,Habakkuk,Zephaniah,Haggai,Zechariah,Malachi,Matthew,Mark,Luke,John,Acts,Romans,1 Corinthians,2 Corinthians,Galatians,Ephesians,Philippians,Colossians,1 Thessalonians,2 Thessalonians,1 Timothy,2 Timothy,Titus,Philemon,Hebrews,James,1 Peter,2 Peter,1 John,2 John,3 John,Jude,Revelation|} ${2:chapter}:${3:verses}](https://biblia.com/bible/esv/${1/(.*)/${1:/downcase}/}/$2/$3)"
    ],
    "description": "Insert a Markdown link for a Bible passage from biblia.com."
},

"Footnote": {
    "prefix": "foot",
    "body": [
        "[^${1:number}]: ${2:author}, ${3:title}, ${4:page}."
    ],
    "description": "Insert a footnote."
},

"Superscription": {
    "prefix": "sup",
    "body": [
        "<sup>${1:superscription}</sup>"
    ],
    "description": "Insert a superscription."
}
```

These user settings (in `settings.json`) are helpful for snippet usage.

``` json
"[markdown]": {
    "editor.snippetSuggestions": "top",
    "editor.quickSuggestions": {
        "comments": "on",
        "strings": "on",
        "other": "on"
    },
    "editor.wordBasedSuggestions": "off"
}
```