# FluentBit - CloudWatch
- Sends logs for application, host and dataplane
- https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Container-Insights-setup-logs-FluentBit.html#Container-Insights-FluentBit-setup
- Setup IRSA:
    -   eksctl utils associate-iam-oidc-provider --cluster shubhams-eksctl-test --approve
    - eksctl create iamserviceaccount \                                            
    --name fluent-bit \             
    --namespace amazon-cloudwatch \
    --cluster shubhams-eksctl-test \
    --attach-policy-arn "arn:aws:iam::aws:policy/CloudWatchAgentServerPolicy" \                       
    --approve \
    --override-existing-serviceaccounts
    - Restart fluentbit pods

# Control Plane Logging
 - Just enable it in the console and then you'll find logs in cloudwatch

# K8s Dashboard
- https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/

# Prometheus
- install EBS CSI Driver Plugin - https://docs.aws.amazon.com/eks/latest/userguide/ebs-csi.html
- follow https://docs.aws.amazon.com/eks/latest/userguide/prometheus.html

# Grafana
- https://grafana.com/docs/grafana/latest/setup-grafana/installation/helm/
- Use Prometheus Pod IP address instead of Localhost IP address while setting up the dashboard