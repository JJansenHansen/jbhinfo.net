# personal-website

This is a personal website intended to be used as the front end for personal cloud platform engineering projects. This includes code for creating the docker images and deploying a minimal Kubernetes cluster to host the images.

This template is tested and worked on:
- Windows 22H2
  - Chrome 128
  - Edge 128
- Android 14
  - Chrome 128 (Website is not currently responsive to sreen sizes and experiences wrapping issues in mobile)

# Problems and Bugs
Here are the problems and bugs that I plan to address in the future. If you fixed them, please do not hesitate to send me a pull request, and I would be very grateful. Please also report problems and bugs in [GitHub Issues](https://github.com/JJansenHansen/jbhinfo.net/issues).

- Elements to not respond to smaller screen sizes. This is an issue for smaller screens especially on mobile

# Future Plans for Feature Enhancement
Here are features that I plan to add in the future. If you wish to contribute, please email me to discuss the design before submitting pull requests.

- Automatic logging

# How to Deploy
This site is specifically used in my projects with AWS resources to deploy via multiple means. You can use the instructions below to deploy a similar infrastructure. I have split the deployment up into two specific versions.

## The Simple Version (S3 Bucket Hosting)
<details><summary> Click to Expand </summary>
<pre>
This website is static meaning it displays the same content to every user regardless of time, location, etc. and does not provide any interactive features. As such, it can easily be deployed from an AWS S3 bucket at minimal cost. This is the recommended way of hosting a simple HTML file such as this.

Default Amazon S3 endpoints do not support HTTPS or access points. I recommend using Amazon CloudFront to serve a static website hosted on Amazon S3 [AWS Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/website-hosting-custom-domain-walkthrough.html)

</pre></details>

## The Complex Version (Building Your Own Platform on AWS)
<details><summary> Click to Expand </summary>
<pre>
This method is NOT recommended for long-term hosting. The build demonstrated below is gross overkill for hosting a simple HTML file and should only be used to practice building with AWS, Docker, and Kubernetes clusters. In testing, this setup costs about $80 per month to run mostly due to the size of the EC2 instances running on the Kubernetes cluster. In practice, these instances are spending more resoures managing the cluster itself than hosting the application containers.

</pre></details>
