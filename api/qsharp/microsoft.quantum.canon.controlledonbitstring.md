---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: Controlledonbitstring-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 176170cc972ca67b812b84f79cf97ba5418be9b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840801"
---
# <a name="controlledonbitstring-function"></a>Controlledonbitstring-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen einheitlichen Vorgang zurück, der ein Oracle auf das Ziel Register anwendet, wenn der Steuerelement Registrierungs Zustand einer angegebenen Bitmaske entspricht.

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a>Beschreibung

Die Ausgabe dieser Funktion ist ein Vorgang, der durch eine einheitliche Transformation $U $ dargestellt werden kann, sodass \begin{align} U \ket{b_0 B_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 B_1 \cdots b_ {n-1}} \otimes \begin{Cases} V \ket{\psi} & \textrm{if} (b_0 B_1 \cdots b_ {n-1}) = \texttt{Bits} \\ \\ \ket{\psi} & \textrm{otherwits} \end{Cases}, \end{align}, wobei $V $ eine einheitliche Transformation ist, die die Aktion des `oracle` Vorgangs darstellt.

## <a name="input"></a>Eingabe

### <a name="bits--bool"></a>Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Die Bitzeichenfolge, für die der angegebene einheitliche Vorgang gesteuert werden soll.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Der auf das Ziel Register anzuwendende einheitliche Vorgang.



## <a name="output--qubitt--unit--is-adj--ctl"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher Vorgang, `oracle` der für das Ziel Register gilt, wenn der Steuerelement Registrierungs Zustand der Bitmaske entspricht `bits` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="example"></a>Beispiel

Die folgenden Code Ausschnitte sind gleichwertig:

```qsharp
(ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
```

and

```qsharp
within {
    ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
} apply {
    Controlled oracle(controlRegister, targetRegister);
}
```

Der folgende Code bereitet den Status $ \frac {1} {2} (\ket {00} -\ket {01} + \ket {10} + \ket {11} ) $:

```qsharp
using (register = Qubit[2]) {
    ApplyToEach(H, register);
    (ControlledOnBitString([false], Z))(register[0..0], register[1]);
}
```

## <a name="remarks"></a>Bemerkungen

Das von angegebene Muster `bits` ist möglicherweise kürzer als `controlRegister` . in diesem Fall werden zusätzliche Steuerungs-Qubits ignoriert (d. h., Sie werden nicht für "$ \ket {0} $" und "$ \ket $" gesteuert {1} ).
Wenn `bits` länger als ist `controlRegister` , wird ein Fehler ausgelöst.

Bei einem booleschen Array `bits` und einem einheitlichen Vorgang `oracle` ist die Ausgabe dieser Funktion ein Vorgang, der die folgenden Schritte ausführt:

* wenden `X` Sie einen Vorgang auf jedes Qubit des Steuerelement Registrierungs Elements an, das dem- `false` Element von entspricht `bits` .
* `Controlled oracle`auf das Steuerelement und die Ziel Register anwenden;
* wenden `X` Sie einen Vorgang auf jedes Qubit des Steuerelement Registrierungs Elements an, das dem- `false` Element des-Elements entspricht, `bits` um das Steuerelement in den ursprünglichen Zustand zurückzukehren.

Die Ausgabe des `Controlled` funktors ist ein Sonderfall von `ControlledOnBitString` , wobei `bits` gleich ist `[true, ..., true]` .