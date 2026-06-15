# News Situation Reports

Situation Reports are Aunoo Intelligence's up-to-date situational awareness on breaking AI and technology events. Aunoo Intelligence is the research and advisory team at Aunoo.

Each report is built on Aunoo news-intelligence and ships as a SITREP plus distribution collateral (PDF bulletins, a web page, a LinkedIn post, and a social cover).

## Layout

Each report lives in its own folder under `reports/`, named by event. The current example is the US export-control suspension of Anthropic's Fable 5 and Mythos 5.

## Building the PDFs

```bash
python -c "from weasyprint import HTML; HTML('bulletin.html').write_pdf('bulletin.pdf')"
```

Requires `weasyprint`. Reports are compiled from open-source reporting and should be checked against primary sources before use.
