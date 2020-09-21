---
title: Mitwirken von Beispielen an das Microsoft QDK
description: Erfahren Sie, wie Sie Beispielcode zum Microsoft Quantum Development Kit (QDK) beitragen.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
no-loc:
- Q#
- $$v
ms.openlocfilehash: ae29614cc9c8bf965ea3cb373dc17470aec21252
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759185"
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

Das heißt, die Beispiele im [Microsoft/quantum-Repository](https://github.com/microsoft/Quantum) werden nach Themenbereich in verschiedene Ordner aufgeteilt `algorithms/` , z. b `arithmetic/` ., oder `characterization/` .
Innerhalb des Ordners für jeden Themenbereich besteht jedes Beispiel aus einem einzelnen Ordner, der alle Elemente sammelt, die ein Benutzer zum Durchsuchen und verwenden dieses Beispiels benötigt.

## <a name="how-samples-are-structured"></a>Strukturieren von Beispielen

Sehen wir uns die Dateien an, aus denen sich die einzelnen Ordner bilden, betrachten wir das [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/chsh-game) Beispiel.

| Datei              | BESCHREIBUNG                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | Q# Das Projekt, mit dem das Beispiel mit dem .net Core SDK erstellt wird. |
| `Game.qs`         | Q# Vorgänge und Funktionen für das Beispiel                 |
| `Host.cs`         | Zum Ausführen des Beispiels verwendetes c#-Host Programm                     |
| `host.py`         | Zum Ausführen des Beispiels verwendetes python-Host Programm                 |
| `README.md`       | Dokumentation zur Funktionsweise des Beispiels und zur Verwendung    |

Nicht alle Samples verfügen über genau denselben Satz von Dateien (z. b. können einige Beispiele nur c#-Code enthalten, andere verfügen möglicherweise nicht über einen python-Host, oder einige Beispiele erfordern möglicherweise, dass die Datendateien für die Daten ordnungsgemäß funktionieren).

## <a name="anatomy-of-a-helpful-readme-file"></a>Anatomie einer hilfreichen Infodatei

Eine besonders wichtige Datei ist allerdings die `README.md` Datei, die die Benutzer für den Einstieg in Ihr Beispiel benötigen.

Jede `README.md` sollte mit einigen Metadaten beginnen, die Ihnen helfen, ihren Beitrag zu docs.Microsoft.com/Samples finden.

> [!div class="nextstepaction"]
> [Sehen Sie sich an, wie das Beispiel für das CHSH-Spiel](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

Diese Metadaten werden als [YAML-Header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) bereitgestellt, der angibt, welche Sprachen Ihr Beispiel abdeckt (in der Regel, `qsharp` `csharp` und `python` ) und welche Produkte in Ihrem Beispiel behandelt werden (in der Regel nur `qdk` ).

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> Der `page_type: sample` Schlüssel im-Header ist erforderlich, damit das Beispiel unter docs.Microsoft.com/Samples angezeigt wird.
> Ebenso sind der `product` -Schlüssel und der- `language` Schlüssel wichtig, um Benutzern zu helfen, das Beispiel zu finden und auszuführen.

Danach ist es hilfreich, eine kurze Einführung zu erhalten, in der das neue Beispiel angezeigt wird:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

Benutzer Ihres Beispiels können auch wissen, was Sie benötigen, um es auszuführen (z. b. benötigen Benutzer nur das Quantum Development Kit selbst oder benötigen zusätzliche Software, wie z. b. node.js?):

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

Damit können Sie die Benutzer darüber informieren, wie das Beispiel ausgeführt werden soll:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

Schließlich ist es hilfreich, Benutzern mitzuteilen, was jede Datei in Ihrem Beispiel tut und wo Sie weitere Informationen erhalten können:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> Stellen Sie sicher, dass Sie hier absolute URLs verwenden, da das Beispiel unter einer anderen URL angezeigt wird, wenn es unter docs.Microsoft.com/Samples gerendert wird.
