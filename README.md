# Individual quarto file

If there are multiple individual rmarkdown docs, use `appPrimaryDoc` to specify the intended doc.

```
library(rsconnect)
writeManifest(appPrimaryDoc='report2.Rmd')
```

manifest.json

```

{
  "version": 1,
  "locale": "en_US",
  "platform": "4.3.2",
  "metadata": {
    "appmode": "rmd-static",
    "primary_rmd": "report2.Rmd",
    "primary_html": null,
    "content_category": null,
    "has_parameters": false
  },
  "packages": {
    "R6": {
      "Source": "CRAN",
      "Repository": "https://cran.rstudio.com",
      "description": {
        "Package": "R6",
        "Title": "Encapsulated Classes with Reference Semantics",
        "Version": "2.5.1",
  
  .....
  
  
  

```


# Sites

If the output is a complex quarto type (site, blog, book, etc...). 

```
writeManifest(appDir='book', appPrimaryDoc = 'index.html', contentCategory='site')
```

manifest.json:

```

{
  "version": 1,
  "locale": "en_US",
  "platform": "4.3.2",
  "metadata": {
    "appmode": "quarto-static",
    "primary_rmd": "index.html",
    "primary_html": null,
    "content_category": "site",
    "has_parameters": false
  },
  "quarto": {
    "version": "1.4.549",
    "engines": ["markdown"]
  },
  
  .......

```

If you don't pass the primary doc or name it a site, no primary file would be specified. 

