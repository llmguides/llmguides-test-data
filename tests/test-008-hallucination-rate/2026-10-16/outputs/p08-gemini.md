The General Data Protection Regulation (GDPR) ends at **Article 99** (which covers the law's entry into force and application date) and does not contain an **Article 99a**.

If you are looking for recent legislative changes that modify or expand upon **Article 22** (automated individual decision-making and profiling), you are likely thinking of one of two major regulatory developments:

1. **UK GDPR Reform (Articles 22A–22D):** Introduced by the UK's Data (Use and Access) Act 2025 (effective February 2026), which formally replaced Article 22 in the UK.
2. **The EU AI Act (specifically Article 86):** Which operates alongside EU GDPR Article 22 to add new transparency and explanation obligations for high-risk automated decisions in the EU.

Below is how the baseline **EU GDPR Article 22** works, how those newer frameworks alter the rules, and what companies must do to comply.

---

## 1. Baseline Rules: EU GDPR Article 22

In the European Union, Article 22 remains unchanged in the text of the GDPR. It treats **solely automated decision-making** (including profiling) that produces *legal effects* or *similarly significant effects* on an individual (such as an automatic loan rejection or automated hiring filter) as **prohibited by default**.

Companies can only use solely automated decision-making if one of three narrow exceptions applies:

* **Contractual Necessity:** The decision is strictly necessary to enter into or perform a contract with the individual.
* **Legal Authorization:** Union or Member State law explicitly authorizes the processing and provides suitable safeguards (e.g., fraud and tax-evasion prevention).
* **Explicit Consent:** The individual has given clear, specific, and freely withdrawable consent. *(Note: "Legitimate interests" under Article 6(1)(f) cannot be used as a legal basis for Article 22 decisions.)*

---

## 2. What Changed Recently? (UK vs. EU)

Depending on your jurisdiction, the rules around Article 22 have evolved in two distinct ways:

| Feature | EU GDPR (Article 22 + EU AI Act) | UK GDPR (New Articles 22A–22D) |
| --- | --- | --- |
| **Default Stance** | **Prohibited** unless one of the 3 narrow exceptions (contract, law, explicit consent) applies. | **Permitted** for standard personal data using *any* valid lawful basis (including standard legitimate interests), provided safeguards are met. |
| **Special Category (Sensitive) Data** | Prohibited unless based on **explicit consent** or **substantial public interest**. | Strictly restricted under **Article 22B**: requires explicit consent, or contractual necessity / legal authority paired with substantial public interest. |
| **Explanation Rights** | GDPR Articles 13–15 require "meaningful information about the logic involved." **EU AI Act Art. 86** adds a concrete right to a clear explanation of the AI's role and main decision parameters. | **Article 22C** mandates proactive information about the significant decision, alongside the right to human review and contestation. |

---

## 3. Core Obligations for Companies

Whether operating under the EU GDPR's strict exception model or the UK GDPR's safeguard-focused model (Articles 22A–22D), companies deploying automated decision-making systems must implement four primary operational safeguards:

* **Provide Proactive Transparency & Logic Explanations:** Under EU GDPR Articles 13(2)(f) and 14(2)(g) (and UK Article 22C), companies must notify individuals *before* or *at the time* data is collected that solely automated decision-making is taking place, explain the underlying logic in plain language, and outline the envisaged consequences.
* **Guarantee Meaningful Human Intervention:** Individuals have the right to request a human review of an automated decision. Regulators require that the human reviewer be competent, independent of the algorithm's output, given access to all relevant context, and **hold the actual authority to overturn the automated decision**—rubber-stamping an algorithm's output does not qualify.
* **Enable Representation and Contestation:** Companies must build an accessible mechanism allowing individuals to express their point of view, submit additional context or correcting data, and formally contest the outcome within a reasonable timeframe.
* **Conduct a Data Protection Impact Assessment (DPIA):** Because automated decision-making with significant effects inherently carries high risk to individual rights and freedoms, Article 35(3)(a) requires companies to complete a formal DPIA before putting the system into production, documenting bias mitigation, error rates, and security controls.
