# Optimizing Security Monitoring: A Hybrid Approach with Containerized Wazuh and Splunk, and Locally Deployed Suricata

## Objective
This project aims to enhance security monitoring capabilities for small and medium businesses (SMBs) by integrating various security tools in a hybrid environment. The focus is on optimizing resource consumption while maintaining effective real-time monitoring.

## Components

### 1. Wazuh
- **Role**: Acts as the Security Information and Event Management (SIEM) tool, collecting and analyzing security data.
- **Containerization**: Running Wazuh in a container on the cloud allows SMBs to reduce on-site resource consumption while enabling remote monitoring.

### 2. Splunk
- **Role**: Functions as the analytics and visualization platform, processing log data from Wazuh for insights and alerts.
- **Containerization**: Similar to Wazuh, containerizing Splunk on the cloud simplifies management and scales efficiently, minimizing local resource use.

### 3. Suricata
- **Role**: An open-source intrusion detection and prevention system (IDS/IPS) that monitors network traffic in real-time.
- **Local Deployment**: Running Suricata and the Wazuh agent locally ensures low latency in threat detection, while the more resource-intensive components run in the cloud.

## Methodology
- **Integration**: This setup integrates Suricata, Wazuh, and Splunk to create a comprehensive security monitoring solution:
  - Suricata captures network traffic and generates alerts.
  - Wazuh processes these alerts and correlates them with log data from other sources.
  - Splunk visualizes this data for security monitoring.

- **Hybrid Approach**: The project uses on-premise machines for Suricata and the Wazuh agent, while Wazuh Manager, ELK, and Splunk are containerized and run in the cloud. This hybrid model reduces on-site resource consumption while maintaining powerful monitoring capabilities.

## Challenges Addressed
The primary challenge addressed by this methodology is resource consumption. Running traditional solutions like Splunk and Wazuh can be resource-intensive, especially for SMBs. By leveraging cloud infrastructure for these applications, SMBs can optimize their resource usage while still effectively monitoring their systems.

## Expected Outcomes
- Enhanced real-time monitoring capabilities accessible remotely from anywhere.
- Reduced on-site resource consumption by offloading heavy processing to the cloud.
- Improved visibility into security events and threats.

## Future Enhancements
- Deploying containerized tools in the cloud to further decrease on-site resource usage. 
- Utilizing flexible pricing options from cloud providers like Amazon EC2 to make the solution more affordable.
- Allowing integration with preferred monitoring tools (e.g., Windows Sentinel One) while maintaining the core architecture of local information collectors and cloud-based monitoring tools.

## Implementation Plan
A rough implementation plan is portrayed through attached image.

## Technology Stack
All components are implemented using the latest versions of Wazuh, Splunk, and Suricata to leverage the latest features and improvements.

## Security Practices
- **Network Segmentation**: Ensure that local machines running Suricata and Wazuh agents are on a separate network segment to minimize risk.
- **Data Encryption**: Use encryption for data in transit between cloud services and local machines to protect sensitive information.
- **Access Control**: Implement strict access controls for both cloud and local resources to ensure that only authorized personnel can access sensitive monitoring data.
- **Regular Updates**: Keep all software components up to date to mitigate vulnerabilities and take advantage of security patches.
