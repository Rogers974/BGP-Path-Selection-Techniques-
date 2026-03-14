# BGP Path Selection Techniques

BGP Path Selection Techniques Demonstrated

This lab demonstrates how different BGP attributes can be used to influence route selection and traffic flow across multiple autonomous systems. Each technique was implemented using routing policies to simulate real-world traffic engineering scenarios used by network engineers and service providers.

# Weight

Weight was configured on customer edge routers to control outbound traffic selection at the local router level. By assigning a higher weight value to a preferred BGP neighbor, the router selects that path as the best route when multiple paths exist.

# Purpose:

To ensure traffic from the local router prefers a specific upstream provider.

# Local Preference

Local Preference was implemented within the provider network to influence which exit point the entire autonomous system should use. Routes received from preferred upstream links were assigned a higher local preference value using route-maps.

# Purpose:

To ensure all routers within the AS prefer a specific path when exiting the network.

# AS Path Prepending

AS Path Prepending was applied on outbound BGP advertisements to artificially increase the AS path length for certain routes. This makes the path less attractive to external networks, encouraging them to choose alternative routes.

# Purpose:

To influence inbound traffic from external autonomous systems.

# AS Path Filtering

AS Path filtering was configured using AS-path access lists to control which routes are accepted from BGP neighbors. Routes containing specific AS numbers in the AS path were filtered to enforce routing policies.

# Purpose:

To prevent routes from unwanted or specific autonomous systems from being installed in the routing table.

# Verification Commands used.

The following commands were used to validate BGP operation:

show ip bgp

show ip bgp summary

show ip bgp neighbors

show ip route bgp

Connectivity between PC1 and PC2 was verified using:

ping
traceroute
These tests confirmed correct best path selection and traffic engineering behavior.


# Technologies Used

GNS3

Cisco IOS

BGP

Route Maps

Prefix Lists

AS Path Access Lists

VPCS

# Key Skills Demonstrated

BGP configuration and troubleshooting
Traffic engineering using routing policies
Multi-AS network design
ISP routing concepts
Professional network documentation

# Author

# Engineer Rogers Mulyowa
Telecommunications Engineer
Networking | Routing | Service Provider Technologies
