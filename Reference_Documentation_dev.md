# Reference

## **Data Dictionary** 

To customize the web app’s data, the data needs to meet the data requirements as outlined in the following data dictionary. 

| Column | Data Type | Possible Values | Description |
| :---- | :---- | :---- | :---- |
| Year | Integer | \> 0 | The album’s release year |
| Ranking | Integer | \>= 1 and \<= count(albums this year) | Ranking (row\_number) of the album for the year it came out, given its rating |
| Album | String | Any str | Album name |
| Artist | String | Any str | Artist name |
| Rating | Integer | \>= 1 and \<= 10 | Rating out of 10 (inclusive) |
| Vinyl | String | “v” or NULL | Indicate that the album is owned on vinyl |
| EP | String | “EP” or NULL | Indicate that the album is an EP (extended play) album |
| Live | String | “Live” or NULL | Indicate that the album is a live (recorded live) album |

##### **Key distinctions:**

- Rating: An album's rating (1 to 10, inclusive) at the time it was released.  
- Ranking: An album's ranking against other albums that were released in the same year. This follows the SQL row\_number ranking system (where each ranking must be unique, and none are skipped).  
- Album: If an album contains a comma, you should input it into your sheet surrounded by quotation marks.  
- Artist: If an artist contains a comma, you should input it into your sheet surrounded by quotation marks.  

## **Troubleshooting Guide**

- *No such file or directory” when importing data into RStudio*

Filepaths can be very difficult to troubleshoot. 

1. Check your current working directory by running `getwd()`.  
2. Set the correct directory using `setwd("path/to/your/folder")`.  
3. Confirm the change by running `getwd()` again.  
4. Make sure your data file is inside that folder (use `list.files()` to check).

Alternatively, follow this [tutorial](https://www.sthda.com/english/wiki/running-rstudio-and-setting-up-your-working-directory-easy-r-programming) to learn how to set up your working directory in RStudio. If you want a video explanation, try watching a YouTube video such as: [R: Read in data error "no such file/dir": solution setwd()](https://www.youtube.com/watch?v=-qtRSEc7svQ).

- *Shiny App isn’t publishing*  
1. In the bottom left space of the RStudio UI grid, paste `install.packages("shiny")` and hit enter in the **Console** tab.  
2. Alternatively, try following this [Shiny tutorial](https://shiny.posit.co/r/articles/share/shinyapps/). The tutorial is an official walkthrough for creating a demo app. 

- *RStudio versus Visual Studio Code (VS Code)*

You will need to use RStudio to follow the My Favorite Albums documentation. RStudio natively integrates with publishing Shiny Apps once the package is installed to make the process very simple. However, you could use VS Code with a bit more effort and the Shiny extension. See this [tutorial](https://shiny.posit.co/blog/posts/shiny-vscode-1.0.0/) on using the Shiny extension in VS Code. 

## **Glossary**

* R \- A coding language most commonly used in academia for data and statistical analysis.   
* IDE \- Integrated development environment, such as RStudio. This is where you, the developer, actually change and save the code.   
* CSV file \- A file that stores lines of comma-separated values, most frequently used to store tables of data.   
* Source code \- The initial code for an existing project.   
* ZIP file \- A file that compresses several files or folders into a single file.   
* Package \- A collection of pre-written, publicly available code that can be downloaded, installed, and used.   
* Hard-coded \- Non-dynamic values stored in code that need to be manually defined.   
* Data dictionary \- A description of a data table that typically contains field names, attributes, constraints, descriptions, and data types.   
* Workbook/sheet \- A GUI interface, typically associated with Google Sheets or Microsoft Excel, for interacting with CSV files. 