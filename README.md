# Deploy-a-Dockerized-Web-Application-on-the-Cloud


---

## 🎯 Objective

The goal of this task is to **containerize a simple web application** using Docker and deploy it on the cloud.  
This demonstrates **containerization, portability, and cloud-native deployment**.

---


## 📦 Project Files

### **app.py**


from flask import Flask

app = Flask(__name__)

@app.route('/')

def home():

return "Hello from my Dockerized Cloud App!"

if __name__ == '__main__':

app.run(host='0.0.0.0', port=8080)


---

## 🧭 Step-by-Step Deployment

#### 1️⃣ Build Docker Image Locally

docker build -t mycloudapp 

---

#### 2️⃣ Run Container Locally

docker run -p 8080:8080 mycloudapp



✅ Visit: http://localhost:8080
  --- 

#### 3️⃣ Push Image to Cloud Registry

Example (Google Cloud):

docker tag mycloudapp gcr.io/PROJECT_ID/mycloudapp

docker push gcr.io/PROJECT_ID/mycloudapp

----


#### 4️⃣ Deploy on Cloud Platform

Use Cloud Run / ECS / Azure Container Instances

Select the pushed image

Allow public access

Deploy → get public URL

✅ Take screenshot of deployed app with URL visible.

----

#### 📝 Short Note

This is a Dockerized Flask web application.

The app responds with a greeting message.

Docker ensures portability and consistent environment across local and cloud.

The container can be deployed to any cloud platform for scalable, reliable hosting.

This demonstrates cloud-native deployment with containerization.