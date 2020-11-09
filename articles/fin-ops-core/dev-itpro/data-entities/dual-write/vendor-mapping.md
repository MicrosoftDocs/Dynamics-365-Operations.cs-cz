---
title: Integrovaná hlavní data dodavatelů
description: Toto téma popisuje integraci dat dodavatele mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5c4cc92fd7809f4016d8421c98f41a85fcfedc7b
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997640"
---
# <a name="integrated-vendor-master"></a>Integrovaná hlavní data dodavatelů

[!include [banner](../../includes/banner.md)]



Pojem *dodavatel* se týká dodavatelské organizace nebo jediného majitele, který dodává zboží nebo služby nějakému podniku. Ačkoli je *dodavatel* zavedeným konceptem v aplikacích Microsoft Dynamics 365 Supply Chain Management, v modelem řízených aplikacích Dynamics 365 žádný koncept dodavatele neexistuje. Chcete-li však uložit informace o dodavateli, můžete přetížit entitu **Účet/kontakt**. Integrovaná hlavní data dodavatelů zavádí explicitní koncept dodavatele v modelem řízených aplikacích Dynamics 365. V entitě **Účet/kontakt** můžete použít nový návrh dodavatele nebo uložit data dodavatele. Dvojitý zápis podporuje oba přístupy.

U obou přístupů jsou data dodavatele integrována mezi Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service a portály Power Apps. V Supply Chain Management jsou data k dispozici pro workflowy, jako jsou nákupní žádanky a nákupní objednávky.

## <a name="vendor-data-flow"></a>Tok dat dodavatele

Pokud nechcete uložit data dodavatele v entitě **Účet/kontakt** v Common Data Service, můžete použít nový návrh dodavatele.

![Tok dat dodavatele](media/dual-write-vendor-data-flow.png)

Pokud nechcete nadále ukládat data dodavatele v entitě **Účet/kontakt** , můžete použít rozšířený návrh dodavatele. Chcete-li použít rozšířený návrh dodavatele, je nutné nakonfigurovat workflowy dodavatele v balíčku řešení dvojitého zápisu. Další informace naleznete v tématu [Přepínání mezi návrhy dodavatele](vendor-switch.md).

![Rozšířený tok dat dodavatele](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Používáte portály Power Apps pro samoobslužné dodavatele, mohou informace o dodavateli téci přímo do aplikací Finance and Operations.

## <a name="templates"></a>Šablony

Data dodavatele zahrnují všechny informace o dodavateli, například skupinu dodavatelů, adresy, kontaktní informace, platební profil a profil faktury. Kolekce mapování entit pracují společně během interakce s daty dodavatele, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations | Jiné aplikace Dynamics 365     | Popis
----------------------------|-----------------------------|------------
Dodavatel V2                   | Účet                     | Firmy, které používají entitu obchodní vztah k ukládání informací o dodavateli, jí mohou nadále používat stejným způsobem. Mohou také využít explicitní funkce dodavatele, které přicházejí z důvodu integrace s aplikacemi Finance and Operations.
Dodavatel V2                   | Msdyn\_vendors              | Firmy, které používají vlastní řešení pro dodavatele, mohou využít výhod integrované koncepce dodavatele, která je zaváděna v Common Data Service z důvodu integrace s aplikacemi Finance and Operations. 
Skupiny dodavatelů               | msdyn\_vendorgroups         | Tato šablona slouží k synchronizaci informací o skupinách dodavatele.
Platební metoda dodavatele       | msdyn\_vendorpaymentmethods | Tato šablona slouží k synchronizaci informací o způsobu platby dodavatele.
CDS kontakty V2             | kontakty                    | Šablona [kontakty](customer-mapping.md#cds-contacts-v2-to-contacts) synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.
Řádky platebního kalendáře      | msdyn\_paymentschedulelines | Šablona [řádky platebního kalendáře](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synchronizuje referenční data pro odběratele a dodavatele.
Platební kalendář            | msdyn\_paymentschedules     | Šablona [plány plateb](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) synchronizuje referenční data pro odběratele a dodavatele.
Řádky dnů platby CDS V2    | msdyn\_paymentdaylines      | Šablona [řádky dní platby](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synchronizuje referenční data řádků dní platby pro odběratele a dodavatele.
Dny platby CDS            | msdyn\_paymentdays          | Šablona [dny platby](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) synchronizuje referenční data dní plateb pro odběratele a dodavatele.
Platební podmínky            | msdyn\_paymentterms         | Šablona [platební podmínky](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) synchronizuje referenční data platebních podmínek pro odběratele a dodavatele.
Přípony názvu                | msdyn\_nameaffixes          | Šablona [přípony názvů](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) synchronizuje referenční data přípon názvů pro odběratele a dodavatele.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
