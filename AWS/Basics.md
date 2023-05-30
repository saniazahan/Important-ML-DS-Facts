## AWS Training and Certification Events

https://aws.amazon.com/training/events/?get-certified-vilt-courses-cards.sort-by=item.additionalFields.startDateSort&get-certified-vilt-courses-cards.sort-order=asc&awsf.get-certified-vilt-courses-type=*all&awsf.get-certified-vilt-courses-series=*all&awsf.get-certified-vilt-locations=*all&awsf.get-certified-vilt-countries=*all&awsf.get-certified-vilt-languages=*all&awsf.get-certified-vilt-courses-level=*all&awsf.get-certified-vilt-courses-tech-category=*all


## Free AWS basic course
https://explore.skillbuilder.aws/learn/course/1851/AWS%2520Technical%2520Essentials

Ways to interact with the AWS APIs
- AWS management console
- AWS command line interface
- AWS software development kits

## AWS Identity and Access Management

## EC2 launch user data
"""
#!/bin/bash -ex
#Update yum
yum -y update
# Add node's source repo
curl -sL https://rpm.nodesource.com/setup_15.x | bash-
# Install nodejs
yum -y install nodejs
# Create a dedicated directory for the application
mkdir -p /var/app
# Get the app from S3
wget https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/ILT-TF-100-TECESS-5/app/app.zip
# Unzip it into a specific folder
unzip app.zip -d /var/app/
cd /var/app/
#install dependencies
npm install
# Start your app
npm start
"""

video url https://youtu.be/XI7R1W3PPbg

#!/bin/bash
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo "Hello Sania from $(hostname -f)" > /var/www/html/index.html
