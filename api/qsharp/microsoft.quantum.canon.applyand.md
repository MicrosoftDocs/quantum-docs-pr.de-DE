---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: Applyand-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: b749013584c89273375da002ac36b3575085b7f2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219293"
---
# <a name="applyand-operation"></a>Applyand-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Kehrt ein angegebenes Ziel-Qubit nur dann ein, wenn beide Steuerelement-Qubits den Status 1 aufweisen, wobei die Messung zum Ausführen des Adjoint-Vorgangs verwendet wird.

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Kehrt `target` nur dann zu, wenn beide Steuerelemente 1 sind, jedoch wird davon ausgegangen, dass `target` sich der Status 0 (null) befindet.  Der Vorgang hat t-count 4, T-Tiefe 2 und erfordert kein Hilfsobjekt und ist daher möglicherweise einem ccnot-Vorgang vorzuziehen, wenn `target` bekanntermaßen 0 ist.  Das Adjoint-Ergebnis dieses Vorgangs ist Messungs basiert und erfordert keine T-Gates.

Die kontrollierte Anwendung dieses Vorgangs erfordert kein Hilfsobjekt, `2^c` `Rz` Gates und ist nicht für die Tiefe optimiert, wobei `c` die Anzahl der allgemeinen Steuerungs Qubits einschließlich der beiden Steuerelemente des `ApplyAnd` Vorgangs ist.  Die Adjoint-gesteuerte Anwendung erfordert `2^c - 1` `Rz` Gates (bei einem doppelten Winkel die Größe des nicht-Adjoint-Vorgangs), kein hilfssbit und ist nicht für die Tiefe optimiert.

## <a name="input"></a>Eingabe

### <a name="control1--qubit"></a>Control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit für erstes Steuerelement


### <a name="control2--qubit"></a>Control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit für zweites Steuerelement


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Zusätzliches Qubit für Ziel muss den Status 0 aufweisen.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- Cody Jones: "neuartige Konstruktionen für das Fault-tolerante yffoli Gate", Phys. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/physreva. 87.022328
- Craig Gidney: "halbieren der Kosten der Quantum-Addition", Quantum 2, Seite 74, 2018 [arXiv: 1709.06648](https://arxiv.org/abs/1709.06648) doi: 10.1103/physreva. 85.044302
- Mathias soeken: "Quantum Oracle-Leitungen und das Weihnachtsbaum Muster", [Blog-Artikel vom 19. Dezember 2019](https://msoeken.github.io/blog_qac.html) (Hinweis: erläutert die mehrfach gesteuerte Konstruktion)