Task:
You are executing inside an EC2 instance intended to serve as a base image for an ONA (Gitpod) development environment.

Design and run a deterministic, non-interactive sanity test that validates the presence and basic functionality of the following runtimes and package managers:
	•	JavaScript (Node.js + npm/pnpm/yarn if present)
	•	Python (python3 + pip, via venv)
	•	.NET (dotnet SDK)
	•	Java (JDK; Maven or Gradle if installed)

Constraints:
	•	Do not require root privileges
	•	Assume outbound network access may be restricted or proxied
	•	Use minimal, stable dependencies
	•	Avoid long-running or resource-heavy operations

Validation criteria (per language):
	•	Runtime binary exists and reports a version
	•	Package manager can resolve and install at least one dependency (or verify local cache if offline)
	•	A minimal program compiles and/or executes successfully

Write and execute the test steps, collect logs under /tmp/sanity, and output a final structured summary indicating success or failure for each language.