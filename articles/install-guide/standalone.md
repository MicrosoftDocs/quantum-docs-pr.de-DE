---
title: 'F #-Programme ohne Treiber und Host Sprache ausführen'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706800"
---
# <a name="q-command-line-applications"></a>F #-Befehlszeilen Anwendungen

F #-Programme können eigenständig, ohne Treiber in einer Host Sprache wie c#, F # oder python ausgeführt werden.

## <a name="pre-requisites"></a>Voraussetzungen

- [.NET Core SDK 3.1 oder höher](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installation

Obwohl Sie in jeder IDE q #-Befehlszeilen Anwendungen erstellen können, wird dringend empfohlen, Visual Studio Code (vs Code) oder die Visual Studio-IDE für Ihre Q #-Anwendungen zu verwenden. Wenn Sie vs Code oder Visual Studio und die QDK-Visual Studio Code Erweiterung verwenden, erhalten Sie Zugriff auf umfangreichere Funktionen.

- Installieren von [vs Code](https://code.visualstudio.com/download) (Windows, Linux und Mac)
- Installieren Sie die [QDK-Erweiterung für vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) oder
- [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload
- Herunterladen und Installieren der [Visual Studio-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)


## <a name="develop-with-q-using-vs-code"></a>Entwickeln mit Q # mithilfe von vs Code

Installieren Sie die Quantum-Projektvorlagen:

- Gehe zu **Anzeige** -> -**Befehls Palette**
- Auswählen von " **Q #: Install Project Templates** "

Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.
- Erstellen eines neuen Projekts:
  - Gehe zu **Anzeige** -> -**Befehls Palette**
  - Wählen Sie **Q #: Neues Projekt erstellen** aus.
  - **Eigenständige Konsolenanwendung** auswählen
  - Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.
  - Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).
        
- Untersuchen des Projekts
  - Sie sollten sehen, dass eine Datei `Program.qs` mit dem Namen created erstellt wurde. Hierbei handelt es sich um ein Q #-Programm, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.

- Führen Sie die Anwendung aus.
  - Zum **Terminal** -> **neuen Terminal** wechseln
  - Geben Sie `dotnet run` ein.
  - Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.


> [!NOTE]
> * Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt. Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.

## <a name="develop-with-q-using-visual-studio"></a>Entwickeln mit Q # mithilfe von Visual Studio

Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung

- Erstellen einer neuen Q#-Anwendung
  - Wechseln Sie zu **Datei** -> **Neues** -> **Projekt** .
  - Geben Sie im Suchfeld als Suchbegriff `Q#` ein.
  - Wählen Sie **Q#-Anwendung** aus.
  - Klicken Sie auf **Weiter**.
  - Wählen Sie einen Namen und Speicherort für Ihre Anwendung aus.
  - Klicken Sie auf **Erstellen**

- Untersuchen des Projekts
  - Sie sollten sehen, dass eine Datei `Program.qs` mit dem Namen erstellt wurde. Hierbei handelt es sich um ein Q #-Programm, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.

- Ausführen der Anwendung
  - **Debuggen** -> **Starten ohne Debugging** auswählen
  - Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.

> [!NOTE]
> * Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.  


## <a name="whats-next"></a>Ausblick

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.
