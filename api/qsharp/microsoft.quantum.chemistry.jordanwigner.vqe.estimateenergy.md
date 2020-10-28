---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Estimateenergy-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: 52e527a68818c80f93bc177d3563064fd0f2aea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703086"
---
# <a name="estimateenergy-operation"></a>Estimateenergy-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paketen [](https://nuget.org/packages/)


Schätzt die Energie des Moleküls, indem die von den einzelnen Jordan-Wigner Begriffen beigetragene Energie summiert wird.

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a>BESCHREIBUNG

Dieser Vorgang basiert implizit auf der Indizierungs Konvention für die Aufgliederung.

## <a name="input"></a>Eingabe

### <a name="jwhamiltonian--jordanwignerencodingdata"></a>jwhamiltonan: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Der Jordan-Wigner hamiltonan.


### <a name="nsamples--int"></a>nsamples: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Samplings, die für die Schätzung der Begriffs Erwartungen verwendet werden sollen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Die geschätzte Energie des Moleküls