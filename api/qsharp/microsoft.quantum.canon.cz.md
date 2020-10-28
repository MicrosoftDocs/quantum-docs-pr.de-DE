---
uid: Microsoft.Quantum.Canon.CZ
title: CZ-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CZ
qsharp.summary: >-
  Applies the controlled-Z (CZ) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: bc38cd43a0dcaf7aea735ef6468a394e91c85593
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704271"
---
# <a name="cz-operation"></a><span data-ttu-id="5f9ad-102">CZ-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5f9ad-102">CZ operation</span></span>

<span data-ttu-id="5f9ad-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5f9ad-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5f9ad-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5f9ad-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5f9ad-105">Wendet das Tor der kontrollierten-Z (CZ) auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-105">Applies the controlled-Z (CZ) gate to a pair of qubits.</span></span>

<span data-ttu-id="5f9ad-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 0 & 0 &-1 \end{align}, $ $, wobei Zeilen und Spalten im Quantum-Konzept Handbuch organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CZ (control : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="5f9ad-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f9ad-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="5f9ad-108">Control: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5f9ad-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5f9ad-109">Steuerelement-Qubit für das CZ-Gate.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-109">Control qubit for the CZ gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="5f9ad-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5f9ad-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5f9ad-111">Ziel-Qubit für das CZ-Gate.</span><span class="sxs-lookup"><span data-stu-id="5f9ad-111">Target qubit for the CZ gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5f9ad-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5f9ad-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5f9ad-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f9ad-113">Remarks</span></span>

<span data-ttu-id="5f9ad-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="5f9ad-114">Equivalent to:</span></span>

```qsharp
Controlled Z([control], target);
```