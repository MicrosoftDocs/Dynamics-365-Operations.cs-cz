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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019682"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Integrace dat téměř v reálném čase pomocí Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

V současném digitálním světě používají podnikatelské ekosystémy aplikace Microsoft Dynamics 365 jako celek. Protože data od osob, zákazníků, operací a zařízení s internetem věcí (IoT) proudí do jednoho zdroje, existuje příležitost pro digitální smyčky zpětné vazby. Pro dosažení těchto zkušeností je nezbytná integrace mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365. Některé aplikace jsou postaveny nad službou Common Data Service. Integrace mezi daty aplikací Finance and Operations s Common Data Service umožní jiným aplikacím komunikovat koherentně a plynule s Finance and Operations.

Aplikace Finance and Operations a Common Data Service poskytují synchronizaci dat téměř v reálném čase mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365 prostřednictvím rámce pro dvojí zápis. Pokrytí je široké a pokrývá 28 povrchových oblastí aplikace. Cílem je poskytnout uživateli jednu zkušenost s Dynamics 365 pomocí plynulých datových toků, které spojují obchodní procesy mezi aplikacemi.

![Diagram přehledu architektury](media/dual-write-overview.jpg)

Jsou k dispozici následující propozice hodnot:

+ [Organizační hierarchie v Common Data Service](organization-mapping.md)
+ [Koncept společnosti v Common Data Service](company-data.md)
+ [Integrovaná hlavní data odběratelů](customer-mapping.md)
+ [Integrovaná hlavní kniha](ledger-mapping.md)
+ [Sjednocené prostředí produktu](product-mapping.md)
+ [Integrovaná hlavní data dodavatelů](vendor-mapping.md)
+ [Integrované sklady a pracoviště](sites-warehouses-mapping.md)
+ [Integrovaná hlavní data daní](tax-mapping.md)

## <a name="system-requirements"></a>Systémové požadavky

Synchronní, obousměrný datový tok téměř v reálném čase vyžaduje následující verze:

+ Microsoft Dynamics 365 for Finance and Operations verze 10.0.4 (července 2019) s aktualizací Platform Update 28 nebo vyšší
+ Microsoft Dynamics 365 for Customer Engagement verze Platform 9.1 (4.2) nebo novější

## <a name="setup-instructions"></a>Nastavit instrukce

Chcete-li nastavit integraci mezi aplikacemi Finance and Operations a Common Data Service, postupujte podle následujících kroků:
    
1. Chcete-li nastavit systém s dvojím zápisem, přečtěte si [podrobný návod](https://aka.ms/dualwrite-docs) k oznámení verze Preview dvojího zápisu.
2. Stáhněte a nainstalujte řešení ze skupiny [Integrace finančních operací a CDS/CE prostřednictvím dvojího zápisu](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer. Balíček obsahuje pět řešení:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Postupujte podle pořadí provádění pro [synchronizaci počátečních referenčních dat](initial-sync.md).
4. Setkáte-li se s problémy se synchronizací dvojího zápisu, nahlédněte do [Poradce při potížích s integrací dat](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Vedle sebe nelze spustit dvojí zápis a [zpeněžení potenciálního zákazníka](../../../../supply-chain/sales-marketing/prospect-to-cash.md). Pokud spouštíte řešení zpeněžení potenciálního zákazníka, je nutné jej odinstalovat. Musíte také zakázat šablony dvojího zápisu zákazníků a dodavatelů, které jsou součástí řešení zpeněžení potenciálního zákazníka.
