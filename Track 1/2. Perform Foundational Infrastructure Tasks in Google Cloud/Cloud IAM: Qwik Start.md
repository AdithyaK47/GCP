# Cloud IAM: Qwik Start

# IAM (Identity and Access Management)

IAM lets user to grant granular access to specific Google Cloud resources and helps prevent access to other resources. 
IAM lets the user to adopt the security principle of least privilege, where one can grant only necessary permissions to access specific resources.

With IAM, one can manage access control by defining who (identity) has what access (role) for which resource. 
For example, Compute Engine virtual machine instances, Google Kubernetes Engine (GKE) clusters, and Cloud Storage buckets are all Google Cloud resources. 
The organizations, folders, and projects that one use to organize their resources are also resources.
In IAM, permission to access a resource isn't granted directly to the end user. Instead, permissions are grouped into roles, and roles are granted to authenticated members. 
An IAM policy defines and enforces what roles are granted to which members, and this policy is attached to a resource. 
When an authenticated member attempts to access a resource, IAM checks the resource's policy to determine whether the action is permitted.

For understanding roles: https://cloud.google.com/iam/docs/understanding-roles#primitive_roles
