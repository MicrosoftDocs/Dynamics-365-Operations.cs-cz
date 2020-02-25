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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019674"
---
# <a name="integrated-vendor-master"></a>Integrovaná hlavní data dodavatelů

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Pojem *dodavatel* označuje dodavatelskou organizaci nebo jediného majitele, který je součástí procesu dodavatelského řetězce a který dodává zboží pro podnik. Ačkoli je *dodavatel* zavedeným konceptem v aplikacích Finance and Operations, koncept dodavatele neexistuje v ostatních aplikacích Dynamics 365. Místo toho některé firmy přetíží entitu Obchodní vztah a ukládají informace o zákaznících i informace o dodavateli. Jiné společnosti používají vlastní koncept dodavatele. Integrace Common Data Service podporuje oba tyto návrhy. Proto můžete povolit kterýkoli z návrhů v závislosti na vašem obchodním scénáři.

Integrace dat dodavatele mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365 umožňuje více hlavních dat. Bez ohledu na to, odkud data dodavatele pocházejí, jsou integrována v pozadí mezi hranicemi aplikace a rozdíly v infrastruktuře. 

### <a name="vendor-data-flow"></a>Tok dat dodavatele

Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete izolovat informace o dodavateli od informací o zákazníkovi, můžete použít nový návrh dodavatele.

![Tok dat dodavatele](media/dual-write-vendor-data-flow.png)

Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete pokračovat v používání entity obchodního účtu pro ukládání informací o dodavateli, můžete použít nový rozšířený návrh dodavatele. V tomto návrhu jsou rozšířené informace o dodavateli, například skupina dodavatelů a účetní profil dodavatele, uloženy v podrobnostech dodavatele.

![Rozšířený tok dat dodavatele](media/dual-write-vendor-detail.jpg)

Kontaktní informace dodavatele se podobají kontaktním informacím o zákaznících. Na pozadí jsou informace kontaktní osoby uloženy a načteny ze stejných entit.

## <a name="templates"></a>Šablony

Data dodavatele zahrnují všechny informace o dodavateli, například skupinu dodavatelů, adresy, kontaktní informace, platební profil a profil faktury. Kolekce mapování entit pracují společně během interakce s daty dodavatele, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations | Jiné aplikace Dynamics 365         | Popis
----------------------------|---------------------------------|------------
Dodavatel V2               | Účet | Firmy, které používají entitu obchodní vztah k ukládání informací o dodavateli, jí mohou nadále používat stejným způsobem. Mohou také využít explicitní funkce dodavatele, které přicházejí z důvodu integrace s aplikacemi Finance and Operations.
Dodavatel V2               | Msdyn\_vendors | Firmy, které používají vlastní řešení pro dodavatele, mohou využít výhod integrované koncepce dodavatele, která je zaváděna v Common Data Service z důvodu integrace s aplikacemi Finance and Operations. 
Skupiny dodavatelů | msdyn_vendorgroups | Tato šablona slouží k synchronizaci informací o skupinách dodavatele.
Platební metoda dodavatele | msdyn_vendorpaymentmethods | Tato šablona slouží k synchronizaci informací o způsobu platby dodavatele.
CDS kontakty V2             | kontakty                        | Šablona [kontakty](customer-mapping.md#cds-contacts-v2-to-contacts) synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.
Řádky platebního kalendáře      | msdyn_paymentschedulelines      | Šablona [řádky platebního kalendáře](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synchronizuje referenční data pro odběratele a dodavatele.
Platební kalendář            | msdyn_paymentschedules          | Šablona [plány plateb](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) synchronizuje referenční data pro odběratele a dodavatele.
Řádky dnů platby CDS V2    | msdyn_paymentdaylines           | Šablona [řádky dní platby](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synchronizuje referenční data řádků dní platby pro odběratele a dodavatele.
Dny platby CDS            | msdyn_paymentdays               | Šablona [dny platby](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) synchronizuje referenční data dní plateb pro odběratele a dodavatele.
Platební podmínky            | msdyn_paymentterms              | Šablona [platební podmínky](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) synchronizuje referenční data platebních podmínek pro odběratele a dodavatele.
Přípony názvu                | msdyn_nameaffixes               | Šablona [přípony názvů](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) synchronizuje referenční data přípon názvů pro odběratele a dodavatele.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
