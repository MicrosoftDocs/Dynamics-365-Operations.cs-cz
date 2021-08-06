---
title: Integrovaná hlavní data dodavatelů
description: Toto téma popisuje integraci dat dodavatele mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 36cfed92535c1df3ba55fd56bc8aa2f9eccf3003
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542432"
---
# <a name="integrated-vendor-master"></a>Integrovaná hlavní data dodavatelů

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Pojem *dodavatel* se týká dodavatelské organizace nebo jediného majitele, který dodává zboží nebo služby nějakému podniku. Ačkoli je *dodavatel* zavedeným konceptem v aplikacích Microsoft Dynamics 365 Supply Chain Management, v aplikacích customer engagement žádný koncept dodavatele neexistuje. Chcete-li však uložit informace o dodavateli, můžete přetížit tabulku **Účet/kontakt**. Integrovaná hlavní data dodavatelů zavádí explicitní koncept dodavatele v aplikacích customer engagement. V tabulce **Účet/kontakt** můžete použít nový návrh dodavatele nebo uložit data dodavatele. Dvojitý zápis podporuje oba přístupy.

U obou přístupů jsou data dodavatele integrována mezi Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service a portály Power Apps. V Supply Chain Management jsou data k dispozici pro workflowy, jako jsou nákupní žádanky a nákupní objednávky.

## <a name="vendor-data-flow"></a>Tok dat dodavatele

Pokud nechcete uložit data dodavatele v tabulce **Účet/kontakt** v Dataverse, můžete použít nový návrh dodavatele.

![Tok dat dodavatele.](media/dual-write-vendor-data-flow.png)

Pokud nechcete nadále ukládat data dodavatele v tabulce **Účet/kontakt**, můžete použít rozšířený návrh dodavatele. Chcete-li použít rozšířený návrh dodavatele, je nutné nakonfigurovat workflowy dodavatele v balíčku řešení dvojitého zápisu. Další informace naleznete v tématu [Přepínání mezi návrhy dodavatele](vendor-switch.md).

![Rozšířený tok dat dodavatele.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Používáte portály Power Apps pro samoobslužné dodavatele, mohou informace o dodavateli téci přímo do aplikací Finance and Operations.

## <a name="templates"></a>Šablony

Data dodavatele zahrnují všechny informace o dodavateli, například skupinu dodavatelů, adresy, kontaktní informace, platební profil a profil faktury. Kolekce mapování tabulek pracují společně během interakce s daty dodavatele, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations | Aplikace Customer Engagement     | popis
----------------------------|-----------------------------|------------
[CDS kontakty V2](mapping-reference.md#115) | kontakty | Tato šablona synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.
[Přípony názvu](mapping-reference.md#155) | msdyn_nameaffixes | Tato šablona synchronizuje referenční data přípon názvů pro odběratele a dodavatele.
[Řádky dnů platby CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Tato šablona synchronizuje referenční data řádků dnů platby pro odběratele a dodavatele.
[Dny platby CDS](mapping-reference.md#158) | msdyn_paymentdays | Tato šablona synchronizuje referenční data dnů platby pro odběratele a dodavatele.
[Řádky platebního kalendáře](mapping-reference.md#159) | msdyn_paymentschedulelines | Synchronizuje referenční data řádků platebního kalendáře pro odběratele i dodavatele.
[Platební kalendář](mapping-reference.md#160) | msdyn_paymentschedules | Tato šablona synchronizuje referenční data platebního kalendáře pro odběratele a dodavatele.
[Platební podmínky](mapping-reference.md#161) | msdyn_paymentterms | Tato šablona synchronizuje referenční data platebních podmínek (podmínek platby) pro odběratele a dodavatele.
[Dodavatelé V2](mapping-reference.md#202) | msdyn_vendors | Firmy, které používají vlastní řešení pro dodavatele, mohou využít výhod integrované koncepce dodavatele, která je zaváděna v Dataverse z důvodu integrace s aplikacemi Finance and Operations.
[Skupiny dodavatelů](mapping-reference.md#200) | msdyn_vendorgroups | Tato šablona slouží k synchronizaci informací o skupinách dodavatele.
[Platební metoda dodavatele](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Tato šablona slouží k synchronizaci informací o způsobu platby dodavatele.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
