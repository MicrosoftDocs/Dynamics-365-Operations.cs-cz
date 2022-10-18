---
title: Srovnání funkcí cloudu a on-premises
description: Tento článek popisuje funkce, které jsou podporovány v cloudu a instalaci on-premises.
author: sericks007
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: e3b200186096a49f800d5b650ac81a45fe5e9e30
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644134"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Srovnání funkcí cloudu a on-premises

[!include [banner](../includes/banner.md)]

V tomto článku je uvedeno porovnání funkcí dostupných v cloudu a místně pro následující aplikace:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Jsou zde také [uvedeny informace o funkcích vývoje a správy](cloud-prem-comparison.md#development-and-administration-features).

Následující tabulka uvádí oblasti aplikace. Podpora cloudu a instalace on-premise je uvedena pro funkci jako celek. Tam, kde se konkrétní funkce liší od celkové oblasti, jsou funkce uvedeny na odděleném řádku ve sloupci Funkce.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Plošný**             | **Funkce**                | **Cloud** | **Místní** |
|---------------------|-----------------------------|-----------|-----------------|
| Dodržování předpisů a certifikáty        |                                                                                           | Ano       | Ano             |
|                                      | SOC 1 Typ 1 certifikace                                                                | Ano       | Ne              |
| Integrace a správa dat      |                                                                                           | Ano       | Ano             |
|                                      | Export dat do svého vlastního datového skladu                                                    | Ano       | Ano             |
|                                      | Povolení exportu přírůstkových aktualizací datových entit                                 | Ano       | Ano             |
|                                      | Integrace dat                                                                         | Ano       | Ano             |
| Správa dokumentů                  |                                                                                           | Ano       | Ano             |
| Správa financí                 |                                                                                           | Ano       | Ano             |
| Nápověda                                 |                                                                                           | Ano       | Ne              |
| Lidské zdroje                      |                                                                                           | Ano       | Ano             |
| Intelligence                         |                                                                                           | Ano       | Ano             |
|                                      | Elektronické výkaznictví (EV)                                                                 | Ano       | Ano             |
|                                      | ER: Integrace s LCS                                                                  | Ano       | Ne              |
|                                      | ER: Integrace se službou SharePoint                                                           | Ano       | Ne              |
|                                      | ER: Integrace se službou Regulatory Configuration Services (RCS)                              | Ano       | Ne              |
|                                      | ER: Používá místní systém souborů jako úložiště konfigurací ER přístupné z úložišť ER | Ne        | Ano             |
|                                      | Integrace s PowerBI.com                                                              | Ano       | Ne              |
|                                      | Integrace s PowerBI Desktop                                                          | Ne        | Ano             |
|                                      | Analytické pracovní prostory                                                                     | Ano       | Ne              |
|                                      | Inteligentní obchodní proces: doporučení                                             | Ano       | Ne              |
|                                      | Vytváření sestav Power BI s OData pomocí pracovní plochy Power BI nebo nástroje PowerQuery aplikace Excel    | Ano       | Ne              |
|                                      | Služba SQL Server Reporting Services podporuje rozšiřování                                 | Ano       | Ano             |
|                                      | Telemetrie je přenesena do cloudu                                                   | Ano       | Ne              |
| Lifecycle Services                   |                                                                                           | Ano       | Ano             |
|                                      | Konfigurovatelné obchodní procesy                                                           | Ano       | Ne              |
| Lokalizace                        |                                                                                           | Ano       | Ano             |
| Mobilní aplikace, pracovní prostory a platformy |                                                                                           | Ano       | Ano             |
| Integrace s Office                   |                                                                                           | Ano       | Ano             |
| Správa organizace          |                                                                                           | Ano       | Ano             |
| Mzdy                              |                                                                                           | Ano       | Ano             |
|                                      | Přímý vklad                                                                            | Ano       | Ne              |
| Řízení projektů a účetnictví    |                                                                                           | Ano       | Ano             |
| Zabezpečení                             |                                                                                           | Ano       | Ano             |
| Správa servisu                   |                                                                                           | Ano       | Ano             |
| Webový klient                           |                                                                                           | Ano       | Ano             |
|                                      | Záznamník úloh - Uložení nebo načtení záznamu úloh z knihovny BPM                         | Ano       | Ne              |
| Podpora                              |                                                                                           | Ano       | Ano             |
|                                      | Přístup k podpoře prostřednictvím nabídky nápovědy a podporu                                             | Ano       | Ne              |
|                                      | Obchodní události                                                                           | Ano       | Ano (je vyžadováno připojení k Internetu nebo vlastní koncové body pro odesílání a příjmu obchodních událostí v rámci sítě intranet)              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Plošný**                | **Funkce**             | **Cloud** | **Místní** |
|-------------------------|-------------------|-----------|-----------------|
| Správa majetku                     |                                                                                           | Ano       | Ano             |
| Dodržování předpisů a certifikáty        |                                                                                           | Ano       | Ano             |
|                                      | SOC 1 Typ 1 certifikace                                                                | Ano       | Ne              |
| Nákladové účetnictví                      |                                                                                           | Ano       | Ano             |
|                                      | Balíček obsahu Nákladové účetnictví pro Power BI                                                 | Ano       | Ne              |
|                                      | Pracovní prostor nákladového účetnictví pro mobilní aplikaci                                                  | Ano       | Ne              |
| Správa nákladů                      |                                                                                           | Ano       | Ano             |
|                                      | Balíček obsahu správy nákladů pro Power BI                                                 | Ano       | Ne              |
| Integrace a správa dat      |                                                                                           | Ano       | Ano             |
|                                      | Rozšíření na základě konfigurace                                                            | Ano       | Ne              |
|                                      | Export dat do svého vlastního datového skladu                                                    | Ano       | Ano             |
|                                      | Povolení exportu přírůstkových aktualizací datových entit                                 | Ano       | Ano             |
|                                      | Integrace dat                                                                         | Ano       | Ano             |
| Správa dokumentů                  |                                                                                           | Ano       | Ano             |
| Nápověda                                 |                                                                                           | Ano       | Ne              |
| Intelligence                         |                                                                                           | Ano       | Ano             |
|                                      | Elektronické výkaznictví (EV)                                                                 | Ano       | Ano             |
|                                      | ER: Integrace s LCS                                                                  | Ano       | Ne              |
|                                      | ER: Integrace se službou SharePoint                                                           | Ano       | Ne              |
|                                      | ER: Integrace se službou Regulatory Configuration Services (RCS)                              | Ano       | Ne              |
|                                      | ER: Používá místní systém souborů jako úložiště konfigurací ER přístupné z úložišť ER | Ne        | Ano             |
|                                      | Integrace s PowerBI.com                                                              | Ano       | Ne              |
|                                      | Integrace s PowerBI Desktop                                                          | Ne        | Ano             |
|                                      | Analytické pracovní prostory                                                                     | Ano       | Ne              |
|                                      | Inteligentní obchodní proces: doporučení                                             | Ano       | Ne              |
|                                      | Vytváření sestav Power BI s OData pomocí pracovní plochy Power BI nebo nástroje PowerQuery aplikace Excel    | Ano       | Ne              |
|                                      | Služba SQL Server Reporting Services podporuje rozšiřování                                 | Ano       | Ano             |
|                                      | Telemetrie je přenesena do cloudu                                                   | Ano       | Ne              |
| Řízení zásob                 |                                                                                           | Ano       | Ano             |
| Lifecycle Services                   |                                                                                           | Ano       | Ano             |
|                                      | Konfigurovatelné obchodní procesy                                                           | Ano       | Ne              |
| Lokalizace                        |                                                                                           | Ano       | Ano             |
| Výroba                        |                                                                                           | Ano       | Ano             |
| Hlavní plánování a prognóza      |                                                                                           | Ano       | Ano             |
|                                      | Optimalizace plánování                                                                     | Ano       | Číslo              |
|                                      | Prognóza poptávky                                                                        | Ano       | Číslo              |
| Mobilní aplikace, pracovní prostory a platformy |                                                                                           | Ano       | Ano             |
| Integrace s Office                   |                                                                                           | Ano       | Ano             |
| Správa organizace          |                                                                                           | Ano       | Ano             |
| Zásobování a zdroje             |                                                                                           | Ano       | Ano             |
|                                      | Funkce punch-out pro externí katalog z nákupní žádanky                                   | Ano       | Ne              |
|                                      | Sestavy Power BI analýzy nákupu a výdajů                                                  | Ano       | Ne              |
| Řízení informací o produktech       |                                                                                           | Ano       | Ano             |
| Data základního produktu                  |                                                                                           | Ano       | Ano             |
| Výroba                           |                                                                                           | Ano       | Ano             |
|                                      | Sestavy výkonnosti výroby v Power BI                                                   | Ano       | Ne              |
| Řízení a účetnictví projektů    |                                                                                           | Ano       | Ano             |
| Prodej.                                |                                                                                           | Ano       | Ano             |
|                                      | Sestavy výkonu prodeje a ziskovosti v Power BI                                      | Ano       | Ne              |
| Zabezpečení                             |                                                                                           | Ano       | Ano             |
| Správa servisu                   |                                                                                           | Ano       | Ano             |
| Správa dodavatelsko-odběratelského řetězce              |                                                                                           | Ano       | Ano             |
| Správa přepravy            |                                                                                           | Ano       | Ano             |
| Dodavatelská spolupráce                 |                                                                                           | Ano       | Ne              |
| Řízení skladu                 |                                                                                           | Ano       | Ano             |
|                                      | Mobilní aplikace skladu                                                                      | Ano       | Ano             |
|                                      | Sestavy skladu v Power BI                                                              | Ano       | Ne              |
| Webový klient                           |                                                                                           | Ano       | Ano             |
|                                      | Záznamník úloh - Uložení nebo načtení záznamu úloh z knihovny BPM                         | Ano       | Ne              |
| Podpora                              |                                                                                           | Ano       | Ano             |
|                                      | Přístup k podpoře prostřednictvím nabídky nápovědy a podporu                                             | Ano       | Ne              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Pokud chcete zobrazit seznam možností, které jsou k dispozici v místním nasazení, přečtěte si téma [Možnosti Commerce, které jsou k dispozici v místním nasazení](../../../commerce/retail-onprem.md).

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **Oblast**         | **Funkce**         | **Cloud** | **Místní** |
|------------------|---------------------|-----------|-----------------|
| Všechny oblasti Human Resources | Všechny funkce Human Resources | Ano       | Ne              |

## <a name="development-and-administration-features"></a>Funkce pro vývoj a správu

| **Oblast**                   | **Funkce**                               | **Cloud** | **Místní** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Sestavení a testování             |                                           | Ano       | Ano             |
| Rozšiřitelnost              |                                           | Ano       | Ano             |
| Monitorování a telemetrie   |                                           | Ano       | Ano             |
| Kompatibilita platformy     |                                           | Ano       | Ano             |
| Servis                  |                                           | Ano       | Ano             |
|                            | Upgrade v různých prostředích                    | Ano       | Ne              |
| Trace Parser               |                                           | Ano       | Ano             |
| PerfTimer                  |                                           | Ano       | Ano\*           |
| Upgrade                    |                                           | Ano       | Ano             |
|                            | Upgrade                                   | Ano       | Ne              |
|                            | Upgrade a podpora předchozích verzí | Ano       | Ne              |
| Vývoj Visual Studio  |                                           | Ano       | Ano             |

\* V místních prostředích zobrazuje PerfTimer pouze výsledky pro klienta.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
