# Azure Solution Templates 🚀

A curated collection of Azure CLI scripts for deploying popular cloud infrastructure patterns and solutions. Perfect for learning, prototyping, and rapid deployment of Azure resources.

## 📋 Template Catalog

### 🌐 Networking
- **[Hub-Spoke Firewall](./templates/networking/hub-spoke-firewall.azcli)** - Complete hub-and-spoke network topology with Azure Firewall
- **[VPN Gateway Setup](./templates/networking/vpn-gateway.azcli)** - Site-to-Site VPN configuration
- **[Load Balancer with Backend Pool](./templates/networking/load-balancer.azcli)** - Application load balancer setup

### 🖥️ Web Applications
- **[LAMP Stack](./templates/web-apps/lamp-stack.azcli)** - Linux, Apache, MySQL, PHP web application
- **[Static Website + CDN](./templates/web-apps/static-website-cdn.azcli)** - Static site hosting with Azure CDN
- **[App Service + Database](./templates/web-apps/webapp-database.azcli)** - Scalable web app with Azure SQL Database

### 🗄️ Databases
- **[Azure SQL + Backup](./templates/databases/sql-database-backup.azcli)** - SQL Database with automated backup
- **[Cosmos DB Multi-Region](./templates/databases/cosmosdb-multiregion.azcli)** - Globally distributed NoSQL database
- **[PostgreSQL Flexible Server](./templates/databases/postgresql-flexible.azcli)** - Managed PostgreSQL with high availability

### 🐳 Containers
- **[AKS Cluster](./templates/containers/aks-cluster.azcli)** - Azure Kubernetes Service with monitoring
- **[Container Instances](./templates/containers/container-instances.azcli)** - Serverless container deployment
- **[Container Registry](./templates/containers/container-registry.azcli)** - Private Docker registry setup

### 💾 Storage
- **[Blob Storage + CDN](./templates/storage/blob-storage-cdn.azcli)** - Scalable blob storage with CDN
- **[File Share](./templates/storage/file-share.azcli)** - Azure Files for shared storage
- **[Data Lake](./templates/storage/data-lake.azcli)** - Big data storage solution

### 🔒 Security
- **[Key Vault Setup](./templates/security/key-vault.azcli)** - Secure secrets management
- **[Identity Management](./templates/security/identity-management.azcli)** - Azure AD integration
- **[Security Center](./templates/security/security-center.azcli)** - Security monitoring setup

### ⚡ Compute
- **[Auto-Scaling VM Set](./templates/compute/vmss-autoscale.azcli)** - Virtual Machine Scale Set with auto-scaling
- **[Windows VM Domain Join](./templates/compute/windows-vm-domain.azcli)** - Windows VM with domain integration
- **[GPU Compute](./templates/compute/gpu-compute.azcli)** - High-performance computing setup

### 📊 Analytics
- **[Data Factory Pipeline](./templates/analytics/data-factory.azcli)** - ETL pipeline setup
- **[Synapse Analytics](./templates/analytics/synapse-analytics.azcli)** - Data warehouse solution
- **[Stream Analytics](./templates/analytics/stream-analytics.azcli)** - Real-time data processing

## 🚀 Quick Start

### Prerequisites
- Azure CLI installed and configured
- Active Azure subscription
- Appropriate permissions for resource creation

### Usage
1. **Clone the repository:**
   ```bash
   git clone https://github.com/mrcloudchase/good-azure-tools.git
   cd good-azure-tools
   ```

2. **Choose a template:**
   ```bash
   cd templates/[category]/
   ```

3. **Review and customize variables:**
   ```bash
   # Edit the script to match your requirements
   nano [template-name].azcli
   ```

4. **Execute the template:**
   ```bash
   # Make script executable
   chmod +x [template-name].azcli
   
   # Run the script
   ./[template-name].azcli
   ```

## 📖 Template Structure

Each template follows a consistent structure:

```bash
#!/bin/bash
###############################
####### SCRIPT DETAILS ########
# Name: [Template Name]
# Purpose: [Brief description]
# Category: [networking|web-apps|databases|etc.]
# Estimated Cost: [Cost estimate]
# Deployment Time: [Time estimate]
###############################

##############################
##### START - VARIABLES ######
##############################
# [Variable definitions with descriptions]

##############################
##### END - VARIABLES ########
##############################

##############################
####### START - SCRIPT #######
##############################
# [Resource creation commands with comments]

##############################
######## END - SCRIPT ########
##############################
```

## 🛠️ Customization Guidelines

### For Azure Sandbox/Learning Environments:
Most templates are pre-configured for sandbox environments with automatic resource group detection:
```bash
$rg = az group list --query '[].name' -o tsv
$location = az group list --query '[].location' -o tsv
```

### For Production Use:
1. Replace resource group variables with your own:
   ```bash
   rg="your-resource-group-name"
   location="your-preferred-location"
   ```

2. Review and adjust:
   - Resource naming conventions
   - SKU sizes and pricing tiers
   - Security configurations
   - Network address spaces

## 💡 Best Practices

- **Review costs** before deployment using Azure Pricing Calculator
- **Start with smaller SKUs** for testing and scale up as needed
- **Use resource tags** for organization and cost tracking
- **Enable monitoring** and alerting for production workloads
- **Follow security best practices** (least privilege, network segmentation)

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/new-template`)
3. **Follow the template structure** outlined above
4. **Test your template** thoroughly
5. **Update the README** with your new template
6. **Submit a pull request**

### Template Contribution Checklist:
- [ ] Follows consistent naming convention
- [ ] Includes comprehensive comments
- [ ] Has variable definitions at the top
- [ ] Includes error handling where appropriate
- [ ] Tested in sandbox environment
- [ ] Documentation added to README

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

These templates are designed for learning and development purposes. For production deployments:
- Review security configurations
- Adjust resource sizing appropriately
- Implement proper backup and disaster recovery
- Follow your organization's compliance requirements

## 📞 Support

- **Issues**: Report bugs or request features via [GitHub Issues](https://github.com/mrcloudchase/good-azure-tools/issues)
- **Discussions**: Join the conversation in [GitHub Discussions](https://github.com/mrcloudchase/good-azure-tools/discussions)

---

**Happy Cloud Building!** ☁️✨