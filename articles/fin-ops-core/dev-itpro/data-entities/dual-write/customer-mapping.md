---
title: Integrovaná hlavní data odběratelů
description: Toto téma popisuje integraci dat zákazníků mezi aplikacemi Finance and Operations a Common Data Service.
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
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019683"
---
# <a name="integrated-customer-master"></a>Integrovaná hlavní data odběratelů

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Pro záznamy zákazníků je typické, že je možné je řídit ve více než jedné aplikaci. Prodejní aktivita může například přinést záznamy komerčních zákazníků prostřednictvím aplikace Sales a elektronický obchod nebo maloobchodní prodej mohou přinést záznamy zákazníků v rámci Finance and Operations. Bez ohledu na to, odkud záznam odběratele pochází, je integrován v pozadí mezi hranicemi aplikace a rozdíly v infrastruktuře. Integrované řízení zákazníků pomáhá zvládat scénáře vícenásobného řízení a poskytuje komplexní přehled o zákaznících do sady aplikací Dynamics 365.

## <a name="customer-data-flow"></a>Tok dat odběratele

*Odběratel* je dobře definovaný koncept v aplikacích. Proto integrace zákaznických dat pouze zahrnuje harmonizaci koncepce zákazníků mezi těmito dvěmi aplikacemi. Následující obrázek znázorňuje tok dat odběratele.

![Tok dat odběratele](media/dual-write-customer-data-flow.png)

Zákazníci mohou být široce řazeni do dvou typů: obchodní/organizační zákazníci a spotřebitelé/koncoví uživatelé. Tyto dva typy zákazníků jsou ukládány a zpracovávány odlišně v aplikacích Finance and Operations a Common Data Service.

V aplikaci Finance and Operations jsou obchodní/organizační zákazníci i spotřebitelé/koncoví uživatelé řízeni v jedné tabulce s názvem **CustTable** (CustomerCustomerV3Entity) a jsou klasifikováni podle atributu **Typ**. (Je -li **Typ** nastaven na **Organizace**, je zákazníkem obchodní/organizační zákazník a pokud je **Typ** nastaven na **Osoba**, je zákazníkem zákazník/koncový uživatel.) Informace o primární kontaktní osobě jsou zpracovány prostřednictvím entity SMMContactPersonEntity.

V Common Data Service jsou obchodní/organizační zákazníci ovládáni entitou obchodní vztah a jsou identifikováni jako zákazníci, když je atribut **RelationshipType** nastaven na **Odběratel**. Entita kontakt reprezentuje spotřebitele/koncové uživatele i kontaktní osobu. Chcete-li zajistit jasné oddělení mezi spotřebitelem/koncovým uživatelem a kontaktní osobou, má entita **Kontakt** logický příznak, který se jmenuje **Prodejné**. Pokud je **Prodejné** je **True** je kontaktem spotřebitel/koncový uživatel a nabídky a objednávky lze vytvořit pro kontakt. Je-li **Prodejné** je **False** je kontaktem pouze primární kontaktní osoba zákazníka.

Pokud se procesu nabídky nebo objednávky účastní neprodejný kontakt, je **Prodejné** nastaveno na **True** pro označení kontaktu jako prodejného. Kontakt, který se stal prodejním kontaktem, zůstává prodejním kontaktem.

## <a name="templates"></a>Šablony

Data odběratele zahrnují všechny informace o odběrateli, například skupinu odběratelů, adresy, kontaktní informace, platební profil a profil faktury a věrnostní stav. Kolekce mapování entit pracuje společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations | Jiné aplikace Dynamics 365         | Popis
----------------------------|---------------------------------|------------
CDS kontakty V2             | kontakty                        | Tato šablona synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.
Skupiny odběratelů             | msdyn_customergroups            | Tato šablona slouží k synchronizaci informací o skupinách odběratele.
Způsob platby odběratele     | msdyn_customerpaymentmethods    | Tato šablona slouží k synchronizaci informací o způsobu platby odběratele.
Zákazníci V3                | účty                        | Tato šablona synchronizuje hlavní informace o zákaznících pro komerční a organizační zákazníky.
Zákazníci V3                | kontakty                        | Tato šablona synchronizuje hlavní data odběratele pro spotřebitele a koncové uživatele.
Věrnostní karta                | msdyn_loyaltycards              | Tato šablona slouží k synchronizaci informací o věrnostních kartách.
Přípony názvu                | msdyn_nameaffixes               | Tato šablona synchronizuje referenční data přípon názvů pro odběratele a dodavatele.
Řádky dnů platby CDS V2    | msdyn_paymentdaylines           | Tato šablona synchronizuje referenční data řádků dnů platby pro odběratele a dodavatele.
Dny platby CDS            | msdyn_paymentdays               | Tato šablona synchronizuje referenční data dnů platby pro odběratele a dodavatele.
Řádky platebního kalendáře      | msdyn_paymentschedulelines      | Synchronizuje referenční data řádků platebního kalendáře pro odběratele i dodavatele.
Platební kalendář            | msdyn_paymentschedules          | Tato šablona synchronizuje referenční data platebního kalendáře pro odběratele a dodavatele.
Platební podmínky            | msdyn_paymentterms              | Tato šablona synchronizuje referenční data platebních podmínek (podmínek platby) pro odběratele a dodavatele.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
