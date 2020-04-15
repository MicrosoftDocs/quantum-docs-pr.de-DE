---
title: Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) aktualisieren.
description: 'Hier wird beschrieben, wie Sie die Q#-Projekte und die Microsoft Quantum Development Kit auf die aktuelle Version aktualisieren.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 264b5640216b2c0a468b625cdef4b9e0123d8b39
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904756"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Aktualisieren des Microsoft Quantum Development Kit (QDK)

Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) auf die neueste Version aktualisieren.

In diesem Artikel wird davon ausgegangen, dass Sie das QDK bereits installiert haben. Wenn Sie zum ersten Mal installieren, finden Sie weitere Informationen im [Installationshandbuch](xref:microsoft.quantum.install).

Es wird empfohlen, mit der neuesten QDK-Version auf dem neuesten Stand zu bleiben. Führen Sie dieses Update Handbuch aus, um ein Upgrade auf die neueste Version des QDK auszuführen. Der Prozess besteht aus zwei Teilen:
1. Aktualisieren vorhandener Q#-Dateien und-Projekte, um Ihren Code mit einer beliebigen aktualisierten Syntax auszurichten
2. Das QDK selbst für die ausgewählte Entwicklungsumgebung wird aktualisiert. 

## <a name="updating-q-projects"></a>Aktualisieren von Q#-Projekten 

Unabhängig davon, ob Sie oder C# python zum Hosten von Q#-Vorgängen verwenden, befolgen Sie diese Anweisungen, um Ihre Q#-Projekte zu aktualisieren.

1. Überprüfen Sie zunächst, ob Sie über die neueste Version des [.net Core SDK 3,1](https://dotnet.microsoft.com/download)verfügen. Führen Sie den folgenden Befehl an der Eingabeaufforderung aus:

    ```dotnetcli
    dotnet --version
    ```

    Überprüfen Sie, ob die Ausgabe `3.1.100` oder höher ist. Falls nicht, installieren Sie die [neueste Version](https://dotnet.microsoft.com/download) , und überprüfen Sie Sie erneut. Befolgen Sie dann die Anweisungen unten abhängig von Ihrem Setup (Visual Studio, Visual Studio Code oder direkt über die Befehlszeile).

### <a name="update-q-projects-in-visual-studio"></a>Aktualisieren von Q#-Projekten in Visual Studio
 
1. Ein Update auf die neueste Version von Visual Studio 2019 finden Sie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .
2. Öffnen Sie die Projekt Mappe in Visual Studio
3. Wählen Sie im Menü -> Projekt Mappe **Bereinigen** **Erstellen** aus.
4. Aktualisieren Sie in jeder ihrer csproj-Dateien das Ziel Framework auf `netcoreapp3.0` (oder `netstandard2.1`, wenn es sich um ein Bibliotheksprojekt handelt).
    Das heißt, Sie bearbeiten die Zeilen in der Form:

    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```

    Weitere Informationen zum Angeben von Ziel Frameworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).
5. Speichern und schließen Sie alle Dateien in der Projekt Mappe.
6. Wählen Sie **Tools** -> **Befehlszeile** -> aus **Developer-Eingabeaufforderung**
7. Führen Sie für jedes Projekt in der Projekt Mappe den folgenden Befehl aus:

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Wenn Ihre Projekte andere Microsoft. Quantum-Pakete (z. b. Microsoft. Quantum. Numerics) verwenden, führen Sie den Befehl ebenfalls für diese aus.
8. Schließen *Sie die* Eingabeaufforderung, und wählen Sie **Build** ** -> Projekt Mappe erstellen (** Projekt Mappe neu erstellen) aus.

Nun können Sie mit [Aktualisieren Ihrer Visual Studio-QDK-Erweiterung](#update-visual-studio-qdk-extension)fortfahren.


### <a name="update-q-projects-in-visual-studio-code"></a>Aktualisieren von Q#-Projekten in Visual Studio Code

1. Öffnen Sie in Visual Studio Code den Ordner mit dem zu Aktualisier nenden Projekt.
2. **Terminal** -> **neues Terminal** auswählen
3. Befolgen Sie die Anweisungen zum Aktualisieren mithilfe der Befehlszeile (direkt unten).

### <a name="update-q-projects-using-the-command-line"></a>Aktualisieren von Q#-Projekten mithilfe der Befehlszeile

1. Navigieren Sie zu dem Ordner, der die Projektdatei enthält.
2. Führen Sie den folgenden Befehl aus:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Aktualisieren Sie in jeder ihrer csproj-Dateien das Ziel Framework auf `netcoreapp3.0` (oder `netstandard2.1`, wenn es sich um ein Bibliotheksprojekt handelt).
    Das heißt, Sie bearbeiten die Zeilen in der Form:

    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```

    Weitere Informationen zum Angeben von Ziel Frameworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).
4. Führen Sie den folgenden Befehl aus:

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    Wenn das Projekt andere Microsoft. Quantum-Pakete (z. b. Microsoft. Quantum. Numerics) verwendet, führen Sie den Befehl ebenfalls für diese aus.
5. Speichern und schließen Sie alle Dateien.
6. Wiederholen Sie 1-4 für jede Projekt Abhängigkeit, und navigieren Sie dann zurück zu dem Ordner, der das Hauptprojekt enthält, und führen Sie aus

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

Nachdem Sie Ihre Q#-Projekte aktualisiert haben, befolgen Sie die nachfolgenden Anweisungen, um das QDK selbst zu aktualisieren.

## <a name="updating-the-qdk"></a>Aktualisieren des QDK

Der Aktualisierungsprozess für das QDK hängt von der Entwicklungssprache und-Umgebung ab.
Wählen Sie unten Ihre Entwicklungsumgebung aus.

* [Python: Aktualisieren der IQ#-Erweiterung](#update-iq-for-python)
* [Jupyter-Notebooks: Aktualisieren der IQ#-Erweiterung](#update-iq-for-jupyter-notebooks)
* [Visual Studio: Aktualisieren der QDK-Erweiterung](#update-visual-studio-qdk-extension)
* [VS Code: Aktualisieren der QDK-Erweiterung](#update-vs-code-qdk-extension)
* [Befehlszeile und C#: Aktualisieren von Projektvorlagen](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a>Aktualisieren von IQ# für python

1. Aktualisieren des `iqsharp` Kernel 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Überprüfen der `iqsharp` Version

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Die folgende Ausgabe wird angezeigt.

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    Machen Sie sich keine Sorgen, wenn Ihre `iqsharp` Version höher ist, sollte Sie der [neuesten](xref:microsoft.quantum.relnotes)Version entsprechen.

3. Aktualisieren des `qsharp` Pakets

    ```bash
    pip install qsharp --upgrade
    ```

4. Überprüfen der `qsharp` Version

    ```bash
    pip show qsharp
    ```

    Die folgende Ausgabe wird angezeigt.

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. Führen Sie den folgenden Befehl am Speicherort Ihrer `.qs` Dateien aus.

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. Sie können jetzt die aktualisierte QDK-Version verwenden, um Ihre vorhandenen Quantum-Programme auszuführen.

### <a name="update-iq-for-jupyter-notebooks"></a>Aktualisieren von IQ# für jupyter-Notebooks

1. Aktualisieren des `iqsharp` Kernel

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Überprüfen der `iqsharp` Version

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Die Ausgabe sollte in etwa wie folgt aussehen:

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    Machen Sie sich keine Sorgen, wenn Ihre `iqsharp` Version höher ist, sollte Sie der [neuesten](xref:microsoft.quantum.relnotes)Version entsprechen.

3. Führen Sie den folgenden Befehl aus einer Zelle im Jupyter Notebook aus:

    ```
    %workspace reload
    ```

4. Sie können jetzt ein vorhandenes jupyter Notebook öffnen und es mit dem aktualisierten QDK ausführen.

### <a name="update-visual-studio-qdk-extension"></a>Visual Studio-QDK-Erweiterung aktualisieren

1. Aktualisieren der Q# Visual Studio-Erweiterung

    - Visual Studio fordert Sie auf, Aktualisierungen der [Erweiterung von Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) zu akzeptieren.
    - Akzeptieren des Updates

    > [!NOTE]
    > Die Projektvorlagen werden mit der Erweiterung aktualisiert. Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte. Der Code für die vorhandenen Projekte wird nicht aktualisiert, wenn die Erweiterung aktualisiert wird.

### <a name="update-vs-code-qdk-extension"></a>Update vs Code QDK-Erweiterung

1. Aktualisieren der Quantum-vs Code Erweiterung

    - Neustart vs Code
    - Navigieren Sie zur Registerkarte **Erweiterungen** .
    - Wählen Sie die **Microsoft Quantum Development Kit für Visual Studio Code Erweiterung aus** .
    - Erweiterung erneut laden

2. Aktualisieren Sie die Quantum-Projektvorlagen:

   - Navigieren Sie zu **Ansicht** -> **Befehlspalette**.
   - Auswählen von " **Q#: Install Project Templates** "
   - Nach wenigen Sekunden sollte ein Popup mit der Bestätigung angezeigt werden, dass die Projektvorlagen erfolgreich installiert wurden.

### <a name="c-using-the-dotnet-command-line-tool"></a>C#mit dem Befehlszeilen Tool "`dotnet`"

1. Aktualisieren der Quantum-Projektvorlagen für .net

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a>Wie geht es weiter?

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung aktualisiert haben, können Sie weiterhin ihre Quantum-Programme entwickeln und ausführen. Wenn Sie noch kein Programm geschrieben haben, können Sie mit [Ihrem ersten Quantum-Programm](xref:microsoft.quantum.write-program)beginnen.
