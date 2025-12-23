# DKP-1-IMPACT-001
## Impact Measurement Protocol

### Version
0.3

### Status
Final Freeze Candidate

---

## 1. Purpose

The Impact Measurement Protocol defines how changes in the Physical State Vector **S(t)** are transformed into time-indexed, bounded, and auditable impact metrics.

This protocol performs measurement only.  
It does not interpret value, intent, utility, justice, or policy.

---

## 2. System Position and Anchoring

This protocol operates above the Physical Truth Layer (DKP-0-ORACLE-001) and below all justice, governance, and economic protocols.

All inputs to this protocol MUST originate from Physical Truth Layer outputs.

All reference bounds **Bᵢ** MUST be explicitly imported from DKP-1-AXIOMS-001 or from normatively defined Physical Truth Layer indices (e.g., biosphere survival thresholds anchored in Genesis Block constants).

This protocol is bound to Genesis Block #0 (2025-12-10).

---

## 3. Scope

This protocol governs:

- Measurement of state change between two physical states
- Time-indexed impact evaluation over an externally supplied horizon
- Detection of boundary crossings relative to axiom-defined limits
- Classification of reversibility and externalization
- Production of structured, channel-separated impact outputs

This protocol explicitly excludes:

- Optimization, scoring, or weighting
- Aggregation across channels
- Decision-making or enforcement
- Compensation logic
- Any form of utility calculation

---

## 4. Core Definitions

**Physical State Vector S(t)**  
An immutable, time-indexed vector of measured physical variables produced by DKP-0-ORACLE-001.

**Baseline State S(t₀)**  
The reference physical state prior to an evaluated change.

**Observed State S(t₁)**  
The measured physical state after the evaluated change.

**Impact Horizon Δt**  
A time interval supplied as an external parameter defining the evaluation window.

**Impact Channel**  
A logically independent dimension of physical impact.

Normatively declared impact channels include, but are not limited to:

- Biosphere Integrity (e.g., B(t))
- Atmospheric Composition (e.g., CO₂ concentration)
- Human Health Proxies (derived from S(t))
- Resource Depletion (e.g., land-use change)

**Impact Vector Iᵢ(t₀ → t₁, Δt)**  
A channel-specific, bounded physical change metric.

**Reference Bounds Bᵢ**  
Invariant physical limits imported from DKP-1-AXIOMS-001 or PTL indices.

**Reversibility Flag Rᵢ**  
A boolean indicator of physical irreversibility.

**Externality Flag Xᵢ**  
A boolean indicator of boundary-crossing impact.

**Uncertainty Envelope Uᵢ**  
A bounded confidence interval propagated from PTL uncertainty.

---

## 5. Measurement Principle

Impact is defined strictly as the difference between two physical states:

S(t₀) → S(t₁) over Δt

For each impact channel *i*, let **Sᵢ(t)** denote the projection of **S(t)** onto channel *i*.

The protocol computes:

Iᵢ = ( Sᵢ(t₁) − Sᵢ(t₀) ) / Bᵢ

The resulting value is unaggregated and auditable.

If |Iᵢ| ≥ 1, a boundary crossing SHALL be flagged.

No aggregation across channels is permitted.

---

## 6. Reference Bounds and Boundary Detection

1. Each impact channel SHALL declare its applicable bounds **Bᵢ**.
2. Bounds MUST be:
   - Physically defined
   - Immutable within this protocol
   - Traceable to DKP-1-AXIOMS-001 or PTL indices
3. The protocol SHALL detect:
   - Boundary approach
   - Boundary crossing
4. Bounds SHALL NOT be modified, normalized, or reinterpreted.

---

## 7. Reversibility Classification

1. For each impact channel, the protocol SHALL evaluate reversibility using formal physical criteria.
2. Criteria MUST be:
   - Explicitly defined
   - Physically grounded
   - Binary in output
3. Illustrative criteria MAY include:
   - Entropy increase beyond reversible regimes
   - Irrecoverable loss of measured biospheric structures
   - Physically irreversible phase transitions  
   as verified via Physical Truth Layer data.
4. Subjective or intent-based assessments are forbidden.

---

## 8. Externality Detection

1. The protocol SHALL distinguish between internal and external impact.
2. System boundary SHALL default to planetary scale unless explicitly narrowed by higher-layer protocols.
3. Any detected boundary crossing SHALL set **Xᵢ = True**.
4. Absence of an explicit boundary definition SHALL be treated as full externality exposure.

---

## 9. Uncertainty Propagation

1. Measurement uncertainty from PTL inputs SHALL be propagated into each impact channel.
2. Propagation SHALL be deterministic; illustrative methods MAY include Bayesian ensembles derived from PTL posteriors (e.g., ±3σ confidence intervals).
3. Uncertainty SHALL NOT be used to suppress, downgrade, or invalidate detected impact.

---

## 10. Outputs

| Output | Description |
|--------|-------------|
| Iᵢ | Impact vector per channel |
| Bᵢ | Reference bounds per channel |
| Rᵢ | Reversibility flag |
| Xᵢ | Externality flag |
| Uᵢ | Uncertainty envelope |

No aggregated impact score SHALL be produced.

---

## 11. Cross-Layer Isolation Invariant

No higher-layer protocol may:

- Alter reference bounds
- Suppress impact channels
- Override reversibility or externality flags
- Inject valuation, weighting, or optimization logic

Violation constitutes a critical architectural breach.

---

## 12. Protocol Finality

Once finalized, this protocol is immutable.

Any modification requires:

- A new protocol identifier
- Explicit declaration of incompatibility
- Full-system revalidation under DKP-8-SIMULATION

**Protocol Hash (SHA-256):** [to be inserted at freeze]

---

## 13. Illustrative Example (Non-Normative)

**Input**

- Channel: Atmospheric Composition  
- S(t₀): CO₂ = 426.91 ppm  
- S(t₁): CO₂ = 427.00 ppm  
- Δt: 1 hour  
- Bᵢ: 450 ppm (Genesis-anchored bound)

**Output**

- Iᵢ ≈ 0.004  
- Rᵢ = False  
- Xᵢ = False  
- Uᵢ = ±0.01 ppm  

This example is illustrative only and not normative.
