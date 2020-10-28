---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: Controlledonbitstring-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: ca5a6e116eff187060f7a160e42836b170f0362d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704327"
---
# <a name="controlledonbitstring-function"></a>Controlledonbitstring-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt einen einheitlichen Vorgang zurück, der ein Oracle auf das Ziel Register anwendet, wenn der Steuerelement Registrierungs Zustand einer angegebenen Bitmaske entspricht.

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a>BESCHREIBUNG

Die Ausgabe dieser Funktion ist ein Vorgang, der durch eine einheitliche Transformation $U $ dargestellt werden kann, sodass \begin{align} U \ket{b_0 B_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 B_1 \cdots b_ {n-1}} \otimes \begin{Cases} V \ket{\psi} & \textrm{if} (b_0 B_1 \cdots b_ {n-1}) = \texttt{Bits} \\ \\ \ket{\psi} & \textrm{otherwits} \end{Cases}, \end{align}, wobei $V $ eine einheitliche Transformation ist, die die Aktion des `oracle` Vorgangs darstellt.

## <a name="input"></a>Eingabe

### <a name="bits--bool"></a>Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Die Bitzeichenfolge, für die der angegebene einheitliche Vorgang gesteuert werden soll.


### <a name="oracle--t--unit-adj--ctl"></a>Oracle: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der auf das Ziel Register anzuwendende einheitliche Vorgang.



## <a name="output--qubitt--unit-adj--ctl"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein einheitlicher Vorgang, `oracle` der für das Ziel Register gilt, wenn der Steuerelement Registrierungs Zustand der Bitmaske entspricht `bits` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Hinweise

Das von angegebene Muster `bits` ist möglicherweise kürzer als `controlRegister` . in diesem Fall werden zusätzliche Steuerungs-Qubits ignoriert (d. h., Sie werden nicht für "$ \ket {0} $" und "$ \ket $" gesteuert {1} ).
Wenn `bits` länger als ist `controlRegister` , wird ein Fehler ausgelöst.

Bei einem booleschen Array `bits` und einem einheitlichen Vorgang `oracle` ist die Ausgabe dieser Funktion ein Vorgang, der die folgenden Schritte ausführt:

* wenden `X` Sie einen Vorgang auf jedes Qubit des Steuerelement Registrierungs Elements an, das dem- `false` Element von entspricht `bits` .
* `Controlled oracle`auf das Steuerelement und die Ziel Register anwenden;
* wenden `X` Sie einen Vorgang auf jedes Qubit des Steuerelement Registrierungs Elements an, das dem- `false` Element des-Elements entspricht, `bits` um das Steuerelement in den ursprünglichen Zustand zurückzukehren.

Die Ausgabe des `Controlled` funktors ist ein Sonderfall von `ControlledOnBitString` , wobei `bits` gleich ist `[true, ..., true]` .