- Register a domain on Route53
- Issue a SSL certificate with the domain purchased for https requests
- create ingress.yaml load balancer with the certificate and ports 80,443
- Now set record for inside hosted zone in route 53 and select the ingress load balancer created in the previous step.
- Add the ssl redirect annotation to redirect http traffic to https