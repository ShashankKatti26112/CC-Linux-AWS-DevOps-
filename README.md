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

Real-World DevOps/Cloud Projects For Learning from Beginner to Advanced ♐
NotHarshhaa/DevOps-Projects | Trendshift

Forks Stars Issues Last Commit Code of Conduct Contributing

DevOps-Projects

👥 Project Ownership

🌟 Star History
Star History Chart

Welcome to the ultimate resource for learning DevOps through hands-on projects! This repository is designed to cater to aspiring DevOps engineers of all skill levels, from beginners taking their first steps in the field to advanced users looking to deepen their knowledge and expertise.

Welcome Badge

🧠 Purpose of the Repository
This repository serves as a comprehensive resource for aspiring DevOps engineers to learn and implement real-world DevOps projects. It includes guides and solutions for deploying scalable systems, such as deploying a Java application on AWS using a 3-tier architecture and setting up scalable VPC architectures in the cloud.

The README files provide detailed instructions for implementing these projects, emphasizing practical deployment steps, pre-requisites, and validation processes. For example, one project focuses on deploying a Java-based login application integrated with a MySQL database, while another covers creating modular VPC network setups leveraging AWS services.

Purpose of Repository

🔍 Analysis of Features and Technologies
The repository demonstrates extensive use of DevOps concepts and tools, focusing on AWS cloud infrastructure and automation. It features technologies such as:

EC2, RDS, VPC, Auto Scaling, IAM roles
Maven, SonarCloud, JFrog Artifactory
Monitoring via CloudWatch
Custom AMIs, automation scripts
These elements showcase a robust implementation of scalable, secure, and automated systems aligned with real-world DevOps practices.

Analysis of Features

🌐 Real-time DevOps/Cloud Projects Showcase
To improve readability and accessibility for users, this repository is also available as a modern and responsive web interface.

A website showcasing a curated list of major real-time DevOps and Cloud projects, ranging from beginner to advanced levels. Built using Next.js and styled with Tailwind CSS, this project leverages a modern starter template for fast and responsive development. Perfect for learning and exploring hands-on DevOps and Cloud concepts!

🔗 Explore the site: projects.prodevopsguytech.com

Showcase Website

🔗 Related AWS Projects Repository
For comprehensive AWS-specific projects and hands-on learning experiences, visit our dedicated AWS Projects repository:

AWS Projects Repository Highlights:

Real-world AWS Projects from beginner to advanced levels
AWS DevOps Focus with practical implementation guides
Hands-on Learning with AWS services and best practices
Industry-Relevant projects covering EC2, VPC, RDS, Lambda, and more
Community Driven with active contributions and AWS expertise
🔗 Visit the AWS repository: AWS-Projects

AWS Projects

Repository Contents for DevOps Projects from Beginner to Advanced Levels
Important

This repository contains a comprehensive collection of DevOps projects, each meticulously crafted to provide a hands-on learning experience. The projects are categorized into different skill levels to ensure that everyone, regardless of their current expertise, can find a suitable starting point and progressively enhance their skills.

Beginner Projects: Simple, foundational projects that introduce basic DevOps concepts and tools.
Intermediate Projects: More complex projects that require a good understanding of DevOps fundamentals.
Advanced Projects: Challenging projects designed to push your limits and deepen your understanding of sophisticated DevOps practices.
DevOps Levels

Integration of DevOps Technology with Other Technologies
Note

In the modern tech landscape, DevOps doesn't exist in isolation. It intersects with a variety of other technologies, enhancing and being enhanced by them. This repository includes projects that integrate DevOps with several key technologies, allowing you to see how these integrations work in real-world scenarios.

Machine Learning: Implement DevOps practices to manage and deploy machine learning models efficiently.
Version Control with Git & GitHub: Learn how to manage code versions and collaborate with others using Git and GitHub.
CI/CD Pipelines: Set up continuous integration and continuous deployment pipelines to automate the testing and deployment of your applications.
Cloud Platforms (AWS, Azure, GCP): Deploy applications on cloud platforms and leverage their services for scalability and reliability.
Containerization (Docker, Kubernetes): Use container technologies to ensure that your applications run consistently across different environments.
Integration

Project Scope
Important

The projects span a wide array of topics within the DevOps domain, each designed to provide practical experience and insights into real-world scenarios. Here’s a detailed look at the areas covered:

Automated Deployment: Learn how to automate the deployment process to ensure that your applications are deployed quickly and reliably.
Continuous Integration & Continuous Deployment (CI/CD): Understand how to set up and manage CI/CD pipelines to automate the testing and deployment of your code.
Infrastructure as Code (IaC): Use tools like Terraform and CloudFormation to manage your infrastructure through code, ensuring consistency and scalability.
Monitoring & Logging: Implement monitoring and logging solutions to keep track of your applications’ performance and troubleshoot issues.
Security & Compliance: Learn how to incorporate security practices into your DevOps workflows to ensure that your applications are secure and compliant with regulations.
Scalability & Performance Optimization: Understand how to scale your applications and optimize their performance to handle increasing loads.
Project Scope

Why Explore This Repository?
Note

This repository is a treasure trove of learning opportunities, tailored to help you grow in the DevOps field. Here's why you should dive in:

Hands-on Experience: Each project is designed to provide you with practical, hands-on experience. You'll work through real-world challenges and gain the skills you need to succeed in the industry.
Skill Enhancement: Whether you're just starting or looking to build on existing skills, the projects are structured to guide you through a learning path that will enhance your capabilities.
Industry Relevance: Stay up-to-date with the latest trends and technologies in DevOps. The projects reflect current industry practices, ensuring that what you learn is relevant and applicable.
Community Engagement: Join a community of like-minded learners and professionals. Share your projects, seek feedback, and collaborate on exciting DevOps initiatives.
Why Explore This Repository

Code of Conduct
Caution

We are committed to fostering a welcoming and respectful environment for all contributors. Please take a moment to review our Code of Conduct before participating in this community.

Code of Conduct

Contribute and Collaborate
Tip

This repository thrives on community contributions and collaboration. Here’s how you can get involved:

Fork the Repository: Create your own copy of the repository to work on.
Submit Pull Requests: Contribute your projects or improvements to existing projects by submitting pull requests.
Engage with Others: Participate in discussions, provide feedback on others’ projects, and collaborate to create better solutions.
Share Your Knowledge: If you’ve developed a new project or learned something valuable, share it with the community. Your contributions can help others in their learning journey.
We follow best practices for contribution.

Contributing

🌍 Join the Community
Important

Be a part of our active DevOps community:

Join Telegram Follow on GitHub

⭐ Hit the Star!
If you find this helpful, don’t forget to give this repository a star. Your support matters! ⭐

Star Badge

🛠️ Author & Community
This project is crafted by Harshhaa 💡
I’d love to hear your feedback! Feel free to share your thoughts.

Author Badge

📧 Connect with me:
LinkedIn GitHub Telegram Dev.to Hashnode

📢 Stay Connected
Follow Me

Stay Connected
