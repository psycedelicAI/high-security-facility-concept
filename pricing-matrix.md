# High-Security Facility Pricing Matrix

## Mockup Concept

This repository contains a mockup pricing matrix for future high-security facility projects.  
It shows how project characteristics can affect estimated pricing.

All values are shown in **USD**.

---

## Pricing Formula

**Total Price = Base Fee × Threat Multiplier × Size Multiplier × Floor Multiplier × Site Multiplier**

---

## Base Fee

| Item | Value |
|---|---:|
| Base Fee | $20,000 |

---

## Threat Model Matrix

| Threat Level | Multiplier | Description |
|---|---:|---|
| Low | 1.0 | Standard security environment |
| Medium | 1.25 | Elevated security needs |
| High | 1.5 | Strong access control / monitoring |
| Critical | 2.0 | Very sensitive or high-risk environment |

---

## Facility Size Matrix

| Facility Size | Multiplier | Description |
|---|---:|---|
| Small | 1.0 | Compact footprint |
| Medium | 1.2 | Moderate area |
| Large | 1.4 | Significant footprint |
| Very Large | 1.7 | Campus-scale or complex footprint |

---

## Floor Matrix

| Floors | Multiplier | Description |
|---|---:|---|
| 1 Floor | 1.0 | Simple layout |
| 2–3 Floors | 1.1 | Some vertical complexity |
| 4–6 Floors | 1.2 | More access and coordination complexity |
| 7+ Floors | 1.3 | High structural and security complexity |

---

## Site Matrix

| Number of Sites | Multiplier | Description |
|---|---:|---|
| 1 Site | 1.0 | Single location |
| 2 Sites | 1.2 | Extra coordination |
| 3 Sites | 1.4 | Multi-site complexity |
| 4+ Sites | 1.6 | Heavy coordination load |

---

## Automatic Escalation Rules

A site should be upgraded to at least **Medium** if it contains any of the following:

- server room or root access
- privileged technical access
- escorted access zones
- sensitive infrastructure
- operationally critical systems

A site should be upgraded to **High** if it contains:

- multiple critical points
- broader technical control areas
- several privileged zones
- high-value or high-risk operations

A site should be upgraded to **Critical** if compromise would cause:

- serious operational disruption
- major security incident
- safety risk
- high-value infrastructure exposure

---

## Example Calculations

### Example A
- Threat: Medium = 1.25
- Size: Medium = 1.2
- Floors: 2–3 = 1.1
- Sites: 1 = 1.0

**$20,000 × 1.25 × 1.2 × 1.1 × 1.0 = $33,000**

---

### Example B
- Threat: High = 1.5
- Size: Large = 1.4
- Floors: 4–6 = 1.2
- Sites: 2 = 1.2

**$20,000 × 1.5 × 1.4 × 1.2 × 1.2 = $60,480**

---

### Example C
- Threat: Critical = 2.0
- Size: Very Large = 1.7
- Floors: 7+ = 1.3
- Sites: 3 = 1.4

**$20,000 × 2.0 × 1.7 × 1.3 × 1.4 = $123,520**

---

## Purpose

This project is a conceptual mockup intended to show how future project scope can influence pricing.  
It is not a final commercial quote.

---

## Notes

- All prices are shown in **USD**
- The model is intended for demonstration and planning
- Multipliers can be adjusted depending on future project complexity
