---
title: Mitwirken am Microsoft Quantum Development Kit
description: Es wird beschrieben, wie Sie zum Microsoft Quantum Development Kit und zur Quantum-Entwicklercommunity beitragen können.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing
ms.openlocfilehash: cf913a09395f0694a51645ec8f91171e5b1555c3
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022475"
---
# <a name="contributing-to-the-quantum-development-kit"></a>Mitwirken am Quantum Development Kit

Das Quantum Development Kit ist mehr als eine Sammlung von Tools zum Schreiben von Quantenprogrammen.
Es ist in eine große Community von Personen eingebettet, die das Quantencomputing entdecken möchten, Forschung zu Quantenalgorithmen betreiben, neue Anwendungen für Quantengeräte entwickeln und anderweitig aktiv sind, um die Quantenprogrammierung bestmöglich zu nutzen.
Mit dem Quantum Development Kit als Teil dieser Community sollen Quantenentwickler mit den unterschiedlichsten Hintergründen mit den benötigten Features versorgt werden.
Mit Ihren Beiträgen zum Quantum Development Kit unterstützen Sie die Erreichung dieses Ziels, indem Sie die von anderen Quantenentwicklern genutzten Tools und die zugehörige Dokumentation verbessern. Sie können sogar neue Features und Funktionen erstellen, um die gesamte Community für die Quantenprogrammierung zu einem Ort zu machen, an dem Entdeckungen und Erstellungen noch besser möglich sind.
Wir sind Ihnen für Ihre Beiträge sehr dankbar und freuen uns darüber, zusammen mit Ihnen für unsere Community das bestmögliche Ergebnis erzielen zu können.

Dieser Leitfaden enthält einige Hinweise dazu, wie Sie Ihre Beiträge für die gesamte Community zur Quantenprogrammierung möglichst wertvoll gestalten.

## <a name="building-community"></a>Schaffen einer echten Community

Bei Ihrer Mitwirkung sollten Sie vor allem immer zuerst an die Community denken, zu der Sie Ihren Beitrag leisten.
Indem Sie die Personen der Community für die Quantenprogrammierung und darüber hinaus stets respektvoll und professionell behandeln, können Sie sicherstellen, dass Sie mit Ihrer Arbeit zur Schaffung einer optimalen, einladenden Community beitragen.

Im Rahmen dieser Maßnahmen wurden für alle Quantum Development Kit-Projekte die [Microsoft Open-Source-Verhaltensregeln](https://opensource.microsoft.com/codeofconduct/) eingeführt.
Weitere Informationen finden Sie in den [häufig gestellten Fragen zum Verhaltenskodex](https://opensource.microsoft.com/codeofconduct/faq/). Sie können sich auch an [opencode@microsoft.com](mailto:opencode@microsoft.com) wenden, falls Sie weitere Fragen oder Anmerkungen haben.

## <a name="what-kinds-of-contributions-help-the-community"></a>Welche Arten von Beiträgen sind für die Community hilfreich?

Es gibt viele verschiedene Möglichkeiten, wie Sie die Community für die Quantenprogrammierung mit Beiträgen unterstützen können.
In diesem Leitfaden werden die drei Optionen beschrieben, die für das Quantum Development Kit am relevantesten sind.
All diese Optionen sind wichtig für die Schaffung einer Quantencommunity, die den Benutzern weiterhilft und ihnen viele Möglichkeiten eröffnet.
Die hier angegebene Liste deckt aber nicht alle Eventualitäten ab. Wir möchten Sie ermutigen, auch andere Möglichkeiten zu erkunden, wie Sie die Community in Bezug auf die Quantenprogrammierung voranbringen können!

- **Melden von Fehlern**: Der erste Schritt beim Beheben von Fehlern und anderen Arten von Problemen ist deren Identifizierung. Wenn Sie im Quantum Development Kit einen Fehler finden und uns darüber informieren, können wir ihn beheben und die Tools für die Community zur Quantenprogrammierung verbessern.
- **Verbessern der Dokumentation**: Jede Dokumentation kann verbessert, um neue Details erweitert und besser zugänglich gemacht werden.
- **Mitwirken am Code**: Einer der direktesten Wege zum Leisten eines Beitrags ist natürlich das Hinzufügen von neuem Code zum Quantum Development Kit.

Diese unterschiedlichen Arten von Beiträgen sind äußerst wertvoll und werden von uns sehr geschätzt.
Der restliche Teil des Leitfadens enthält Hinweise dazu, wie Sie beim Leisten von Beiträgen jeweils vorgehen.

## <a name="where-do-contributions-go"></a>Wohin fließen Beiträge?

Das Quantum Development Kit enthält eine Reihe unterschiedlicher Bestandteile, die miteinander verknüpft sind, um eine Plattform zum Schreiben von Quantenprogrammen zu erhalten.
Jeder dieser unterschiedlichen Bestandteile wird in einem eigenen Repository aufbewahrt, und einer der ersten Schritte besteht in der Ermittlung, wohin ein Beitrag gehört.

- [**microsoft/Quantum**](https://github.com/Microsoft/Quantum): Beispiele und Tools als Einstiegshilfe für das Quantum Development Kit.
- [**microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries): Standard- und domänenspezifische Bibliotheken für das Quantum Development Kit.
- [**microsoft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas): Programmierübungen für das eigenverantwortliche Selbststudium zum Erlernen des Quantencomputings und der Programmiersprache Q#.
- [**microsoft/qsharp-compiler**](https://github.com/microsoft/qsharp-compiler): Q#-Compiler, Visual Studio-Erweiterung und Visual Studio Code-Erweiterung.
- [**microsoft/qsharp-runtime**](https://github.com/microsoft/qsharp-runtime): Simulationsframework, Codegenerierung und Simulationszielcomputer für das Quantum Development Kit.
- [**microsoft/iqsharp**](https://github.com/microsoft/iqsharp): Jupyter-Kernel- und Python-Hostfunktionen für Q# sowie Docker-Images zur Verwendung von IQ# in Cloudumgebungen.
- [**MicrosoftDocs/quantum-docs-pr**](https://github.com/MicrosoftDocs/quantum-docs-pr): Quellcode für die unter https://docs.microsoft.com/quantum veröffentlichte Dokumentation.

> [!NOTE]
> Leider können wir derzeit keine Code- und Dokumentationsbeiträge im Repository [**microsoft/Quantum-NC**](https://github.com/microsoft/Quantum-NC) akzeptieren, aber wir sind Ihnen für das Melden von Fehlern trotzdem sehr dankbar.

Es sind auch einige spezielle Repositorys vorhanden, die für andere Ereignisse oder Hilfsfunktionen des Quantum Development Kit bestimmt sind.

- [**msr-quarc/qsharp.sty**](https://github.com/msr-quarc/qsharp.sty): Unterstützung der LaTeX-Formatierung für Q#-Syntax.
- [**msr-quarc/intern-workshop-2019**](https://github.com/msr-quarc/intern-workshop-2019): IQ#-Notebook für das Tutorial „Deutsch-Jozsa“ aus dem Intern Workshop 2019.

## <a name="next-steps"></a>Nächste Schritte

Vielen Dank, dass Sie sich an der Quantum Development Kit-Community beteiligen. Wir freuen uns auf Ihre Beiträge!
Falls Sie mehr über Möglichkeiten zur Mitwirkung erfahren möchten, helfen Ihnen die folgenden Leitfäden weiter.

> [!div class="nextstepaction"]
> [Erfahren Sie mehr zum Melden von Fehlern](xref:microsoft.quantum.contributing.reporting)

> [!div class="nextstepaction"]
> [Erfahren Sie mehr zu Beiträgen zur Dokumentation](xref:microsoft.quantum.contributing.docs)

> [!div class="nextstepaction"]
> [Erfahren Sie mehr zum Erstellen von Pull Requests](xref:microsoft.quantum.contributing.pulls)
