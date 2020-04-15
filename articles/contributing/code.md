---
title: Beitragen von Code an das Microsoft QDK
description: Erfahren Sie, wie Sie Beispiel-und Bibliotheks Code zum Microsoft Quantum Development Kit (QDK) beitragen.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.code
ms.openlocfilehash: edc52dc4434e91258bece28812fd76b66329c6f9
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022468"
---
# <a name="contributing-code"></a>Mitwirken am Code

Zusätzlich zum Melden von Problemen und zum Verbessern der Dokumentation kann das Hinzufügen von Code zum Quantum Development Kit ein sehr direkter Weg sein, um Ihre Peers in der Quantum-Programmier Community zu unterstützen.
Durch die Bereitstellung von Code können Sie Probleme beheben, neue Beispiele bereitstellen, die Verwendung vorhandener Bibliotheken vereinfachen oder sogar völlig neue Funktionen hinzufügen.

In diesem Leitfaden wird ausführlich erläutert, was wir sehen, wenn wir Pull Requests überprüfen, um Ihnen bei der optimalen Durchführung ihres Beitrags zu helfen.

## <a name="what-we-look-for"></a>Was wir suchen

Ein idealer Code Beitrag baut auf der vorhandenen Arbeit in einem Quantum Development Kit-Repository auf, um Probleme zu beheben, vorhandene Funktionen zu erweitern oder neue Funktionen hinzuzufügen, die sich innerhalb des Bereichs eines Repository befinden.
Wenn wir einen Code Beitrag akzeptieren, wird er Teil des Quantum Development Kit, sodass neue Features auf die gleiche Weise wie der Rest des Quantums Development Kit veröffentlicht, gewartet und entwickelt werden.
Daher ist es hilfreich, wenn die durch einen Beitrag hinzugefügten Funktionen gut getestet und dokumentiert werden.

### <a name="unit-tests"></a>Komponententests

Die Q#-Funktionen,-Vorgänge und benutzerdefinierten Typen, die Bibliotheken wie den-Kanon bilden, werden automatisch als Teil der Entwicklung im [**Microsoft/quantrelibraries-** ](https://github.com/Microsoft/QuantumLibraries/) Repository getestet.
Wenn eine neue Pull Request beispielsweise geöffnet wird, prüft unsere [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) Konfiguration, ob die Änderungen im Pull Request vorhandene Funktionen, von denen die Quantum-Programmier Community abhängt, nicht unterbrechen.

Mit der neuesten Q#-Version werden Komponententests mithilfe des `@Test("QuantumSimulator")`-Attributs definiert. Das Argument kann entweder "Quantensimulator", "-ffolisimulator", "tracesimulator" oder ein beliebiger voll qualifizierter Name sein, der das Ausführungs Ziel angibt. Mehrere Attribute, die verschiedene Ausführungs Ziele definieren, können an dieselbe Aufruf Bare angefügt werden. Bei einigen unserer Tests wird weiterhin das veraltete [Microsoft. Quantum. xUnit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) -Paket verwendet, das alle Q#-Funktionen und-Vorgänge verfügbar macht, die `Test` mit dem [xUnit](https://xunit.github.io/) -Framework enden. Dieses Paket wird nicht mehr zum Definieren von Komponententests benötigt. 

Die folgende Funktion wird verwendet, um sicherzustellen, dass die Funktionen <xref:microsoft.quantum.canon.fst> und <xref:microsoft.quantum.canon.snd> beide die richtigen Ausgaben in einem repräsentativen Beispiel zurückgeben.
Wenn die Ausgabe von `Fst` oder `Snd` nicht korrekt ist, wird die `fail`-Anweisung verwendet, um den Test zu einem Fehler zu führen.

```qsharp
@Test("QuantumSimulator")
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

```Q#
@Test("QuantumSimulator")
operation TestApplyWith() : Unit {
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


## <a name="when-well-reject-a-pull-request"></a>Wenn wir einen Pull Request ablehnen

Manchmal lehnen wir die Pull Request für einen Beitrag ab.
Wenn dies der Fall ist, bedeutet das nicht, dass es schlecht ist, da es eine Reihe von Gründen gibt, warum wir möglicherweise nicht in der Lage sind, einen bestimmten Beitrag zu akzeptieren.
In den meisten Fällen ist ein Beitrag zur Quantum-Programmier Community eine wirklich gute, aber die Quantum Development Kit-Depots sind nicht der richtige Ort, um Sie zu entwickeln.
In solchen Fällen empfehlen wir dringend, Ihr eigenes Repository zu erstellen,---Bestandteil der Stärke des Quantum Development Kit ist, dass es einfach ist, eigene Bibliotheken mithilfe von GitHub und NuGet.org zu verteilen und auf die gleiche Weise zu verteilen, wie wir den Kanon und die Chemie verteilen. Bibliotheken heute.

Zu einem anderen Zeitpunkt können wir einen guten Beitrag ablehnen, einfach weil wir noch nicht bereit sind, ihn zu verwalten und zu entwickeln.
Es kann schwierig sein, alles zu erledigen. Daher planen wir, welche Features wir am besten als Roadmap bearbeiten können.
Dies kann ein weiterer Fall sein, wenn das Freigeben eines Features als Bibliothek eines Drittanbieters sehr sinnvoll ist.
Alternativ können wir Ihnen helfen, Ihre Hilfe beim Ändern eines Features zu ändern, um eine bessere Anpassung in unsere Roadmap zu erreichen, damit wir die bestmögliche Arbeit erreichen können.

Außerdem werden Sie aufgefordert, Änderungen an einer Pull Request vorzunehmen, wenn Sie weitere Dokumentationen oder Komponententests erfordert, damit wir Sie nutzen können, oder wenn Sie sich im Stil von den restlichen Q#-Bibliotheken unterscheiden, sodass Sie den Benutzern das Auffinden Ihrer Funktion erschweren.
In diesen Fällen versuchen wir, einige Ratschläge in Bezug auf Code Überprüfungen zu bieten, die hinzugefügt oder geändert werden können, um das einbeziehen Ihres Beitrags zu vereinfachen.

Schließlich können wir keine Beiträge akzeptieren, die zu Schäden der Quantum Computing-Community führen, wie im [Microsoft Open Source-Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/)erläutert.
Wir möchten sicherstellen, dass Beiträge der gesamten Quantum Computing-Community unterliegen, und zwar sowohl in der aktuellen als auch in der Zukunft.
Wir freuen uns auf Ihre Hilfe bei der Umsetzung dieses Ziels.

## <a name="next-steps"></a>Nächste Schritte

Vielen Dank, dass Sie das Quantum Development Kit zu einer großartigen Ressource für die gesamte Quantum-Programmier Community machen!
Weitere Informationen finden Sie im folgenden Leitfaden für Q# Style.

> [!div class="nextstepaction"]
> [Informationen zu Q#-Stilrichtlinien](xref:microsoft.quantum.contributing.style)

Abhängig von der Art des Codes, den Sie mitwirken, sind möglicherweise weitere Aspekte zu beachten, die Ihnen dabei helfen können, ihren Beitrag für die Community so gut wie möglich zu gestalten.

> [!div class="nextstepaction"]
> [Weitere Informationen zu Beitragenden Beispielen](xref:microsoft.quantum.contributing.samples)
