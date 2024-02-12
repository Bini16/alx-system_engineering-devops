Issue Summary:

Duration: The outage occurred from February 10th, 2024, 10:00 AM to February 10th, 2024, 2:00 PM (UTC).
Impact: The primary service affected was our web application, resulting in a complete outage for 30% of users and degraded performance for the remaining 70%, causing slow page load times and intermittent errors.
Root Cause:

The root cause of the outage was identified as a misconfigured load balancer in our web stack, leading to uneven distribution of traffic among backend servers, ultimately overwhelming some instances and causing a cascading failure.

Timeline:

10:00 AM (UTC): The issue was first detected through monitoring alerts indicating unusually high latency and error rates.
10:10 AM: Engineers began investigating the issue, suspecting a potential backend server overload.
10:30 AM: After ruling out server-side issues, attention turned to the load balancer configuration.
11:00 AM: Initial attempts to tweak load balancer settings to alleviate the issue proved unsuccessful.
12:00 PM: Escalation to the infrastructure team as the investigation intensified.
1:00 PM: Collaborative effort led to the discovery of the misconfigured load balancer as the root cause.
2:00 PM: Load balancer configuration was corrected, restoring normal traffic distribution and resolving the outage.
Root Cause and Resolution:

The misconfigured load balancer was inadvertently set to favor specific backend servers, leading to uneven traffic distribution and subsequent server overload. The issue was resolved by adjusting the load balancer configuration to evenly distribute incoming requests among all backend servers.

Corrective and Preventative Measures:

Improvements: Regular audits of load balancer configurations to ensure proper settings and prevent similar incidents. Enhanced monitoring for load balancer performance metrics to detect anomalies promptly.
Tasks to Address the Issue:
Perform a thorough review of load balancer configurations across all environments.
Implement automated checks to verify load balancer settings align with best practices.
Enhance monitoring alerts for load balancer performance and traffic distribution.
Conduct team-wide training on load balancer management and troubleshooting procedures.
By implementing these corrective measures and addressing the identified tasks, we aim to mitigate the risk of similar incidents in the future and uphold the reliability and performance of our web stack.
