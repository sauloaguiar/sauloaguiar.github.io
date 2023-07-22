---
layout: post
title: AWS - Writing to S3 bucket in different accounts
---


When writing to a s3 bucket from a different account, we might need need a different ACL policy.

From the [knowledge center](https://repost.aws/knowledge-center/s3-bucket-owner-full-control-acl), I noticed this

"By default, in a cross-account scenario where other AWS accounts upload objects to your Amazon S3 bucket, the objects remain owned by the uploading account. When the bucket-owner-full-control ACL is added, the bucket owner has full control over any new objects that are written by other accounts.""




Code to include the specified policy

```jsx
const uploadParams = {
  Bucket: bucket,
  Key: filePath,
  Body: buffer,
  ContentType: contentType,
  ACL: 'bucket-owner-full-control',
};
const command = new PutObjectCommand(uploadParams);
```

When the bucket-owner-full-control ACL is added, the bucket owner has full control over any new objects that are written by other AWS accounts. This ACL is also required if the destination bucket has enabled S3 Object Ownership. When S3 Object Ownership is enabled, it updates the owner of new objects to the destination account. <br />

*Important*: Granting cross-account access through bucket and object ACLs doesn't work for buckets that have S3 Object Ownership set to Bucket Owner Enforced

[Reference material for object ownership](https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html)