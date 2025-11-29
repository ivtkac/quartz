---
created: 2025-11-21
title: Є мікросервіси розгорнута на ECS і фронтенд, де буде NAT gateway?
tags:
  - question
  - devops
aliases:
---
- NAT gateway завжди розміщується у публічній підмережі (Public subnet) вашого [[AWS VPC]], але основна мета це забезпечити вихідний (Outbound) доступ до інтернету для ресурів, що знаходяться у приватній підмережі (Private subnet) 
- public: NAT gateway, application load balancer, internet gateway (IGW)
- private: frontend+microservice