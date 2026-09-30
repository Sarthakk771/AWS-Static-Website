# Design and Deploy a Static Website on AWS using Amazon S3

## 1. Project Title

**Design and Deploy a Static Website on AWS using Amazon S3**

## 2. Project Objective

The objective of this project is to design a simple static website using HTML, CSS, and JavaScript and deploy it on Amazon S3 using S3 Static Website Hosting.

The project demonstrates:
- Creating an Amazon S3 bucket
- Uploading website files
- Configuring static website hosting
- Configuring the required bucket permissions
- Testing the deployed website
- Accessing the website through an S3 website endpoint

## 3. Technologies Used

### Frontend
- HTML
- CSS
- JavaScript

### Cloud Service
- Amazon S3

### Development Tool
- Visual Studio Code

## 4. AWS Implementation

Only Amazon S3 is used for the cloud implementation.

The S3 bucket is configured to host the static website and serve the HTML, CSS, and JavaScript files through an S3 website endpoint.

## 5. Project Structure

```text
AWS-Static-Website/
├── index.html
├── style.css
├── script.js
└── README.md
```

## 6. Website Files

### index.html
Contains the structure and content of the website.

### style.css
Contains the styling and layout of the website.

### script.js
Adds interaction to the website. The Click Me button displays a success message.

## 7. S3 Bucket Configuration

**Bucket name:** `aws-static-website-sarthak-2026`

**AWS Region:** `us-east-1` (US East - N. Virginia)

**Bucket type:** General purpose

**Object Ownership:** Bucket owner enforced

**Bucket Versioning:** Disabled

**Object Lock:** Disabled

**Default Encryption:** SSE-S3

## 8. Static Website Hosting Configuration

S3 Static Website Hosting was enabled with:

```text
Static website hosting: Enabled
Hosting type: Bucket hosting
Index document: index.html
```

The website is served through the S3 website endpoint.

## 9. Permissions Configuration

Block Public Access was disabled for this bucket because the traditional S3 static website endpoint requires public access to the website objects.

A bucket policy was configured to allow public read access to the website files.

The policy grants:

```text
Action: s3:GetObject
```

The public users can read the website files but are not given permissions to upload, modify, or delete objects.

## 10. Architecture

```text
User / Browser
      |
      | Website URL
      v
Amazon S3 Bucket
      |
      ├── index.html
      ├── style.css
      └── script.js
      |
      v
S3 Static Website Hosting
      |
      v
Website displayed in browser
```

## 11. Deployment Steps

1. Created the website files in Visual Studio Code.
2. Tested the website locally.
3. Created an Amazon S3 bucket.
4. Configured the required public access settings.
5. Uploaded `index.html`, `style.css`, and `script.js`.
6. Enabled S3 Static Website Hosting.
7. Set `index.html` as the index document.
8. Configured the bucket policy for public `s3:GetObject` access.
9. Opened the S3 website endpoint in a browser.
10. Tested the HTML, CSS, and JavaScript functionality.

## 12. Website URL

```text
http://aws-static-website-sarthak-2026.s3-website-us-east-1.amazonaws.com
```

## 13. Testing Results

| Test Case | Expected Result | Actual Result | Status |
|---|---|---|---|
| Website URL | Website opens in browser | Website opened successfully | PASS |
| HTML | Website content loads | Content loaded correctly | PASS |
| CSS | Website styling loads | Styling applied successfully | PASS |
| JavaScript | Button displays message | Success message displayed | PASS |

## 14. Screenshots

The project submission should include screenshots showing:

1. S3 bucket creation
2. Website files uploaded to S3
3. Static website hosting configuration
4. Bucket policy / permissions
5. Working website URL in the browser
6. JavaScript test result

## 15. GitHub Repository

The project source code and documentation will also be uploaded to a GitHub repository.

The GitHub repository will contain:

```text
index.html
style.css
script.js
README.md
```

GitHub is used for source-code and documentation storage. Amazon S3 is used for the actual cloud website hosting.

## 16. Result

The static website was successfully designed and deployed using Amazon S3. The HTML, CSS, and JavaScript files were uploaded to the S3 bucket, static website hosting was enabled, the required permissions were configured, and the website was successfully accessed through the S3 website endpoint.

## 17. Conclusion

This project demonstrates the basic process of deploying a static website using Amazon S3. It provides practical understanding of S3 buckets, object storage, static website hosting, bucket policies, public read permissions, and website testing.
