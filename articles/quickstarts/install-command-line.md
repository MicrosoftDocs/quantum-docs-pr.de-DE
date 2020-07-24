---
title: Entwickeln mit Q#-Befehlszeilenanwendungen
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 3d70838289e72afdd0a48bbdff0bec407428d125
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871432"
---
# <a name="develop-with-q-command-line-applications"></a>Entwickeln mit Q#-Befehlszeilenanwendungen

Q#-Programme können allein ohne Treiber in einer Hostsprache wie C#, F# oder Python ausgeführt werden.

## <a name="prerequisites"></a>Voraussetzungen

- [.NET Core SDK 3.1 oder höher](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installation

Sie können Q#-Befehlszeilenanwendungen zwar in einer beliebigen IDE erstellen, aber wir empfehlen Ihnen, für die lokale Entwicklung Ihrer Q#-Anwendungen Visual Studio Code (VS Code) oder die Visual Studio-IDE zu nutzen. Für die Entwicklung in der Cloud über den Webbrowser wird Visual Studio Codespaces empfohlen. Die Entwicklung in diesen Umgebungen umfasst die umfangreichen Funktionen der QDK-Erweiterung, einschließlich Warnungen, Syntaxhervorhebung, Projektvorlagen und mehr. 

Gehen Sie zum Konfigurieren von VS Code wie folgt vor:

1. Laden Sie [VS Code](https://code.visualstudio.com/download) herunter, und führen Sie die Installation durch (Windows, Linux und Mac).
2. Installieren Sie das [Microsoft QDK für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Gehen Sie zum Konfigurieren von Visual Studio wie folgt vor:

1. Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 oder höher herunter, und installieren Sie die Anwendung mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload.
2. Laden Sie das [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) herunter, und installieren Sie es.

So konfigurieren Sie Visual Studio Codespaces:

1. [Erstellen eines Azure-Kontos](https://azure.microsoft.com/free/).
2. Erstellen Sie eine Codespaces-Umgebung. Führen Sie dazu die Schritte in der [Schnellstartanleitung](https://docs.microsoft.com/visualstudio/online/quickstarts/browser) aus. Wir empfehlen, beim Erstellen der Codespaces-Umgebung `microsoft/Quantum` in das Feld „Git-Repository“ einzugeben, um QDK-spezifische Einstellungen zu laden.
3. Nun können Sie Ihre neue Umgebung starten und mit der Entwicklung im Browser über die [VS Codespaces-Cloud-IDE](https://online.visualstudio.com/environments) beginnen. Alternativ können Sie die lokale Installation von VS Code und Codespaces als [Remoteumgebung](https://docs.microsoft.com/visualstudio/online/how-to/vscode) verwenden.


Geben Sie Folgendes in die Befehlszeile ein, um das QDK für eine andere Umgebung zu installieren:

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-q"></a>Entwickeln mit Q#

Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Umgebung entspricht.

### <a name="vs-code"></a>[VS-Code](#tab/tabid-vscode)

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

### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs)

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

### <a name="other-editors-with-the-command-line"></a>[Andere Editoren mit der Befehlszeile](#tab/tabid-cmdline)

Überprüfen Sie Ihre Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.

1. Installieren Sie die Projektvorlagen.

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

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
