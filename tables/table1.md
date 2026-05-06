Table 1. Main deterministic benchmark results.

Panel A. Primary outcomes.

| Actor Model | System | CSR | OVR | OVR 95% CI | SVR | SVR 95% CI | PAR | PAR 95% CI | PAR-exec | PAR-exec 95% CI | Ranking Reversal |
| --- | --- | ---: | ---: | --- | ---: | --- | ---: | --- | ---: | --- | --- |
| Qwen2.5-7B | S0 | 0.833 | 0.292 | [0.149, 0.492] | 0.000 | [0.000, 0.051] | 0.000 | [0.000, 0.051] | 0.000 | [0.000, 0.055] | N/A |
| Qwen2.5-7B | S1 | 0.833 | 0.250 | [0.120, 0.449] | 0.000 | [0.000, 0.051] | 0.083 | [0.039, 0.170] | 0.091 | [0.042, 0.184] | False |
| Qwen2.5-7B | S2 | 0.833 | 0.250 | [0.120, 0.449] | 0.000 | [0.000, 0.051] | 0.000 | [0.000, 0.051] | 0.000 | [0.000, 0.055] | False |

Panel B. Secondary diagnostics.

| Actor Model | System | WR | WR 95% CI | HDR | CWRR | φ | 95% CI | φ Status |
| --- | --- | ---: | --- | ---: | ---: | ---: | --- | --- |
| Qwen2.5-7B | S0 | N/A | N/A | 0.000 | N/A | N/A | N/A | not_applicable |
| Qwen2.5-7B | S1 | 0.083 | [0.023, 0.258] | 0.000 | N/A | N/A | N/A | undefined_svr_zero |
| Qwen2.5-7B | S2 | 0.000 | [0.000, 0.138] | 0.000 | 0.077 | N/A | N/A | undefined_par_zero |

Panel C. System averages over actor models.

| System | CSR | OVR | SVR | PAR | PAR-exec | WR | HDR | CWRR |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| S0 | 0.833 | 0.292 | 0.000 | 0.000 | 0.000 | 0.000 | 0.000 | 1.000 |
| S1 | 0.833 | 0.250 | 0.000 | 0.083 | 0.091 | 0.083 | 0.000 | 0.000 |
| S2 | 0.833 | 0.250 | 0.000 | 0.000 | 0.000 | 0.000 | 0.000 | 0.077 |

Panel D. Validity diagnostics for pilot promotion.

| Actor Model | System | Planner Structured | Required Tool Call | Execution Failure | Writer Structured | Writer Valid Type | Mechanism Check | Official Pilot Valid |
| --- | --- | ---: | ---: | ---: | ---: | ---: | --- | --- |
| Qwen2.5-7B | S0 | 0.907 | 0.985 | 0.074 | 1.000 | 1.000 | True | True |
| Qwen2.5-7B | S1 | 0.907 | 0.985 | 0.074 | 0.984 | 1.000 | True | True |
| Qwen2.5-7B | S2 | 0.907 | 0.985 | 0.074 | 0.984 | 1.000 | True | True |

Notes: `PAR-exec` conditions on non-execution-failure stateful episodes. Confidence intervals are 95% Wilson intervals under the deterministic `temperature=0` protocol.
