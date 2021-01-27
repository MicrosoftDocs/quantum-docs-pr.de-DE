---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Estimateenergy-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: a64ac3970e3e67568f91b4e67775d834a80c04a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835728"
---
# <a name="estimateenergy-operation"></a>Estimateenergy-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Schätzt die Energie des Moleküls, indem die von den einzelnen Jordan-Wigner Begriffen beigetragene Energie summiert wird.

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a>Beschreibung

Dieser Vorgang basiert implizit auf der Indizierungs Konvention für die Aufgliederung.

## <a name="input"></a>Eingabe

### <a name="jwhamiltonian--jordanwignerencodingdata"></a>jwhamiltonan: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Der Jordan-Wigner hamiltonan.


### <a name="nsamples--int"></a>nsamples: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Samplings, die für die Schätzung der Begriffs Erwartungen verwendet werden sollen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Die geschätzte Energie des Moleküls