---
title: Entwickeln mit Q# und Binder
description: Hier erfahren Sie, wie Sie mithilfe von Binder eine Anwendung vom Typ Q# erstellen.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: quickstart
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f7e9b1ae67d6275ec7ba39ea411842dc537536c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856710"
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
