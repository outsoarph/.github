---
name: Outsoar PH Internal Infrastructure
description: Documentation of Outsoar PH's internal infrastructure, including servers, services, and configurations
---

# Outsoar PH Internal Infrastructure

Approach: Monolitch, single EC2 instance hosting multiple web applications with shared services for now, to keep costs low and management simple.
Applications should be loosely coupled via Redis event bus for inter-service communication. 

## Infrastructure Components

Server: AWS EC2 t3.medium
Database: MariaDB
Storage: AWS S3 for backups and static assets
Cache: Redis for events, sessions, and queues
CI/CD: GitHub Actions for automated deployments
Web Server: Nginx
PHP Version: 8.4    
Framework: Laravel 10.x
OS: Aws Linux 2 2023 | Arm64

## Web Applications:

1. CooperWebApp
2. CooperBot
3. Klauber - HRIS ( Payroll, Attendance, Employee Management )
4. Truesight - Accounting System

