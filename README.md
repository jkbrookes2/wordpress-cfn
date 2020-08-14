# wordpress-cfn
This is a CloudFormation script that downloads and installs a wordpress site without any interaction.

The historical need for this for me was that I was using a temporary cloud playground where I 1) did not have access to the Bitnami wordpress AMIs and 2) that was regularly cleaned up and terminated.  This script allows me to spin up a stock site and give me some options to continue playing with the infrastructure.

Some changes I'd like to continue making to this script:
* Separate out the RDS database as that takes so much time to spin up.  I could have a separate cfn that exports the required information for the application to use.
* Autogenerate the database and wordpress passwords here and store them as secrets
* Use an Aurora cluster instead of a single MySQL RDS instance
* Go from a single web server to a cluster backed by EFS
