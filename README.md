# Fastdoc

## Description

Fastdoc lets you write your code documentation using text or markdown directly in your code.
It finds and extracts all snippets and joins them to markdown files (.md).

✓ Made for Github and npm  
✓ Table of contents generator  
✓ Easy to learn and use

## Installation

	npm install -g fastdoc

## Usage

	fastdoc [OPTIONS] [INPUT FILES/DIRS] [--output FILE/DIR]

Parse one file to stdout

	fastdoc main.js

## Markup

Just add "doc" to your comment syntax, before or after the comment.

### C-style

	/*doc*
	Multiline comment
	*/

	/*
	Multiline comment
	*doc*/

	//doc// Single line comment

	// Single line comment //doc

### Bash-style

	#doc# Single line comment

	# Single line comment #doc

## Table of contents

Fastdoc generates a Github friendly table of contents. Just place this inside your comment:

	{fastdoc-toc}

If you just want to list main headlines, you can set the depth (1-5):

	{fastdoc-toc-3}

# Appendix

## Why did I write Fastdoc?

Does the world need another fancy documentation generator? No, not really. But I think there is a gap between what a programmer needs, when he writes code, and what a documentation and project management enthusiast thinks is good :-)

I wanted something that is no effort to learn and use. Written in 100 lines of code alongside with 100 words of documentation.

## Why is Fastdoc not documented with Fastdoc?

Fastdoc is made for big projects, but Fastdoc itself is not a big project.

## More examples

Parse two files to a file

	fastdoc main.js function.js --output README.md

Parse a folder to a file

	fastdoc src/ --output README.md

Parse a folder to a folder. There will be one markdown file (.md) for every matching code file.

	fastdoc src/ --output documentation/
