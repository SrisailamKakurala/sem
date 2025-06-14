
### **Unit 1:**

1. **Agile Development Model:**
   Agile is an iterative, incremental approach focusing on collaboration, customer feedback, and flexible responses to change. It breaks projects into small cycles called sprints. *(Diagram shows iterative cycles with planning, development, testing, review.)*

2. **DevOps and ITIL not mutually exclusive:**
   DevOps focuses on rapid delivery and automation, while ITIL provides best practices for IT service management. They complement by improving service reliability alongside speed.

3. **DevOps Continuous Delivery Pipeline:**
   It automates building, testing, and deploying code continuously through stages: commit, build, test, release, deploy, and monitor to enable faster delivery.

4. **Bottlenecks in CI/CD:**
   Examples include slow builds, flaky tests, manual approvals, infrastructure limitations, and poor integration between tools.

5. **DevOps Process Example:**
   Developers commit code → Automated build & test → Continuous integration server triggers deployment → Monitoring and feedback for improvement.

---

### **Unit 2:**

1. **DevOps Life-cycle for Business Agility:**
   DevOps integrates development, testing, deployment, and monitoring to rapidly deliver high-quality software, enabling quick responses to market changes.

2. **Continuous Testing in DevOps:**
   Automated testing at every stage ensures early defect detection, improves quality, and accelerates releases, but requires robust test frameworks.

3. **Monolithic Architecture:**
   A single unified codebase where all components are tightly integrated. Simple to develop but harder to scale or update independently. *(Diagram shows one big block for app)*

4. **Handling Database Migrations:**
   Use version control for DB schema changes, automated migration tools, and backward-compatible changes to ensure smooth updates.

5. **Microservices Architecture:**
   Breaks app into small, independent services communicating over APIs, improving scalability and flexibility. *(Diagram shows multiple small service blocks)*

6. **Resilience in DevOps:**
   Designs systems to handle failures gracefully with redundancy, automated recovery, and monitoring to maintain uptime.

---

### **Unit 3:**

1. **Need for Source Code Control:**
   Manages code versions, enables collaboration, tracks changes, and supports rollback to earlier code versions.

2. **Source Code Management for Roles:**
   Developers use it for coding and branching, testers for validating code versions, release managers for coordinating deployments.

3. **Source Code Migrations:**
   Moving repos between systems requires planning, mapping histories, resolving conflicts, and testing post-migration.

4. **Shared Authentication:**
   Centralized access control for repos improves security but risks if credentials leak.

5. **Hosted Git Servers:**
   Platforms like GitHub, GitLab, and Bitbucket provide cloud-based repo hosting with collaboration and CI/CD integration.

6. **Docker Intermission:**
   Likely refers to Docker’s role in isolating environments for consistent builds and deployments.

7. **Pull Request Model:**
   Code changes are proposed via pull requests, reviewed, approved, then merged, ensuring quality and collaboration.

8. **GitLab:**
   An all-in-one DevOps platform offering Git repo hosting, CI/CD pipelines, issue tracking, and project management.

---

### **Unit 4:**

1. **Build Systems:**
   Examples include Jenkins, Travis CI, Bamboo, TeamCity, and CircleCI; automate compiling and packaging code.

2. **Using Jenkins to Create Builds:**
   Configure jobs with source repo, triggers, build scripts, and post-build actions for automated builds.

3. **Build Slaves:**
   Distributed nodes that run builds in parallel, improving scalability and speed.

4. **Triggers:**
   Events like code commits, schedules, or manual starts that initiate builds automatically.

5. **Job Chaining & Build Pipelines:**
   Sequence dependent jobs to automate complex workflows from build to deployment.

6. **Builds by Dependency Order:**
   Configure jobs so dependent components build after their prerequisites to avoid failures.

---

### **Unit 5:**

1. **Pros and Cons of Automated Testing:**
   Pros: Faster, repeatable, early bug detection. Cons: Initial setup cost, maintenance overhead.

2. **Selenium:**
   A popular web testing tool automating browser actions; supports multiple languages but limited to web UI testing.

3. **JavaScript Testing:**
   Involves unit and integration tests for JS code using frameworks like Jest, Mocha, ensuring code quality.

4. **TDD vs REPL-driven Development:**
   TDD writes tests before code for quality; REPL allows interactive, rapid prototyping with instant feedback.

5. **Puppet, Chef, Ansible, SaltStack:**
   All automate infrastructure: Puppet and Chef use declarative/imperative models with agents; Ansible is agentless with YAML; SaltStack offers event-driven automation.

---

