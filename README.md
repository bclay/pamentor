PennApps Mentorship Website
===========================

## Getting set-up

Changes to be made to markdown documents in /Markdown and then complied HTML using Sublime Text + Markdown Preview (Cmd + Shft + P in Sublime Text in the file to be compiled > type in "Markdown Preview" > select "Save to HTML") and then to be moved to the top-level directory. For Markdown preview use Markdown Flavored (Not Github-Flavored) add the following to User Settings (Sublime Text > Preferences > Package Settings > Markdown Preview) in order to compile custom CSS and use syntax highlighting:

    {
        "enable_highlight": true,
        "css" : "*.css"
    }

## Editing Markdown

First open [this](http://daringfireball.net/projects/markdown/syntax) in a new tab. Keep that open to refer to, it's teh syntax docs for Markdown. The most important things to keep in mind:

- Any code you type in will be parsed as code UNLESS you either
    + place it within backticks (`) for inline code
    + place the entire code block at least one tab in
- Use hashtags (`#`) to signify headers, the number of hashtags refers to the level of the header. So `## Header 2` is an `h2` header. You can also use `=======` below some text as shorthand for `h1` and `--------` for `h2`.
- Use `*` for `em`, `[link text](url)` for links and `![alt image text](src)` for images.
- Again, please be careful when typing in code, ensure that it's either tabbed on inside backticks.
