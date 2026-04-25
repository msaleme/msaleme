# Michael K. Saleme

**Decision Governance for Autonomous Agents** — I research how AI agents fail under adversarial conditions, publish the findings, and ship the tools to test for them.

5 published papers | 3 NIST submissions | CVE-2026-25253 | 430 security tests | PyPI package

---

## Research

I study the gap between *who an agent is* and *how it behaves* — what I call the **WHO vs. HOW problem**. Identity and permissions don't prevent an authorized agent from being manipulated into unsafe decisions. My work formalizes this gap and provides empirical evidence.

| Paper | DOI | Key finding |
|---|---|---|
| **Decision Load Index (DLI)** | [10.5281/zenodo.18217577](https://doi.org/10.5281/zenodo.18217577) | AI agents increase cognitive burden on operators. Here's how to measure it. |
| **Constitutional Self-Governance (CSG)** | [10.5281/zenodo.19162104](https://doi.org/10.5281/zenodo.19162104) | The WHO vs. HOW governance gap — 77 days production data, 56 agents. |
| **Normalization of Deviance (NoD)** | [10.5281/zenodo.19195516](https://doi.org/10.5281/zenodo.19195516) | Gateway defenses provide zero protection against protocol-level attacks. |
| **Beyond Identity Governance** | [10.5281/zenodo.19343034](https://doi.org/10.5281/zenodo.19343034) | Empirical evidence: gateways miss protocol-layer attacks. The gap, formalized. |
| **Community-Driven Security** | [10.5281/zenodo.19343108](https://doi.org/10.5281/zenodo.19343108) | Scaling security testing through community contribution without degrading integrity. |

**Standards engagement:** 3 NIST submissions — CAISI RFI (Mar 1), NIST-CONCEPT-1 (Mar 12), NCCoE follow-up (Mar 21, 2026).

---

## Agent Security Harness

The research above is implemented as an open-source testing framework: **430 executable tests across 29 modules**, covering MCP, A2A, L402, and x402 wire protocols.

**[red-team-blue-team-agent-fabric](https://github.com/msaleme/red-team-blue-team-agent-fabric)** — Production-validated at 97.9% pass rate (Wilson 95% CI [0.943, 0.994]).

```bash
pip install agent-security-harness
agent-security test mcp --url http://your-server
```

- **[GitHub Action](https://github.com/msaleme/red-team-blue-team-agent-fabric#cicd-integration)** — gate deploys in one line
- **[MCP Server](https://github.com/msaleme/red-team-blue-team-agent-fabric#mcp-server)** — any AI agent can invoke security tests directly
- **[AIUC-1 Prep](https://github.com/msaleme/red-team-blue-team-agent-fabric#aiuc-1-certification-prep)** — maps to 15 of 20 testable certification requirements
- **CVE-2026-25253** (CVSS 8.8) — our MCP tests catch this exact supply chain attack vector

---

## Enterprise Architecture

15+ years building production integration systems across Oil & Gas, Energy/Utilities, and CPG — MuleSoft, Salesforce, SAP, Oracle, Kafka, Azure.

| Repository | Description |
|---|---|
| [agent-fabric-oilgas-apis](https://github.com/msaleme/agent-fabric-oilgas-apis) | OpenAPI 3.1 specs for Agent Fabric in Oil & Gas |
| [energy-field-service-integration](https://github.com/msaleme/energy-field-service-integration) | Agentforce + ServiceNow + SAP field service |
| [energy-api-evolution](https://github.com/msaleme/energy-api-evolution) | 36 APIs unifying grid ops, renewables, building optimization |
| [oracle-fusion-mulesoft-best-practices](https://github.com/msaleme/oracle-fusion-mulesoft-best-practices) | Oracle Fusion Cloud integration patterns |
| [SharePointVectors](https://github.com/msaleme/SharePointVectors) | RAG pipeline: SharePoint to vectors to Salesforce |

---

## Connect

- **ORCID:** [0009-0003-6736-1900](https://orcid.org/0009-0003-6736-1900)
- **X:** [@mikesaleme](https://x.com/mikesaleme)
- **LinkedIn:** [mikesaleme](https://www.linkedin.com/in/mikesaleme/)
- **PyPI:** [agent-security-harness](https://pypi.org/project/agent-security-harness/)
- **Book time:** [Calendly](https://calendly.com/mspro3210/new-meeting) | trusted@synapseops.com
