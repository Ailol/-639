# Probe — independent confirmation without asking around

**Input:** one falsifiable claim, versioned source, expected output and safe local/test conditions.
**Output:** reproduction recipe and one of PASS, FAIL, NOT RUN, INCONCLUSIVE.
**Check:** a reader can reach the same files and verify the claim without privately asking an author.

Five checks: source link; input; transformation; output; known limitation. Preserve failures and empty repositories. Avoid “works” when only a README exists.

Anchors: playwright-course for browser testing; HealthCareChallenge for idempotency/race-condition test questions; ai-architecture for test_handler_minimal.py; bitmemory/scripts/benchmark_baselines.py; DevopsBasics for continuous integration.

Evidence: https://github.com/Ailol/HealthCareChallenge/blob/master/README.md and https://github.com/Ailol/ai-architecture/blob/main/test_handler_minimal.py

Do not make reproducibility depend on access to private patient data, credentials or other people's systems.
