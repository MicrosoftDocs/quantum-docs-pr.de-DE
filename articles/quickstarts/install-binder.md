---
title: Entwickeln mit Q# und Binder
description: Hier erfahren Sie, wie Sie mithilfe von Binder eine Anwendung vom Typ Q# erstellen.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f993a1145dd8c01045d4cc7cfd0c98efd574ea78
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90836534"
---
# <a name="develop-with-no-locq-and-binder"></a>Entwickeln mit Q# und Binder

Sie können Binder verwenden, um Ihre Jupyter Notebook-Instanzen online auszuführen und freizugeben.

## <a name="use-binder-with-the-microsoft-qdk-samples"></a>Verwenden von Binder mit den Microsoft QDK-Beispielen

So konfigurieren Sie Binder automatisch für die Verwendung der Microsoft QDK-Beispiele:

1. Öffnen Sie einen Browser, und führen Sie https://aka.ms/try-qsharp aus.
1. Klicken Sie auf der Landing Page für **Quantum Development Kit-Beispiele** auf **Q#-Notebook**, um zu erfahren, wie Sie IQ# zum Schreiben eigener Quantenanwendungsnotebooks verwenden können.

![Landing Page für das QDK](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a>Verwenden von Binder mit eigenen Notebooks und eigenem Repository

Wenn Sie bereits über Notebooks in einem GitHub-Repository verfügen, können Sie Binder für die Verwendung des Repositorys konfigurieren:

1. Stellen Sie sicher, dass sich im Repositorystamm eine Datei namens *Dockerfile* befindet. Die Datei muss mindestens die folgenden Zeilen enthalten:

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > Sie können die aktuelle Version von IQ# in den [Versionshinweisen](xref:microsoft.quantum.relnotes) überprüfen.

    Weitere Informationen zum Erstellen eines Dockerfile finden Sie in der [Referenz zu Dockerfile](https://docs.docker.com/engine/reference/builder/).

2. Öffnen Sie in einem Browser [mybinder.org](https://mybinder.org).
3. Geben Sie den Repositorynamen als **GitHub-URL** (z. B. *MyName/MyRepo*) ein, und klicken Sie auf **Start**.

![MyBinder-Formular](~/media/mybinder.png)
    
## <a name="next-steps"></a>Nächste Schritte

Nach dem Einrichten Ihrer Binder-Umgebung können Sie nun [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.
