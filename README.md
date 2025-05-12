# Java OOP Payment System – Dockerized CLI Application
---

##  How to Run This Program

Make sure you have **Docker** installed on your system.

###  Step-by-step Commands to Run:

```bash
1. Pull the Docker image from Docker Hub
docker pull priyeshrai711/payment-controller-v4

# 2. Run the container (port is optional since it's a CLI app)
docker run -it priyeshrai711/payment-controller-v4
docker run -it -p 8080:8080 priyeshrai711/payment-controller-v4
 Note: -it is needed for interactive input (Scanner in Java).
```
### Docker Hub Link
[DockerHub : priyeshrai711](<https://hub.docker.com/repository/docker/priyeshrai711/payment-controller-v4/general>)

###  Project Structure
Good_Questions/
│
├── All_OOPS/
│   └── PaymentController.java
├── Dockerfile
└── README.md

### 🐳 Dockerfile Used
```
FROM openjdk:17

WORKDIR /app

COPY All_OOPS ./All_OOPS

WORKDIR /app/All_OOPS

RUN javac PaymentController.java

CMD ["java", "All_OOPS.PaymentController"]

```

###  Sample Run Output
```
Enter User ID (1–20) or 0 to Exit: 3
👤 Welcome, User3
Choose Payment Method:
1. UPI
2. Card
3. NetBanking
1
Choose Operation:
1. Deposit
2. Withdraw
3. Pay
4. Check Balance
1
Enter amount to deposit: 500
✅ Deposited ₹500. Current Balance: ₹500
👋 Exit
```
