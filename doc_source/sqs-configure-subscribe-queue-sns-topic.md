# Subscribing an Amazon SQS queue to an Amazon SNS topic \(console\)<a name="sqs-configure-subscribe-queue-sns-topic"></a>

You can subscribe one or more Amazon SQS queues to an Amazon Simple Notification Service \(Amazon SNS\) topic\. When you publish a message to a topic, Amazon SNS sends the message to each of the subscribed queues\. Amazon SQS manages the subscription and any necessary permissions\. For more information about Amazon SNS, see [What is Amazon Simple Notification Service?](https://docs.aws.amazon.com/sns/latest/dg/welcome.html) in the *Amazon Simple Notification Service Developer Guide*\.

When you subscribe an Amazon SQS queue to an SNS topic, Amazon SNS uses HTTPS to forward messages to Amazon SQS\. For information about using Amazon SNS with encrypted Amazon SQS queues, see [Configure KMS permissions for AWS services](sqs-key-management.md#compatibility-with-aws-services)\.

**To subscribe a queue to an SNS topic \(console\)**

1. Open the Amazon SQS console at [https://console\.aws\.amazon\.com/sqs/](https://console.aws.amazon.com/sqs/)\.

1. In the navigation pane, choose **Queues**\.

1. From the list of queues, choose the queue to subscribe to the SNS topic\.

1. From **Actions**, choose **Subscribe to Amazon SNS topic**\.

1. From the **Specify an Amazon SNS topic available for this queue** menu, choose the SNS topic for your queue\. 

   If the SNS topic isn't listed in the menu, choose **Enter Amazon SNS topic ARN** and then enter the topic's Amazon Resource Name \(ARN\)\.

1. Choose **Save**\. 

1. To verify the result of the subscription, publish to the topic and then view the message that the topic sends to the queue\. For more information, see [Publishing a message to an Amazon SNS topic](https://docs.aws.amazon.com/sns/latest/dg/sns-publishing-messages.html) in the *Amazon Simple Notification Service Developer Guide*\.

If your Amazon SQS queue and SNS topic are in different AWS accounts, the topic owner must first confirm the subscription\. For more information, see [Confirm the subscription](https://docs.aws.amazon.com/sns/latest/dg/SendMessageToHttp.confirm.html) in the *Amazon Simple Notification Service Developer Guide*\.

For information on subscribing to a cross\-region SNS topic, see [Sending Amazon SNS messages to an Amazon SQS queue or AWS Lambda function in a different Region](https://docs.aws.amazon.com/sns/latest/dg/sns-cross-region-delivery.html) in the *Amazon Simple Notification Service Developer Guide*