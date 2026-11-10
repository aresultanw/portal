# Anweshika Scholarship Exam Portal 2026

A static results portal for the Anweshika Scholarship Exam, an initiative by Netaji Sadharan Pathagar. Students can look up their result using their full name and roll number, then open and print or save a certificate.

The site includes a student-focused results homepage and an About page with information about the initiative.

## Features

- Search results by name and roll number.
- Display the student's class, school, guardian, and marks when a record matches.
- Generate a certificate populated with the matched student's details.
- Responsive page styling for desktop and mobile screens.

## Run Locally

The site has no build step. From the project directory, start a local static server:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000> in a browser. The portal uses relative file paths, so serving the directory is preferable to opening the HTML file directly.

## Project Files

- `index.html` - scholarship portal and result lookup form.
- `about.html` - information about the scholarship exam and its organizing initiative.
- `certificate.html` - printable certificate page.
- `js/cScript-2026.js` - result lookup logic and student records.
- `css/` - Bootstrap, site, and responsive stylesheets.
- `images/` - logos and page imagery.

## Student Data

Student records are embedded in `js/cScript-2026.js` as Base64-encoded JSON and decoded in the browser. Base64 is only an encoding, not encryption; anyone who can access the site files can retrieve those records. Do not use this approach for confidential data. Review and update the records in that script before publishing results.

The page also loads third-party libraries and fonts from CDNs, so those resources require an internet connection.