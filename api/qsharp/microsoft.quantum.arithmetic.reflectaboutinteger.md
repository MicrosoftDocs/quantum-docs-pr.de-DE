---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Reflectaboutinteger-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: 4d451c4e8e002f86c892b394f58ea2d7e9dd6a48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842977"
---
# <a name="reflectaboutinteger-operation"></a>Reflectaboutinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Reflektiert ein Quantum-Register über eine angegebene klassische Ganzzahl.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

Wenn ein Quantum-Register anfänglich im Status $ \ sum_i \ alpha_i \ket{i} $, wobei jede $ \ket{i} $ ein Basiszustand ist, der eine ganze Zahl $i $ darstellt, gibt den Status des Registers zum Basisstatus für eine gegebene Ganzzahl $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $ an.

## <a name="input"></a>Eingabe

### <a name="index--int"></a>Index: [int](xref:microsoft.quantum.lang-ref.int)

Die klassische Ganzzahl, die den Basiszustand indiziert, der reflektiert werden soll.


### <a name="reg--littleendian"></a>reg: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Dieser Vorgang wird direkt implementiert, ohne dass zusätzliche Qubits explizit zugeordnet werden müssen.