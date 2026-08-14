# Testing Types

## 1. Functional Testing

Functional testing verifies that the software behaves according to specified business and system requirements.

### 1.1 Unit Testing

Tests individual componentes, functions, methods or classes in isolation.
- Verify small units of code independently.
- Detect defects earlier in development.
- Validate expected inputs, outputs and edge cases.

Scope: Function, method, class or component.

### 1.2 Integration Testing

Tests interactions and data flow between two or more components, services, modules or systems.
- Verify if integrated components work together correctly.
- Detect interface and communication defects.
- Validate data exchange between those components.

Scope: APIs, services, databases, modules and external integrations.

### 1.3 Smoke Testing

High-level test performed on a new build to determine whether the build is stable enough for more detailed testing.
- Verify Critical functionality works.
- Quickly identify major build-breaking problems.
- Prevent wasted effort on an unstable build.

Scope: Critical application paths.

### 1.4 Sanity Testing

A focused test performed after minor changes, bug fixes or updates to verify that the affected functionality works as expected.
- Confirms if that a specific change or fix workds.
- Check that related functionality still remains reasonable.
- Quickly determine whether further testing is justified.

Scope: narrow and change-focused.

### 1.5 Regression Testing

Tests previously working functionality after code changes to ensure that existing behaviour has not been unintentionally broken.
- Detect unintended side effects.
- Validate existing features after changes
- Mainten confidence in application stability.

Scope: Existing functionality affected by directly or indirectly by changes.

### 1.6 Exploratoy Testing

Testers simultaneously learn about the system, design tests and execute them rather than following predefined cases.
- Discover unexpected defects.
- Investigate ares that scripted testes may overlook.
- Use tester experience and critical thinking to explore the product.

Scope: Flexible and dynamically determined.

### 1.7 User Acceptance Testing(UAT)

Testing focused in determing that the system satisfies business requirements and is acceptable to its intended users or stakeholders.
- Validate business workflow.
- Confirm that the system supports real-world user needs.
- Determine readiness for release and deployment.

Scope: End-to-end business scenarios.

## 2. Non-functional Testing

Evaluates system characteristics that goes beyond functional behaviour, such as performance, stability, security and compatibility.

### 2.1 Load Testing

Evaluates system behaviour under expected or specified levels of concurrent users, requests, transcations or data.
- Determine if it handles expected workload.
- Identify performance degradation under normal load.
- Estabilish response-time and throughput baselines.

### 2.2 Performance Testing

Evaluates system responsiveness, speed,throughtput, resource utilization and stability.
- Evaluate response times.
- Measure throughput.
- Identify performance bottlenecks
- Assess resource consumption

-> Load testing is a type of performance testing with focus on behaviour under a defined workload.

### 2.3 Stress Testing

Pushes the system beyond operating limits to determine how it behaves under extreme conditions.
- Identify system breaking point.
- Observe failure behaviour.
- Evaluate recovery and stability after excessive load.

### 2.4 Security Testing

Evaluates if the application protects data, functionality, users and system resources against unhauthorized access and other security threats.
- Identify security vulnerabilities.
- Verify authentication and authorization controls.
- Validate protection of sensitive data.
- Assess common attack surfaces.

### 2.5 Accessility Testing
Evaluates if the software can be effectively used by people with different disabilities and accessibility needs.
- Verify keyboard accessibility.
- Evaluate screen-reader compatibility.
- Check appropriate semantic structure and labeling.
- Validate sufficient text and interface accessibility.

### 2.6 Compatibility Testing
Evaluates if the application works correctly across different environments.

- Browsers
- Operating systems
- Devices
- Screen sizes
- Hardware configurations
- Network environments
- Software versions

# 3. Taxonomy Overview

│
├── Functional Testing
│ ├── Unit Testing
│ ├── Integration Testing
│ ├── Smoke Testing
│ ├── Sanity Testing
│ ├── Regression Testing
│ ├── Exploratory Testing
│ └── User Acceptance Testing (UAT)
│
└── Non-Functional Testing
├── Load Testing
├── Performance Testing
├── Stress Testing
├── Security Testing
├── Accessibility Testing
└── Compatibility Testing
└── Theory only at this stage

# 4. Quick Classification

| Category | Testing Type | Primary Focus |
|---|---|---|
| Functional | Unit | Individual code units |
| Functional | Integration | Component interactions |
| Functional | Smoke | Build stability |
| Functional | Sanity | Specific changes/fixes |
| Functional | Regression | Existing functionality |
| Functional | Exploratory | Unscripted discovery |
| Functional | UAT | Business acceptance |
| Non-Functional | Load | Expected workload |
| Non-Functional | Performance | Speed, throughput, resources |
| Non-Functional | Stress | Extreme workload |
| Non-Functional | Security | Protection and vulnerabilities |
| Non-Functional | Accessibility | Usability for people with disabilities |
| Non-Functional | Compatibility | Behavior across environments |