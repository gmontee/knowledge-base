Service Mesh
is a pattern or paradigm
manages communication between microservices

Challenges of a microservice architecture
- Business Logic
- Communication Config (end point for each service)
- Security Logic (proxy, firewall, cluster)
- Retry logic (robust)
- Metrics & Tracing Logic

Solution: Service Mesh with Sidecar Pattern
- Handles networking logic
- acts as a Proxy
- third-party application
- cluster operators can configure it easily
- Control Plane injects the Sidecar Proxy

Core Feature
- Traffic Split (sort of like Feature Flags, A/B testing deployment, Canary Deployment)

Istio Architecture
- Control Plane: configuration, discovery, certificates
	- Istiod: manages data plane
- Data Plane: mesh traffic
	- Envoy Proxy

Istio is configured with Kubernetes YAML files
- uses Kubernetes CustomResourceDefinitions (CRD)
	- extending the Kubernetes API
	- custom Kubernetes component/object for e.g., third-party technologies (like Istio, Prometheus, etc)
	- traffic routing
	- which services can communicate
	- traffic split
	- retry rules

 Traffic Routing
 - VirtualService
	 - How you route your traffic **TO** a given destination
 - DestinationRule
	 - Configure what happens to traffic **FOR** that destination
 - Istiod converts these into high level routing rules into Envoy-specific configurations
 - Configuration is propagated into Proxy sidecars
