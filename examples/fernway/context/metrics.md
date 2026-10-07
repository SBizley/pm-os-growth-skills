# Metrics

_Fictional example_

## North star
**Booked class spots per studio per week** (attended or paid). It
captures value for studios (full classes) and for Fernway (payments
volume).

## The tree under it
```
Booked spots per studio per week
├── New customer bookings
├── Repeat bookings (retention)
└── Spots recovered from cancellations   ← where this example lives
    ├── Late cancellations (< 12h before class)
    └── % of late-cancelled spots re-filled
```

## Guardrails
| Guardrail | Worry if |
|---|---|
| Customer app notification opt-out rate | Up more than 2 points |
| Studio churn | Any rise in the segment we change |
