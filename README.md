As a devops or cloud engineer its our responsibility to check the resources on cloud and monitor if there is unnecessary resources are there or resource which are no longer in use but developer did not delete that resource it can cause huge billing.
In this project, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.
**Description:**
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
