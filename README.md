# jenkins-docker-agents
A collection of Docker images pre-configured as Jenkins agents with various tools and dependencies for diverse CI/CD workflows.

## Available Images

### 1. Base Image

**Docker image:** 
```
ghcr.io/pinklink-app/jenkins-agent:base
```

**Description:**
- Jenkins inbound agent (JNLP).
- Includes OpenJDK 17.
- Ideal as a general-purpose Jenkins agent for Java-based projects and basic CI/CD tasks.

### 2. .NET Image

**Docker image:** 
```
ghcr.io/pinklink-app/jenkins-agent:dotnet
```

**Description:**
- Built on top of the Base Image.
- Includes .NET SDK 8.0 and ASP.NET Core Runtime 8.0.
- Optimized for .NET development, testing, and deployment pipelines.

### 3. Node.js Image

**Docker image:** 
```
ghcr.io/pinklink-app/jenkins-agent:nodejs
```

**Description:**
- Built on top of the Base Image.
- Includes Node.js (LTS version 20.x), npm, and yarn.
- Ideal for Node.js/JavaScript development, testing, and deployment tasks.

