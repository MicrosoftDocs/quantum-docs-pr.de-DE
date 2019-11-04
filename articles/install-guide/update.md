---
title: Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) aktualisieren.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ebf1f15d65a12c921cd3f04e4111d463d1060f8e
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463284"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Aktualisieren des Microsoft Quantum Development Kit (QDK)

Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) auf die neueste Version aktualisieren.

In diesem Artikel wird davon ausgegangen, dass Sie das QDK bereits installiert haben. Wenn Sie zum ersten Mal installieren, finden Sie weitere Informationen im [Installationshandbuch](xref:microsoft.quantum.install).


## <a name="updating-q-projects"></a>Aktualisieren von f #-Projekten 

1. Installieren Sie zunächst die neueste Version des [.net Core SDK 3,0](https://dotnet.microsoft.com/download) , und führen Sie den folgenden Befehl an der Eingabeaufforderung aus:
```bash
dotnet --version
```
 Überprüfen Sie, ob die Ausgabe 3.0.100 oder höher ist, und befolgen Sie dann die Anweisungen unten abhängig von Ihrem Setup.

### <a name="in-visual-studio"></a>In Visual Studio
 
 1. Ein Update auf die neueste Version von Visual Studio 2019 finden Sie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .
 2. Öffnen Sie die Projekt Mappe in Visual Studio
 3. Wählen Sie im Menü > Projekt Mappe bereinigen erstellen aus. 
 4. [Aktualisieren Sie das Ziel Framework](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in jeder ihrer csproj-Dateien auf netcoreapp 3.0 (oder netstandard 2.1, wenn es sich um ein Bibliotheksprojekt handelt).
 5. Speichern und schließen Sie alle Dateien in der Projekt Mappe.
 6. Wählen Sie Tools > Befehlszeile > aus Developer-Eingabeaufforderung
 7. Führen Sie für jedes Projekt in der Projekt Mappe den folgenden Befehl aus:
 ```bash
 dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
 ```
Wenn in Ihren Projekten andere Microsoft. Quantum-Pakete verwendet werden, führen Sie den Befehl ebenfalls für diese aus. 
 8. Schließen Sie die Eingabeaufforderung, und wählen Sie > Projekt Mappe erstellen aus (Wählen Sie *nicht* neu erstellen aus, da die Neuerstellung anfänglich fehlschlägt).

### <a name="in-visual-studio-code"></a>In Visual Studio Code

1. Öffnen Sie in Visual Studio Code den Ordner mit dem zu Aktualisier nenden Projekt.
1. Terminal > neues Terminal auswählen
1. Befolgen Sie die Anweisungen zum Aktualisieren mithilfe der Befehlszeile.

### <a name="using-the-command-line"></a>Verwenden der Befehlszeile

1. Navigieren Sie zu dem Ordner, der die Projektdatei enthält.
2. Führen Sie den folgenden Befehl aus:
```bash
dotnet clean [project_name].csproj
```

3. [Aktualisieren Sie das Ziel Framework](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in jeder ihrer csproj-Dateien auf netcoreapp 3.0 (oder netstandard 2.1, wenn es sich um ein Bibliotheksprojekt handelt).
4. Führen Sie den folgenden Befehl aus:
```bash
dotnet add package Microsoft.Quantum.Development.Kit
```
Wenn das Projekt andere Microsoft. Quantum-Pakete verwendet, führen Sie den Befehl ebenfalls für diese aus.

5. Alle Dateien speichern und schließen
6. Wiederholen Sie 1-4 für jede Projekt Abhängigkeit, und navigieren Sie dann zurück zu dem Ordner, der das Hauptprojekt enthält, und führen Sie aus
```bash
dotnet build [project_name].csproj
```

## <a name="update-iq-for-python"></a>Aktualisieren von IQ # für python

1. Aktualisieren des `iqsharp` Kernel

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Überprüfen der `iqsharp` Version

    ```bash
    dotnet iqsharp --version
    ```

    Die folgende Ausgabe wird angezeigt.

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```

1. Aktualisieren des `qsharp` Pakets

    ```bash
    pip install qsharp --upgrade
    ```

1. Überprüfen der `qsharp` Version

    ```bash
    pip show qsharp
    ```

    Die folgende Ausgabe wird angezeigt.

    ```bash
    Name: qsharp
    Version: 0.10.1911.307
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
1. Führen Sie den folgenden Befehl am Speicherort Ihrer `.qs` Dateien aus.
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

1. Sie können jetzt die aktualisierte QDK-Version verwenden, um Ihre vorhandenen Quantum-Programme auszuführen.

## <a name="update-iq-for-jupyter-notebooks"></a>Aktualisieren von IQ # für jupyter-Notebooks

1. Aktualisieren des `iqsharp` Kernel

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Überprüfen der `iqsharp` Version

    ```bash
    dotnet iqsharp --version
    ```

    Die folgende Ausgabe wird angezeigt.

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```
1. Führen Sie den folgenden Befehl aus einer Zelle im Jupyter Notebook aus:
    ```
    %workspace reload
    ```

1. Sie können jetzt ein vorhandenes jupyter Notebook öffnen und es mit dem aktualisierten QDK ausführen.

## <a name="update-visual-studio-qdk-extension"></a>Visual Studio-QDK-Erweiterung aktualisieren

1. Aktualisieren der f # Visual Studio-Erweiterung

    - Visual Studio fordert Sie auf, Aktualisierungen der [Erweiterung von Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) zu akzeptieren.
    - Akzeptieren des Updates

    > [!NOTE]
    > Die Projektvorlagen werden mit der Erweiterung aktualisiert. Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte. Der Code für die vorhandenen Projekte wird nicht aktualisiert, wenn die Erweiterung aktualisiert wird.

## <a name="update-vs-code-qdk-extension"></a>Update vs Code QDK-Erweiterung

1. Aktualisieren der Quantum-vs Code Erweiterung

    - Neustart vs Code
    - Navigieren Sie zur Registerkarte **Erweiterungen** .
    - Wählen Sie die **Microsoft Quantum Development Kit für Visual Studio Code Erweiterung aus** .
    - Erweiterung erneut laden

1. Aktualisieren Sie die Quantum-Projektvorlagen:

   - Gehe zu **Ansicht** -> **Befehls Palette**
   - Auswählen von " **Q #: Install Project Templates** "

## <a name="c-using-the-dotnet-command-line-tool"></a>C#mit dem Befehlszeilen Tool "`dotnet`"

1. Aktualisieren der Quantum-Projektvorlagen für .net

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a>Wie geht es weiter?

Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung aktualisiert haben, können Sie weiterhin ihre Quantum-Programme entwickeln und ausführen. Wenn Sie noch kein Programm geschrieben haben, können Sie mit [Ihrem ersten Quantum-Programm](xref:microsoft.quantum.write-program)beginnen.
