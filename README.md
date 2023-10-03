# xray-cli-tests

- AGPL: https://www.nuget.org/packages/itext7.font-asian
- Unlicensed: https://www.nuget.org/packages/Application.DTO
- MIT: https://www.nuget.org/packages/kafkaflow.retry


## xRay configuration

 - Policy with rule that ban "Unlicense" and Disallow Unknown License
 - Rule that ban "AGPL-*" licenses and Disallow Unknown License
 - Watch named "Licensing" for nuget public repositories  


## Run audit
1. Go to `Sample/SampleLibrary/`
2. Run `jf audit --watches "Licensing"`

### Result

Security Violations
┌───────────────────────────────────┐
│ No security violations were found │
└───────────────────────────────────┘
License Compliance Violations
┌─────────┬─────────┬─────────┬─────────┬─────────┬─────────┬─────────┬───────┐
│ LICENSE │ SEVERIT │ CONTEXT │ DIRECT  │ DIRECT  │ IMPACTE │ IMPACTE │ TYPE  │
│         │ Y       │ UAL     │ DEPENDE │ DEPENDE │ D       │ D       │       │
│         │         │ ANALYSI │ NCY     │ NCY     │ DEPENDE │ DEPENDE │       │
│         │         │ S       │         │ VERSION │ NCY     │ NCY     │       │
│         │         │         │         │         │         │ VERSION │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ System. │ 4.7.0   │ NuGet │
│         │         │         │ ow.Retr │         │ Windows │         │       │
│         │         │         │ y       │         │ .Extens │         │       │
│         │         │         │         │         │ ions    │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │         │         │ root    │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ SampleL │         │ SampleL │         │ NuGet │
│         │         │         │ ibrary  │         │ ibrary  │         │       │
│         │         │         │         │         │         │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ Applica │ 1.0.0   │ AutoMap │ 3.2.1   │ NuGet │
│         │         │         │ tion.DT │         │ per     │         │       │
│         │         │         │ O       │         │         │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ Microso │ 2.1.3   │ NuGet │
│         │         │         │ ow.Retr │         │ ft.IO.R │         │       │
│         │         │         │ y       │         │ ecyclab │         │       │
│         │         │         │         │         │ leMemor │         │       │
│         │         │         │         │         │ yStream │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ AGPL-3. │ 🔥High  │         │ itext7. │ 8.0.1   │ itext7. │ 8.0.1   │ NuGet │
│ 0       │         │         │ font-as │         │ font-as │         │       │
│         │         │         │ ian     │         │ ian     │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ itext7. │ 8.0.1   │ itext.f │ 8.0.1   │ NuGet │
│         │         │         │ font-as │         │ ont-asi │         │       │
│         │         │         │ ian     │         │ an      │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ KafkaFl │ 2.2.15  │ NuGet │
│         │         │         │ ow.Retr │         │ ow.Abst │         │       │
│         │         │         │ y       │         │ raction │         │       │
│         │         │         │         │         │ s       │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ KafkaFl │ 2.2.15  │ NuGet │
│         │         │         │ ow.Retr │         │ ow.Seri │         │       │
│         │         │         │ y       │         │ alizer  │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ KafkaFl │ 2.2.15  │ NuGet │
│         │         │         │ ow.Retr │         │ ow.Seri │         │       │
│         │         │         │ y       │         │ alizer. │         │       │
│         │         │         │         │         │ Newtons │         │       │
│         │         │         │         │         │ oftJson │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ KafkaFl │ 2.2.15  │ NuGet │
│         │         │         │ ow.Retr │         │ ow.Type │         │       │
│         │         │         │ y       │         │ dHandle │         │       │
│         │         │         │         │         │ r       │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ Microso │ 4.7.0   │ NuGet │
│         │         │         │ ow.Retr │         │ ft.Win3 │         │       │
│         │         │         │ y       │         │ 2.Syste │         │       │
│         │         │         │         │         │ mEvents │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ Applica │ 1.0.0   │ Applica │ 1.0.0   │ NuGet │
│         │         │         │ tion.DT │         │ tion.DT │         │       │
│         │         │         │ O       │         │ O       │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ KafkaFl │ 2.1.2   │ NuGet │
│         │         │         │ ow.Retr │         │ ow.Retr │         │       │
│         │         │         │ y       │         │ y       │         │       │
├─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼─────────┼───────┤
│ Unknown │ 🔥High  │         │ KafkaFl │ 2.1.2   │ KafkaFl │ 2.2.15  │ NuGet │
│         │         │         │ ow.Retr │         │ ow      │         │       │
│         │         │         │ y       │         │         │         │       │
└─────────┴─────────┴─────────┴─────────┴─────────┴─────────┴─────────┴───────

## Run Scan

1. Download the kafkaflow.retry packages above (version 2.1.2)
2. Run the scan `jf scan kafkaflow.retry.2.1.2.nupkg --watches "Licensing"`

```
Security Violations
┌───────────────────────────────────┐
│ No security violations were found │
└───────────────────────────────────┘
License Compliance Violations
┌─────────────────────────────────────────────┐
│ No license compliance violations were found │
└─────────────────────────────────────────────┘
14:04:56 [🔵Info] Scan completed successfully.
```
