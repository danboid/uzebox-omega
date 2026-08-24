# Converting markdown (.md) to PDF

I found that the markdown version of the assembly guide did not print well under most browsers.

I converted the markdown assembly guide into a PDF under Debian using these commands:

```
sudo apt install pandoc weasyprint
cd uzebox-omega/schematics/Uzebox-Omega/V1.1.1
pandoc Uzebox-Omega-V1.1.1-assembly-guide.md -o Uzebox-Omega-V1.1.1-assembly-guide.pdf --pdf-engine=weasyprint --css=style.css
```

