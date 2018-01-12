# Mail Merge

This is a particularly interesting report. It creates a mail merged letter, but pulls the content of the letter from a Google doc. This makes it easy to change the contents of the letter, and have someone who is unfamiliar with HTML or Liquid change the report if needed.

Three variables need to be set. The first two are image files for headers and footers of letterhead. If that is not needed the HTML can simply be removed. The third variable is called google_doc_key and is a string that references the file on the Google Drive.

The document should be setup with no margins and published to the web. When that is done find the link which should look something like:

https://docs.google.com/document/d/e/[String Goes Here]/pub

Copy the value of the string between /d/e/ and /pub. Set this as the google_doc_key variable in the report and it should work properly.

I copied this method from someone else but forgot who. If this was your implementation let me know so I can give you full credit!

This report is best generated as a PDF file.

[Download Here](https://raw.githubusercontent.com/tschieck/PCO-Reports/master/mail_merge.liquid)

# Attendance Checklist

This report generates a checklist that can be printed off and used to take attendance. Be default it will put an asterisk by any name that is a member, and will break out those tagged as Visitors to a separate block.

It also has a few lines at the end for writing in the name of guests.

This report is best generated as an HTML file.

[Download Here](https://raw.githubusercontent.com/tschieck/PCO-Reports/master/attendance_checklist.liquid)

# Grade Report

This report generates a list of children with their grade, school, and age. Starting from 12th and going in descending order. Any child younger than Pre-K is put in at the end under "No Grade".

It's not a particularly detailed report but is helpful for seeing how many kids are in each grade.

This report works as either HTML or PDF

[Download Here](https://raw.githubusercontent.com/tschieck/PCO-Reports/master/grade_report.liquid)

[Home](../)
