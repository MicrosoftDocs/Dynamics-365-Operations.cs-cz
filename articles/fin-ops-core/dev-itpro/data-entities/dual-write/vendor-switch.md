---
title: Přepínání mezi návrhy dodavatele
description: Toto téma popisuje způsob přepínání mezi integrací dat dodavatele mezi aplikacemi Finance and Operations a Common Data Service.
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
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019673"
---
# <a name="switch-between-vendor-designs"></a>Přepínání mezi návrhy dodavatele

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a>Tok dat dodavatele 

Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete izolovat informace o dodavateli od zákazníků, použijte tento základní návrh dodavatele.  

![Základní tok dodavatele](media/dual-write-vendor-data-flow.png)
 
Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete pokračovat v používání entity **Účet** pro ukládání informací o dodavateli, můžete použít tento rozšířený návrh dodavatele. V tomto návrhu jsou rozšířené informace o dodavateli, jako je například stav blokovaných dodavatelů a profil dodavatele, uloženy v entitě **dodavatelé** v Common Data Service. 

![Rozšířený tok dodavatele](media/dual-write-vendor-detail.jpg)
 
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
    5. Aktivujte workflowy, které jste vytvořili v entitách **Účet** a **Dodavatel**, abyste mohli začít používat entitu **Účet** k ukládání informací o dodavateli. 
 
