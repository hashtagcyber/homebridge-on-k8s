# homebridge-on-k8s
My config for running homebridge with MetalLB on microk8s.
- Uses MetalLB to expose HomebridgeUI on port 80
- Configures Homebridge in "insecure mode" (Allows for Alexa integration)
- Persists homebridge data by mounting /containers/homebridge (host) as /homebridge (container)


1. Edit line 23 of 03-service.yaml to include an IP address available on MetalLB
2. `kubectl apply -f .`
