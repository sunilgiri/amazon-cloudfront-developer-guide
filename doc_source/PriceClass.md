# Choosing the Price Class for a CloudFront Distribution<a name="PriceClass"></a>

CloudFront has edge locations all over the world\. Our cost for each edge location varies and, as a result, the price that we charge you varies depending on the edge location from which CloudFront serves your requests\.

CloudFront edge locations are grouped into geographic regions, and we've grouped regions into price classes\. The default price class includes all regions\. Another price class includes most regions \(the United States; Europe; Hong Kong, Korea, and Singapore; Japan; and India regions\) but excludes the most\-expensive regions\. A third price class includes only the least\-expensive regions \(the United States and Europe regions\)\.

By default, CloudFront responds to requests for your objects based only on performance: objects are served from the edge location for which latency is lowest for that viewer\. If you're willing to accept higher latency for your viewers in some geographic regions in return for lower cost, you can choose a price class that doesn't include all CloudFront regions\. Although CloudFront will serve your objects only from the edge locations in that price class, it still serves content from the edge location that has the lowest latency among the edge locations in your selected price class\. However, some of your viewers, especially those in geographic regions that are not in your price class, may see higher latency than if your content were being served from all CloudFront edge locations\. For example, if you choose the price class that includes only the United States and Europe, viewers in Australia and in Asia may experience higher latency than if you choose the price class that includes Australia and Asia\.

If you choose a price class that does not include all edge locations, CloudFront may still occasionally serve requests for your content from an edge location in a region that is not included in your price class\. When this happens, you are not charged the rate for the more expensive region from which your objects were served\. Instead, you're charged the rate for the least\-expensive region in your selected price class\.

You can choose a price class when you create or update a CloudFront web distribution or RTMP distribution\. To find the applicable topic about creating or updating a web or an RTMP distribution using the CloudFront console or API, see [Working with Distributions](distribution-working-with.md)\. 

If you're creating or updating a distribution by using the CloudFront API, one of the AWS SDKs, or AWS CloudFormation, see the applicable topic for a list of valid values \(search for `PriceClass`\):

+ **Web distributions** – [DistributionConfig Complex Type](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DistributionConfig.html)

+ **RTMP distributions** – [StreamingDistributionConfig Complex Type](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_StreamingDistributionConfig.html)

For more information about CloudFront pricing and price classes, go to [Amazon CloudFront Pricing](http://aws.amazon.com/cloudfront/pricing/)\.