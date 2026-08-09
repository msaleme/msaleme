# Michael K. Saleme

**Enterprise architect.** 30 years building production integration and architecture across Oil & Gas, Energy/Utilities, and CPG since 1996.

I am defining **Enterprise Agent Architecture**: the fifth domain enterprise architecture needs for a workforce of humans and AI agents. TOGAF, Zachman, SABSA, and NIST model what the enterprise builds and runs. None model a non-human actor that holds delegated authority, acts autonomously, and composes tools it was never explicitly granted. That gap is the work.

**Read the series:** [Enterprise Agent Architecture on Substack](https://msale00.substack.com) — the fifth domain, one part at a time.

`CVE-2026-25253 reproduction · 5 peer-citable papers (DOIs) · 3 NIST submissions · 603 executable security tests`

**Start here:** [msaleme/start-here](https://github.com/msaleme/start-here)

---

## The evidence

I do not just write about the agent workforce. I build the tools that prove how it fails and the research that measures it.

### Research

I study the gap between *who an agent is* and *how it behaves* — what I call the **WHO vs. HOW problem**. Identity and permissions don't prevent an authorized agent from being manipulated into unsafe decisions. My work formalizes this gap and provides empirical evidence.

| Paper | DOI | Key finding |
|---|---|---|
| **Decision Load Index (DLI)** | [10.5281/zenodo.18217577](https://doi.org/10.5281/zenodo.18217577) | AI agents increase cognitive burden on operators. Here's how to measure it. |
| **Constitutional Self-Governance (CSG)** | [10.5281/zenodo.19162104](https://doi.org/10.5281/zenodo.19162104) | The WHO vs. HOW governance gap — 77 days production data, 56 agents. |
| **Normalization of Deviance (NoD)** | [10.5281/zenodo.19195516](https://doi.org/10.5281/zenodo.19195516) | Gateway defenses provide zero protection against protocol-level attacks. |
| **Beyond Identity Governance** | [10.5281/zenodo.19343034](https://doi.org/10.5281/zenodo.19343034) | Empirical evidence: gateways miss protocol-layer attacks. The gap, formalized. |
| **Community-Driven Security** | [10.5281/zenodo.19343108](https://doi.org/10.5281/zenodo.19343108) | Scaling security testing through community contribution without degrading integrity. |

**Standards engagement:** 3 NIST submissions — CAISI RFI (Mar 1), NIST-CONCEPT-1 (Mar 12), NCCoE follow-up (Mar 21, 2026).

### Agent Security Harness

The research above is implemented as an open-source testing framework: **603 executable tests across 43 test-bearing modules**, covering MCP, A2A, L402, and x402 wire protocols.

**[red-team-blue-team-agent-fabric](https://github.com/msaleme/red-team-blue-team-agent-fabric)** (v4.15.0) — 97.9% pass rate measured at v4.4.2 (Wilson 95% CI [0.943, 0.994]), not re-measured since.

```bash
pip install agent-security-harness
agent-security test mcp --url http://your-server
```

- **[GitHub Action](https://github.com/msaleme/red-team-blue-team-agent-fabric#cicd-integration)** — CI/CD integration
- **[MCP Server](https://github.com/msaleme/red-team-blue-team-agent-fabric#mcp-server)** — any AI agent can invoke security tests directly
- **[AIUC-1 Prep](https://github.com/msaleme/red-team-blue-team-agent-fabric#aiuc-1-certification-prep)** — maps to 15 of 20 testable certification requirements
- **CVE-2026-25253** (CVSS 8.8) — our MCP tests catch this exact supply chain attack vector

---

## Enterprise Architecture

30 years building production integration systems across Oil & Gas, Energy/Utilities, and CPG since 1996.

---

## Connect

- **ORCID:** [0009-0003-6736-1900](https://orcid.org/0009-0003-6736-1900)
- **X:** [@mikesaleme](https://x.com/mikesaleme)
- **LinkedIn:** [mikesaleme](https://www.linkedin.com/in/mikesaleme/)
- **PyPI:** [agent-security-harness](https://pypi.org/project/agent-security-harness/)
