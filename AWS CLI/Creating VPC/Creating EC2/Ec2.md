#### Creating Ec2 instance

* Google command is : Aws cli run inatance

command is : aws cli <servicename> <command> [<subcommands>] [--argname argvalue] [argvalue]

                   : aws ec2 run-instances \
                     --image-id ami-0123b531fc646552f \
                     --count 1 \
                     --instance-type t2.micro

                     
      aws ec2 run-instances --image-id ami-0123b531fc646552f --count 1 --instance-type t2.micro            o/p : "PrivateIpAddress": "172.31.24.128",         