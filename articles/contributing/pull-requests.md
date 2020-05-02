---
title: Öffnen von Pull Requests
description: Erfahren Sie, wie Sie eine GitHub-Pull Request übermitteln, wenn Sie bereit sind, Code oder Dokumentation für die Microsoft Quantum Development Kit beizutragen.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.pulls
ms.openlocfilehash: 82af3b5123588cc06882f746ffcb0402ad3f0f2e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "82686852"
---
# <a name="opening-pull-requests"></a>Öffnen von Pull Requests #

Die gesamte Dokumentation für das Quantum Development Kit wird mithilfe des git-Versionskontrollsystems durch die Verwendung mehrerer in GitHub gehosteter Depots verwaltet.
Die gemeinsame Verwendung von git und GitHub erleichtert die Zusammenarbeit mit dem Quantum Development Kit.
Vor allem kann ein git-Repository geklont oder verzweigt werden, um eine vollständig unabhängige Kopie dieses Repository zu erstellen.
Auf diese Weise können Sie mit den Tools und in einem von Ihnen bevorzugten Tempo an Ihrem Beitrag arbeiten.

Wenn Sie bereit sind, können Sie uns eine Anforderung senden, ihren Beitrag in unsere Repos aufzunehmen, indem Sie die _Pull Request_ Funktionen von GitHub verwenden.
Die Seite für die einzelnen Pull Request enthält Details zu allen Änderungen, die ihren Beitrag vornehmen, eine Liste der Kommentare zu Ihrem Beitrag und eine Reihe von Überprüfungs Tools, mit denen andere Mitglieder der Community Feedback und Ratschläge bereitstellen können.

> [!NOTE]
> Während ein vollständiges Tutorial zu git über den Rahmen dieses Handbuchs hinausgeht, können wir die folgenden Links für weitere Ressourcen zum Erlernen von git vorschlagen:
>
> - [Erlernen von git](https://www.atlassian.com/git): eine Reihe von git-Tutorials von Atlassian.
> - [Versionskontrolle in Visual Studio Code](https://code.visualstudio.com/docs/editor/versioncontrol): eine Anleitung zur Verwendung Visual Studio Code als GUI für git.
> - [GitHub-Lernlabor](https://lab.github.com/): eine Reihe von Online Kursen zur Verwendung von git, GitHub und verwandten Technologien.
> - [Visualisieren von git](https://git-school.github.io/visualizing-git/): ein interaktives Tool zum Visualisieren der Änderung des Status eines Repository durch git-Befehle.
> - [Versionskontrolle mit git (epqis 2016)](https://nbviewer.jupyter.org/github/QuinnPhys/PythonWorkshop-science/blob/master/lecture-1-scicomp-tools-part1.ipynb#Version-Control-with-Git-(50-Minutes)): ein git-Tutorial, das auf wissenschaftliche Berechnungen ausgerichtet ist.
> - [Erlernen von git-Verzweigungen](https://learngitbranching.js.org/): ein interaktiver Satz von Verzweigungen und neustützten rätseln zum Erlernen neuer git-Features.

## <a name="what-is-a-pull-request"></a>Was ist ein Pull Request? ##

Wenn Sie die oben genannten Punkte erwähnt haben, ist es hilfreich, etwas zu sagen, was ein Pull Request **ist**.
Beim Arbeiten mit git werden alle Änderungen als _Commits_ dargestellt, die beschreiben, wie diese Änderungen mit dem Zustand des Repository in Beziehung stehen, bevor diese geändert werden.
Wir zeichnen häufig Diagramme, in denen Commits als Kreise mit Pfeilen aus vorherigen Commits gezeichnet werden.

Angenommen, Sie haben einen Beitrag in einer _Verzweigung_ mit dem Namen `feature`gestartet.
Ihre Verzweigung von **Microsoft/Quantum** könnte etwa wie folgt aussehen:

![Eine funktionierende Verzweigung in GitHub](~/media/git-workflow-step0.png)

Wenn Sie Ihre Änderungen in Ihrem lokalen Repository vornehmen, können Sie Änderungen aus einem anderen Repository per _Pull_ abrufen, um alle Änderungen zu erfassen, die mit upstreamvorgängen durchgeführt wurden.

![Pullen und Zusammenführen von Änderungen von einem upstreamrepository](~/media/git-workflow-step1.png)

Pull Requests funktionieren auf die gleiche Weise, aber in umgekehrter Reihenfolge: Wenn Sie einen Pull Request öffnen, bitten Sie das upstreamrepository, in den Beitrag zu ziehen.

![Anfordern von Pull der Änderungen zurück in das ursprüngliche Repository](~/media/git-workflow-step2.png)

Wenn Sie eine Pull Request in einem unserer Depots öffnen, bietet GitHub anderen Benutzern in der Community die Möglichkeit, eine Zusammenfassung Ihrer Änderungen anzuzeigen, Sie zu kommentieren und Vorschläge für einen noch besseren Beitrag zu geben.

![Screenshot einer Pull Request in GitHub](~/media/pull-request-header.png)

Mithilfe dieses Prozesses können wir die GitHub-Funktionalität nutzen, um Beiträge zu verbessern und ein qualitativ hochwertiges Produkt für die Quantum-Programmier Community zu erhalten.

## <a name="how-to-make-a-pull-request"></a>So erstellen Sie einen Pull Request ##

Es gibt zwei Hauptmethoden, um eine Pull Request zu erstellen.  
Bei kleinen Änderungen, die nur eine einzelne Datei betreffen, kann die GitHub-Webschnittstelle verwendet werden, um eine Pull Request vollständig online zu machen. Navigieren Sie einfach zu der Datei, die Sie bearbeiten möchten, und verwenden Sie das Bearbeitungs Symbol.  
Für kompliziertere Beiträge ist es am häufigsten einfacher, das Repository auf Ihren lokalen Computer zu klonen, um zuerst eine Pull Request vorzubereiten.

<!--
### Using the Web Interface ###

**TODO**

### Command-Line and GitHub Flow ###

Most of the time, it's easier to prepare a pull request on your own computer; that makes it easier to work incrementally, and to test your changes.
If you haven't already done so, the first step is to _fork_ the repository that you'd like to contribute to.
Forking makes a complete clone of the original repository, but under your GitHub account instead of under [Microsoft](http://github.com/Microsoft/) or [MicrosoftDocs](http://github.com/MicrosoftDocs/).
This way, you can edit your personal fork to your heart's content before making a pull request for your work.

**TODO: pick up here**

## Code Review and Etiquette ##

**TODO: PR ettiquette, reviews, etc.**

-->

## <a name="next-steps"></a>Nächste Schritte ##

Herzlichen Glückwunsch zur Verwendung von git, um die Quantum Development Kit-Community zu unterstützen!
Weitere Informationen zum mitwirken von Code finden Sie im folgenden Handbuch.

> [!div class="nextstepaction"]
> [Weitere Informationen zum mitwirken von Code](xref:microsoft.quantum.contributing.code)
