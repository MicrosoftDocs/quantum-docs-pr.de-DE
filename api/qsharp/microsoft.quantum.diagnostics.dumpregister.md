---
uid: Microsoft.Quantum.Diagnostics.DumpRegister
title: Dumpregiester-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpRegister
qsharp.summary: Dumps the current target machine's status associated with the given qubits.
ms.openlocfilehash: 835c7a9edb22b4be630ebfc04587c12b3ff668b2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829231"
---
# <a name="dumpregister-function"></a><span data-ttu-id="f475a-102">Dumpregiester-Funktion</span><span class="sxs-lookup"><span data-stu-id="f475a-102">DumpRegister function</span></span>

<span data-ttu-id="f475a-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f475a-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f475a-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="f475a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="f475a-105">Sichert den aktuellen Status des Ziel Computers, der mit den angegebenen Qubits verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="f475a-105">Dumps the current target machine's status associated with the given qubits.</span></span>

```qsharp
function DumpRegister<'T> (location : 'T, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f475a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f475a-106">Input</span></span>

### <a name="location--t"></a><span data-ttu-id="f475a-107">Speicherort: 't</span><span class="sxs-lookup"><span data-stu-id="f475a-107">location : 'T</span></span>

<span data-ttu-id="f475a-108">Enthält Informationen dazu, wo der Zustands Speicher generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f475a-108">Provides information on where to generate the state's dump.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="f475a-109">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f475a-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f475a-110">Die Liste der zu berichtenden Qubits.</span><span class="sxs-lookup"><span data-stu-id="f475a-110">The list of qubits to report.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f475a-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f475a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="f475a-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="f475a-112">None.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f475a-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f475a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f475a-114">GIF</span><span class="sxs-lookup"><span data-stu-id="f475a-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="f475a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f475a-115">Remarks</span></span>

<span data-ttu-id="f475a-116">Mit dieser Methode können Sie die Informationen, die dem Zustand der angegebenen Qubits zugeordnet sind, in einer Datei oder an einem anderen Speicherort speichern.</span><span class="sxs-lookup"><span data-stu-id="f475a-116">This method allows you to dump the information associated with the state of the given qubits into a file or some other location.</span></span>
<span data-ttu-id="f475a-117">Die tatsächlich generierten Informationen und die Semantik von `location` sind für jeden Zielcomputer spezifisch.</span><span class="sxs-lookup"><span data-stu-id="f475a-117">The actual information generated and the semantics of `location` are specific to each target machine.</span></span> <span data-ttu-id="f475a-118">Wenn Sie jedoch ein leeres Tupel als Speicherort () bereitstellen, bedeutet dies in `()` der Regel, dass die Ausgabe in der Konsole generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f475a-118">However, providing an empty tuple as a location (`()`) typically means to generate the output to the console.</span></span>

<span data-ttu-id="f475a-119">Für den lokalen vollständigen Zustands Simulator, der als Teil des Quantum Development Kit verteilt ist, erwartet diese Methode eine Zeichenfolge mit dem Pfad zu einer Datei, in der der Zustand der angegebenen Qubits (d. h. die Wave-Funktion des entsprechenden Subsystems) als eindimensionales Array komplexer Zahlen geschrieben wird, wobei jedes Element die Verstärkung der Wahrscheinlichkeit darstellt, dass der entsprechende Zustand gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="f475a-119">For the local full state simulator distributed as part of the Quantum Development Kit, this method  expects a string with the path to a file in which it will write the state of the given qubits (i.e. the wave function of the corresponding  subsystem) as a one-dimensional array of complex numbers, in which each element represents the amplitudes of the probability of measuring the corresponding state.</span></span>
<span data-ttu-id="f475a-120">Wenn die angegebenen Qubits mit einem anderen Qubit entkoppelt werden und ihr Zustand nicht getrennt werden kann, meldet Sie lediglich, dass die Qubits entkoppelt sind.</span><span class="sxs-lookup"><span data-stu-id="f475a-120">If the given qubits are entangled with some other qubit and their state can't be separated, it just reports that the qubits are entangled.</span></span>