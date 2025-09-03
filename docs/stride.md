# Matriz STRIDE (resumen)

| Amenaza | Riesgo | Mitigaciones |
|---|---|---|
| Spoofing | Suplantación de identidades (tokens, dispositivos) | OIDC con PKCE, mTLS interno, JWT audience binding, detección de reuse refresh |
| Tampering | Alteración de datos y mensajes | Firmas/HMAC en auditoría, hash encadenado, TLS1.2+, WORM para evidencias |
| Repudiation | Negación de acciones | Logs con traceId, auditoría inmutable, sincronía reloj NTP, firmas |
| Information Disclosure | Fuga de datos personales/financieros | Cifrado en reposo (KMS), seudonimización, mínimos privilegios, tokenización PAN |
| Denial of Service | Agotamiento de recursos/colapso SPI/Core | Rate limiting, circuit breakers, colas, autoscaling, bulkheads |
| Elevation of Privilege | Escalada de permisos | ABAC/OPA, RBAC en consola, MFA admin, revisión de permisos periódica |