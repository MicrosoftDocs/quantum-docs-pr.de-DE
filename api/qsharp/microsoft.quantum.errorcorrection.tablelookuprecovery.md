---
uid: Microsoft.Quantum.ErrorCorrection.TableLookupRecovery
title: Tablelookuprecovery-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: TableLookupRecovery
qsharp.summary: For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.
ms.openlocfilehash: e4136add99ab7fb6904d7cac3c7f3e5076cc3176
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213666"
---
# <a name="tablelookuprecovery-function"></a>Tablelookuprecovery-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Für eine gegebene Tabelle von Pauli-Vorgängen für ein bestimmtes Register von Qubits gibt diese Funktion ein Objekt vom Typ zurück, `RecoveryFn` das alle Informationen enthält, die erforderlich sind, um eine Table-Lookup-Decodierung in Bezug auf das angegebene Array von Pauli-Vorgängen auszuführen.

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a>Eingabe

### <a name="table--pauli"></a>Tabelle: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Tabelle von Pauli-Vorgängen, die für ein bestimmtes Qubit-Register ausgeführt werden



## <a name="output--recoveryfn"></a>Ausgabe: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Ein Objekt vom Typ `RecoveryFn` , d. h. eine Zuordnung, `Syndrome -> Pauli[]` die einem angegebenen-Syndrom-Array einen entsprechenden Pauli-Korrektur Vorgang zuordnet.