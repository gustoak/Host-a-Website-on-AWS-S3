<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** gustavo.carvalho.br@gmail.com  
**Email:** gustavo.carvalho.br@gmail.com

---

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

In today's project, we will demonstrate how to host your own website on Amazon S3, thereby explaining how to store files in the cloud using AWS S3.

### Tools and concepts

Key Concepts of the Project
Creation of an Amazon S3 Bucket
The project guides users through the creation of an Amazon S3 bucket, which will serve as the repository for the website files.

Uploading Website Content
Participants upload essential files such as index.html, images, and other necessary assets required for the website's functionality.

Static Website Hosting Configuration
The bucket is configured to enable static website hosting, allowing the content to be served directly over the internet.

Permissions and Access Policy Management
The project covers the setup of bucket policies to control public access to the content, ensuring that files are accessible as needed.

Website Testing and Validation
After configuration, participants test the website endpoint to verify that everything is functioning correctly.

Project Documentation
The project emphasizes the importance of documenting each step of the process, promoting best practices for development and maintenance.

### Project reflection

I spent a total of 30 minutes, including setup, review, and documentation.



---

## How I Set Up an S3 Bucket

Provisioning an S3 bucket, including configuring ACL permissions to allow public access, took less than five minutes.

Central Canada was chosen because it is closer to me, where the S3 bucket resources will be used.

S3 bucket names must be globally unique because they form part of a public URL and prevent conflicts across AWS. This ensures DNS resolution, cross-region accessibility, and exclusive ownership. If a name is taken, choose a unique one.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### index.html and image assets

The index.html file was used as the primary entry point for the application. Additionally, the NextWork - Everyone...love_files.zip archive was extracted to retrieve the associated subdirectory containing all necessary static resources for the page, such as JavaScript, CSS, HTML fragments, and image files.

These assets were structured to support the correct rendering and behavior of the web page during deployment to the cloud storage environment.

The project involved downloading the index.html file, designated as the primary entry point for the web application. Additionally, a subdirectory containing all related static assets was retrieved. This asset bundle included JavaScript (.js), Cascading Style Sheets (.css), supplementary HTML files, and image resources (.jpg).

These assets are critical for client-side rendering and ensure the proper functionality and styling of the web page. The files were prepared for deployment to an S3 bucket configured for static website hosting, with the appropriate ACL policies applied to permit public read access.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

Website hosting refers to the process of storing website files on a web server and making them accessible over the internet. This allows users to view and interact with the website by entering its domain name or IP address in a browser.

In the Properties section of the created bucket, you should find the Static Website Hosting option and click on Edit. Next, enable Static Website Hosting and specify the main document for the page, which in this case was index.html.

An Access Control List (ACL) in S3 is a legacy permission system that grants read/write access to specific AWS accounts or public users at the bucket or object level.  

In this project, I enabled ACLs to manage access permissions.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

A bucket website endpoint URL is the special web address (URL) that AWS S3 provides when you enable static website hosting on a bucket.
It allows users to access the contents of the S3 bucket through a public HTTP web address.

When I first visited thWhen you visit the bucket website endpoint URL, you should see the static website that you uploaded — typically starting with your index.html file.

If everything is configured correctly, you will see:

The main page rendered (styled with your CSS)

Functional JavaScript interactions (if any)

Images and other assets loading properly

If something is wrong, you might see:

A 403 Forbidden error (usually permissions issue — bucket or object ACL not allowing public read)

A 404 Not Found error (wrong file name or missing index.html)e bucket endpoint URL, I saw... The reason for this error was...

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

To resolve this 403 added a bucket policy that explicitly grants public for all files I uploaded3 Forbidden error, I...

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

A bucket policy is a JSON-based access policy that you attach directly to an Amazon S3 bucket.
It defines what actions are allowed or denied for specific users, accounts, or the public, and under what conditions.

The bucket policy defines specific access rules for the S3 bucket.
It controls who can perform what actions (like GetObject, DeleteObject, etc.) on which resources (like index.html or all files in the bucket), and sometimes under what conditions.

![Image](http://learn.nextwork.org/compassionate_teal_gentle_red_currant/uploads/aws-host-a-website-on-s3_sm2sm2sm)

---

---
