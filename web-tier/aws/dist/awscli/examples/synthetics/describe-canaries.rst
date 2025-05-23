**To list canaries in your account**

The following ``describe-canaries`` example lists the details of canaries in your account. ::

    aws synthetics describe-canaries

Output::

    {
        "Canaries": [
            {
                "Id": "a1b2c3d4-5678-90ab-cdef-example11111",
                "Name": "demo_canary",
                "Code": {
                    "SourceLocationArn": "arn:aws:lambda:us-east-1:123456789012:layer:cwsyn-demo_canary-a1b2c3d4-5678-90ab-cdef-example11111b8:1",
                    "Handler": "pageLoadBlueprint.handler"
                },
                "ExecutionRoleArn": "arn:aws:iam::123456789012:role/service-role/CloudWatchSyntheticsRole-demo_canary-a12-a123bc456789",
                "Schedule": {
                    "Expression": "rate(5 minutes)",
                    "DurationInSeconds": 0
                },
                "RunConfig": {
                    "TimeoutInSeconds": 300,
                    "MemoryInMB": 1000,
                    "ActiveTracing": false
                },
                "SuccessRetentionPeriodInDays": 31,
                "FailureRetentionPeriodInDays": 31,
                "Status": {
                "State": "RUNNING"
                },
                "Timeline": {
                    "Created": "2024-10-15T18:55:15.168000+05:30",
                    "LastModified": "2024-10-15T18:55:40.540000+05:30",
                    "LastStarted": "2024-10-15T18:55:40.540000+05:30"
                },
                "ArtifactS3Location": "cw-syn-results-123456789012-us-east-1/canary/us-east-1/demo_canary-a12-a123bc456789",
                "EngineArn": "arn:aws:lambda:us-east-1:123456789012:function:cwsyn-demo_canary-a1b2c3d4-5678-90ab-cdef-example111118:1",
                "RuntimeVersion": "syn-nodejs-puppeteer-9.1",
                "Tags": {
                    "blueprint": "heartbeat"
                }
            }
        ]
    }

For more information, see `Synthetic monitoring (canaries) <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics_Canaries.html>`__ in the *Amazon CloudWatch User Guide*.