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
# <a name="contributing-code"></a>Beitragen von Code #

Zusätzlich zum Melden von Problemen und zum Verbessern der Dokumentation kann das Hinzufügen von Code zum Quantum Development Kit ein sehr direkter Weg sein, um Ihre Peers in der Quantum-Programmier Community zu unterstützen.
Durch die Bereitstellung von Code können Sie Probleme beheben, neue Beispiele bereitstellen, die Verwendung vorhandener Bibliotheken vereinfachen oder sogar völlig neue Funktionen hinzufügen.

In diesem Leitfaden wird ausführlich erläutert, was wir sehen, wenn wir Pull Requests überprüfen, um Ihnen bei der optimalen Durchführung ihres Beitrags zu helfen.

## <a name="what-we-look-for"></a>Was wir suchen ##

Ein idealer Code Beitrag baut auf der vorhandenen Arbeit in einem Quantum Development Kit-Repository auf, um Probleme zu beheben, vorhandene Funktionen zu erweitern oder neue Funktionen hinzuzufügen, die sich innerhalb des Bereichs eines Repository befinden.
Wenn wir einen Code Beitrag akzeptieren, wird er Teil des Quantum Development Kit, sodass neue Features auf die gleiche Weise wie der Rest des Quantums Development Kit veröffentlicht, gewartet und entwickelt werden.
Daher ist es hilfreich, wenn die durch einen Beitrag hinzugefügten Funktionen gut getestet und dokumentiert werden.

### <a name="unit-tests"></a>Komponenten Tests ###

Die Q #-Funktionen,-Vorgänge und benutzerdefinierten Typen, die Bibliotheken wie den-Kanon bilden, werden automatisch als Teil der Entwicklung im [**Microsoft/quantrelibraries-** ](https://github.com/Microsoft/QuantumLibraries/) Repository getestet.
Wenn eine neue Pull Request beispielsweise geöffnet wird, prüft unsere [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) Konfiguration, ob die Änderungen im Pull Request vorhandene Funktionen, von denen die Quantum-Programmier Community abhängt, nicht unterbrechen.
Diese Tests werden mithilfe des [Microsoft. Quantum. xUnit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) -Pakets geschrieben, das Q #-Funktionen und-Vorgänge als Tests für das [xUnit](https://xunit.github.io/) -Framework verfügbar macht.

Der [`Standard/tests/Standard.Tests.csproj`](https://github.com/microsoft/QuantumLibraries/blob/master/Standard/tests/Standard.Tests.csproj) verwendet diese xUnit-Integration, um alle Funktionen oder Vorgänge auszuführen, die auf `Test`enden.
Beispielsweise wird die folgende Funktion verwendet, um sicherzustellen, dass die Funktionen <xref:microsoft.quantum.canon.fst> und <xref:microsoft.quantum.canon.snd> beide die richtigen Ausgaben in einem repräsentativen Beispiel zurückgeben.
Wenn die Ausgabe von `Fst` oder `Snd` nicht korrekt ist, wird die `fail`-Anweisung verwendet, um den Test zu einem Fehler zu führen.

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

Kompliziertere Bedingungen können mithilfe der Techniken im [Abschnitt "Tests](xref:microsoft.quantum.libraries.diagnostics) " des Handbuchs "Standardbibliotheken" überprüft werden.
Der folgende Test prüft z. b., ob `H(q); X(q); H(q);`, wie von <xref:microsoft.quantum.canon.applywith> aufgerufen, dasselbe Ergebnis wie `Z(q)`.

```qsharp
operation WithTest () : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

Wenn Sie neue Features hinzufügen, empfiehlt es sich, auch neue Tests hinzuzufügen, um sicherzustellen, dass Ihr Beitrag die Voraussetzungen erfüllt.
Dies unterstützt den Rest der Community bei der Verwaltung und Entwicklung Ihres Features. insbesondere können andere Entwickler wissen, dass Sie sich auf ihre Funktion verlassen können.

> [!NOTE]
> Dies funktioniert auch auf andere Weise.
> Wenn es ein vorhandenes Feature gibt, das einige Tests fehlt, würde das Hinzufügen von Test Coverage zu einem großen Beitrag für die Community führen.

Lokal können Komponententests mit dem Test-Explorer von Visual Studio oder mit dem Befehl `dotnet test` ausgeführt werden, damit Sie Ihren Beitrag vor dem Öffnen einer Pull Request überprüfen können.

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->

## <a name="when-well-reject-a-pull-request"></a>Wenn wir einen Pull Request ablehnen ##

Manchmal lehnen wir die Pull Request für einen Beitrag ab.
Wenn dies der Fall ist, bedeutet das nicht, dass es schlecht ist, da es eine Reihe von Gründen gibt, warum wir möglicherweise nicht in der Lage sind, einen bestimmten Beitrag zu akzeptieren.
In den meisten Fällen ist ein Beitrag zur Quantum-Programmier Community eine wirklich gute, aber die Quantum Development Kit-Depots sind nicht der richtige Ort, um Sie zu entwickeln.
In solchen Fällen empfehlen wir dringend, Ihr eigenes Repository zu erstellen,---Bestandteil der Stärke des Quantum Development Kit ist, dass es einfach ist, eigene Bibliotheken mithilfe von GitHub und NuGet.org zu verteilen und auf die gleiche Weise zu verteilen, wie wir den Kanon und die Chemie verteilen. Bibliotheken heute.

Zu einem anderen Zeitpunkt können wir einen guten Beitrag ablehnen, einfach weil wir noch nicht bereit sind, ihn zu verwalten und zu entwickeln.
Es kann schwierig sein, alles zu erledigen. Daher planen wir, welche Features wir am besten als Roadmap bearbeiten können.
Dies kann ein weiterer Fall sein, wenn das Freigeben eines Features als Bibliothek eines Drittanbieters sehr sinnvoll ist.
Alternativ können wir Ihnen helfen, Ihre Hilfe beim Ändern eines Features zu ändern, um eine bessere Anpassung in unsere Roadmap zu erreichen, damit wir die bestmögliche Arbeit erreichen können.

Außerdem werden Sie aufgefordert, Änderungen an einer Pull Request vorzunehmen, wenn Sie weitere Dokumentationen oder Komponententests erfordert, damit wir Sie nutzen können, oder wenn Sie sich im Stil von den restlichen Q #-Bibliotheken unterscheiden, sodass Sie den Benutzern das Auffinden Ihrer Funktion erschweren.
In diesen Fällen versuchen wir, einige Ratschläge in Bezug auf Code Überprüfungen zu bieten, die hinzugefügt oder geändert werden können, um das einbeziehen Ihres Beitrags zu vereinfachen.

Schließlich können wir keine Beiträge akzeptieren, die zu Schäden der Quantum Computing-Community führen, wie im [Microsoft Open Source-Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/)erläutert.
Wir möchten sicherstellen, dass Beiträge der gesamten Quantum Computing-Community unterliegen, und zwar sowohl in der aktuellen als auch in der Zukunft.
Wir freuen uns auf Ihre Hilfe bei der Umsetzung dieses Ziels.

## <a name="next-steps"></a>Nächste Schritte ##

Vielen Dank, dass Sie das Quantum Development Kit zu einer großartigen Ressource für die gesamte Quantum-Programmier Community machen!
Weitere Informationen finden Sie im folgenden Leitfaden für Q # Style.

> [!div class="nextstepaction"]
> [Informationen zu f #-Stilrichtlinien](xref:microsoft.quantum.contributing.style)
