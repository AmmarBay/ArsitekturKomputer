# Arbitrasi Bus Sistem

## Diagram Simulasi Arbitrasi Bus
Diagram di bawah ini menunjukkan bagaimana *Bus Arbiter* mengatur akses agar tidak terjadi tabrakan data saat modul I/O ingin mengirim data.

```mermaid
sequenceDiagram
    participant CPU
    participant Arbiter as Bus Arbiter
    participant IO as Modul I/O
    
    IO->>Arbiter: Request Bus
    Arbiter-->>IO: Grant Bus (Access)
    IO->>IO: Transmisi Data
    IO->>Arbiter: Release Bus
```
