---
title: Mitwirken von Beispielen an das Microsoft QDK
description: Erfahren Sie, wie Sie Beispielcode zum Microsoft Quantum Development Kit (QDK) beitragen.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024150"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a>Mitwirken von Beispielen für das Quantum Development Kit

Wenn Sie an dem [beispielrepository](https://github.com/Microsoft/Quantum)Code mitwirken möchten, vielen Dank, dass Sie die Quantum Development Community besser platzieren!

## <a name="the-quantum-development-kit-samples-repository"></a>Das Quantum Development Kit-beispielrepository

Um Ihnen bei der Vorbereitung Ihres Beitrags zu helfen, so weit wie möglich zu helfen, ist es hilfreich, sich einen kurzen Blick darauf zu verschaffen, wie das beispielrepository angelegt wird:

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

Das heißt, die Beispiele im [Microsoft/quantum-Repository](https://github.com/microsoft/Quantum) werden nach Themenbereich in verschiedene Ordner aufgeteilt, wie z. b. `algorithms/`, `arithmetic/`oder `characterization/`.
Innerhalb des Ordners für jeden Themenbereich besteht jedes Beispiel aus einem einzelnen Ordner, der alle Elemente sammelt, die ein Benutzer zum Durchsuchen und verwenden dieses Beispiels benötigt.

## <a name="how-samples-are-structured"></a>Strukturieren von Beispielen

Sehen wir uns die Dateien an, aus denen sich die einzelnen Ordner bilden, betrachten wir das [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) Beispiel.

| Datei              | BESCHREIBUNG                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | Q#-Projekt, das zum Erstellen des Beispiels mit dem .net Core SDK verwendet wird |
| `Game.qs`         | Q#-Vorgänge und-Funktionen für das Beispiel                 |
| `Host.cs`         | C#zum Ausführen des Beispiels verwendetes Host Programm                     |
| `host.py`         | Zum Ausführen des Beispiels verwendetes python-Host Programm                 |
| `README.md`       | Dokumentation zur Funktionsweise des Beispiels und zur Verwendung    |

Nicht alle Samples haben genau denselben Satz von Dateien (z. b. können einige Beispiele vorhanden sein C#, andere verfügen möglicherweise nicht über einen python-Host, oder einige Beispiele erfordern möglicherweise, dass die Datendateien für die Daten ordnungsgemäß funktionieren).

## <a name="anatomy-of-a-helpful-readme-file"></a>Anatomie einer hilfreichen Infodatei

Eine besonders wichtige Datei ist jedoch die `README.md`-Datei, da die Benutzer für den Einstieg in Ihr Beispiel benötigen.

Jede `README.md` sollte mit einigen Metadaten beginnen, mit deren Hilfe docs.Microsoft.com/Samples ihren Beitrag finden kann.

> [!div class="nextstepaction"]
> [Sehen Sie sich an, wie das Beispiel für das CHSH-Spiel](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

Diese Metadaten werden als [YAML-Header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) bereitgestellt, der angibt, welche Sprachen Ihr Beispiel abdeckt (in der Regel `qsharp`, `csharp`und `python`) und welche Produkte in Ihrem Beispiel behandelt werden (in der Regel nur `qdk`).

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> Der `page_type: sample`-Schlüssel im-Header ist erforderlich, damit das Beispiel unter docs.Microsoft.com/Samples angezeigt wird.
> Ebenso sind die `product`-und `language` Schlüssel wichtig, um Benutzern zu helfen, das Beispiel zu finden und auszuführen.

Danach ist es hilfreich, eine kurze Einführung zu erhalten, in der das neue Beispiel angezeigt wird:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

Benutzer Ihres Beispiels können auch wissen, was Sie benötigen, um es auszuführen (z. b. benötigen Benutzer nur das Quantum Development Kit selbst oder benötigen zusätzliche Software, wie z. b. Node. js?):

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

Damit können Sie die Benutzer darüber informieren, wie das Beispiel ausgeführt werden soll:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

Schließlich ist es hilfreich, Benutzern mitzuteilen, was jede Datei in Ihrem Beispiel tut und wo Sie weitere Informationen erhalten können:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> Stellen Sie sicher, dass Sie hier absolute URLs verwenden, da das Beispiel unter einer anderen URL angezeigt wird, wenn es unter docs.Microsoft.com/Samples gerendert wird.
