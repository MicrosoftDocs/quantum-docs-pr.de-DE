---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: Applypauli-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: b3557c6d8b5a90019f6d4cfa7b405475a3ab39fb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844752"
---
# <a name="applypauli-operation"></a><span data-ttu-id="c3ffc-102">Applypauli-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c3ffc-102">ApplyPauli operation</span></span>

<span data-ttu-id="c3ffc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c3ffc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c3ffc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c3ffc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c3ffc-105">Wenn ein Multi-Qubit-Pauli-Operator angegeben ist, wendet den entsprechenden-Vorgang auf ein Register an.</span><span class="sxs-lookup"><span data-stu-id="c3ffc-105">Given a multi-qubit Pauli operator, applies the corresponding operation to a register.</span></span>

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c3ffc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3ffc-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="c3ffc-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="c3ffc-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="c3ffc-108">Ein multiqubit-Pauli-Operator, der als Array von Single-Qubit-Pauli-Operatoren dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c3ffc-108">A multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="c3ffc-109">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c3ffc-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c3ffc-110">Registrieren Sie sich, um den angegebenen Pauli-Vorgang auf anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="c3ffc-110">Register to apply the given Pauli operation on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3ffc-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3ffc-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="c3ffc-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c3ffc-112">Example</span></span>

<span data-ttu-id="c3ffc-113">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="c3ffc-113">The following are equivalent:</span></span>

```qsharp
ApplyPauli([PauliY, PauliZ, PauliX], target);
```

<span data-ttu-id="c3ffc-114">and</span><span class="sxs-lookup"><span data-stu-id="c3ffc-114">and</span></span>

```qsharp
Y(target[0]);
Z(target[1]);
X(target[2]);
```