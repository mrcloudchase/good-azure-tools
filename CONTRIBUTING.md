# Contributing to Azure Solution Templates

Thank you for your interest in contributing to this repository! This guide will help you create consistent, high-quality Azure solution templates.

## 📋 Template Categories

We organize templates into the following categories:

- **`networking/`** - Network infrastructure, firewalls, VPNs, load balancers
- **`web-apps/`** - Web applications, static sites, app services
- **`databases/`** - SQL databases, NoSQL, data storage solutions
- **`containers/`** - Kubernetes, container instances, registries
- **`storage/`** - Blob storage, file shares, data lakes
- **`security/`** - Key vaults, identity management, security centers
- **`compute/`** - Virtual machines, scale sets, functions
- **`analytics/`** - Data factories, analytics workspaces, AI/ML

## 🏗️ Template Structure Standard

Every template must follow this exact structure:

```bash
#!/bin/bash
###############################
####### SCRIPT DETAILS ########
# Name: [Descriptive Template Name]
# Purpose: [Brief description of what this template creates]
# Category: [category-name]
# Estimated Cost: [Monthly cost estimate in USD]
# Deployment Time: [Expected deployment duration]
# Disclaimer: This script is intended for ACG Azure Cloud Sandbox environments
###############################

##############################
##### START - VARIABLES ######
##############################

# Get resource group and set to variable $rg
rg=$(az group list --query '[].name' -o tsv)

# Assign location variable to playground resource group location
location=$(az group list --query '[].location' -o tsv)

# [Your template-specific variables here]
# Use descriptive names and include comments

##############################
##### END - VARIABLES ########
##############################

##############################
####### START - SCRIPT #######
##############################

echo "🚀 Starting [Template Name] deployment..."

# [Your deployment logic here]
# Include progress indicators with emoji
# Add descriptive comments for each major section

## OUTPUT INFORMATION
echo ""
echo "🎉 [Template Name] deployment completed successfully!"
echo ""
echo "📋 Deployment Summary:"
echo "====================="
# [Include all important deployment details]

##############################
######## END - SCRIPT ########
##############################
```

## ✅ Template Requirements

### 1. Header Information
- **Name**: Clear, descriptive template name
- **Purpose**: One-line description of what the template creates
- **Category**: Must match directory structure
- **Estimated Cost**: Monthly cost in USD (use ranges like $10-30)
- **Deployment Time**: Realistic time estimate
- **Disclaimer**: Include ACG disclaimer for sandbox usage

### 2. Variables Section
- **Resource Group**: Always use `$(az group list --query '[].name' -o tsv)`
- **Location**: Always use `$(az group list --query '[].location' -o tsv)`
- **Naming**: Use descriptive variable names with consistent patterns
- **Random Elements**: Use `$(shuf -i 1000-9999 -n 1)` for unique naming
- **Comments**: Explain the purpose of each variable group

### 3. Script Logic
- **Progress Indicators**: Use emoji and descriptive messages
- **Error Handling**: Include basic error handling where appropriate
- **Modularity**: Break complex deployments into logical sections
- **Comments**: Document each major section and complex commands

### 4. Output Section
- **Summary**: Comprehensive deployment summary
- **URLs/Endpoints**: All access points and management URLs
- **Commands**: Useful management commands for ongoing operations
- **Portal Links**: Direct links to Azure Portal resources
- **Security Notes**: Important security considerations
- **Tips**: Best practices and optimization suggestions

## 📝 Content Guidelines

### Naming Conventions
- **Files**: Use kebab-case (e.g., `hub-spoke-firewall.azcli`)
- **Resources**: Include random suffix for uniqueness
- **Variables**: Use camelCase or snake_case consistently

### Documentation
- **Comments**: Explain WHY, not just WHAT
- **Error Messages**: Be helpful and actionable
- **Success Messages**: Include next steps and usage information

### Resource Configuration
- **SKUs**: Start with basic/standard tiers for cost efficiency
- **Security**: Enable security features by default
- **Monitoring**: Include logging and monitoring where appropriate
- **Tags**: Consider adding resource tags for organization

## 🧪 Testing Requirements

Before submitting a template:

1. **Test in ACG Environment**: Verify the template works in a fresh ACG sandbox
2. **Validate Output**: Ensure all resources are created correctly
3. **Check URLs**: Verify all provided URLs and portal links work
4. **Cost Validation**: Confirm cost estimates are reasonable
5. **Documentation**: Test all provided commands and examples

## 📥 Submission Process

1. **Fork the Repository**
   ```bash
   git fork https://github.com/mrcloudchase/good-azure-tools.git
   ```

2. **Create Feature Branch**
   ```bash
   git checkout -b feature/new-template-name
   ```

3. **Add Your Template**
   - Place in appropriate category directory
   - Follow the exact structure standard
   - Test thoroughly

4. **Update README**
   - Add your template to the appropriate category section
   - Include the template link and description
   - Maintain alphabetical order within categories

5. **Submit Pull Request**
   - Use descriptive title: "Add [Template Name] template"
   - Include testing details in description
   - Reference any issues addressed

## 🔍 Review Criteria

Templates are reviewed for:

- **Structure Compliance**: Follows exact template standard
- **Functionality**: Creates resources as described
- **Documentation**: Clear, complete, and accurate
- **Security**: Follows Azure security best practices
- **Cost Efficiency**: Reasonable cost estimates and resource sizing
- **Error Handling**: Graceful handling of common failure scenarios
- **Code Quality**: Clean, readable, well-commented code

## 💡 Template Ideas

Looking for inspiration? Consider these popular solution patterns:

### High Priority
- WordPress on App Service + MySQL
- DevOps pipeline with Azure DevOps
- Monitoring solution with Application Insights
- Backup solution with Recovery Services Vault
- Auto-scaling web app with Application Gateway

### Medium Priority
- IoT solution with IoT Hub and Stream Analytics
- Machine learning workspace with Azure ML
- Data pipeline with Event Hubs and Functions
- Multi-tier application with App Gateway
- Disaster recovery setup

### Advanced
- Microservices architecture with Service Fabric
- Big data processing with HDInsight
- Enterprise integration with Logic Apps
- Hybrid connectivity with ExpressRoute
- Zero-trust security architecture

## 🚀 Quality Standards

### Code Excellence
- Use latest Azure CLI syntax
- Include parameter validation where appropriate
- Handle common error scenarios gracefully
- Optimize for readability and maintainability

### User Experience
- Clear progress indicators throughout deployment
- Comprehensive output with actionable information
- Helpful error messages with troubleshooting hints
- Links to relevant documentation and resources

### Security First
- Enable security features by default
- Use least privilege access principles
- Include security recommendations in output
- Validate inputs to prevent injection attacks

## 📞 Getting Help

- **Questions**: Open a [GitHub Discussion](https://github.com/mrcloudchase/good-azure-tools/discussions)
- **Bugs**: Report via [GitHub Issues](https://github.com/mrcloudchase/good-azure-tools/issues)
- **Ideas**: Share in [GitHub Discussions](https://github.com/mrcloudchase/good-azure-tools/discussions)

## 📄 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for contributing to the Azure community!** 🌟