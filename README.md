# AWS Lambda - RDS Start / Stop Script

AWS RDS Start and Stop Lambda Script.

- Python 3.10

## Json

- All Database

  ```json
  {
    "Region": "xxxxxx",
    "Action": "start"   // start or stop
  }
  ```

- Tag filter

  ```json
  {
    "Region": "xxxxxx",
    "TagKey": "xxxxxx",
    "TagValue": "xxxxxx",
    "Action": "start"   // start or stop
  }
  ```

  

## Lambda IAM Role Policy

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Action": [
                "logs:CreateLogGroup",
                "logs:CreateLogStream",
                "logs:PutLogEvents",
                "rds:DescribeDBClusterEndpoints",
                "rds:DescribeDBClusterParameterGroups",
                "rds:DescribeDBClusterParameters",
                "rds:DescribeDBClusters",
                "rds:DescribeDBEngineVersions",
                "rds:DescribeDBInstances",
                "rds:DescribeDBLogFiles",
                "rds:DescribeGlobalClusters",
                "rds:DescribeOptionGroups",
                "rds:DescribePendingMaintenanceActions",
                "rds:DescribeReservedDBInstances",
                "rds:DescribeReservedDBInstancesOfferings",
                "rds:DescribeSourceRegions",
                "rds:DescribeValidDBInstanceModifications",
                "rds:ListTagsForResource",
                "rds:StartDBCluster",
                "rds:StartDBInstance",
                "rds:StopDBCluster",
                "rds:StopDBInstance"
            ],
            "Effect": "Allow",
            "Resource": "*"
        }
    ]
}
```

