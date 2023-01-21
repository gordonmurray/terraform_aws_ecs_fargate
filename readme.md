# Terraform AWS ECS Fargate service

## Cost estimate

```
Project: gordonmurray/terraform_aws_ecs_fargate

 Name                                Monthly Qty  Unit              Monthly Cost 
                                                                                 
 aws_ecr_repository.main                                                         
 └─ Storage                       Monthly cost depends on usage: $0.10 per GB    
                                                                                 
 aws_ecs_service.main                                                            
 ├─ Per GB per hour                            1  GB                       $3.24 
 └─ Per vCPU per hour                        0.5  CPU                     $14.78 
                                                                                 
 aws_lb.main                                                                     
 ├─ Application load balancer                730  hours                   $16.43 
 └─ Load balancer capacity units  Monthly cost depends on usage: $5.84 per LCU   
                                                                                 
 aws_nat_gateway.main[0]                                                         
 ├─ NAT gateway                              730  hours                   $32.85 
 └─ Data processed                Monthly cost depends on usage: $0.045 per GB   
                                                                                 
 aws_nat_gateway.main[1]                                                         
 ├─ NAT gateway                              730  hours                   $32.85 
 └─ Data processed                Monthly cost depends on usage: $0.045 per GB   
                                                                                 
 aws_nat_gateway.main[2]                                                         
 ├─ NAT gateway                              730  hours                   $32.85 
 └─ Data processed                Monthly cost depends on usage: $0.045 per GB   
                                                                                 
 OVERALL TOTAL                                                           $133.00 
──────────────────────────────────
47 cloud resources were detected:
∙ 7 were estimated, 5 of which include usage-based costs, see https://infracost.io/usage-file
∙ 40 were free:
  ∙ 6 x aws_route_table_association
  ∙ 6 x aws_subnet
  ∙ 4 x aws_route
  ∙ 4 x aws_route_table
  ∙ 3 x aws_eip
  ∙ 2 x aws_alb_listener
  ∙ 2 x aws_appautoscaling_policy
  ∙ 2 x aws_iam_role
  ∙ 2 x aws_iam_role_policy_attachment
  ∙ 2 x aws_security_group
  ∙ 1 x aws_alb_target_group
  ∙ 1 x aws_ecr_lifecycle_policy
  ∙ 1 x aws_ecs_cluster
  ∙ 1 x aws_ecs_task_definition
  ∙ 1 x aws_iam_policy
  ∙ 1 x aws_internet_gateway
  ∙ 1 x aws_vpc
  ```