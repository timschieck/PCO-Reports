# PCO-Reports
Custom Reports for Planning Center

These are reports that I've written up for my church. I'm not exactly a whiz with coding so they might not be a good example of "best practices" but they get the job done. I'm always happy to receive feedback!

## Version 2.0 Release - Alpha
Version 2 is focused on adding a few new reports and also changing pretty fundamentally how these reports are setup.

### New Reports (Planned)
* Children's Roster
* Directory

### Changes
Most every report uses the same header and footer. It supports adding a custom stylesheet defined by a liquid variable. However, most styling uses the bootstrap framework that PCO utilizes.

This is what the header looks like:
```liquid
<!DOCTYPE html>
{% assign use_style = true %}
{% assign custom_style = "[custom stylesheet]" %}
{% assign org_logo = "[logo_url]" %}
{% assign people = people | sort: 'last_name' %}
<html lang="en">
<head>
  <title>{{ report.name }}  - {{ 'now' | date: "%B %d, %Y" }}</title>
  <meta charset="utf-8">
  {{ helpers.bootstrap }}
  {% if use_style %}<link href="{{ custom_style }}" rel="stylesheet">{% endif %}
</head>
<body>
  <div class="header">
    <div class="header_left">
      <img src="{{ org_logo }}" alt="Organization Logo" />
    </div>
    <div class="header_right">
      <h1 class="title">{{ report.name }}</h1><br />
      <p style="display: inline;">List Updated: {{ list.updated_at  | date: "%B %d, %Y" }}</p>
    </div>
  </div>
```

And this is the attribution footer. The author denotes who originally wrote the report. However these reports may differ from that original file.

```liquid
{% comment %}
Report Name - PCO Reports Version #
http://tschieck.github.io/PCO-Reports/
Author: 
{% endcomment %}
```

## Version 1.0 Release - 1/11/18
Version 1 is locked down and contains 3 reports:
* Mail Merge (Full-page mail merge letters)
* Attendance Checklist (Printable attendance sheets)
* Grade Report (Summary of what grade students are in)

[Zip Download v1.0](https://github.com/tschieck/PCO-Reports/archive/v1.0.zip)
[Documentation](docs/)
