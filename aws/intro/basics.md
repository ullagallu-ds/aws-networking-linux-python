# S3
- it is highly avialable[always accessible no downtime] sclable[storage any amount of data] and durable[dataloss] object storage
- store any type of data[audio,video,zip,tar,logs,pdf]
- s3 service is global buckets are regional bucket names are unique
- realtime used for vpc flow logs,cloud trail logs, LB access logs,waf logs and payment invoices
- unlimited storage but single object size more than 5TB only


**storage classes**
1. S3 standard
2. Intelligent tiering
3. S3 standard-IA[vpc flow logs,cloud trail logs, LB access logs,waf logs]
4. S3 one-zone-IA[In Prod we cannot use]
5. S3 Glacier
as per security policy we need to maintain vpc flow logs atleast 18 months we place in S3 Glacier
S3 Life Cycle to move vpc flow logs from standard to Glacier Deep archive after 18 months we can delete

We are disabled ACL's recommend we use bucket policy for object management

**Bucket versioning**
- keep the multiple versions of object
- without bucket versioning if you upload object again and again it will overide
- if you enable bucket versioning it keep the multiple versions of same object
- Generally we use terraform.tfstate we can enable for logs and all we don't 

we are always use SSE encryption only 

**server access logging**
- capture uploading and downloding of objects in bucket 99% we won't enable server logging

**event notifications**
- any event happend inside buket like creation,deleteion,upload object it will send notifications
- frequntly used in realtime

**static website hosting**


