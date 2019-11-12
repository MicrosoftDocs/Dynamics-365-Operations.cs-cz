---
title: Integrace dat téměř v reálném čase pomocí Common Data Service
description: Toto téma poskytuje přehled integrace mezi Finance and Operations a Common Data Service.
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
ms.openlocfilehash: d70bce4e47c05a7974c1b974fdca17682e5370aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550850"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Integrace dat téměř v reálném čase pomocí Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

V současném digitálním světě používají podnikatelské ekosystémy aplikace Microsoft Dynamics 365 jako celek. Protože data od osob, zákazníků, operací a zařízení s internetem věcí (IoT) proudí do jednoho zdroje, existuje příležitost pro digitální smyčky zpětné vazby. Pro dosažení těchto zkušeností je nezbytná integrace mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365. Některé aplikace jsou postaveny nad službou Common Data Service. Integrace mezi daty aplikací Finance and Operations a Common Data Service umožňuje dalším aplikacím komunikovat vzájemně a plynně s aplikací Finance and Operations.

Aplikace Finance and Operations a Common Data Service poskytují synchronizaci dat téměř v reálném čase mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365 prostřednictvím rámce pro dvojí zápis. Pokrytí je široké a pokrývá 28 povrchových oblastí aplikace. Cílem je poskytnout uživateli jednu zkušenost s Dynamics 365 pomocí plynulých datových toků, které spojují obchodní procesy mezi aplikacemi.

![Diagram přehledu architektury](media/dual-write-overview.jpg)

Pro zákazníky jsou k dispozici následující propozice hodnot:

+ [Organizační hierarchie v Common Data Service](dual-write-organization.md)
+ [Koncept společnosti v Common Data Service](dual-write-company.md)
+ [Integrovaná hlavní data odběratelů](dual-write-customer.md)
+ [Integrovaná hlavní data dodavatelů](dual-write-vendor.md)
+ Sjednocený hlavní produkt

## <a name="system-requirements"></a>Systémové požadavky

Synchronní, obousměrný datový tok téměř v reálném čase vyžaduje následující verze:

+ Microsoft Dynamics 365 for Finance and Operations verze 10.0.4 (července 2019) s aktualizací Platform Update 28 nebo vyšší
+ Microsoft Dynamics 365 for Customer Engagement verze Platform 9.1 (4.2) nebo novější

## <a name="setup-instructions"></a>Nastavit instrukce

Pro nastavení integrace mezi aplikacemi Finance and Operations a Common Data Service postupujte podle těchto kroků.
    
1. Chcete-li nastavit systém s dvojím zápisem, přečtěte si [podrobný návod](https://aka.ms/dualwrite-docs) k oznámení verze Preview dvojího zápisu.
2. Stáhněte a nainstalujte řešení ze skupiny [integrace Finance and Operations, Common Data Service a Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer Balíček obsahuje pět řešení:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Postupujte podle pořadí provádění pro [synchronizaci počátečních referenčních dat](dual-write-initial.md).
4. Setkáte-li se s problémy se synchronizací dvojího zápisu, nahlédněte do [Poradce při potížích s integrací dat](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Vedle sebe nelze spustit dvojí zápis a [zpeněžení potenciálního zákazníka](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct). Pokud spouštíte řešení zpeněžení potenciálního zákazníka, je nutné jej odinstalovat. Musíte také zakázat šablony dvojího zápisu zákazníků a dodavatelů, které jsou součástí řešení zpeněžení potenciálního zákazníka.
