---
uid: Microsoft.Quantum.Preparation.QuantumROMQubitCount
title: Quantenromqubitcount-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: QuantumROMQubitCount
qsharp.summary: Returns the total number of qubits that must be allocated to the operation returned by `QuantumROM`.
ms.openlocfilehash: 988d5efa3e27cf5e9a276ab3ab443c10f88fe1ad
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722933"
---
# <a name="quantumromqubitcount-function"></a>Quantenromqubitcount-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paketen [](https://nuget.org/packages/)


Gibt die Gesamtanzahl der Qubits zurück, die dem von zurückgegebenen Vorgang zugeordnet werden müssen `QuantumROM` .

```qsharp
function QuantumROMQubitCount (targetError : Double, nCoeffs : Int) : (Int, (Int, Int))
```


## <a name="input"></a>Eingabe

### <a name="targeterror--double"></a>targeterror: [Double](xref:microsoft.quantum.lang-ref.double)

Der Ziel Fehler $ \epsilon $.


### <a name="ncoeffs--int"></a>ncoeffs: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl der in angegebenen Koeffizienten `QuantumROM` .



## <a name="output--intintint"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)))

## <a name="first-parameter"></a>Erster Parameter

Ein Tupel `(x,(y,z))` , bei dem `x = y + z` die Gesamtzahl der zugeordneten Qubits ist, `y` die Anzahl der Qubits für das `LittleEndian` Register und `z` die Anzahl der Garbage Qubits.