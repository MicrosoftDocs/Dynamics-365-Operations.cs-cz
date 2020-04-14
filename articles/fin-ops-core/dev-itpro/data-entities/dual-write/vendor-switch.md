---
title: Přepínání mezi návrhy dodavatele
description: Tohle téma popisuje způsob přepínání integrace dat dodavatele mezi aplikacemi Finance and Operations a Common Data Service.
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
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173032"
---
# <a name="switch-between-vendor-designs"></a>Přepínání mezi návrhy dodavatele

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Tok dat dodavatele 

Pokud se rozhodnete použít entitu **Účet** k ukládání dodavatelů typu **Organizace** a entitu **Kontakt** k ukládání dodavatelů typu **Osoba**, nakonfigurujte následující workflowy. V opačném případě není tato konfigurace nutná.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Použití rozšířeného návrhu dodavatele pro dodavatele typu Organizace

Balíček řešení **Dynamics365FinanceExtended** obsahuje následující šablony procesu workflowu. Pro každou šablonu vytvoříte workflow.

+ Vytvořte dodavatele v entitě Účty.
+ Vytvořte dodavatele v entitě Dodavatelé.
+ Aktualizujte dodavatele v entitě Účty.
+ Aktualizujte dodavatele v entitě Dodavatelé.

Pro vytvoření nových procesů workflowu pomocí šablon procesů workflowu postupujte následovně.

1. Vytvořte proces workflowu pro entitu **Dodavatel** a vyberte šablonu procesu workflowu **Vytvoření dodavatelů v entitě Účty**. Pak vyberte **OK**. Tento workflow zpracovává scénář vytvoření dodavatele pro entitu **Účet**.

    ![Proces workflowu Vytvoření dodavatelů v entitě Účty](media/create_process.png)

2. Vytvořte proces workflowu pro entitu **Dodavatel** a vyberte šablonu procesu workflowu **Aktualizace dodavatelů v entitě Účty**. Pak vyberte **OK**. Tento workflow zpracovává scénář aktualizace dodavatele pro entitu **Účet**.
3. Vytvořte proces workflowu pro entitu **Účet** a vyberte šablonu procesu workflowu **Vytvoření dodavatelů v entitě Dodavatelé**.
4. Vytvořte proces workflowu pro entitu **Účet** a vyberte šablonu procesu workflowu **Aktualizace dodavatelů v entitě Dodavatelé**.
5. Pracovní postupy můžete konfigurovat buď jako workflowy v reálném čase nebo na pozadí v závislosti na vašich požadavcích. Chcete-li nakonfigurovat workflow jako workflow na pozadí, vyberte možnost **Převést na workflow na pozadí**.

    ![Tlačítko Převést na workflow na pozadí](media/background_workflow.png)

6. Aktivujte workflowy, které jste vytvořili pro entity **Účet** a **Dodavatel**, abyste mohli začít používat entitu **Účet** k ukládání informací pro dodavatele typu **Organizace**.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Použití rozšířeného návrhu dodavatele pro dodavatele typu Osoba

Balíček řešení **Dynamics365FinanceExtended** obsahuje následující šablony procesu workflowu. Pro každou šablonu vytvoříte workflow.

+ V entitě Dodavatelé vytvořte dodavatele typu Osoba.
+ V entitě Kontakty vytvořte dodavatele typu Osoba.
+ V entitě Kontakty aktualizujte dodavatele typu Osoba.
+ V entitě Dodavatelé aktualizujte dodavatele typu Osoba.

Pro vytvoření nových procesů workflowu pomocí šablon procesů workflowu postupujte následovně.

1. Vytvořte proces workflowu pro entitu **Dodavatel** a vyberte šablonu procesu workflowu **Vytvoření dodavatelů typu Osoba v entitě Kontakty**. Pak vyberte **OK**. Tento workflow zpracovává scénář vytvoření dodavatele pro entitu **Kontakt**.
2. Vytvořte proces workflowu pro entitu **Dodavatel** a vyberte šablonu procesu workflowu **Aktualizace dodavatelů typu Osoba v entitě Kontakty**. Pak vyberte **OK**. Tento workflow zpracovává scénář aktualizace dodavatele pro entitu **Kontakt**.
3. Vytvořte proces workflowu pro entitu **Kontakt** a vyberte šablonu **Vytvoření dodavatelů typu Osoba v entitě Dodavatelé**.
4. Vytvořte proces workflowu pro entitu **Kontakt** a vyberte šablonu **Aktualizace dodavatelů typu Osoba v entitě Dodavatelé**.
5. Pracovní postupy můžete konfigurovat buď jako workflowy v reálném čase nebo na pozadí v závislosti na vašich požadavcích. Chcete-li nakonfigurovat workflow jako workflow na pozadí, vyberte možnost **Převést na workflow na pozadí**.
6. Aktivujte workflowy, které jste vytvořili v entitách **Kontakt** a **Dodavatel**, abyste mohli začít používat entitu **Kontakt** k ukládání informací pro dodavatele typu **Osoba**.
