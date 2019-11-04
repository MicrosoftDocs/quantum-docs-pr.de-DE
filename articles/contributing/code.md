---
title: Beitragen von Code | Microsoft-Dokumentation
description: Beitragen von Code
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.code
ms.openlocfilehash: cca50e6c63d4bb982aa5f0a59fc19d08ecbec508
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185901"
---
# <a name="contributing-code"></a><span data-ttu-id="9ccfd-103">Beitragen von Code</span><span class="sxs-lookup"><span data-stu-id="9ccfd-103">Contributing Code</span></span> #

<span data-ttu-id="9ccfd-104">Zusätzlich zum Melden von Problemen und zum Verbessern der Dokumentation kann das Hinzufügen von Code zum Quantum Development Kit ein sehr direkter Weg sein, um Ihre Peers in der Quantum-Programmier Community zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-104">In addition to reporting issues and improving documentation, contributing code to the Quantum Development Kit can be a very direct way to help your peers in the quantum programming community.</span></span>
<span data-ttu-id="9ccfd-105">Durch die Bereitstellung von Code können Sie Probleme beheben, neue Beispiele bereitstellen, die Verwendung vorhandener Bibliotheken vereinfachen oder sogar völlig neue Funktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-105">By contributing code, you can help to fix issues, provide new examples, make existing libraries easier to use, or even add entirely new features.</span></span>

<span data-ttu-id="9ccfd-106">In diesem Leitfaden wird ausführlich erläutert, was wir sehen, wenn wir Pull Requests überprüfen, um Ihnen bei der optimalen Durchführung ihres Beitrags zu helfen.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-106">In this guide, we'll detail a bit of what we look for when we review pull requests to help your contribution do the most good.</span></span>

## <a name="what-we-look-for"></a><span data-ttu-id="9ccfd-107">Was wir suchen</span><span class="sxs-lookup"><span data-stu-id="9ccfd-107">What We Look For</span></span> ##

<span data-ttu-id="9ccfd-108">Ein idealer Code Beitrag baut auf der vorhandenen Arbeit in einem Quantum Development Kit-Repository auf, um Probleme zu beheben, vorhandene Funktionen zu erweitern oder neue Funktionen hinzuzufügen, die sich innerhalb des Bereichs eines Repository befinden.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-108">An ideal code contribution builds on the existing work in a Quantum Development Kit repository to fix issues, expand existing features, or to add new features that are within the scope of a repository.</span></span>
<span data-ttu-id="9ccfd-109">Wenn wir einen Code Beitrag akzeptieren, wird er Teil des Quantum Development Kit, sodass neue Features auf die gleiche Weise wie der Rest des Quantums Development Kit veröffentlicht, gewartet und entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-109">When we accept a code contribution, it becomes a part of the Quantum Development Kit itself, such that new features will be released, maintained, and developed in the same way as the rest of the Quantum Development Kit.</span></span>
<span data-ttu-id="9ccfd-110">Daher ist es hilfreich, wenn die durch einen Beitrag hinzugefügten Funktionen gut getestet und dokumentiert werden.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-110">Thus, it is helpful when functionality added by a contribution is well-tested and is documented.</span></span>

### <a name="unit-tests"></a><span data-ttu-id="9ccfd-111">Komponenten Tests</span><span class="sxs-lookup"><span data-stu-id="9ccfd-111">Unit Tests</span></span> ###

<span data-ttu-id="9ccfd-112">Die Q #-Funktionen,-Vorgänge und benutzerdefinierten Typen, die Bibliotheken wie den-Kanon bilden, werden automatisch als Teil der Entwicklung im [**Microsoft/quantrelibraries-** ](https://github.com/Microsoft/QuantumLibraries/) Repository getestet.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-112">The Q# functions, operations, and user-defined types that make up libraries such as the canon are automatically tested as a part of development on the [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) repository.</span></span>
<span data-ttu-id="9ccfd-113">Wenn eine neue Pull Request beispielsweise geöffnet wird, prüft unsere [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) Konfiguration, ob die Änderungen im Pull Request vorhandene Funktionen, von denen die Quantum-Programmier Community abhängt, nicht unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-113">When a new pull request is opened, for instance, our [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) configuration will check that the changes in the pull request do not break any existing functionality that the quantum programming community depends on.</span></span>
<span data-ttu-id="9ccfd-114">Diese Tests werden mithilfe des [Microsoft. Quantum. xUnit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) -Pakets geschrieben, das Q #-Funktionen und-Vorgänge als Tests für das [xUnit](https://xunit.github.io/) -Framework verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-114">These tests are written using the [Microsoft.Quantum.Xunit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) package, which exposes Q# functions and operations as tests for the [xUnit](https://xunit.github.io/) framework.</span></span>

<span data-ttu-id="9ccfd-115">Der [`Standard/tests/Standard.Tests.csproj`](https://github.com/microsoft/QuantumLibraries/blob/master/Standard/tests/Standard.Tests.csproj) verwendet diese xUnit-Integration, um alle Funktionen oder Vorgänge auszuführen, die auf `Test`enden.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-115">The [`Standard/tests/Standard.Tests.csproj`](https://github.com/microsoft/QuantumLibraries/blob/master/Standard/tests/Standard.Tests.csproj) uses this xUnit integration to run any functions or operations ending in `Test`.</span></span>
<span data-ttu-id="9ccfd-116">Beispielsweise wird die folgende Funktion verwendet, um sicherzustellen, dass die Funktionen <xref:microsoft.quantum.canon.fst> und <xref:microsoft.quantum.canon.snd> beide die richtigen Ausgaben in einem repräsentativen Beispiel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-116">For instance, the following function is used to ensure that the <xref:microsoft.quantum.canon.fst> and <xref:microsoft.quantum.canon.snd> functions both return the right outputs in a representative example.</span></span>
<span data-ttu-id="9ccfd-117">Wenn die Ausgabe von `Fst` oder `Snd` nicht korrekt ist, wird die `fail`-Anweisung verwendet, um den Test zu einem Fehler zu führen.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-117">If the output of `Fst` or `Snd` is incorrect, the `fail` statement is used to cause the test to fail.</span></span>

```qsharp
function PairTest () : Unit {
    let pair = (12, PauliZ);

    if (Fst(pair) != 12) {
        let actual = Fst(pair);
        fail $"Expected 12, actual {actual}.";
    }

    if (Snd(pair) != PauliZ) {
        let actual = Snd(pair);
        fail $"Expected PauliZ, actual {actual}.";
    }
}
```

<span data-ttu-id="9ccfd-118">Kompliziertere Bedingungen können mithilfe der Techniken im [Abschnitt "Tests](xref:microsoft.quantum.libraries.diagnostics) " des Handbuchs "Standardbibliotheken" überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-118">More complicated conditions can be checked using the techniques in the [testing section](xref:microsoft.quantum.libraries.diagnostics) of the standard libraries guide.</span></span>
<span data-ttu-id="9ccfd-119">Der folgende Test prüft z. b., ob `H(q); X(q); H(q);`, wie von <xref:microsoft.quantum.canon.applywith> aufgerufen, dasselbe Ergebnis wie `Z(q)`.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-119">For instance, the following test checks that `H(q); X(q); H(q);` as called by <xref:microsoft.quantum.canon.applywith> does the same thing as `Z(q)`.</span></span>

```qsharp
operation WithTest () : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

<span data-ttu-id="9ccfd-120">Wenn Sie neue Features hinzufügen, empfiehlt es sich, auch neue Tests hinzuzufügen, um sicherzustellen, dass Ihr Beitrag die Voraussetzungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-120">When adding new features, it's a good idea to also add new tests to make sure that your contribution does what it's supposed to.</span></span>
<span data-ttu-id="9ccfd-121">Dies unterstützt den Rest der Community bei der Verwaltung und Entwicklung Ihres Features. insbesondere können andere Entwickler wissen, dass Sie sich auf ihre Funktion verlassen können.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-121">This helps the rest of the community to maintain and develop your feature, and in particular helps other developers know that they can rely on your feature.</span></span>

> [!NOTE]
> <span data-ttu-id="9ccfd-122">Dies funktioniert auch auf andere Weise.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-122">This works the other way around, too!</span></span>
> <span data-ttu-id="9ccfd-123">Wenn es ein vorhandenes Feature gibt, das einige Tests fehlt, würde das Hinzufügen von Test Coverage zu einem großen Beitrag für die Community führen.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-123">If there's an existing feature that's missing some tests, helping us add test coverage would make a great contribution to the community.</span></span>

<span data-ttu-id="9ccfd-124">Lokal können Komponententests mit dem Test-Explorer von Visual Studio oder mit dem Befehl `dotnet test` ausgeführt werden, damit Sie Ihren Beitrag vor dem Öffnen einer Pull Request überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-124">Locally, unit tests can be run using the Visual Studio Test Explorer or the `dotnet test` command, so that you can check your contribution before opening up a pull request.</span></span>

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->

## <a name="when-well-reject-a-pull-request"></a><span data-ttu-id="9ccfd-125">Wenn wir einen Pull Request ablehnen</span><span class="sxs-lookup"><span data-stu-id="9ccfd-125">When We'll Reject a Pull Request</span></span> ##

<span data-ttu-id="9ccfd-126">Manchmal lehnen wir die Pull Request für einen Beitrag ab.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-126">Sometimes, we'll reject the pull request for a contribution.</span></span>
<span data-ttu-id="9ccfd-127">Wenn dies der Fall ist, bedeutet das nicht, dass es schlecht ist, da es eine Reihe von Gründen gibt, warum wir möglicherweise nicht in der Lage sind, einen bestimmten Beitrag zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-127">If this happens to you, it doesn't mean that it's bad, as there's a number of reasons why we might not be able to accept a particular contribution.</span></span>
<span data-ttu-id="9ccfd-128">In den meisten Fällen ist ein Beitrag zur Quantum-Programmier Community eine wirklich gute, aber die Quantum Development Kit-Depots sind nicht der richtige Ort, um Sie zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-128">Perhaps most commonly, a contribution to the quantum programming community is a really good one, but the Quantum Development Kit repositories aren't the right place to develop it.</span></span>
<span data-ttu-id="9ccfd-129">In solchen Fällen empfehlen wir dringend, Ihr eigenes Repository zu erstellen,---Bestandteil der Stärke des Quantum Development Kit ist, dass es einfach ist, eigene Bibliotheken mithilfe von GitHub und NuGet.org zu verteilen und auf die gleiche Weise zu verteilen, wie wir den Kanon und die Chemie verteilen. Bibliotheken heute.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-129">In such cases, we strongly encourage you to make your own repository --- part of the strength of the Quantum Development Kit is that it's easy to make and distribute your own libraries using GitHub and NuGet.org, the same way that we distribute the canon and chemistry libraries today.</span></span>

<span data-ttu-id="9ccfd-130">Zu einem anderen Zeitpunkt können wir einen guten Beitrag ablehnen, einfach weil wir noch nicht bereit sind, ihn zu verwalten und zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-130">At other times, we may reject a good contribution simply because we aren't yet ready to maintain and develop it.</span></span>
<span data-ttu-id="9ccfd-131">Es kann schwierig sein, alles zu erledigen. Daher planen wir, welche Features wir am besten als Roadmap bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-131">It can be difficult to do everything, so we plan out what features we're best able to work on as a roadmap.</span></span>
<span data-ttu-id="9ccfd-132">Dies kann ein weiterer Fall sein, wenn das Freigeben eines Features als Bibliothek eines Drittanbieters sehr sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-132">This can be another case where releasing a feature as a third-party library can make a lot of sense.</span></span>
<span data-ttu-id="9ccfd-133">Alternativ können wir Ihnen helfen, Ihre Hilfe beim Ändern eines Features zu ändern, um eine bessere Anpassung in unsere Roadmap zu erreichen, damit wir die bestmögliche Arbeit erreichen können.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-133">Alternatively, we may ask for your help in modifying a feature to better fit into our roadmap so that we can do the best work we can with it.</span></span>

<span data-ttu-id="9ccfd-134">Außerdem werden Sie aufgefordert, Änderungen an einer Pull Request vorzunehmen, wenn Sie weitere Dokumentationen oder Komponententests erfordert, damit wir Sie nutzen können, oder wenn Sie sich im Stil von den restlichen Q #-Bibliotheken unterscheiden, sodass Sie den Benutzern das Auffinden Ihrer Funktion erschweren.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-134">We'll also ask for changes to a pull request if it requires more documentation or unit tests to help us make use of it, or if it differs enough in style from the rest of the Q# libraries that it will make it harder for users to find your feature.</span></span>
<span data-ttu-id="9ccfd-135">In diesen Fällen versuchen wir, einige Ratschläge in Bezug auf Code Überprüfungen zu bieten, die hinzugefügt oder geändert werden können, um das einbeziehen Ihres Beitrags zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-135">In these cases, we'll try to offer some advice in code reviews about what can be added or changed to make your contribution easier for us to include.</span></span>

<span data-ttu-id="9ccfd-136">Schließlich können wir keine Beiträge akzeptieren, die zu Schäden der Quantum Computing-Community führen, wie im [Microsoft Open Source-Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/)erläutert.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-136">Finally, we cannot accept contributions that cause harm the quantum computing community, as outlined in the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).</span></span>
<span data-ttu-id="9ccfd-137">Wir möchten sicherstellen, dass Beiträge der gesamten Quantum Computing-Community unterliegen, und zwar sowohl in der aktuellen als auch in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-137">We want to ensure that contributions serve the entire quantum computing community, both in its current wonderful diversity, and in the future as it grows to become still more inclusive.</span></span>
<span data-ttu-id="9ccfd-138">Wir freuen uns auf Ihre Hilfe bei der Umsetzung dieses Ziels.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-138">We appreciate your help in realizing this goal.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9ccfd-139">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9ccfd-139">Next steps</span></span> ##

<span data-ttu-id="9ccfd-140">Vielen Dank, dass Sie das Quantum Development Kit zu einer großartigen Ressource für die gesamte Quantum-Programmier Community machen!</span><span class="sxs-lookup"><span data-stu-id="9ccfd-140">Thanks for helping to make the Quantum Development Kit a great resource for the entire quantum programming community!</span></span>
<span data-ttu-id="9ccfd-141">Weitere Informationen finden Sie im folgenden Leitfaden für Q # Style.</span><span class="sxs-lookup"><span data-stu-id="9ccfd-141">To learn more, please continue with the following guide on Q# style.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="9ccfd-142">Informationen zu f #-Stilrichtlinien</span><span class="sxs-lookup"><span data-stu-id="9ccfd-142">Learn about Q# style guidelines</span></span>](xref:microsoft.quantum.contributing.style)
