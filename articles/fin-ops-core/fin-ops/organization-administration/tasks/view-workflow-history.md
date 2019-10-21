---
title: Zobrazení historie workflow
description: Toto téma popisuje, jak zobrazit stav dokumentu odeslaného do systému workflowu ke zpracování a schválení.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189791"
---
# <a name="view-workflow-history"></a>Zobrazení historie workflow

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toto téma popisuje, jak zobrazit stav dokumentu odeslaného do systému workflowu ke zpracování a schválení. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejde na **Navigační podokno > Moduly > Obecné > Dotazy > Workflow > Historie workflowu**.
    - Pomocí tohoto formuláře můžete zobrazit stav dokumentu odeslaného do systému workflowu ke zpracování a schválení.  
    - **ID instance** je identifikační kód instance workflowu, která zpracovává nebo již zpracovala daný dokument.  
    - **Stav** je stav workflowu dokumentu.  
    - **ID workflowu** je identifikační kód workflowu, který zpracovává nebo již zpracoval daný dokument.  
    - **Dokument** je identifikační kód dokumentu.  
    - **Typ dokumentu** je typ dokumentu, který byl odeslán ke zpracování.  
    - **Workflow** je název workflowu, který zpracovává nebo již zpracoval daný dokument.  
    - **Verze** je číslo verze workflowu, který zpracovává nebo již zpracoval daný dokument.  
    - **Datum a čas vytvoření** je datum a čas odeslání dokumentu.  
    - **Uplynulý čas** je doba, která uplynula od odeslání dokumentu.  
    - Tlačítkem **Pokračovat** můžete obnovit proces workflowu pro vybraný dokument.  
    - Tlačítkem **Odvolat** můžete stornovat vybraný dokument tak, aby nebyl zpracován.   
2. Vyberte odkaz na požadovaném řádku v seznamu.
    - Ujistěte se, že je rozbalená část **Pracovní položky**. V této sekci můžete zobrazit pracovní položky, které jsou přidruženy k vybranému dokumentu. Může být například nutné dokončit určitou úlohu nebo schválit určitý dokument.  
    - Tlačítko **Opětovné přiřazení** otevře dialogové okno, ve kterém můžete opětovně přiřadit pracovní položku jinému uživateli.  
    - Ujistěte se, že je rozbalená část **Sledování podrobností**. V této sekci můžete zobrazit historii workflowu vybraného dokumentu.  

