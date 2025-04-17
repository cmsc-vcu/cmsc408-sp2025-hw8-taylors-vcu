# cmsc408-sp2025-hw8

Homework 8 - World Bank Indicator Analysis

This homework assignment goes over the scenario where we are tasked with pulling data from very large databases that present information about World Development Indicators. 

We will be working with this data from these large WDI (World Development Index) databases from the World Bank to determine the post potent factors that determine the level of development that a country may currently have as well as the trend of such countries. Furthermore, we want to identify which countries are in need of technical and financial assistance to boost human and national development.

## Project Structure

This project has the following structure: 
```bash
.
├── README.md
├── poetry.lock
├── pyproject.toml
├── reports
│   ├── _quarto.yml
│   ├── helpers.py
│   ├── report.html
│   ├── report.qmd
│   └── report.quarto_ipynb
└── source-data
    ├── README.md
    ├── loader.html
    └── loader.qmd

3 directories, 11 files
```

- `reports/`: This directory stores our `.qmd` files that we will generate into HTML files that can be rendered in a browser. It also houses the `_quarto.yml` file that enables us to broadly apply dates and author fields into our HTML files as well as specify which directory we want the `.qmd` files to be generated in (in our case, it is in the `reports/` directory). We can even apply different report themes giving the reports a customized feel. 


## Configuration & Customization
We can customize our `quarto` rendering by editing the `_quarto.yml` file which is inside of the `reports` directory. 

As an example, we've laid out our default configuration here which specifies the date, subtitle, authors, among other fields. We can even choose where we want the HTML reports to be generated (which in our case is the `reports` directory). We can even customize the format for the report HTML. As we can see below, we've applied the minty theme to our default report generation giving it a tidy, modern feel. 

```yaml
author:
    - name: Sagai Taylor
      email: taylors@vcu.edu

date: last-modified

format:
    html:
        theme: cosmo
        toc: true
        embed-resources: true
        code-copy: true

execute:
  echo: true
  eval: true
  cache: false
```

## Usage
The final products within this repo are the deliverable documents that are generated in HTML from the `.qmd` (Quarto Markdown) files, however for this assignment we will focus on generating the Deliverable 6 Document report which is named `report.qmd`. 

We will need the `quarto` command-line tool to render the following report to HTML so we can view it in our default browser. 

Furthermore, the steps for downloading `quarto` can be found [here](https://quarto.org/docs/get-started/)

We can generate the **Homework 7 Report** via the steps velow: 

1. Git clone this project via the following command:
```bash
git clone https://github.com/cmsc-vcu/cmsc408-sp2025-hw8-taylors-vcu.git
```

2. Change directories to the `reports` folder:
```bash
cd cmsc408-sp2025-hw8-taylors-vcu
```

3. Render the `report.qmd` file with `quarto`:
```bash
quarto render reports/report.qmd
```

4. We can now view the generated HTML report for Deliverable 5 in our default browser:

- Mac (This opens the default browser): 
```bash
open reports/report.html
```

- Linux (Assuming we are using Google Chrome):
```bash
google-chrome reports/report.html
```

- Windows (Assuming we are using Google Chrome):
```powershell
"C:\Program Files\Google\Chrome\Application\chrome.exe" "C:\Users\$env:USERNAME\Downloads\cmsc408-sp2025-hw8-taylors-vcu\reports\report.html"
```


