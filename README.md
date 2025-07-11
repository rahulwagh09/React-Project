# 🚀 React App CI/CD with Travis CI and AWS 

This project demonstrates how to deploy a Dockerized **React.js** application using **Travis CI** and **AWS Elastic Beanstalk**, following a complete **CI/CD pipeline** best practice.

---

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

### ⚙️ Automated Steps via Travis CI
- Triggered automatically when code is merged into `master`
- Performs:
  - Docker build
  - (Optional) Tests
  - Uploads artifact to **S3 bucket**
  - Deploys to **Elastic Beanstalk**

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
