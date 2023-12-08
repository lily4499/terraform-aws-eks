module "eks" {    
    source         = "lily4499/eks/aws"   
    region         = "us-east-1" // Set your desired region here 
    version        = ">= 1.0.0, < 2.0.0"    
    vpc_cidr       = "10.0.0.0/16"    
    dns_hostnames  = true    
    dns_support    = true    
    pub_one_cidr   = "10.0.1.0/24"    
    pub_two_cidr   = "10.0.2.0/24"    
    priv_one_cidr  = "10.0.3.0/24"    
    priv_two_cidr  = "10.0.4.0/24"    
    vpc_id         = "aws_vpc.eks_vpc.id"    
    eks_version    = "1.26"    
    ami_type       = "AL2_x86_64"    
    instance_types = ["t3.small", "t3.medium", "t3.large"]   
    capacity_type  = "ON_DEMAND"    
}  

