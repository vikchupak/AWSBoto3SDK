### Boto3 lib
https://pypi.org/project/boto3/

```bash
pip install boto3
```

### Boto3 documentation
https://boto3.amazonaws.com/v1/documentation/api/latest/index.html

```python
import boto3

ec2_client = boto3.client('ec2')
ec2_resource = boto3.resource('ec2')

# Returns dictionary
vpcs = ec2_client.describe_vpcs()

# Returns newly created resource instnce
new_vpc_resource = ec2_resource.create_vpc(CidrBlock='10.0.0.0/16')
new_vpc_resource.create_subnet(CidrBlock='10.0.1.0/24')
```

### client vs resource
- client
  - more low level API
  - one-to-one mapping to underlying HTTP operations
- resource
  - provides resource objects to access attributes and perform actions
  - high-level and object-oriented
