---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Selectz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 2b38be5c196d81635daa8b478f6e727fdf378c62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850237"
---
# <a name="selectz-operation"></a><span data-ttu-id="8cd9f-102">Selectz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8cd9f-102">SelectZ operation</span></span>

<span data-ttu-id="8cd9f-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="8cd9f-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="8cd9f-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8cd9f-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="8cd9f-105">Ein einheitlicher $U $, der die Pauli $Z $ Gate auf eine Qubits $p $ anwendet, die auf einem Index Status $ \ket{p} $ bedingt ist.</span><span class="sxs-lookup"><span data-stu-id="8cd9f-105">A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$.</span></span> <span data-ttu-id="8cd9f-106">Das heißt: $ $ \begin{align} u\ket {p} \ Ket {\ PSI} = \ket{p}Z \_ p\ket {\ PSI} \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="8cd9f-106">That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$</span></span>

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="8cd9f-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8cd9f-107">Input</span></span>

### <a name="indexregister--littleendian"></a><span data-ttu-id="8cd9f-108">Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8cd9f-108">indexRegister : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8cd9f-109">Der Status $ \ket{p} $ dieses Registers bestimmt das Qubit, auf dem $Z $ angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cd9f-109">The state $\ket{p}$ of this register determines the qubit on which $Z$ is applied.</span></span>


### <a name="targetregister--qubit"></a><span data-ttu-id="8cd9f-110">targetregiester: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8cd9f-110">targetRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8cd9f-111">Das Register der Qubits, auf die die Pauli-Operatoren angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cd9f-111">Register of qubits on which the Pauli operators are applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8cd9f-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8cd9f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

