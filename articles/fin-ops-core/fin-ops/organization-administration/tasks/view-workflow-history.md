---
title: Zobrazení historie workflow
description: Toto téma popisuje, jak zobrazit stav dokumentu odeslaného do systému workflowu ke zpracování a schválení.
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351f9c80eab8e9810fa6a4538f003eaef1a4a4fd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747218"
---
# <a name="view-workflow-history"></a>Zobrazení historie workflow

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]