---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Reflectaboutinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706338"
---
# <a name="reflectaboutinteger-operation"></a>Reflectaboutinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Reflektiert ein Quantum-Register über eine angegebene klassische Ganzzahl.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Wenn ein Quantum-Register anfänglich im Status $ \ sum_i \ alpha_i \ket{i} $, wobei jede $ \ket{i} $ ein Basiszustand ist, der eine ganze Zahl $i $ darstellt, gibt den Status des Registers zum Basisstatus für eine gegebene Ganzzahl $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $ an.

## <a name="input"></a>Eingabe

### <a name="index--int"></a>Index: [int](xref:microsoft.quantum.lang-ref.int)

Die klassische Ganzzahl, die den Basiszustand indiziert, der reflektiert werden soll.


### <a name="reg--littleendian"></a>reg: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Dieser Vorgang wird direkt implementiert, ohne dass zusätzliche Qubits explizit zugeordnet werden müssen.