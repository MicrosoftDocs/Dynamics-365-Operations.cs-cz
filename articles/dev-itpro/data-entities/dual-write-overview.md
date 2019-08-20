---
title: Integrace dat téměř v reálném čase mezi aplikací Finance and Operations a Common Data Service
description: Toto téma poskytuje přehled integrace mezi Microsoft Dynamics 365 for Finance and Operations a Common Data Service.
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
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797221"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Integrace dat téměř v reálném čase mezi aplikací Finance and Operations a Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

V současném digitálním světě používají podnikatelské ekosystémy sadu Microsoft Dynamics 365 jako celek. Protože data od osob, zákazníků, operací a zařízení s internetem věcí (IoT) proudí do jednoho zdroje, existuje příležitost pro digitální smyčky zpětné vazby. Pro dosažení těchto zkušeností je nezbytná integrace mezi aplikacemi Dynamics 365 for Finance and Operations a Dynamics 365 for Customer Engagement. Aplikace Customer Engagement jsou postaveny nad službou Common Data Service. Integrace mezi daty Finance and Operations a Common Data Service umožňuje aplikacím Customer Engagement komunikovat vzájemně a plynně s aplikací Finance and Operations.

Finance and Operations a Common Data Service poskytují synchronizaci dat téměř v reálném čase mezi aplikacemi Finance and Operations a Customer Engagement prostřednictvím rámce pro dvojí zápis. Pokrytí je široké a pokrývá 28 povrchových oblastí Finance and Operations. Cílem je poskytnout uživateli jednu zkušenost s Dynamics 365 pomocí plynulých datových toků, které spojují obchodní procesy mezi aplikacemi.

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

Pro nastavení integrace mezi aplikací Finance and Operations a Common Data Service postupujte podle těchto kroků.
    
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
