### Creating VPC:

command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            Google it for aws cli vpc
            aws ec2 create-vpc --cidr-block '192.168.0.0/16' --instance-tenancy dedicated
            vpcid = vpc-00edce496d2f57c95


### Creating subnet1:

command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli subnet
            aws ec2 create-subnet --availability-zone 'ap-south-1a' --cidr-block '192.168.0.0/24' --vpc-id vpc-00edce496d2f57c95

            subnet1id = subnet-07b777847d8fd5cdb

### creating subnet2:

command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli subnet
            aws ec2 create-subnet --availability-zone 'ap-south-1b' --cidr-block '192.168.1.0/24' --vpc-id vpc-00edce496d2f57c95

            subnet2id = subnet-0c4cd58c6b289c2b6
            
### creating subnet3:

command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli subnet
            aws ec2 create-subnet --availability-zone 'ap-south-1c' --cidr-block '192.168.2.0/24' --vpc-id vpc-00edce496d2f57c95
        
            subnet2id = subnet-0dce844fe76a2dae1

### create&attaching Internetgateway to VPC:

command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli internetgateway
            aws ec2 create-internet-gateway     
            igwid = igw-0cdb26c1f7650a499
    
### attaching igw id to VPC: aws attach-internet-gateway:

command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli attach internetgateway
            aws ec2 attach-internet-gateway --internet-gateway-id igw-0cdb26c1f7650a499 --vpc-id vpc-00edce496d2f57c95

### creating route table:

command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli routetable
            aws ec2 create-route-table --vpc-id vpc-00edce496d2f57c95
            routetableid = rtb-07b2165dc313e37e7

### associating-route table:

### subnet1:
command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli associate-route-table
            aws ec2 associate-route-table --route-table-id rtb-07b2165dc313e37e7 --subnet-id subnet-07b777847d8fd5cdb

            AssociationId = rtbassoc-062f8ca8b32321104

### subnet2:
command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli associate-route-table
            aws ec2 associate-route-table --route-table-id rtb-07b2165dc313e37e7 --subnet-id subnet-0c4cd58c6b289c2b6

            AssociationId = rtbassoc-0b291555fce1ec8e8

### subnet3:
command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli associate-route-table
            aws ec2 associate-route-table --route-table-id rtb-07b2165dc313e37e7 --subnet-id subnet-0dce844fe76a2dae1

            AssociationId = rtbassoc-08eb496c4990693ea

### creating route && attaching to internetgateway:

command is: aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

            aws cli route
            aws ec2 create-route --destination-cidr-block '0.0.0.0/0' --gateway-id igw-0cdb26c1f7650a499 --route-table-id rtb-07b2165dc313e37e7 





            
                                
