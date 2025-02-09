# 🔗 SnipUrlAwsLambda
## 📝 Description
A serverless URL shortening service built with AWS Lambda. This application generates and manages short URLs efficiently using serverless architecture.

## 🚀 Technologies & Tools
- [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) - Programming Language
- [AWS Lambda](https://aws.amazon.com/lambda/) - Serverless Computing
- [Maven](https://maven.apache.org/) - Dependency Management
- [Lombok 1.18.24](https://projectlombok.org/) - Boilerplate Reduction
- [Jackson 2.13.1](https://github.com/FasterXML/jackson) - JSON Processing
- [Log4j2](https://logging.apache.org/log4j/2.x/) - Logging Framework

## 🏗️ Project Structure
```
src/
└── main/
    └── java/
        └── dev/
            └── diogosoares/
                └── Main.java      # 🎯 Main Lambda function
```

## 📋 Prerequisites
- ☕ Java 17 JDK
- 📦 Maven
- 🔑 AWS Account with Lambda access
- 🛠️ AWS CLI configured

## 🚀 Getting Started

### 📥 Clone the Repository
```bash
git clone <repository-url>
cd SnipUrlAwsLambda
```

### 💻 Build Project
```bash
mvn clean package
```

## ☁️ AWS Configuration

### Lambda
1. Create a new Lambda function
2. Configure handler: `dev.diogosoares.Main::handleRequest`
3. Upload generated JAR file

## 📦 Main Dependencies
```xml
<dependencies>
    <dependency>
        <groupId>com.amazonaws</groupId>
        <artifactId>aws-lambda-java-core</artifactId>
        <version>1.2.1</version>
    </dependency>
    <dependency>
        <groupId>com.amazonaws</groupId>
        <artifactId>aws-lambda-java-log4j2</artifactId>
        <version>1.4.0</version>
    </dependency>
    <dependency>
        <groupId>org.projectlombok</groupId>
        <artifactId>lombok</artifactId>
        <version>1.18.24</version>
    </dependency>
    <dependency>
        <groupId>com.fasterxml.jackson.core</groupId>
        <artifactId>jackson-databind</artifactId>
        <version>2.13.1</version>
    </dependency>
</dependencies>
```

## 🛠️ Features
- ✂️ URL Shortening
- 📊 Efficient URL Management
- ⚡ Serverless Architecture
- 📝 Comprehensive Logging

## 🔐 Security
- 🔒 AWS Lambda Security Model
- 🛡️ IAM Role-based Access
- 🔑 Secure URL Processing

## 📝 Logging and Monitoring
- 📊 Log4j2 Integration
- 📈 AWS CloudWatch Logs
- 🔍 Lambda Execution Monitoring

## 🚀 Deploy
```bash
mvn clean package
aws lambda update-function-code \
    --function-name SnipUrlAwsLambda \
    --zip-file fileb://target/SnipUrlAwsLambda-1.0-SNAPSHOT.jar
```

## ⚙️ Configuration
### Maven Build Plugin
The project uses the Maven Shade Plugin for creating an uber-jar with all dependencies:
```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-shade-plugin</artifactId>
    <version>3.2.4</version>
</plugin>
```

## 🔧 Environment Setup
Configure your AWS credentials and region:
```bash
aws configure
```

Made with ❤️ by Diogo Soares
