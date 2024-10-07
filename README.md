# Multi-Service Web Application

A comprehensive web application using microservices architecture, featuring a Node.js frontend, Node.js and Java backends, and Nginx as a reverse proxy.

![Project Banner](path/to/banner/image.png)

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()
[![Version](https://img.shields.io/badge/version-1.0.0-blue)]()
[![License](https://img.shields.io/badge/license-MIT-green)]()

## Table of Contents
- [Overview](#overview)
- [Architecture](#architecture)
- [Services](#services)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project demonstrates a microservices-based web application with separate frontend and backend services, orchestrated using Docker Compose and Nginx as a reverse proxy.

## Architecture

![Architecture Diagram](path/to/architecture/diagram.png)

The application consists of:
- Frontend web application (Node.js)
- Node.js API
- Java API
- Nginx reverse proxy
- MongoDB database
- MySQL database

## Services

### 1. Client (Web Application)
- Built with Node.js 14
- Served via Nginx
- Located in `./client` directory

### 2. Node.js API
- Backend service built with Node.js
- Located in `./nodeapi` directory

### 3. Java API
- Backend service built with Java
- Located in `./javaapi` directory

### 4. Nginx
- Acts as a reverse proxy
- Configuration in `./nginx/default.conf`

### 5. Databases
- MongoDB (for Node.js API)
- MySQL (for Java API)

## Prerequisites

- Docker
- Docker Compose

## Installation
# Multi-Service Web Application Workflow

## 1. Client (Frontend)
- Location: `./client`
- Process:
  1. Build web app using Node.js 14
  2. Copy build output to Nginx content directory
- Note: Confirm build artifact path with developer

## 2. Node.js API
- Location: `./nodeapi`
- Process:
  1. Install dependencies
  2. Copy API to working directory
  3. Configure start command

## 3. Java API
- Location: `./javaapi`
- Process:
  1. Build artifact using Maven
  2. Copy artifact to working directory

## 4. Nginx Configuration
- Location: `./nginx`
- Setup: Reverse proxy for multiple services
- IP: 192.168.0.188
- Handles requests on different ports

## 5. Docker Compose
- File: `docker-compose.yml`
- Purpose: Orchestrate all microservices
- Services included:
  - Frontend
  - Node.js API
  - Java API
  - Nginx
  - Databases (if applicable)

## Deployment Flow
1. Build individual services (Steps 1-3)
2. Configure Nginx (Step 4)
3. Define and run all services using Docker Compose (Step 5)
