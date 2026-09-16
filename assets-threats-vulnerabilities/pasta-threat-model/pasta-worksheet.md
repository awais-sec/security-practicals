# PASTA Worksheet: Sneaker Company Application

| Stage | Sneaker Company |
|---|---|
| **I. Define business and security objectives** | An application that connects sellers and shoppers. It should be secure, easy to manage, and provide privacy so users feel confident using it. Proper payment handling should be available to avoid legal issues. |
| **II. Define the technical scope** | Technologies used by the application: Application Programming Interface (API), Public Key Infrastructure (PKI), SHA-256, SQL. SQL should be a focus area because it can be exploited through SQL injection attacks, which could let an attacker retrieve sensitive information from the database. |
| **III. Decompose application** | The user searches for a product or service. Since SQL is used, the query runs in the background and the results are displayed from the database. *(See the sample data flow diagram resource.)* |
| **IV. Threat analysis** | Two types of threats that are risks to the information being handled by the application: **Internal threat** — an employee can leak data or make a system vulnerable, either knowingly or unknowingly (e.g. if exploited by a threat actor using social engineering). **External threat** — threat actors who want the data or want to sell it for financial gain, using SQL injection or a virus to disrupt the organization. |
| **V. Vulnerability analysis** | Two vulnerabilities that could be exploited: flaws in the network (e.g. session hijacking); flaws in the codebase (e.g. SQL injection). |
| **VI. Attack modeling** | Threat actors can manipulate an employee to gain false authentication access to the system, or use SQL injection to steal users' credentials from the database. *(See the sample attack tree diagram resource.)* |
| **VII. Risk analysis and impact** | Four security controls that can reduce risk: training employees about social engineering; prepared statements to prevent SQL injection; vulnerability assessments; secure payment methods. |
