Configure CloudWatch using the AWS Console :

# Step 1 : Create a new Kinesis Data Firehose Delivery Stream

1. Sign in to the AWS Management Console and open the Kinesis console at [https://console.aws.amazon.com/kinesis](https://console.aws.amazon.com/kinesis).
2. Choose <b>Data Firehose</b> in the navigation panel.
3. Choose <b>Create delivery stream</b>.
4. The stream’s Source should be <b>Direct PUT</b> and Destination set to <b>HTTP Endpoint</b> with the following details:<br/>
   <b>Kinesis endpoint:</b> https://{ACCOUNT-UID}.middleware.io/v1/metrics/cloudwatch <br/>
   <b>API Key:</b> Enter your Middleware API key {ACCOUNT_KEY}.
5. In the Backup settings, select an S3 backup bucket to receive any failed events that exceed the retry duration.


## Step 2 : Create a new CloudWatch Metric Stream

1. Open the CloudWatch AWS console at [https://console.aws.amazon.com/cloudwatch/](https://console.aws.amazon.com/cloudwatch).
2. In the left navigation pane, choose <b>Metrics → Streams</b>.
3. Click the <b>Create metric stream button</b>.
4. Choose the <b>All namespaces </b> in the metric stream.
5. Choose <b>Select an existing Firehose owned by your account</b>, and select the Firehose Delivery Stream you created earlier.
6. Specify an <b>Output Format of OpenTelemetry 0.7</b>.
7. Optionally, specify a name for this metric stream under <b>Metric Stream Name</b>.
8. Choose <b>Create metric stream</b>.
