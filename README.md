# HNG13 Stage 0 - DevOps

**Name:** John Abioye  
**Slack username:** [John Billion]  
**Project:** NGINX webserver serving a custom index.html for HNG13 Stage 0.  
**Server:** http://54.158.6.245/   
**Deployed on:** AWS EC2 (Ubuntu 22.04)  
**Deployed:** 2025-10-17


### **Project Overview**

This project demonstrates a basic **DevOps workflow** by deploying a simple static website on an **AWS EC2 instance** using **Nginx** as the web server. The deployment showcases the ability to configure infrastructure, manage services, and verify end-to-end connectivity.

---

### **Steps Performed**

1. **Provisioned EC2 Instance**

   * Launched an **Ubuntu 22.04** instance on AWS.
   * Configured **security group** to allow HTTP (port 80) and SSH (port 22) access.

2. **Installed and Configured Nginx**

   * Installed Nginx using:

     ```bash
     sudo apt update && sudo apt install nginx -y
     ```
   * Verified the service was running:

     ```bash
     sudo systemctl status nginx
     ```

3. **Deployed Custom HTML Website**

   * Replaced the default `/var/www/html/index.html` file with a personalized HTML page:

     ```bash
     sudo nano /var/www/html/index.html
     ```
   * Edited content to include:

     * Project title and name
     * Deployment date
     * Success message confirming EC2 deployment

4. **Verified Web Deployment**

   * Tested locally on the instance using:

     ```bash
     curl http://localhost
     ```
   * Verified externally from a personal system using the EC2 public IP:

     ```bash
     curl http://<EC2-PUBLIC-IP>
     ```
   * Confirmed successful HTTP response with the custom HTML content.

---

### **Technologies Used**

* **AWS EC2** – Virtual server hosting
* **Ubuntu 22.04** – Operating system
* **Nginx** – Web server
* **Nano** – Command-line text editor
* **cURL** – Network testing tool

---

### **Key Takeaways**

* Learned how to deploy and manage a basic web server on AWS.
* Practiced Linux command-line skills for configuration and debugging.
* Demonstrated foundational DevOps concepts: **Infrastructure Setup → Service Configuration → Deployment → Verification**.

---

### **Outcome**

✅ Successfully deployed a static website accessible via public IP:
`http://<your-ec2-public-ip>`

---
