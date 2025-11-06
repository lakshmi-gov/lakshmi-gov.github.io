---
layout: default
permalink: /cv/
title: cv
nav: true
nav_order: 2
# cv_pdf: example_pdf.pdf
description: Please feel free to reach out to me if you've any questions. Or if you want to talk science! Email [first-name]n [at] mit [dot] edu
# toc:
#   sidebar: left
---

{% capture cv_pdf_url %}{{ 'assets/pdf/lng_cv_2025.pdf' | relative_url }}{% endcapture %}

<iframe src="{{ cv_pdf_url }}" width="100%" height="800px">
  This browser does not support PDFs. Please download the PDF to view it: 
  <a href="{{ cv_pdf_url }}">Download PDF</a>
</iframe>