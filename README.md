# Hugo MacOS Terminal

A Hugo shortcode for beautiful MacOS-like terminals in your web pages. More information can be found on my blog: [Sick and tired terminal screenshots?](https://jiridj.be/posts/macos-terminal-in-css/).

## Example usage

'''
{{< terminal "jiri@jiri-mbp-pro" "~/Sites/jiridj.be (zsh)" >}}
$ ls -l ~
total 40
drwx------+  8 jiri  staff    272 Mar 21 14:30 Desktop
drwx------+ 11 jiri  staff    374 Mar 21 16:47 Documents
drwx------+ 10 jiri  staff    340 Mar 22 13:36 Downloads
drwx------@ 70 jiri  staff   2380 Mar 15 12:44 Library
drwx------+  8 jiri  staff    272 Feb 14 04:54 Movies
drwx------+  5 jiri  staff    170 Oct 19 17:07 Music
drwx------+  9 jiri  staff    306 Feb  3 10:26 Pictures
drwxr-xr-x+  5 jiri  staff    170 Oct 19 14:23 Public
$ _
{{< /terminal >}}
'''

## Note

If you look at the HTML code, you'll notice I include the comment ```<!-- htmlmin:ignore -->``` before and after list of items. In command-line output whitespace is important.

I use [HTMLMinifier](https://github.com/kangax/html-minifier) to compress the generated static site (html, css and javascript). HTMLMinifier needs to leave the whitespace in the terminal blocks alone. These comments instruct HTMLMinifier to ignore anything in between them. 

You can leave out these two lines if you do not use HTMLMinifier. If you use another minifier, you'll have to customise this part to work for you.