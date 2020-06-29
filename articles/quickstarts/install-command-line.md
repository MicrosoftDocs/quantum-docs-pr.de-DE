---
title: Entwickeln mit Q#-Befehlszeilenanwendungen
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274120"
---
# <a name="develop-with-q-command-line-applications"></a>Entwickeln mit Q#-Befehlszeilenanwendungen

Q#-Programme können allein ohne Treiber in einer Hostsprache wie C#, F# oder Python ausgeführt werden.

## <a name="prerequisites"></a>Voraussetzungen

- [.NET Core SDK 3.1 oder höher](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installation

Sie können Q#-Befehlszeilenanwendungen zwar in einer beliebigen IDE erstellen, aber wir empfehlen Ihnen, für Ihre Q#-Anwendungen Visual Studio Code (VS Code) oder Visual Studio als IDE zu nutzen. Bei der Entwicklung in diesen Tools haben Sie Zugriff auf einen großen Funktionsumfang.

Gehen Sie zum Konfigurieren von VS Code wie folgt vor:

1. Laden Sie [VS Code](https://code.visualstudio.com/download) herunter, und führen Sie die Installation durch (Windows, Linux und Mac).
2. Installieren Sie das [Microsoft QDK für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Gehen Sie zum Konfigurieren von Visual Studio wie folgt vor:

1. Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 oder höher herunter, und installieren Sie die Anwendung mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload.
2. Laden Sie das [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) herunter, und installieren Sie es.


## <a name="develop-with-q-using-vs-code"></a>Entwickeln mit Q# mithilfe von VS Code

Installieren Sie die Q#-Projektvorlagen:

1. Öffnen Sie Visual Studio Code.
2. Klicken Sie auf **Ansicht** -> **Befehlspalette**.
3. Wählen Sie **Q#: Projektvorlagen installieren** aus.

Wenn die Meldung mit dem Hinweis angezeigt wird, dass die **Installation der Projektvorlagen erfolgreich war**, ist das QDK für die Verwendung mit Ihren eigenen Anwendungen und Bibliotheken bereit.

Erstellen Sie wie folgt ein neues Projekt:

1. Klicken Sie auf **Ansicht** -> **Befehlspalette**, und wählen Sie **Q#: Neues Projekt erstellen** aus.
2. Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).
3. Navigieren Sie zum Speicherort für die Speicherung des Projekts, und klicken Sie auf **Projekt erstellen**.
4. Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).
        
Untersuchen Sie das Projekt. Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.

So führen Sie die Anwendung aus:
1. Klicken Sie auf **Terminal** -> **Neues Terminal**.
2. Geben Sie an der Eingabeaufforderung des Terminals `dotnet run` ein.
3. Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.


> [!NOTE]
> Arbeitsbereiche mit mehreren Stammordnern werden von der VS Code-Q#-Erweiterung derzeit nicht unterstützt. Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.

## <a name="develop-with-q-using-visual-studio"></a>Entwickeln mit Q# mithilfe von Visual Studio

Überprüfen Sie Ihre Visual Studio-Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.

Erstellen Sie wie folgt eine neue Q#-Anwendung:
1. Öffnen Sie Visual Studio, und klicken Sie auf **Datei** -> **Neu** -> **Projekt**.
2. Geben Sie im Suchfeld den Begriff `Q#` ein, wählen Sie **Q#-Anwendung** aus, und klicken Sie auf **Weiter**.
3. Geben Sie einen Namen und Speicherort für Ihre Anwendung ein, und klicken Sie auf **Erstellen**.


Untersuchen Sie das Projekt. Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.

So führen Sie die Anwendung aus:
1. Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.
2. Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.

> [!NOTE]
> Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe bzw. in einem der Unterordner befinden.  


## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.
