# pandoc-markdown

## dependence

- pandoc
- wkhtmltopdf
- etc.

## to html

```bash
# to html
pandoc -s ./markdown/resume.md -o ./output/resume.html

# with css file
pandoc -s ./markdown/resume.md -o ./output/resume.html -c ../css/resume.css

# If you want css file contained into html file you can use --self-contained
pandoc -s ./markdown/resume.md -o ./output/resume.html -c ./css/resume.css --self-contained

# html to pdf
wkhtmltopdf ./output/resume.html ./output/resume.pdf
```

## to pdf

```bash
# 手动指定 --pdf-engine 为 wkhtmltopdf
pandoc ./markdown/resume.md -o ./output/resume.pdf --css ../css/resume.css --pdf-engine wkhtmltopdf

# 使用 -t html5 默认 --pdf-engine 为 wkhtmltopdf
pandoc ./markdown/resume.md -o ./output/resume.pdf --css ../css/resume.css -t html5
```
