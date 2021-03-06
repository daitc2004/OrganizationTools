# Multi Account Org Setup

Tools to setup Multi-account permissions using AWS Organizations servcice control policies and SSO Permissions Policies.

## Scripts

  * **`update-scp.py`**: updates SCP in the Organization from local SCP files. 

## Configuration Files

  * **`scp`**: directory containing SCP json files.
  * **`sso`**: directory containing AWS SSO Permissions Policies. 
    This is synced manually using AWS Console, since the SSO API is not public. 


## Account Cleaner

Yet another utility to nuke resources from AWS accounts. 
Great after running a class to cleanup resources created in reusable testing accounts, student accounts.

Because resource dependencies may require time to be deleted, you may encounter errors while deleting resources with dependencies. If this happens, pause for awhile to let the dependencies delete, then re-run the script.

### Resources:
  * **'nuke-resources.py'**: Currently used to cleanup DMS, Glue, S3, CloudFormation templates for the data engineering immersion day. 
    Requires short term STS creds environment variables to be set for each account to be cleaned-up.



