---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Featureregistersize-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: bc5d5a23cfb431f9506b15bc404ab6955d1c2a35
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196411"
---
# <a name="featureregistersize-function"></a><span data-ttu-id="2509f-102">Featureregistersize-Funktion</span><span class="sxs-lookup"><span data-stu-id="2509f-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="2509f-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2509f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2509f-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2509f-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="2509f-105">Gibt die Anzahl von Qubits zurück, die erforderlich sind, um einen bestimmten featurevektor zu codieren.</span><span class="sxs-lookup"><span data-stu-id="2509f-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="2509f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2509f-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="2509f-107">Beispiel: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="2509f-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="2509f-108">Ein Beispiel Funktions Vektor, der in ein Qubit-Register codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2509f-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="2509f-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2509f-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2509f-110">Die zum Codieren `sample` in ein Qubit-Register erforderliche Größe, ausgedrückt als Anzahl von Qubits.</span><span class="sxs-lookup"><span data-stu-id="2509f-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>