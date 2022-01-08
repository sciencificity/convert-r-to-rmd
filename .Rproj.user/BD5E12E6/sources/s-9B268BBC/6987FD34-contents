---
title: "Convert R file to Rmd file"
author: "Vebash Naidoo"
date: "08/01/2022"
output: html_document
---

If you, like me, enjoy working with RMarkdown files you will perhaps be searching
for a way to convert an R file you receive via a course, a tutorial,
a colleague, or even an old file of your own into an Rmd file.

1. You can directly create a report from an R file by running `Ctrl + Shift + K` or `Cmd + Shift + K` on an `R` file.
Under the hood an [Rmd file is created and knitted](https://bookdown.org/yihui/rmarkdown-cookbook/spin.html)
to provide the desired report format you're looking for. The actual `.Rmd` file is removed after the knit.

1. You can also call `knitr::spin()` with the arguments you want at 
the console in order to create the `.Rmd` file and knit it yourself.

    ```
    knitr::spin(hair = r"(C:\Users\Vebashini\OneDrive - Rain\Documents\Main-Documents\Learning\Current_Work\sales_analysis.R)", # path to R file 
    knit=FALSE,    # knit = FALSE so report (.Rmd) is generated and kept
    format = "Rmd" # format of file
    )
    ```
    
    - hair = file path to file you want to convert
    - knit = FALSE : I want the RMarkdown document to be created and I will knit it from that (Setting this to TRUE knits to desired format and removes the actual `.Rmd` file).
    - format = "Rmd" : If you read the Help file (`?knitr::spin`) you will see that the format can be multiple and any of `format = c("Rmd", "Rnw", "Rhtml", "Rtex", "Rrst")`
    <br>
    <br>

### Example 1

The first example is from the [RMarkdown Cookbook](https://bookdown.org/yihui/rmarkdown-cookbook/spin.html). This is the file `rmd-cookbook-example.R` in the repo.

To create the `rmd-cookbook-example.Rmd` file you use:

```
knitr::spin(hair = r"(C:\Current-Work\code-snippets\convert-r-to-rmd\rmd-cookbook-example.R)", 
          knit=FALSE, format = "Rmd")
```

### Example 2

In reality the R script file you have will not be as nicely formatted as
that in the book - you will have to re-format it yourself after conversion.
The second example is a raw file with a small code snippet (`files-in-the-wild.R`) that can be used to observe the output you get in the form of an `.Rmd` file.

```
knitr::spin(hair = r"(C:\Current-Work\code-snippets\convert-r-to-rmd\files-in-the-wild.R)", 
          knit=TRUE,        # knit doc
          format = "Rmd",
          precious = TRUE,  # keep intermediate files
          )
```

Notice here I asked it to be knitted `knit = TRUE` which ordinarily would
have removed the intermediate `.Rmd` file. But I set an additional parameter of
`precious = TRUE` which tells the function to keep the intermediate files including the `.Rmd` file.
