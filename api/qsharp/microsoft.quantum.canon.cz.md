---
uid: Microsoft.Quantum.Canon.CZ
title: CZ-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CZ
qsharp.summary: >-
  Applies the controlled-Z (CZ) gate to a pair of qubits.

  $$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.
ms.openlocfilehash: cef1544fb76d561cfd0949c84c487550d523bb85
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840707"
---
# <a name="cz-operation"></a><span data-ttu-id="d66fe-102">CZ-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d66fe-102">CZ operation</span></span>

<span data-ttu-id="d66fe-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d66fe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d66fe-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d66fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d66fe-105">Wendet das Tor der kontrollierten-Z (CZ) auf ein paar von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="d66fe-105">Applies the controlled-Z (CZ) gate to a pair of qubits.</span></span>

<span data-ttu-id="d66fe-106">$ $ \begin{align} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 0 & 0 &-1 \end{align}, $ $, wobei Zeilen und Spalten im Quantum-Konzept Handbuch organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="d66fe-106">$$ \begin{align} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 0 & 0 & -1 \end{align}, $$ where rows and columns are organized as in the quantum concepts guide.</span></span>

```qsharp
operation CZ (control : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d66fe-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d66fe-107">Input</span></span>

### <a name="control--qubit"></a><span data-ttu-id="d66fe-108">Control: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d66fe-108">control : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d66fe-109">Steuerelement-Qubit für das CZ-Gate.</span><span class="sxs-lookup"><span data-stu-id="d66fe-109">Control qubit for the CZ gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d66fe-110">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d66fe-110">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d66fe-111">Ziel-Qubit für das CZ-Gate.</span><span class="sxs-lookup"><span data-stu-id="d66fe-111">Target qubit for the CZ gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d66fe-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d66fe-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d66fe-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d66fe-113">Remarks</span></span>

<span data-ttu-id="d66fe-114">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="d66fe-114">Equivalent to:</span></span>

```qsharp
Controlled Z([control], target);
```