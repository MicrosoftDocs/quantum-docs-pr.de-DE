---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: Preparesparser multiconfigurationalstate-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 1182f79a33784cdb49cb13db5cc97a0a45e59f9f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703128"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a><span data-ttu-id="e71ba-102">Preparesparser multiconfigurationalstate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e71ba-102">PrepareSparseMultiConfigurationalState operation</span></span>

<span data-ttu-id="e71ba-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="e71ba-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="e71ba-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e71ba-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e71ba-105">Durch das Hinzufügen von Erregung zum anfänglichen Testzustand wird der Zustand der multikonfigurationsestatusvorbereitung des Test Zustands erhöht.</span><span class="sxs-lookup"><span data-stu-id="e71ba-105">Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.</span></span>

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e71ba-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e71ba-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="e71ba-107">initialstatepreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e71ba-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e71ba-108">Einheitlich zum Vorbereiten des anfänglichen Test Zustands.</span><span class="sxs-lookup"><span data-stu-id="e71ba-108">Unitary to prepare initial trial state.</span></span>


### <a name="excitations--jordanwignerinputstate"></a><span data-ttu-id="e71ba-109">Erregung: [jordanwignerinputstate](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="e71ba-109">excitations : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="e71ba-110">Erregung des anfänglichen Test Zustands, der durch die Amplitude der Erregung und die Qubit-Indizes dargestellt wird, für die die Erregung durchgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="e71ba-110">Excitations of initial trial state represented by the amplitude of the excitation and the qubit indices the excitation acts on.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="e71ba-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e71ba-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e71ba-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="e71ba-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e71ba-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e71ba-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

