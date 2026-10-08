# AWS Auto-Scaling E-Commerce Platform 🚀

A highly available and scalable E-Commerce web application built using AWS cloud services.

## 📌 Project Overview

This project demonstrates a highly available 3-tier style web application architecture on AWS.

The application uses an Application Load Balancer to distribute incoming traffic across EC2 instances running in multiple Availability Zones. An Auto Scaling Group manages the application servers, while Amazon RDS MySQL is used as the database layer.

## 🏗️ Architecture

```text
                    Internet
                       |
                       v
              Application Load Balancer
                       |
                       v
                  Target Group
                  /           \
                 v             v
          EC2 Instance    EC2 Instance
          us-east-1a      us-east-1b
                 \             /
                  \           /
                   v         v
                    RDS MySQL
