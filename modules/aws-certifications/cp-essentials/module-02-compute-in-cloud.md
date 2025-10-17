# AWS Cloud Practitioner Essentials 
## Module 2: Compute in the Cloud - Notes

## 🎯 Module Overview
<!-- **Date**: 16/10/2025 -->
**Focus**: AWS Compute Services - EC2, Auto Scaling, Load Balancing, Messaging

## 📚 Core Concepts Mastered

### 1. Amazon EC2 Fundamentals
**What is EC2?**
- Elastic Compute Cloud - virtual servers in the cloud
- On-demand compute capacity without physical hardware
- **Multi-tenancy**: Multiple VMs share physical host with isolation via hypervisor
- Complete control over OS, software, and configurations

**Key EC2 Characteristics:**
- **Flexible**: Choose OS (Windows/Linux), configure software
- **Resizable**: Vertical scaling (change instance size)
- **Cost-effective**: Pay only for running instances
- **Quick deployment**: Minutes vs weeks/months for physical servers

### 2. EC2 Instance Types & Families

| Instance Family | Best For | Use Cases |
|----------------|----------|-----------|
| **General Purpose** | Balanced compute, memory, networking | Web servers, code repositories |
| **Compute Optimized** | Compute-intensive tasks | Gaming servers, HPC, ML modeling |
| **Memory Optimized** | Memory-intensive workloads | Large datasets, real-time analytics |
| **Accelerated Computing** | Graphics/float calculations | GPUs, pattern matching, ML |
| **Storage Optimized** | High local storage performance | Large databases, data warehousing |

### 3. EC2 Pricing Models

**On-Demand Instances**
- Pay by second/hour with no commitment
- Perfect for unpredictable workloads
- No upfront costs

**Savings Plans**
- Commit to 1-3 years for consistent usage
- Up to 72% savings
- Flexible across instance types

**Reserved Instances**
- 1-3 year commitment for specific instances
- Up to 75% savings
- Payment options: All/Partial/No upfront

**Spot Instances**
- Bid on spare capacity (up to 90% off)
- Can be interrupted with 2-minute warning
- Ideal for fault-tolerant workloads

**Dedicated Hosts/Instances**
- Physical server isolation
- For compliance/licensing requirements
- Complete control vs shared infrastructure

### 4. Provisioning AWS Resources

**Three Methods:**
1. **AWS Management Console** - Web UI for visual management
2. **AWS CLI** - Command-line for automation/scripting
3. **AWS SDK** - Programmatic access for application integration

**Shared Responsibility Model for EC2:**
- **AWS**: Physical security, hypervisor, infrastructure
- **Customer**: OS security, applications, data, network config

### 5. Auto Scaling & Elasticity

**Scalability vs Elasticity:**
- **Scalability**: Long-term capacity planning (scale up/out)
- **Elasticity**: Real-time adjustment to demand

**EC2 Auto Scaling Components:**
- **Minimum Capacity**: Baseline instances always running
- **Desired Capacity**: Ideal number for current load
- **Maximum Capacity**: Upper limit to prevent over-scaling

**Benefits:**
- High availability across multiple AZs
- Cost optimization (scale in during low demand)
- Automatic failure recovery

### 6. Elastic Load Balancing (ELB)

**Purpose**: Distribute traffic across multiple EC2 instances

**Routing Methods:**
- **Round Robin**: Cyclic distribution
- **Least Connections**: To least busy server
- **IP Hash**: Consistent server per client IP
- **Least Response Time**: To fastest responding server

**Benefits:**
- Single point of contact for applications
- Automatic traffic distribution
- Works seamlessly with Auto Scaling
- Handles maintenance and failover

### 7. Messaging & Queuing Services

**Tightly Coupled vs Loosely Coupled:**
- **Tight**: Direct communication (cascading failures)
- **Loose**: Buffer/queue between components (fault isolation)

**Amazon SQS (Simple Queue Service)**
- Message queuing for decoupled components
- Messages stored until processed
- Prevents message loss during failures

**Amazon SNS (Simple Notification Service)**
- Publish-subscribe model
- Immediate message delivery
- Supports SMS, email, mobile push

**Amazon EventBridge**
- Event-driven architecture
- Route events between services
- Handles high volumes with reliability

## 💡 Key Technical Insights

### EC2 Launch Process:
1. **Choose AMI** - Pre-configured OS template
2. **Select Instance Type** - Hardware specifications
3. **Configure Networking** - Security groups, VPC
4. **Add Storage** - EBS volumes
5. **Launch** - Instance becomes available in minutes

### Real-World Applications:
- **Web Applications**: EC2 + Auto Scaling + ELB
- **Data Processing**: Spot Instances for cost savings
- **Microservices**: SQS/SNS for inter-service communication
- **Healthcare Systems**: Load balancing for patient portals

## 🎯 Assessment Performance
**Perfect understanding demonstrated in:**
- EC2 instance type selection for specific workloads
- Pricing model optimization
- Auto Scaling configuration
- Load balancing strategies
- Messaging service use cases

## 🔗 Important Resources
- [AWS Compute Services](https://aws.amazon.com/products/compute/)
- [EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/)
- [Auto Scaling Documentation](https://aws.amazon.com/ec2/autoscaling/)
- [Hands-On Compute Tutorials](https://aws.amazon.com/getting-started/hands-on/?awsf.getting-started-category=category%23compute)

---

*Ready for hands-on implementation and Module 3: Exploring Compute Services*