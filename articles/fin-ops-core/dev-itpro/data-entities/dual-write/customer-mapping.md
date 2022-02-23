---
title: Integrovaná hlavní data odběratelů
description: Toto téma popisuje integraci dat zákazníků mezi aplikacemi Finance and Operations a Dataverse.
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
ms.openlocfilehash: b7e9cd27bb918dc3a6088b45803329deb01a864e
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744394"
---
# <a name="integrated-customer-master"></a>Integrovaná hlavní data odběratelů

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Zákaznická data mohou být vyplněna ve více než jedné aplikaci Dynamics 365. Například řádek odběratele může pocházet z prodejní aktivity v Dynamics 365 Sales (aplikace řízená podle modelu v Dynamics 365) nebo může řádek pocházet z maloobchodní aktivity v Dynamics 365 Commerce (aplikace Finance and Operations). Bez ohledu na místo, odkud pocházejí data odběratele, je integrováno na pozadí. Integrovaná hlavní předloha odběratele poskytuje flexibilitu pro hlavní zákaznická data v jakékoli aplikaci Dynamics 365 a poskytuje komplexní přehled o zákaznících v rámci aplikační sady Dynamics 365.

## <a name="customer-data-flow"></a>Tok dat odběratele

*Odběratel* je dobře definovaný koncept v aplikacích. Proto integrace zákaznických dat pouze zahrnuje harmonizaci koncepce zákazníků mezi těmito dvěmi aplikacemi. Následující obrázek znázorňuje tok dat odběratele.

![Tok dat odběratele](media/dual-write-customer-data-flow.png)

Zákazníci mohou být široce řazeni do dvou typů: obchodní/organizační zákazníci a spotřebitelé/koncoví uživatelé. Tyto dva typy zákazníků jsou ukládány a zpracovávány odlišně v aplikacích Finance and Operations a Dataverse.

V aplikaci Finance and Operations jsou obchodní/organizační zákazníci i spotřebitelé/koncoví uživatelé řízeni v jedné tabulce s názvem **CustTable** (CustCustomerV3Entity) a jsou klasifikováni podle atributu **Typ**. (Je -li **Typ** nastaven na **Organizace**, je zákazníkem obchodní/organizační zákazník a pokud je **Typ** nastaven na **Osoba**, je zákazníkem zákazník/koncový uživatel.) Informace o primární kontaktní osobě jsou zpracovány prostřednictvím tabulky SMMContactPersonEntity.

V Dataverse jsou obchodní/organizační zákazníci ovládáni tabulkou obchodní vztah a jsou identifikováni jako zákazníci, když je atribut **RelationshipType** nastaven na **Odběratel**. Tabulka Kontakt reprezentuje spotřebitele/koncové uživatele i kontaktní osobu. Chcete-li zajistit jasné oddělení mezi spotřebitelem/koncovým uživatelem a kontaktní osobou, má tabulka **Kontakt** logický příznak, který se jmenuje **Prodejné**. Pokud je **Prodejné** je **True** je kontaktem spotřebitel/koncový uživatel a nabídky a objednávky lze vytvořit pro kontakt. Je-li **Prodejné** je **False** je kontaktem pouze primární kontaktní osoba zákazníka.

Pokud se procesu nabídky nebo objednávky účastní neprodejný kontakt, je **Prodejné** nastaveno na **True** pro označení kontaktu jako prodejného. Kontakt, který se stal prodejním kontaktem, zůstává prodejním kontaktem.

## <a name="templates"></a>Šablony

Data odběratele zahrnují všechny informace o odběrateli, například skupinu odběratelů, adresy, kontaktní informace, platební profil a profil faktury a věrnostní stav. Kolekce mapování tabulek pracuje společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations | Jiné aplikace Dynamics 365         | Popis
----------------------------|---------------------------------|------------
CDS kontakty V2             | kontakty                        | Tato šablona synchronizuje všechny primární, sekundární a terciární kontaktní informace pro odběratele i dodavatele.
Skupiny odběratelů             | msdyn_customergroups            | Tato šablona slouží k synchronizaci informací o skupinách odběratele.
Způsob platby odběratele     | msdyn_customerpaymentmethods    | Tato šablona slouží k synchronizaci informací o způsobu platby odběratele.
Zákazníci V3                | účty                        | Tato šablona synchronizuje hlavní informace o zákaznících pro komerční a organizační zákazníky.
Zákazníci V3                | kontakty                        | Tato šablona synchronizuje hlavní data odběratele pro spotřebitele a koncové uživatele.
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

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
