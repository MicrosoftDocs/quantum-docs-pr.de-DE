---
uid: Microsoft.Quantum.Canon.ArrangedQubits
title: Arrangedqubits-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ArrangedQubits
qsharp.summary: Arrange control, target, and helper qubits according to an index
ms.openlocfilehash: 7f5cce3429b72f0ff6e00c2079241272881512da
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704498"
---
# <a name="arrangedqubits-function"></a>Arrangedqubits-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Anordnen von Steuerelement-, Ziel-und hilfsqubits gemäß einem Index

```qsharp
function ArrangedQubits (controls : Qubit[], target : Qubit, helper : Qubit[]) : Qubit[]
```


## <a name="description"></a>BESCHREIBUNG

Gibt ein Qubit-Array mit dem Ziel am Index 0 und Control i am Index 2 ^ i zurück.  Die hilfsqubits werden an alle anderen Positionen im Array eingefügt.

## <a name="input"></a>Eingabe

### <a name="controls--qubit"></a>Steuerelemente: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]




### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)




### <a name="helper--qubit"></a>Helper: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]





## <a name="output--qubit"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

