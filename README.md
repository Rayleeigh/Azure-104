### **Table of Contents**
> - [Azure-104 - Learning Path](#azure-104---learning-path)
>    - [Introduction](#introduction)

> NOTE THIS REPO IS STILL UNDER CONSTRUCTION

# **Azure-104 - Learning Path**
> Quick Note: While the official learning path of microsoft is structured soundly, it isn't a one-to-one execute and pass solution, but rather a guide, you still have to learn and develop a strategy on your own which to some can be cumbersome, this is why I reworked the modules and learning path, using the offical Microsoft Learning Path as a source [Microsoft Official Learning Path for Azure 104](https://learn.microsoft.com/en-us/training/paths/az-104-administrator-prerequisites/).

### **Introduction**
Now you may ask, what is different about this Learning Path, it is quite simple; Microsofts official learning path is too linear and theoretical in approach, and to top it off it doesn't force to troubleshoot. My learning path, while drawing from the resources of [Microsoft Official Learning Path for Azure 104](https://learn.microsoft.com/en-us/training/paths/az-104-administrator-prerequisites/), incorporates one crucial aspect the official learning path doesn't:

```
Build → Break → Fix
```

This forces you to actually deploy, break, and troubleshoot; which in turn builds alot of practical experience and theoretical knowledge.
You'll learn these things over 7 phases. These 8 Phases will consist of the following:
* Phase 0: Foundation Reset
* Phase 1: Prerequisites for Azure administrators
* Phase 2: Manage identities and governance in Azure
* Phase 3: Implement and manage storage in Azure
* Phase 4: Deploy and manage Azure compute resources
* Phase 5: Configure and manage virtual networks for Azure administrators
* Phase 6: Monitor and Backup Azure resources
* Phase 7: Exam prep

> very important note: each phase will incorporate material and resources from [Microsoft Official Learning Path for Azure 104](https://learn.microsoft.com/en-us/training/paths/az-104-administrator-prerequisites/), meaning you will still have to visit Microsofts leaning path site to get the full benefit of this learning path.

Here is a **clean, professional, README-grade rewrite** that is clear, structured, and *implicitly elite*.
It explains the structure **without overexplaining**, and it aligns perfectly with how senior engineers document knowledge bases.

You can drop this straight into your main README.

---

### **Knowledge Base Structure**

This repository is organized as a **progressive, phase-based knowledge system**, designed to enforce structured learning and deliberate practice.

```
Phase_Directory            (e.g. 00_Foundation)
│
├─ Phase_Module_Directory  (e.g. 00_1_Azure_Mental_Models)
│   │
│   ├─ Theory
│   ├─ Exercises
│   └─ ExerciseSolutions
```

---

### **How the Structure Works**
* **Phases**
  Each phase represents a **major learning milestone** aligned with the AZ-104 learning objectives.

* **Phase Modules**
  Each phase is broken down into **focused modules**, where **each module corresponds exactly to one focus point** listed in the phase description (e.g. *Azure Mental Models*, *Identity Boundaries*, *Traffic Flow*).

* **Theory**
  Concise, exam-relevant explanations that establish:

  * mental models
  * definitions that the exam assumes you already know
  * boundaries between similar concepts

* **Exercises**
  Hands-on tasks following the **Build → Break → Fix** methodology:

  * deploy intentionally
  * introduce controlled failures
  * troubleshoot with minimal changes

* **ExerciseSolutions**
  Not just “answers”, but **reasoned fixes**, explaining:

  * why the solution works
  * why alternative options are wrong
  * how the exam expects you to think about the scenario

---

# **[Phase 0: Foundation Reset](./00_Foundation/README.md)**
### **Purpose**
Fix weak fundamental **before** Azure complexity hides them.
> Most AZ-104 failures are not "Azure problems", they are **identity, DNS, RBAC, or networking fundamentals problems**

### **What you'll focus on**
* Azure Mental Models
* Identity Boundries
* Scope and Inheritance Drill
* Azure Toolchain Authority Model
* Failure-First Thinking

### **Exit Criteria**
You may not proceed to the next phase unless you can:
* Explain identity flow without notes
* Identify the correct tool for any action
* Explain why one fix is correct and others are wrong

# **[Phase 1: Prerequisites for Azure Administrators](./01_Prerequisites/README.md)**

### **Purpose**

Establish **tool authority**, **deployment literacy**, and **error interpretation** before you touch real workloads.

> If you can’t read deployment failures confidently, you’ll waste hours “trying stuff” instead of fixing root cause.

### **What you'll focus on**

* Tool Authority Mental Model (Portal vs Cloud Shell vs PowerShell vs ARM)
* Deploying the same resources using multiple tools
* Reading and categorizing deployment errors (auth vs template vs region/provider)
* Minimal correction discipline (fix only what’s broken)
* Building a repeatable deployment workflow

### **Exit Criteria**

You may not proceed to the next phase unless you can:

* Choose the correct tool for a task instantly (and justify why)
* Identify deployment failure category in under a minute
* Fix a broken deployment with minimal changes (no redeploy-from-scratch habit)
* Explain why ARM is in-scope and Terraform is not (for AZ-104)

---

# **[Phase 2: Manage Identities and Governance](./02_Identity_Governance/README.md)**

### **Purpose**

Master **who can do what, where, and why** — without falling for scope mistakes.

> Most access issues are not “permissions problems”, they are **scope, role-type, or governance collisions**.

### **What you'll focus on**

* Entra ID roles vs Azure RBAC roles (and when each applies)
* Scope and inheritance across Management Groups → Subscriptions → RGs → Resources
* Least privilege design (no “Global Admin fixes everything” thinking)
* Governance controls: Azure Policy, tags, and locks
* Diagnosing and fixing scope-related failures

### **Exit Criteria**

You may not proceed to the next phase unless you can:

* Instantly distinguish RBAC vs Entra roles vs Policy vs Locks
* Fix access problems without escalating privileges unnecessarily
* Identify “wrong scope” issues quickly and correct them precisely
* Explain why other fixes are wrong (especially “just give Contributor/Owner”)

---

# **[Phase 3: Implement and Manage Storage](./03_Storage/README.md)**

### **Purpose**

Become dangerous with storage by mastering **selection, security, and access troubleshooting**.

> Storage failures are usually **networking or identity failures in disguise**.

### **What you'll focus on**

* Storage decision-making (Blob vs Files vs account types)
* Redundancy and performance considerations
* Access models: Keys vs SAS vs RBAC (and when each is valid)
* Network controls and storage security (public vs restricted access)
* Diagnosing access failures (network vs auth vs configuration)

### **Exit Criteria**

You may not proceed to the next phase unless you can:

* Choose the correct storage solution from requirements (not guessing)
* Diagnose storage access failures correctly (network vs auth) without trial-and-error
* Restore intended access using the correct security method
* Explain why access keys can be the wrong answer even if they “work”

---

# **[Phase 4: Deploy and Manage Compute](./04_Compute/README.md)**

### **Purpose**

Build compute instincts for **availability, scaling, and recovery**, not just VM creation.

> AZ-104 tests whether you understand **what breaks**, not whether you can deploy a VM.

### **What you'll focus on**

* VMs, App Service, Container Instances: when to use what
* Availability sets vs availability zones (and the trade-offs)
* Scaling up vs scaling out (and when each is appropriate)
* Recovering access (NSG/NIC/boot diagnostics) before redesigning
* Minimal viable fixes for compute failures

### **Exit Criteria**

You may not proceed to the next phase unless you can:

* Pick the correct availability strategy from vague requirements
* Restore broken access without redeploying everything
* Explain scaling decisions clearly (up vs out)
* Avoid over-engineering when the requirement is simple

---

# **[Phase 5: Configure and Manage Networking](./05_Networking/README.md)**

### **Purpose**

Develop traffic-flow intuition and troubleshooting discipline.

> If you can’t trace traffic end-to-end, you don’t actually understand Azure networking.

### **What you'll focus on**

* Traffic flow tracing (DNS → routes → NSGs → NICs → service)
* VNet/subnet design and segmentation thinking
* NSGs: priority, direction, effective rules
* Routing + peering concepts and failure modes
* Load Balancer vs Application Gateway basics
* Network Watcher as your primary diagnostic tool

### **Exit Criteria**

You may not proceed to the next phase unless you can:

* Predict whether traffic will pass before testing
* Diagnose NSG/routing/DNS issues using tracing (not guessing)
* Explain LB vs App Gateway differences in one paragraph
* Fix connectivity issues with minimal changes and correct order of operations

---

# **[Phase 6: Monitor and Back Up Resources](./06_Monitoring_Backup/README.md)**

### **Purpose**

Build real recovery competence: **monitoring + backup + restore validation**.

> Backups aren’t valuable because they exist — they’re valuable because they restore successfully.

### **What you'll focus on**

* Azure Backup fundamentals and Recovery Services Vault usage
* VM protection configuration and retention logic
* Alerting mindset (detect before users report)
* Recovery options: what can be restored and how
* Backup vs availability (stop mixing these concepts)

### **Exit Criteria**

You may not proceed to the next phase unless you can:

* Choose the correct recovery method based on the scenario
* Restore data/VM successfully and validate the outcome
* Explain why backup ≠ uptime and how that affects design choices
* Adjust retention and backup scope intentionally (not randomly)

---

# **[Phase 7: Exam Readiness & Failure Conditioning](./07_Exam_Prep/README.md)**

### **Purpose**

Convert skill into **exam dominance** by training how the exam thinks.

> Phase 7 is where you stop “learning Azure” and start mastering **minimum-fix reasoning** under time pressure.

### **What you'll focus on**

* Exam pattern recognition (scope mistakes, misleading wording, over-engineering)
* Minimum viable fix discipline (smallest change that satisfies requirements)
* Time-pressure conditioning (extract requirement/constraint fast)
* Failure Journal (categorize mistakes and build anti-mistake memory)
* Full simulations + post-mortems + weak-area drills

### **Exit Criteria**

You may not consider yourself exam-ready unless you can:

* Consistently reject over-engineered answers
* Identify scope mistakes instantly
* Finish practice exams with time remaining
* Explain why the wrong options are wrong (not just why yours is right)
