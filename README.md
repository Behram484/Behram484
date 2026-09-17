# Behrem Elyas

**BSc (Hons) Computer Science & Artificial Intelligence, First-Class — University of Sussex, 2026**
Based in Calgary, AB, Canada · Authorized to work in Canada, no sponsorship required · Open to relocation across Canada

I build and evaluate developer tooling around local LLMs — test generation, automated repair, and mutation-based quality measurement — plus applied ML and secure backend work.

---

## Featured work

### LLM-Based Automated Unit Test Generation
[`llm-testgen-project`](https://github.com/Behram484/llm-testgen-project) · Java, Python, Ollama, JUnit 5, Maven, PIT

End-to-end pipeline that generates JUnit 5 tests from Java source, validates them through Maven compile and execute, repairs failures in an iterative loop, and scores test quality with PIT mutation analysis.

- Diagnosed ANSI/control-character contamination in raw model output; sanitizing it raised pipeline success from **43.3% to 86.7%** across 40 Java classes
- Mutation-guided augmentation improved mean mutation scores by **14.6–19.4 percentage points**
- 2 x 2 x 2 factorial evaluation across model size (Qwen2.5-Coder 32B / DeepSeek-Coder 6.7B), prompt profile, and repair budget

[![Success rates before and after output sanitation across all eight conditions](https://raw.githubusercontent.com/Behram484/llm-testgen-project/main/charts/ansi-fix-success.png)](https://github.com/Behram484/llm-testgen-project)

### Selenium Regression Suite
[`selenium-regression-suite`](https://github.com/Behram484/selenium-regression-suite) · Java 17, JUnit 5, Selenium WebDriver, Maven, Docker, GitHub Actions

Browser regression tests against a PHP/MySQL security application I had written — auth, 2FA, password reset, RBAC and upload validation.

- **46 tests**, page object model, full suite on every push in headless Chrome in **1m43s**, nothing skipped or excluded
- Found **7 defects** and fixed 6 with a test guarding each — including two **account-enumeration disclosures** (login error text, and the reset flow revealing accounts by showing or hiding the security question)
- Found the app could not be reproduced from a clean clone (missing base schema) and made that a CI-verified step
- The README also records the negative results, and a `ExpectedConditions.stalenessOf` gotcha: it detects staleness by catching `StaleElementReferenceException`, and Chrome 152 throws a different one — so it fails on the very navigation it is meant to wait for

### Data Citation Extraction — Independent Rebuild
[`mdc-data-reference-extraction`](https://github.com/Behram484/mdc-data-reference-extraction) · Python, XML parsing, rule-based NLP

Extracting data citations from scientific full text and classifying each as primary or secondary use.

- Four-stage pipeline raised dev F1 from **0.057 to 0.639**, each stage committed with its own measured delta
- Scored a pre-registered holdout **once** and reported it unchanged: **F1 0.285**. Type rules fitted on 122 articles reversed on 23 — an accession-format prior held 95% on dev and 42% on holdout, worse than a constant baseline
- Effective sample size proved to be articles, not mentions (4 articles carried 86 of 153 labels); added article-level bootstrap confidence intervals that mention-level intervals had hidden

### Make Data Count: Finding Data References — Kaggle Silver Medal
Team lead (5 people) · **42nd of 1,282 teams, top 3.3%**

<!-- Add the solution repo link here once it is up: [`kaggle-make-data-count`](https://github.com/Behram484/kaggle-make-data-count) -->

### Applied Machine Learning
[`applied-machine-learning-projects`](https://github.com/Behram484/applied-machine-learning-projects) · PyTorch, scikit-learn, Sentence-BERT

Spam classification comparing TF-IDF against Sentence-BERT embeddings, and facial keypoint regression using ResNet transfer learning.

### Secure Web Application
[`secure-web-application`](https://github.com/Behram484/secure-web-application) · PHP, MySQL

Authentication and admin system built to OWASP practices: bcrypt hashing, prepared statements, CSRF tokens, XSS output escaping, 2FA, account lockout, role-based access control, and validated file uploads.

### Reborn Wings — Interactive 3D Showroom
[`3D-Web`](https://github.com/Behram484/3D-Web) · Three.js, GLSL, Blender

Browser-based aircraft showroom with custom GLSL shaders and bloom post-processing; aircraft modelled in Blender.

[Live demo](https://behram484.github.io/3D-Web/)

---

## Tools

**Languages** Java · Python · SQL · JavaScript · C# · PHP · HTML/CSS
**Testing** Selenium WebDriver · JUnit 5 · PIT mutation testing · Maven · pytest · page object model
**AI/ML** Local LLM inference (Ollama, Qwen2.5-Coder, DeepSeek-Coder) · prompt engineering · evaluation harnesses · PyTorch · scikit-learn
**Other** Git · GitHub Actions · Docker · Linux · MySQL · Three.js · Unity

---

## Open to

Junior Software Engineer · Backend Developer · Test / QA Automation · AI/ML Engineer — in Canada, on site, hybrid, or remote.

Reach me at **janbehrem@gmail.com** or on [LinkedIn](https://linkedin.com/in/behrem-elyas-86703b411).
