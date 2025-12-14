# CC-Linux-AWS-DevOps

Project 1: Kubernetes troubleshooting lab (50 Kubernetes errors & solutions)
What you’ll do in VS Code:
Write and edit YAML manifests (Deployment, Service, Ingress, PVC, etc.).
Use the integrated terminal to run kubectl commands against your cluster (minikube, kind, or EKS).
Install extensions like Kubernetes and YAML for syntax highlighting and autocompletion.
Workflow:
Create a folder k8s-troubleshooting-lab/.
Add YAML files for each error scenario.
Use VS Code’s terminal to apply configs:

Project 2: DevOps Portfolio Projects (8 Projects)
What you’ll do in VS Code:
Write Dockerfiles, docker-compose.yml, Terraform scripts, Ansible playbooks, and Jenkinsfiles.
Manage multiple repositories (React frontend, Node backend, infra code).
Use extensions like Docker, Terraform, Ansible, and GitLens.

Workflow:
For the two-tier app, create web/ and db/ folders with Dockerfiles.
For the three-tier EKS app, edit Kubernetes manifests in VS Code and push to GitHub.
For Terraform + Ansible, keep infra code in separate folders and run commands in VS Code’s terminal:


Project 3: Ultimate CI/CD Pipeline
What you’ll do in VS Code:
Write and maintain the Jenkinsfile pipeline script.
Edit Kubernetes manifests (ds.yml) for deployment.
Configure monitoring setup files for Prometheus and Grafana.
Use GitHub integration in VS Code to commit and push changes.
Workflow:
Clone your project repo into VS Code.
Create and edit the Jenkinsfile with stages for build, test, scan, deploy.
Push changes to GitHub → Jenkins picks them up automatically.
Use VS Code’s terminal to verify deployments:

kubernetes-troubleshooting-zero-to-hero
Learn how to troubleshoot the most common Kubernetes Issues

Day-01
ImagePullBackOff
Video Link - https://youtu.be/vGab4v3RWEw

When a kubelet starts creating containers for a Pod using a container runtime, it might be possible the container is in Waiting state because of ImagePullBackOff.

The status ImagePullBackOff means that a container could not start because Kubernetes could not pull a container image for reasons such as

Invalid image name or
Pulling from a private registry without imagePullSecret.
The BackOff part indicates that Kubernetes will keep trying to pull the image, with an increasing back-off delay.

Kubernetes raises the delay between each attempt until it reaches a compiled-in limit, which is 300 seconds (5 minutes).

Day-02
CrashLoopBackOff
When you see "CrashLoopBackOff," it means that kubelet is trying to run the container, but it keeps failing and crashing. After crashing, Kubernetes tries to restart the container automatically, but if the container keeps failing repeatedly, you end up in a loop of crashes and restarts, thus the term "CrashLoopBackOff."

This situation indicates that something is wrong with the application or the configuration that needs to be fixed.

Day-03
Pods not schedulable
In Kubernetes, the scheduler is responsible for assigning pods to nodes in the cluster based on various criteria. Sometimes, you might encounter situations where pods are not being scheduled as expected. This can happen due to factors such as node constraints, pod requirements, or cluster configurations.

Node Selector
Node Affinity
Taints
Tolerations
