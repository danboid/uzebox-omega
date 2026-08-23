# Converting markdown (.md) to PDF

I found that the markdown version of the assembly guide did not print well under most browsers.

I converted the markdown assembly guide into a PDF under Debian using these commands:

```
sudo apt install pandoc wkhtmltopdf
cd uzebox-omega/schematics/Uzebox-Omega/V1.1.1
pandoc Uzebox-Omega-V1.1.1-assembly-guide.md -o Uzebox-Omega-V1.1.1-assembly-guide.pdf \
  --from markdown+smart --pdf-engine=wkhtmltopdf --standalone --css style.css
```

**style.css** restricts the image height (**max-height: 180px**) so that each assembly guide step/row will easily fit within a single page boundary and the **page-break-inside: avoid** rule prevents the engine from tearing the table rows apart and printing item descriptions on a separate page to their photo.
