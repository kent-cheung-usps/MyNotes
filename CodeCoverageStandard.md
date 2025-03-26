There isn't a single, universally mandated industrial standard for code coverage that applies across all industries, as it can vary depending on the domain, application type, and specific requirements (e.g., safety-critical systems vs. non-critical web apps). However, from a code quality and cybersecurity perspective, there are widely accepted benchmarks and best practices that organizations often target, particularly in software engineering and secure development lifecycles.

### General Guidelines for Code Coverage
Code coverage is typically measured as a percentage of the source code exercised by automated tests (e.g., unit tests, integration tests). Common metrics include **statement coverage**, **branch coverage**, **function coverage**, and **path coverage**. Here's how these are viewed in terms of quality and security:

1. **70-80% Coverage (Minimum Acceptable Standard)**  
   - For many general-purpose applications, achieving 70-80% code coverage (usually statement or line coverage) is considered a practical minimum for decent code quality.  
   - This level ensures that most of the codebase is tested, reducing the likelihood of untested logic containing bugs or vulnerabilities.  
   - However, this is often seen as insufficient for security-critical applications, as it leaves 20-30% of the code potentially untested and exploitable.

2. **80-90% Coverage (Good Practice)**  
   - This range is a common target for teams prioritizing both quality and security.  
   - It strikes a balance between effort and risk mitigation, ensuring that the majority of code paths are exercised.  
   - Cybersecurity benefits increase here, as more edge cases and potential attack vectors (e.g., input validation, error handling) are likely covered.

3. **90-100% Coverage (High Assurance)**  
   - For industries like aerospace, automotive (e.g., ISO 26262), medical devices (e.g., IEC 62304), or financial systems, 90-100% coverage—often branch or modified condition/decision coverage (MC/DC)—is a common requirement.  
   - From a cybersecurity standpoint, this level minimizes the attack surface by ensuring nearly all code paths are tested, reducing the chance of hidden vulnerabilities.  
   - Achieving 100% coverage is rare in practice due to diminishing returns (e.g., testing trivial or unreachable code), but it’s a goal for critical systems.

### Cybersecurity-Specific Considerations
- **Focus on Risky Areas**: Code coverage alone doesn’t guarantee security. Prioritize testing for high-risk components like authentication, input validation, cryptographic functions, and external interfaces (e.g., APIs). Tools like OWASP’s guidelines or MITRE’s CWE list can help identify these areas.
- **Threat Modeling**: Pair code coverage with threat modeling to ensure tests target security-critical paths, not just functional ones.
- **Dynamic Analysis**: Complement static code coverage with dynamic testing (e.g., fuzzing, penetration testing) to catch runtime vulnerabilities that static metrics might miss.

### Industry Standards and Frameworks
- **MISRA (Automotive)**: Often requires high branch coverage (e.g., 90%+) for safety and security-critical code.
- **DO-178C (Aerospace)**: For Level A software (highest criticality), MC/DC coverage is mandatory, often targeting 100% for critical modules.
- **OWASP**: While not specifying a percentage, OWASP recommends sufficient coverage to mitigate the Top 10 security risks, implying a focus on quality over a raw percentage.
- **ISO/IEC 27001**: Doesn’t mandate a specific coverage level but emphasizes risk-based testing, which often pushes teams toward 80-90% for critical systems.

### Practical Benchmark
For most modern applications balancing quality and cybersecurity:
- **80% statement coverage** is a solid baseline.
- **90% branch coverage** is a stronger target for security-sensitive apps.
- Anything below 70% is generally considered inadequate for production-grade software, especially from a cybersecurity perspective, as it leaves too much code untested and potentially vulnerable.

Ultimately, the "standard" depends on your application's risk profile. A social media app might be fine with 80%, while a banking app might demand 95%+ for critical components. The key is to align coverage goals with quality objectives, security requirements, and industry regulations specific to your domain.
