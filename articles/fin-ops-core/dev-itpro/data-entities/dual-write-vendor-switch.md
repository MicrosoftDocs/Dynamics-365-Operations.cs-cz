---
title: Přepínání mezi návrhy dodavatele
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772357"
---
# <a name="switch-between-vendor-designs"></a>Přepínání mezi návrhy dodavatele

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Tok dat dodavatele 

Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete izolovat informace o dodavateli od zákazníků, použijte tento základní návrh dodavatele.  

![Základní tok dodavatele](media/dual-write-switch-1.png)
 
Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete pokračovat v používání entity **Účet** pro ukládání informací o dodavateli, můžete použít tento rozšířený návrh dodavatele. V tomto návrhu jsou rozšířené informace o dodavateli, jako je například stav blokovaných dodavatelů a profil dodavatele, uloženy v entitě **dodavatelé** v Common Data Service. 

![Rozšířený tok dodavatele](media/dual-write-switch-2.png)
 
Chcete-li použít rozšířený návrh dodavatele, postupujte podle následujících kroků: 
 
1. Balíček řešení **SupplyChainCommon** obsahuje šablony procesu workflow, jak je znázorněno na následujícím obrázku.
    > [!div class="mx-imgBorder"]
    > ![Šablony procesu workflow](media/dual-write-switch-3.png)
2. Vytvoření nových procesů workflowu pomocí šablon procesů workflowu: 
    1. Vytvořte nový proces workflowu pro entitu **Dodavatel** pomocí šablony procesu workflowu **Vytvořit dodavatele v entitě účtu** a klikněte na **OK**. Tento workflow zpracovává scénář vytvoření dodavatele pro entitu **Účet**.
        > [!div class="mx-imgBorder"]
        > ![Vytvořit dodavatele v entitě účet](media/dual-write-switch-4.png)
    2. Vytvořte nový proces workflowu pro entitu **Dodavatel** pomocí šablony procesu workflowu **Aktualizovat entitu účtu** a klikněte na **OK**. Tento workflow zpracovává scénář aktualizace dodavatele pro entitu **Účet**. 
        > [!div class="mx-imgBorder"]
        > ![Aktualizovat entitu Účty](media/dual-write-switch-5.png)
    3. Vytvoření nových procesů workflowu ze šablon vytvořených v entitě **Účty**. 
        > [!div class="mx-imgBorder"]
        > ![Vytvoření dodavatelů v entitě dodavatelů](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Aktualizovat entitu dodavatelů](media/dual-write-switch-7.png)
    4. Pracovní postupy můžete konfigurovat jako pracovní postupy v reálném čase nebo na pozadí na základě vašich požadavků. 
        > [!div class="mx-imgBorder"]
        > ![Převod do workflowu na pozadí](media/dual-write-switch-8.png)
    5. Aktivujte workflowy, které jste vytvořili v entitách **Účet** a **Dodavatel**, abyste mohli začít používat entitu **Účet** Customer Engagement k ukládání informací o dodavateli. 
 
