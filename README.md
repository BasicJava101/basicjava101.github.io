This is a simple static site built with [Jekyll](https://jekyllrb.com/). The goal is to provide basic Java instructions to help students learn Java.

## Contributing

1. Fork the project
2. Clone the project `git clone https://github.com/BasicJava101/basicjava101.github.io.git`
3. Make your edit
4. Create a pull request

## Run the app
How to run the app:

1. Install [ruby](https://www.ruby-lang.org/en/downloads/) (Note Mac has ruby by default)
2. Install your dependencies:

	```
	bundle install
	```

3. Start the server

	```
	bundle exec jekyll serve --port 9000
	```

4. Navigate to [http://localhost:9000](http://localhost:9000) to see the site

## Adding a topic

1. Create a new file in the root folder. I usually put a 0 in front of it to indicate this is a topic. The format for the file name is `0-topic-name.md`. This is written in [Markdown](https://www.markdownguide.org/) style. You can use html inside a Markdown file.

2. This is the format for the page. Make sure you change the title.

```
---
layout: page
title: Object
---

This is the content
```

3. Once you finish writing it, add it to the menu.
	1. Open `_includes/sidebar.html`
	2. Add a link item to the list. The link should be the name of your file with the `html` extension, not `md`.

			```
				<li><a href="0-if-switch.html">9. If & Switch</a></li>
			```
