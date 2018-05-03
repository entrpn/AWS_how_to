# AWS_how_to
List of tutorials on how to do certain aws functions

# Load Balancers with SSL capabilities

- Get a free ssl cert from aws here https://console.aws.amazon.com/acm/home.

- I couldn't figure out dns validation so I did email validation. Before that, make sure your can route admin@example.com to your email to accept. Ex: In name cheap I did this by adding forwarding from admin to my personal email address.
  
- When creating the load balancer, create its own security group with port 443 open.

- Create another security group for the ec2 instances. In inbound, select the port you want to open (Ex: 80, 8080) and make the source custom. Enter the security group id of the load balancer instead of an ip address.

