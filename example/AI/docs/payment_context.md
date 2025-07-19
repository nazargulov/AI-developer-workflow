# Payment Context for AI

## Payment Processing Domain

- **Purpose:** Handle financial transactions securely and efficiently
- **Integration Points:** Payment gateways, fraud detection, currency conversion

## Key Components

- **Payment Methods:** Credit cards, e-wallets, bank transfers
- **Transaction Flow:** Authorization → Capture → Settlement → Reconciliation
- **Fraud Prevention:** Real-time monitoring, risk scoring, behavioral analysis
- **Currency Support:** Multi-currency processing with real-time exchange rates

## Critical Business Rules

- **Transaction Limits:** User-based, method-based, time-based restrictions
- **Validation Requirements:** Compliance, address verification
- **Error Handling:** Graceful failures, retry mechanisms, user notifications
- **Audit Trail:** Complete transaction logging for compliance

## Security Considerations

- **Encryption:** End-to-end encryption for sensitive data
- **Access Control:** Role-based permissions, API security
- **Monitoring:** Real-time fraud detection, anomaly detection

## Integration Examples

```javascript
// Payment processing workflow
async function processPayment(paymentData) {
  // 1. Validate payment data
  // 2. Check fraud rules
  // 3. Process with gateway
  // 4. Handle response
  // 5. Update transaction status
}
```

## Common AI Applications

- Fraud detection and prevention
- Risk assessment automation
- Customer payment behavior analysis
- Automated compliance checking
- Transaction categorization
- Payment optimization suggestions

## Testing Scenarios

- Valid payment processing
- Fraud detection triggers
- Failed payment handling
- Currency conversion accuracy
- Compliance validation
- Performance under load
