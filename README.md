# 🚀 React App CI/CD with Travis CI and AWS 

This project demonstrates how to deploy a Dockerized **React.js** application using **Travis CI** and **AWS Cloud**, following a complete **CI/CD pipeline** best practice.

---

<img width="951" height="505" alt="Project Travis CI   AWS" src="https://github.com/user-attachments/assets/3bbe1d90-7674-443c-b631-dd63a571d34c" />

## 📖 Overview

This project is designed to automate the deployment process of a React frontend using:
- **Docker** for containerization
- **Travis CI** for build and deployment automation
- **AWS Elastic Beanstalk** for cloud hosting

Feature development is managed using Git-based branching and pull requests. Deployment is automatically triggered when code is pushed to the `master` branch.

---

## 🧰 Tech Stack

- **Frontend:** React.js
- **CI/CD:** Travis CI
- **Containerization:** Docker
- **Cloud Hosting:** AWS Elastic Beanstalk
- **Other AWS Services:** EC2, S3, IAM, EBS
- **Version Control:** Git & GitHub

---

## 🔄 CI/CD Workflow

### 🔧 Manual Steps
1. Create a new **feature branch** to develop a feature.
2. Push the feature branch to GitHub.
3. Create a **Pull Request** to merge it into the `master` branch.

<img width="1919" height="971" alt="Screenshot 2025-07-11 193819" src="https://github.com/user-attachments/assets/0dfa10e8-96e8-4606-87a1-c3589394b919" />


<img width="1915" height="959" alt="Screenshot 2025-07-11 193607" src="https://github.com/user-attachments/assets/dfa88467-a7b6-4054-985f-aba87d3d4f84" />



### ⚙️ Automated Steps via Travis CI
- Triggered automatically when code is merged into `master`
- Performs:
  - Docker build
  - (Optional) Tests
  - Uploads artifact to **S3 bucket**
  - Deploys to **Elastic Beanstalk**


<img width="1919" height="565" alt="Screenshot 2025-07-11 183712" src="https://github.com/user-attachments/assets/cfe633ea-e6bb-461f-86c6-8ae9e0fd0354" />



<img width="1569" height="417" alt="Screenshot 2025-07-11 183649" src="https://github.com/user-attachments/assets/8ec64bbb-d73b-4d5f-943d-4b6579ff4cde" />

---

## ☁️ AWS Configuration Summary

- **IAM Roles:**
  - `aws-elasticbeanstalk-ec2-role`
  - `aws-elasticbeanstalk-service-role`
- **Elastic Beanstalk Platform:**
  - Docker running on 64bit Amazon Linux 2
- **Storage:**
  - S3 Bucket for storing app versions
  - EBS for instance volumes
- **Security:**
  - AWS IAM user created for Travis CI deployment with Beanstalk permissions
  - IAM credentials securely stored as environment variables in Travis CI

---

## 🎯 Key Outcomes

- **Reduced deployment time** by ~70% with end-to-end automation.
- **Eliminated manual errors**, boosting environment consistency and uptime.
- **Improved team productivity**, allowing developers to focus on features rather than deployments.

---

## 💻 Available Scripts

In the project directory, you can run:

### `npm start`
Runs the app in development mode.  
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.  
The page will reload when you make changes.  
You may also see any lint errors in the console.

---

### `npm test`
Launches the test runner in the interactive watch mode.  
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

---

### `npm run build`
Builds the app for production to the `build` folder.  
It correctly bundles React in production mode and optimizes the build for the best performance.

---

### `npm run eject`
**Note: this is a one-way operation. Once you eject, you can't go back!**  
It will copy all configuration files and transitive dependencies into your project so you have full control over the build tooling.

---

## 📁 Project Structure
    frontend
    └── 

      ├── .travis.yml
    
      ├── Dockerfile
    
      ├── docker-compose-dev.yml
    
      ├── public/
    
      ├── src/
    
      │ └── App.js
    
      └── README.md
    
---

## 🙌 Acknowledgments

Thanks to the DevOps and AWS community for providing documentation and tools that made this deployment seamless.

---


## 🤝 Connect With Me

📫 [rahulwagh28032003@gmail.com](mailto:rahulwagh28032003@gmail.com)  

🔗 [LinkedIn](https://www.linkedin.com/in/rahul-wagh-cloud/)  

🐙 [GitHub](https://github.com/rahulwagh09)
