---
uid: Microsoft.Quantum.Arithmetic.RippleCarryAdderNoCarryTTK
title: Ripplecarryaddernocarryttk-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: RippleCarryAdderNoCarryTTK
qsharp.summary: Reversible, in-place ripple-carry addition of two integers without carry out.
ms.openlocfilehash: 59451b4f5c992f900a27139332059af7427b9b93
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706250"
---
# <a name="ripplecarryaddernocarryttk-operation"></a>Ripplecarryaddernocarryttk-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Umkehrbar, direkte Ripple-Durchführung von zwei Ganzzahlen ohne Ausführung.

```qsharp
operation RippleCarryAdderNoCarryTTK (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei zwei $n in den littleEndian-Registern und in den littleEndian-Registern codierten $-Bit-Ganzzahlen `xs` `ys` berechnet der Vorgang die Summe der beiden integger Modulo $2 ^ n $, wobei $n $ die bitgröße der Eingaben `xs` und ist `ys` . Das Bit wird nicht berechnet.

## <a name="input"></a>Eingabe

### <a name="xs--littleendian"></a>xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Der littleEndian-Qubit-Register Codierung der ersten ganzzahligen Summe.


### <a name="ys--littleendian"></a>YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Der littleEndian-Qubit-Registrierungs Codierungs Wert für die zweite Ganzzahl sumund wird so geändert, dass die $n minimalen signifikanten Bits der Summe enthalten ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Dieser Vorgang verfügt über die gleiche Funktionalität wie ripplecarryadderttk, gibt jedoch nicht das "Carry"-Bit zurück.

## <a name="references"></a>Referenzen

- Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Additions-und ungebundene Fan-Out", Quantum-Informationen und-Berechnung, Vol. 10, 2010.
  https://arxiv.org/abs/0910.2530