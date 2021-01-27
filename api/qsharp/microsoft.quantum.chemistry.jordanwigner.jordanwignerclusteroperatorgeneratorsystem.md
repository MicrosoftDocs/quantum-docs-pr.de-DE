---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerClusterOperatorGeneratorSystem
title: Jordanwignerclusteroperatorgeneratorsystem-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerClusterOperatorGeneratorSystem
qsharp.summary: Converts a Hamiltonian described by `JWOptimizedHTerms` to a `GeneratorSystem` expressed in terms of the `GeneratorIndex` convention defined in this file.
ms.openlocfilehash: 685ae508e7c2f04ff0de48ecc0a39e80d6d9f2cb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839000"
---
# <a name="jordanwignerclusteroperatorgeneratorsystem-function"></a>Jordanwignerclusteroperatorgeneratorsystem-Funktion

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Konvertiert eine von beschriebene hamiltona `JWOptimizedHTerms` in eine, `GeneratorSystem` die in Bezug auf die `GeneratorIndex` in dieser Datei definierte Konvention ausgedrückt wird.

```qsharp
function JordanWignerClusterOperatorGeneratorSystem (data : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Eingabe

### <a name="data--jordanwignerinputstate"></a>Daten: [jordanwignerinputstate](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]

Beschreibung von hamiltonan im `JWOptimizedHTerms` Format.



## <a name="output--generatorsystem"></a>Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Darstellung von hamiltonan als `GeneratorSystem` .