---
uid: Microsoft.Quantum.ErrorCorrection.TableLookupRecovery
title: Tablelookuprecovery-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: TableLookupRecovery
qsharp.summary: For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.
ms.openlocfilehash: 9f957155e42bb6b5163521171fcba5897f290335
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824394"
---
# <a name="tablelookuprecovery-function"></a><span data-ttu-id="34194-102">Tablelookuprecovery-Funktion</span><span class="sxs-lookup"><span data-stu-id="34194-102">TableLookupRecovery function</span></span>

<span data-ttu-id="34194-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="34194-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="34194-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="34194-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="34194-105">Für eine gegebene Tabelle von Pauli-Vorgängen für ein bestimmtes Register von Qubits gibt diese Funktion ein Objekt vom Typ zurück, `RecoveryFn` das alle Informationen enthält, die erforderlich sind, um eine Table-Lookup-Decodierung in Bezug auf das angegebene Array von Pauli-Vorgängen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="34194-105">For a given table of Pauli operations on a given register of qubits, this function returns an object of type `RecoveryFn` which contains all information needed to perform a table-lookup decoding with respect to the given array of Pauli operations.</span></span>

```qsharp
function TableLookupRecovery (table : Pauli[][]) : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="input"></a><span data-ttu-id="34194-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34194-106">Input</span></span>

### <a name="table--pauli"></a><span data-ttu-id="34194-107">Tabelle: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="34194-107">table : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="34194-108">Tabelle von Pauli-Vorgängen, die für ein bestimmtes Qubit-Register ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="34194-108">Table of Pauli operations that operate on a given qubit register</span></span>



## <a name="output--recoveryfn"></a><span data-ttu-id="34194-109">Ausgabe: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span><span class="sxs-lookup"><span data-stu-id="34194-109">Output : [RecoveryFn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)</span></span>

<span data-ttu-id="34194-110">Ein Objekt vom Typ `RecoveryFn` , d. h. eine Zuordnung, `Syndrome -> Pauli[]` die einem angegebenen-Syndrom-Array einen entsprechenden Pauli-Korrektur Vorgang zuordnet.</span><span class="sxs-lookup"><span data-stu-id="34194-110">An object of type `RecoveryFn`, i.e., a map `Syndrome -> Pauli[]` that associates with a given syndrome array a corresponding Pauli correction operation.</span></span>