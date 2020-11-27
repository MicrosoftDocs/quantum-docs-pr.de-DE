---
title: Entwickeln mit Q#-Anwendungen in einer IDE
description: Hier erfahren Sie, wie Sie eine Anwendung vom Typ Q# erstellen, die über die Eingabeaufforderung ausgeführt wird.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: eeb567dedc1b8123b32faf7ed3a42bb51f16a7d2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228728"
---
# <a name="develop-with-no-locq-applications-in-an-ide"></a>Entwickeln mit Q#-Anwendungen in einer IDE

Q#-Programme können eigenständig ohne Treiber in einer Hostsprache wie C#, F# oder Python ausgeführt werden. Sie können Q#-Anwendungen in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces oder mit einem beliebigen Editor bzw. einer beliebigen IDE entwickeln und Anwendungen über die .NET-Konsole ausführen. 

## <a name="prerequisites-for-all-environments"></a>Voraussetzungen für alle Umgebungen

- [.NET Core SDK 3.1 oder höher](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installation

Q#-Anwendungen können zwar in einer beliebigen IDE erstellt werden, wir empfehlen jedoch, Visual Studio Code (VS Code) oder die Visual Studio-IDE für die lokale Entwicklung Ihrer Q#-Anwendungen zu verwenden. Für die Entwicklung in der Cloud über den Webbrowser wird Visual Studio Codespaces empfohlen. Die Entwicklung in diesen Umgebungen umfasst die umfangreichen Funktionen der QDK-Erweiterung, einschließlich Warnungen, Syntaxhervorhebung, Projektvorlagen und mehr. 

### <a name="to-configure-for-vs-code"></a>Gehen Sie zum Konfigurieren für VS Code wie folgt vor:

1. Laden Sie [VS Code](https://code.visualstudio.com/download) herunter, und führen Sie die Installation durch (Windows, Linux und Mac).
2. Installieren Sie das [Microsoft QDK für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

### <a name="to-configure-for-visual-studio"></a>Gehen Sie zum Konfigurieren für Visual Studio wie folgt vor:

1. Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 oder höher herunter, und installieren Sie die Anwendung mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload.
2. Laden Sie das [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) herunter, und installieren Sie es.

### <a name="to-configure-for-another-environment"></a>Gehen Sie zum Konfigurieren für eine andere Umgebung wie folgt vor: 

1. Geben Sie an der Eingabeaufforderung Folgendes ein:

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

### <a name="to-configure-for-visual-studio-codespaces"></a>Gehen Sie zum Konfigurieren für Visual Studio Codespaces wie folgt vor:

1. [Erstellen eines Azure-Kontos](https://azure.microsoft.com/free/).
2. Erstellen Sie eine Codespaces-Umgebung. Führen Sie dazu die Schritte in der [Schnellstartanleitung](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser) aus. Wir empfehlen, beim Erstellen der Codespaces-Umgebung `microsoft/Quantum` in das Feld „Git-Repository“ einzugeben, um QDK-spezifische Einstellungen zu laden.
3. Nun können Sie Ihre neue Umgebung starten und mit der Entwicklung im Browser über die [VS Codespaces-Cloud-IDE](https://online.visualstudio.com/environments) beginnen. Alternativ können Sie die lokale Installation von VS Code und Codespaces als [Remoteumgebung](https://docs.microsoft.com/visualstudio/online/how-to/vscode) verwenden.

## <a name="develop-with-no-locq"></a>Entwickeln mit Q#

Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Entwicklungsumgebung entspricht.

### <a name="vs-code"></a>[VS-Code](#tab/tabid-vscode)

Erstellen Sie wie folgt ein neues Projekt:

1. Klicken Sie auf **Ansicht** -> **Befehlspalette**, und wählen Sie **Q#: Neues Projekt erstellen** aus.
2. Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).
3. Navigieren Sie zum Speicherort, an dem das Dokument gespeichert werden soll. Geben Sie den Projektnamen ein, und klicken Sie auf **Projekt erstellen**.
4. Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).

Untersuchen Sie das Projekt. Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.

So führen Sie die Anwendung aus:

1. Klicken Sie auf **Terminal** -> **Neues Terminal**.
2. Geben Sie an der Eingabeaufforderung des Terminals `dotnet run` ein.
3. Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.

> [!NOTE]
> Arbeitsbereiche mit mehreren Stammordnern werden von der Q#-Erweiterung für VS Code derzeit nicht unterstützt. Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.

### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs)

Überprüfen Sie Ihre Visual Studio-Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.

So erstellen Sie eine neue Q#-Anwendung:

1. Öffnen Sie Visual Studio, und klicken Sie auf **Datei** -> **Neu** -> **Projekt**.
2. Geben Sie `Q#` in das Suchfeld ein, wählen Sie **Q#-Anwendung** aus, und klicken Sie auf **Weiter**.
3. Geben Sie einen Namen und Speicherort für Ihre Anwendung ein, und klicken Sie auf **Erstellen**.


Untersuchen Sie das Projekt. Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.

So führen Sie die Anwendung aus:

1. Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.
2. Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.

> [!NOTE]
> Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe bzw. in einem der Unterordner befinden.  

### <a name="other-editors-with-the-command-prompt"></a>[Andere Editoren mit der Eingabeaufforderung](#tab/tabid-cmdline)

Überprüfen Sie Ihre Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.

1. Erstellen einer neuen Anwendung:

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. Navigieren Sie zum Anwendungsverzeichnis:

    ```dotnetcli
    cd runSayHello
    ```

    Dieses Verzeichnis sollte nun eine Datei namens `Program.qs` enthalten. Dabei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird. Sie können diese Vorlage mit einem Text-Editor ändern und mit ihren eigenen Quantum-Anwendungen überschreiben. 

1. Führen Sie das Programm aus:

    ```dotnetcli
    dotnet run
    ```

1. Der folgende Text sollte angezeigt werden: `Hello quantum world!`

***

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.
