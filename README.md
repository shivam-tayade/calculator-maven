# Calculator Maven Project

This is a simple calculator project built using Java and Maven. It provides basic arithmetic operations such as addition, subtraction, multiplication, and division.

## Features

- **Addition**: Adds two numbers.
- **Subtraction**: Subtracts one number from another.
- **Multiplication**: Multiplies two numbers.
- **Division**: Divides one number by another and handles division by zero.

## Requirements

- Java 8 or higher (for Java development)
- Maven 3.9.9 or higher (for project build management)

## Getting Started

### Prerequisites

1. Install Java (JDK 8 or higher).
2. Install Maven on your local machine. You can download it from [Apache Maven](https://maven.apache.org/).

### Clone the Repository

To get started, clone the repository:

```bash
git clone https://github.com/shivam-tayade/calculator-maven.git

mvn clean install
mvn exec:java 

Calculator calculator = new Calculator();
System.out.println(calculator.add(5, 3));
Result: 8
```

# Jenkins Guide to Build Calculator Maven Project

This guide explains how to set up Jenkins to build the **Calculator Maven Project**. Jenkins is an open-source automation server that helps automate tasks like building, testing, and deploying code.

## Prerequisites

Before you begin, ensure you have:

- **Jenkins** installed and running on your local machine or a server.
- **Maven** installed on your system.
- **Git** installed for cloning repositories.

You should have also configured a **Jenkins**


### Key Sections:
- **Cloning the Repository**: Shows how to link the GitHub repository with Jenkins.
- **Building the Project**: Explains how to configure Jenkins to run Maven commands.
- **Post-build Actions**: Outlines how to set up additional steps after the build.
- **Troubleshooting**: Provides tips for common issues.

This guide should give you a full setup for using **Jenkins** to build your **Calculator Maven Project**. Let me know if you need more adjustments or additional help!



