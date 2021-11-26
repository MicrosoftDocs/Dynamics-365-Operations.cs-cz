---
title: Integrovaná hlavní data odběratelů
description: Toto téma popisuje integraci dat zákazníků mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48070628aafd7daac65327a484c87dc01ffb3954
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781683"
---
# <a name="integrated-customer-master"></a>Integrovaná hlavní data odběratelů

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Zákaznická data mohou být vyplněna ve více než jedné aplikaci Dynamics 365. Například řádek odběratele může pocházet z prodejní aktivity v Dynamics 365 Sales (aplikace customer engagement) nebo může řádek pocházet z maloobchodní aktivity v Dynamics 365 Commerce (aplikace finance and operations). Bez ohledu na místo, odkud pocházejí data odběratele, je integrováno na pozadí. Integrovaná hlavní předloha odběratele poskytuje flexibilitu pro hlavní zákaznická data v jakékoli aplikaci Dynamics 365 a poskytuje komplexní přehled o zákaznících v rámci aplikační sady Dynamics 365.

## <a name="customer-data-flow"></a>Tok dat odběratele

*Odběratel* je dobře definovaný koncept v aplikacích. Proto integrace zákaznických dat pouze zahrnuje harmonizaci koncepce zákazníků mezi těmito dvěmi aplikacemi. Následující obrázek znázorňuje tok dat odběratele.

![Tok dat odběratele.](media/dual-write-customer-data-flow.png)

Zákazníci mohou být široce řazeni do dvou typů: obchodní/organizační zákazníci a spotřebitelé/koncoví uživatelé. Tyto dva typy zákazníků jsou ukládány a zpracovávány odlišně v aplikacích Finance and Operations a Dataverse.

V aplikaci Finance and Operations jsou obchodní/organizační zákazníci i spotřebitelé/koncoví uživatelé řízeni v jedné tabulce s názvem **CustTable** (CustCustomerV3Entity) a jsou klasifikováni podle atributu **Typ**. (Je -li **Typ** nastaven na **Organizace**, je zákazníkem obchodní/organizační zákazník a pokud je **Typ** nastaven na **Osoba**, je zákazníkem zákazník/koncový uživatel.) Informace o primární kontaktní osobě jsou zpracovány prostřednictvím tabulky SMMContactPersonEntity.

V Dataverse jsou obchodní/organizační zákazníci ovládáni tabulkou obchodní vztah a jsou identifikováni jako zákazníci, když je atribut **RelationshipType** nastaven na **Odběratel**. Tabulka Kontakt reprezentuje spotřebitele/koncové uživatele i kontaktní osobu. Chcete-li zajistit jasné oddělení mezi spotřebitelem/koncovým uživatelem a kontaktní osobou, má tabulka **Kontakt** logický příznak, který se jmenuje **Prodejné**. Pokud je **Prodejné** je **True** je kontaktem spotřebitel/koncový uživatel a nabídky a objednávky lze vytvořit pro kontakt. Je-li **Prodejné** je **False** je kontaktem pouze primární kontaktní osoba zákazníka.

Pokud se procesu nabídky nebo objednávky účastní neprodejný kontakt, je **Prodejné** nastaveno na **True** pro označení kontaktu jako prodejného. Kontakt, který se stal prodejním kontaktem, zůstává prodejním kontaktem.

## <a name="templates"></a>Šablony

Data odběratele zahrnují všechny informace o odběrateli, například skupinu odběratelů, adresy, kontaktní informace, platební profil a profil faktury a věrnostní stav. Kolekce mapování tabulek pracuje společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations | Aplikace Customer Engagement         | popis
----------------------------|---------------------------------|------------
[CDS kontakty V2](mapping-reference.md#115) | kontakty | Tato šablona synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.
[Skupiny odběratelů](mapping-reference.md#126) | msdyn_customergroups | Tato šablona slouží k synchronizaci informací o skupinách odběratele.
[Způsob platby odběratele](mapping-reference.md#127) | msdyn_customerpaymentmethods | Tato šablona slouží k synchronizaci informací o způsobu platby odběratele.
[Zákazníci V3](mapping-reference.md#101) | účty | Tato šablona synchronizuje hlavní informace o zákaznících pro komerční a organizační zákazníky.
[Zákazníci V3](mapping-reference.md#116) | kontakty | Tato šablona synchronizuje hlavní data odběratele pro spotřebitele a koncové uživatele.
[Přípony názvu](mapping-reference.md#155) | msdyn_nameaffixes | Tato šablona synchronizuje referenční data přípon názvů pro odběratele a dodavatele.
[Řádky dnů platby CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Tato šablona synchronizuje referenční data řádků dnů platby pro odběratele a dodavatele.
[Dny platby CDS](mapping-reference.md#158) | msdyn_paymentdays | Tato šablona synchronizuje referenční data dnů platby pro odběratele a dodavatele.
[Řádky platebního kalendáře](mapping-reference.md#159) | msdyn_paymentschedulelines | Synchronizuje referenční data řádků platebního kalendáře pro odběratele i dodavatele.
[Platební kalendář](mapping-reference.md#160) | msdyn_paymentschedules | Tato šablona synchronizuje referenční data platebního kalendáře pro odběratele a dodavatele.
[Platební podmínky](mapping-reference.md#161) | msdyn_paymentterms | Tato šablona synchronizuje referenční data platebních podmínek (podmínek platby) pro odběratele a dodavatele.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
