# Basic Report Templates

Quite a number of people have asked what the report might look like based on our report writing course [The Art of Report Writing](https://training.ogsec.co.uk/courses/29ea6f47-6c95-4e98-9420-59db8b5889bd). These examples do not go into the content specifics - that's covered in the course. What I've put together here is a report shell in a couple of formats for folks to use, either to take away and edit as you desire, or for you to leverage during the exercises within the course

I must stress that the generated documents **do not look pretty**. This repo is purely to give you a starting point to work from, something to fill in while you do the course, or to play around with.

# LaTeX

LaTex is a powerful document creation tool that can be used to make nice looking reports in a repeatable and expected way. It's quite syntax heavy but ogSec has used it to make our own template, and it looks somewhat snazzy. What we're shared here however is very basic and structure focused.

## Installation

In order to build the report you'll need to install the LaTex software. Here's an example from WSL / debian based Linux distribution. 

```bash
$ apt update
$ apt install texlive-full  # Note that this will install all things LaTeX. If you're planning on heavily customising this template you'll probably need it, if not go for texlive-base

```

## Building

To build the project clone this repo and...

```bash
cd example-report/latex
./build.sh
```

The build runs twice, this is to work out the correct table of contents, then again to build the document with this part placed in the report. Once built you should see a number of build artefacts in the same directory, along with your report.pdf.

# Markdown

Markdown is a little simpler than LaTeX but also less flexible. There's a number of plugins and tools that can be used to enhance what you're able to do with this format, but it is limited. That said, you can create some pretty clean content with this and many tools are now supporting this format. 

Note: since this is processed in part by LaTeX you can inject some use thing LaTeX things in. In this example I've used `\newline` and `\pagebreak` to space out the content where required.

## Installation

There's a few options for building this markdown but this example will use pandoc, again using a debian based Linux distribution.

```bash
$ apt update
$ apt install pandoc
$ apt install texlive-xetex  # We'll need this to do the conversion using a latex engine under the hood
```

# Building

Once you have the pre-reqs installed:

```bash
$ cd example-report/markdown
$ ./build
```

Report.pdf should be in the same folder.

## DOCX & ODT

These are similar examples of the markdown and LaTex versions.
