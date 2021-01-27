---
uid: Microsoft.Quantum.AmplitudeAmplification
title: Microsoft. Quantum. amplitudebug-Namespace
ms.date: 1/23/2021 12:00:00 AM
ms.topic: managed-reference
qsharp.kind: namespace
qsharp.name: Microsoft.Quantum.AmplitudeAmplification
qsharp.summary: This namespace contains functions and operations for performing amplitude amplification.
ms.openlocfilehash: a014f923de62c5e660c1c0fc839fbe60e80f8ba9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845826"
---
# <a name="microsoftquantumamplitudeamplification-namespace"></a><span data-ttu-id="814d6-102">Microsoft. Quantum. amplitudebug-Namespace</span><span class="sxs-lookup"><span data-stu-id="814d6-102">Microsoft.Quantum.AmplitudeAmplification namespace</span></span>

<span data-ttu-id="814d6-103">Dieser Namespace enthält Funktionen und Vorgänge zum Durchführen der Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="814d6-103">This namespace contains functions and operations for performing amplitude amplification.</span></span>



## <a name="description"></a><span data-ttu-id="814d6-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="814d6-104">Description</span></span>

<span data-ttu-id="814d6-105">Eine schrägende Amplitude-Verstärkung mit partiellen Reflektionen ist die allgemeinste Form der hier implementierten Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="814d6-105">Oblivious amplitude amplification with partial reflections is the most general form of amplitude amplification implemented here.</span></span>

<span data-ttu-id="814d6-106">Dies wird durch den Vorgang ampampobliviousbyreflectionphasen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="814d6-106">This is called through the operation AmpAmpObliviousByReflectionPhases.</span></span>

<span data-ttu-id="814d6-107">Dies hat zwei Register: `ancillaRegister` und `systemRegister` .</span><span class="sxs-lookup"><span data-stu-id="814d6-107">This has two registers: `ancillaRegister` and `systemRegister`.</span></span>

<span data-ttu-id="814d6-108">Dies akzeptiert zwei Oracles für diese Reflektionen des Typs `ReflectionOracle` , die nur für das `ancillaRegister` Register fungieren.</span><span class="sxs-lookup"><span data-stu-id="814d6-108">This accepts two oracles for these reflections of type `ReflectionOracle` which act only on the `ancillaRegister` register.</span></span>

<span data-ttu-id="814d6-109">Dies akzeptiert eine Oracle-spezielle Verstärkung der Amplitude-Verstärkung des Typs `ObliviousOracle` , die zusammen für beide Register fungiert.</span><span class="sxs-lookup"><span data-stu-id="814d6-109">This accepts an oracle special to oblivious amplitude amplification of type `ObliviousOracle` which acts jointly on both register.</span></span>

<span data-ttu-id="814d6-110">`ancillaRegister`Es wird davon ausgegangen, dass es sich bei dem Eingabe Status von um den eindeutigen $-$1-eigen Status des ersten reflektionsoperators handelt $I-2 \ Ket {s} \ Bra {s} $.</span><span class="sxs-lookup"><span data-stu-id="814d6-110">The input state to `ancillaRegister` is assumed to be the unique $-1$ eigenstate of the first reflection operator $I - 2\ket{s}\bra{s}$.</span></span>

<span data-ttu-id="814d6-111">Reflektionen zu einem Ziel-Quantenzustand werden häufig implementiert, indem der Zugriff auf ein Oracle angenommen wird, das diesen Zustand von der Berechnungsbasis auf "$ \ket{0\cdots 0} $" vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="814d6-111">Reflections about a target quantum state are often implemented by assuming access to an oracle that prepare that state from the computational basis $\ket{0\cdots 0}$.</span></span>

<span data-ttu-id="814d6-112">Unsere Konvention für diese Oracles erfordert zwei Register: ein Single-Qubit- `flagQubit` Register und ein Register für alles andere auf dem Register "ancillaregister".</span><span class="sxs-lookup"><span data-stu-id="814d6-112">Our convention for these oracles requires two registers: a single-qubit `flagQubit` register, and a register for everything else on the ancillaRegister register.</span></span>

<span data-ttu-id="814d6-113">Das Oracle vom Typ `StateOracle` agiert gemeinsam in beiden Registern, um den Ziel Status zu erstellen, der durch $ \ket {1} $ im `flagQubit` Register mit einer echten Amplitude gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="814d6-113">The oracle of type `StateOracle` acts jointly on both registers to create the target state flagged by $\ket{1}$ in the `flagQubit` register with some real amplitude.</span></span>

<span data-ttu-id="814d6-114">Die Reflektion `ReflectionOracle` über den Status dieses Flags wird durch den-Vorgang generiert `TargetStateReflectionOracle` .</span><span class="sxs-lookup"><span data-stu-id="814d6-114">The reflection `ReflectionOracle` about the this flag state is generated by the operation `TargetStateReflectionOracle`.</span></span>

<span data-ttu-id="814d6-115">Die Reflektion des `ReflectionOracle` Eingabe Zustands in `ancillaRegister` wird vom umgekehrten stateoracle generiert und dann über "$ \ket{0\cdots 0} $" mit reflectionstart () reflektiert.</span><span class="sxs-lookup"><span data-stu-id="814d6-115">The reflection `ReflectionOracle` about the input state to `ancillaRegister` is generated by the inverting StateOracle and then reflecting about $\ket{0\cdots 0}$ with ReflectionStart().</span></span>

<span data-ttu-id="814d6-116">Das Oracle vom Typ `DeterministicStateOracle` agiert in den `qubitState` Registern zum Erstellen des Ziel Zustands genau ohne Flag.</span><span class="sxs-lookup"><span data-stu-id="814d6-116">The oracle of type `DeterministicStateOracle` acts on the `qubitState` registers to create the target state exactly with no flag.</span></span>

<span data-ttu-id="814d6-117">`AmpAmpObliviousByOraclePhases` eine Version der schrägen Amplitude-Verstärkung, die Oracles `StateOracle` und `ObliviousOracle` anstelle von Reflektionen akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="814d6-117">`AmpAmpObliviousByOraclePhases` is a version of oblivious amplitude amplification that accepts oracles `StateOracle` and `ObliviousOracle` instead of reflections.</span></span>

<span data-ttu-id="814d6-118">Beachten Sie, dass die Amplitude-Verstärkung ein Sonderfall einer schrägen Amplitude-Verstärkung ist `ObliviousOracle` , wobei der Identitäts Operator ist und keine System-Qubits vorhanden sind, d.h., `systemRegister` ist leer.</span><span class="sxs-lookup"><span data-stu-id="814d6-118">Note that amplitude amplification is a special case of oblivious amplitude amplification where `ObliviousOracle` is the identity operator, and there are no system qubits i.e. `systemRegister` is empty.</span></span>

<span data-ttu-id="814d6-119">Dies wird durch den-Vorgang `AmpAmByReflectionPhases` und den aufgerufen `AmpAmpByOraclePhases` .</span><span class="sxs-lookup"><span data-stu-id="814d6-119">This is called through the operation `AmpAmByReflectionPhases` and `AmpAmpByOraclePhases`.</span></span>

<span data-ttu-id="814d6-120">Die Phasen für partielle Reflektionen im Standardfall der Grover-Suche werden von der Funktion ampampphasesstandard bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="814d6-120">The phases for partial reflections in the standard case of Grover search is provided by the function AmpAmpPhasesStandard.</span></span>

<span data-ttu-id="814d6-121">Beispielsweise haben wir die folgenden Abhängigkeiten: ampampbyoracle-> ampampbyoraclephasen-> ampampobliviousbyoraclephasen-> ampampobliviousbyreflectionphasen.</span><span class="sxs-lookup"><span data-stu-id="814d6-121">For instance, we have the following dependencies: AmpAmpByOracle -> AmpAmpByOraclePhases -> AmpAmpObliviousByOraclePhases -> AmpAmpObliviousByReflectionPhases.</span></span>