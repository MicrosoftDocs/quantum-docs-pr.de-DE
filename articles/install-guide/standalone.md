---
title: 'Entwickeln mit f #-Befehlszeilen Anwendungen'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630271"
---
# <a name="develop-with-q-command-line-applications"></a>Entwickeln mit f #-Befehlszeilen Anwendungen

F #-Programme können eigenständig, ohne Treiber in einer Host Sprache wie c#, F # oder python ausgeführt werden.

## <a name="prerequisites"></a>Voraussetzungen

- [.NET Core SDK 3.1 oder höher](https://www.microsoft.com/net/download)

## <a name="installation"></a>Installation

Obwohl Sie in jeder IDE q #-Befehlszeilen Anwendungen erstellen können, empfiehlt es sich, für Ihre Q #-Anwendungen Visual Studio Code (vs Code) oder die Visual Studio-IDE zu verwenden. Die Entwicklung in diesen Tools ermöglicht den Zugriff auf umfangreiche Funktionen.

So konfigurieren Sie vs Code:

1. Herunterladen und Installieren von [vs Code](https://code.visualstudio.com/download) (Windows, Linux und Mac).
2. Installieren Sie das [Microsoft QDK für vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

So konfigurieren Sie Visual Studio:

1. Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16,3 oder höher herunter, und installieren Sie es, wenn die Arbeitsauslastung der plattformübergreifenden .net Core-Entwicklung aktiviert ist
2. Laden Sie [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)herunter, und installieren Sie es.


## <a name="develop-with-q-using-vs-code"></a>Entwickeln mit Q # mithilfe von vs Code

Installieren Sie die f #-Projektvorlagen:

1. Öffnen Sie Visual Studio Code.
2. Klicken **View**Sie auf  ->  **Befehls Palette**anzeigen.
3. Wählen Sie **Q #: Projektvorlagen installieren**.

Wenn die **Projektvorlagen erfolgreich installiert** wurden, kann das QDK mit ihren eigenen Anwendungen und Bibliotheken verwendet werden.

So erstellen Sie ein neues Projekt:

1. Klicken **View**Sie auf  ->  **Befehls Palette** anzeigen, und wählen Sie **Q #: Neues Projekt erstellen**aus.
2. Klicken Sie auf **eigenständige Konsolenanwendung**.
3. Navigieren Sie zum Speicherort, um das Projekt zu speichern, und klicken Sie auf **Projekt erstellen**.
4. Wenn das Projekt erfolgreich erstellt wurde, klicken Sie auf **Neues Projekt öffnen...** in der unteren rechten Ecke.
        
Überprüfen Sie das Projekt. Es sollte eine Quelldatei mit dem Namen angezeigt `Program.qs` werden, bei der es sich um ein Q #-Programm handelt, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.

So führen Sie die Anwendung aus:
1. Klicken Sie auf **Terminal**  ->  **neues Terminal**.
2. Geben Sie an der Eingabeaufforderung ein `dotnet run` .
3. Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.


> [!NOTE]
> Arbeitsbereiche mit mehreren Stamm Ordnern werden zurzeit von der vs Code Q #-Erweiterung nicht unterstützt. Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.

## <a name="develop-with-q-using-visual-studio"></a>Entwickeln mit Q # mithilfe von Visual Studio

Überprüfen Sie die Visual Studio-Installation, indem Sie eine Q #- `Hello World` Anwendung erstellen.

So erstellen Sie eine neue f #-Anwendung:
1. Öffnen Sie Visual Studio, und klicken Sie auf **Datei**  ->  **neu**  ->  **Projekt**.
2. Geben `Q#` Sie in das Suchfeld ein, wählen Sie **Q # Application** aus, und klicken Sie auf **weiter**.
3. Geben Sie einen Namen und Speicherort für die Anwendung ein, und klicken Sie auf **Erstellen**.


Überprüfen Sie das Projekt. Es sollte eine Quelldatei mit dem Namen angezeigt `Program.qs` werden, bei der es sich um ein Q #-Programm handelt, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.

So führen Sie die Anwendung aus:
1. Wählen Sie **Debuggen**  ->  **Starten ohne Debugging**aus.
2. Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.

> [!NOTE]
> Wenn Sie mehrere Projekte in einer Visual Studio-Projekt Mappe haben, müssen sich alle in der Projekt Mappe enthaltenen Projekte im selben Ordner wie die Projekt Mappe oder in einem ihrer Unterordner befinden.  


## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.
