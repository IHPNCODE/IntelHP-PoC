# IntelHP-PoC
Stand up a High-Performance Computing (HPC) Proof of Concept on AWS using Amazon EC2, Amazon EFS, and AWS ParallelCluster
1. Overview
Goal: Stand up a High-Performance Computing (HPC) Proof of Concept on AWS using Amazon EC2, Amazon EFS, and AWS ParallelCluster.
Scope: Demonstrate end-to-end setup—from network/security config to running a Slurm job—using a minimal configuration.
2. Architecture Diagram (Conceptual)
Head Node (Slurm controller)
Compute Nodes (Autoscaled, on-demand HPC workers)
Shared Storage (Amazon EFS)
VPC + Subnet(s) (Ensure correct routing for public or private access)
Security Groups (Open required ports: SSH, NFS 2049, etc.)
(Include or attach a diagram showing the head node, compute nodes, and EFS.)

3. Prerequisites
AWS Account
Sufficient permissions (IAM) to create EC2, EFS, VPC resources, etc.
Key Pair
For SSH access to HPC cluster head node (e.g., MyKeyPair).
AWS CLI + ParallelCluster
AWS CLI configured for us-east-1.
ParallelCluster v3.x (e.g., 3.12.0).
Public Subnet (Recommended for direct SSH from CloudShell or local machine)
Alternatively, a private subnet with a bastion/VPN.
