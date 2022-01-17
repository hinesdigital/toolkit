# How to write emails with this toolkit

## Email Formatting Basics

### Step 1: Start with `email.html`

Every email begins with `email.html` -- which includes a range of variables and dependencies that the other components rely on to function.

Copy the [raw source code](https://github.com/hinesdigital/toolkit/raw/main/email/email-new.html) of `email.html` and paste it into the *Source Code* view of NationBuilder’s email WYSIWYG editor.

Scroll down to the line that says `<!-- BEGIN EMAIL CONTENT HERE -->`. Write your email in HTML below that line.

### Step 2: Specify the correct landing page URL

Using this toolkit, you will only need to enter the URL of your WinRed landing page one time and it will automatically load into every link, button, and clickable image.

On `Line 6` of `email.html`, you will see:

```
{% capture base_url %}{% endcapture %}
```

Paste your chosen WinRed landing page URL (with not additional URL parameters) like this:

```
{% capture base_url %}https://secure.winred.com/electrepublicans/780196433930189833{% endcapture %}
```

Every link, button, and clickable image will now point to your chosen landing page URL with the correct UTM Codes and WinRed variables applied.

### Step 3: Using HTML Code Blocks

The code blocks in [Buttons](/email/buttons), [Images](/email/images), and [Widgets](/email/widgets) should be pasted into the Source Code editor on their own line (i.e., not inside of a `<p>` tag).

The code blocks in [Links](/email/links) should be included inline within paragraphs.