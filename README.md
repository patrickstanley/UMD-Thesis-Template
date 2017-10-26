# UMD-Thesis-Template
An unofficial, updated template for a University of Maryland Ph.D. Thesis.
Based on the work of Dorothea F. Brosius at IREAP.
Origional documentation and files are located at <https://ireap.umd.edu/resources/thesis-templates>.
This template assumes you are using pdflatex and bibtex.
There is no guarntee that this template matches the Graduate School's guidelines as the rewrite them, but it aims to.

## Glossaries Package for List of Abbreviations
In this template I chose to use the glossaries package to keep track and automatically generate a list of abbreviations and symbols. I have tried to include a few examples in the writing of various formats. If this is not desired, one can go back to the supertabular method in IREAP's template.

## Lipsum
The Lipsum package is used to generate filler text, allowing one to see what the style looks like without having to insert actual text. At the end of your work, once you have completed everything, you should remove the lipsum package from the preamble. If it then gives you an error, you know you accidentally left some Lipsum somewhere in your document. Be sure it is all gone before you submit it to anyone.

## Other Packages
The origional template form IREAP at UMD included a large number of packages, many of which I don't know why were included. I removed some to resolve errors or when I know I removed their purpose, but many are left. You may find that you need to re-add a package or eliminate one due to overlapping calls as you work on your project.
