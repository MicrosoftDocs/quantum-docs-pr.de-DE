---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Vorgang "carryoutcorecdkm"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 6a292e66f6d9911d2a9075f6397f4f5ba97ec64d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707399"
---
# <a name="carryoutcorecdkm-operation"></a>Vorgang "carryoutcorecdkm"

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Der Kern Vorgang in ripplecarryaddercdkm, der mit dem obigen applyoutercdkmadder-Vorgang verwendet wird, der mit diesem Vorgang konjuregiert wurde, um die innere Operation von ripplecarryaddercdkm abzurufen. Mit diesem Vorgang wird das Qubit "ausführen" berechnet und eine Sequenz von "Not Gates" auf einen Teil der Eingabe angewendet `ys` .

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Erstes Qubit-Register.


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Zweites Qubit-Register.


### <a name="ancilla--qubit"></a>Ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das in ripplecarryaddercdkm verwendete Ancilla-Qubit, das an diesen Vorgang übergeben wird.


### <a name="carry--qubit"></a>Carry: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Führen Sie Qubit im ripplecarryaddercdkm-Vorgang aus.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton: "A New Quantum Ripple-Carry Additions Circuit", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1