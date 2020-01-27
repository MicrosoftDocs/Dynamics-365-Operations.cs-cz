---
title: Srovnání funkcí cloudu a on-premises
description: Toto téma popisuje funkce, které jsou podporovány v cloudu a instalaci on-premises.
author: sericks007
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 7837fbaaffdbd61a1adce1698800017bf4f6a018
ms.sourcegitcommit: 282552609fdb82ec4463f801023b4bc01bc151d5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935380"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Srovnání funkcí cloudu a on-premises

[!include [banner](../includes/banner.md)]

V tomto tématu je uvedeno porovnání funkcí dostupných v cloudu a místně pro následující aplikace:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Retail](cloud-prem-comparison.md#dynamics-365-retail)
- [Dynamics 365 Talent](cloud-prem-comparison.md#dynamics-365-talent)

Jsou zde také [uvedeny informace o funkcích vývoje a správy](cloud-prem-comparison.md#development-and-administration-features).

Následující tabulka uvádí oblasti aplikace. Podpora cloudu a instalace on-premise je uvedena pro funkci jako celek. Tam, kde se konkrétní funkce liší od celkové oblasti, jsou funkce uvedeny na odděleném řádku ve sloupci Funkce.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Oblast**             | **Funkce**                | **Cloud** | **Místní** |
|---------------------|-----------------------------|-----------|-----------------|
| Dodržování předpisů a certifikáty        |                                                                                           | Ano       | Ano             |
|                                      | SOC 1 Typ 1 certifikace                                                                | Ano       | Ne              |
| Integrace a správa dat      |                                                                                           | Ano       | Ano             |
|                                      | Rozšíření na základě konfigurace                                                            | Ano       | Žádný              |
|                                      | Export dat do svého vlastního datového skladu                                                    | Ano       | Ano             |
|                                      | Povolení exportu přírůstkových aktualizací datových entit                                 | Ano       | Ano              |
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
|                                      | Integrace s aplikací PowerBI Desktop                                                          | Ne        | Ano             |
|                                      | Analytické pracovní prostory                                                                     | Ano       | Ne              |
|                                      | Inteligentní obchodní proces: doporučení                                             | Ano       | Žádný              |
|                                      | Vytváření sestav Power BI s OData pomocí pracovní plochy Power BI nebo nástroje PowerQuery aplikace Excel    | Ano       | Žádný              |
|                                      | Služba SQL Server Reporting Services podporuje rozšiřování                                 | Ano       | Ne              |
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

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Oblast**                | **Funkce**             | **Cloud** | **Místní** |
|-------------------------|-------------------|-----------|-----------------|
| Dodržování předpisů a certifikáty        |                                                                                           | Ano       | Ano             |
|                                      | SOC 1 Typ 1 certifikace                                                                | Ano       | Žádný              |
| Nákladové účetnictví                      |                                                                                           | Ano       | Ano             |
|                                      | Balíček obsahu Nákladové účetnictví pro Power BI                                                 | Ano       | Žádný              |
|                                      | Pracovní prostor nákladového účetnictví pro mobilní aplikaci                                                  | Ano       | Žádný              |
| Správa nákladů                      |                                                                                           | Ano       | Ano             |
|                                      | Balíček obsahu správy nákladů pro Power BI                                                 | Ano       | Žádný              |
| Integrace a správa dat      |                                                                                           | Ano       | Ano             |
|                                      | Rozšíření na základě konfigurace                                                            | Ano       | Žádný              |
|                                      | Export dat do svého vlastního datového skladu                                                    | Ano       | Ano             |
|                                      | Povolení exportu přírůstkových aktualizací datových entit                                 | Ano       | Ne              |
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
|                                      | Integrace s aplikací PowerBI Desktop                                                          | Ne        | Ano             |
|                                      | Analytické pracovní prostory                                                                     | Ano       | Ne              |
|                                      | Inteligentní obchodní proces: doporučení                                             | Ano       | Žádný              |
|                                      | Vytváření sestav Power BI s OData pomocí pracovní plochy Power BI nebo nástroje PowerQuery aplikace Excel    | Ano       | Žádný              |
|                                      | Služba SQL Server Reporting Services podporuje rozšiřování                                 | Ano       | Žádný              |
|                                      | Telemetrie je přenesena do cloudu                                                   | Ano       | Žádný              |
| Řízení zásob                 |                                                                                           | Ano       | Ano             |
| Lifecycle Services                   |                                                                                           | Ano       | Ano             |
|                                      | Konfigurovatelné obchodní procesy                                                           | Ano       | Ne              |
| Lokalizace                        |                                                                                           | Ano       | Ano             |
| Výroba                        |                                                                                           | Ano       | Ano             |
| Hlavní plánování a prognóza      |                                                                                           | Ano       | Ano             |
| Mobilní aplikace, pracovní prostory a platformy |                                                                                           | Ano       | Ano             |
| Integrace s Office                   |                                                                                           | Ano       | Ano             |
| Správa organizace          |                                                                                           | Ano       | Ano             |
| Zásobování a zdroje             |                                                                                           | Ano       | Ano             |
|                                      | Funkce punch-out pro externí katalog z nákupní žádanky                                   | Ano       | Žádný              |
|                                      | Sestavy Power BI analýzy nákupu a výdajů                                                  | Ano       | Žádný              |
| Řízení informací o produktech       |                                                                                           | Ano       | Ano             |
| Data základního produktu                  |                                                                                           | Ano       | Ano             |
| Výroba                           |                                                                                           | Ano       | Ano             |
|                                      | Sestavy výkonnosti výroby v Power BI                                                   | Ano       | Žádný              |
| Řízení a účetnictví projektů    |                                                                                           | Ano       | Ano             |
| Prodej.                                |                                                                                           | Ano       | Ano             |
|                                      | Sestavy výkonu prodeje a ziskovosti v Power BI                                      | Ano       | Žádný              |
| Zabezpečení                             |                                                                                           | Ano       | Ano             |
| Správa servisu                   |                                                                                           | Ano       | Ano             |
| Správa dodavatelsko-odběratelského řetězce              |                                                                                           | Ano       | Ano             |
| Správa přepravy            |                                                                                           | Ano       | Ano             |
| Dodavatelská spolupráce                 |                                                                                           | Ano       | Žádný              |
| Řízení skladu                 |                                                                                           | Ano       | Ano             |
|                                      | Mobilní aplikace skladu                                                                      | Ano       | Ano             |
|                                      | Sestavy skladu v Power BI                                                              | Ano       | Žádný              |
| Webový klient                           |                                                                                           | Ano       | Ano             |
|                                      | Záznamník úloh - Uložení nebo načtení záznamu úloh z knihovny BPM                         | Ano       | Ne              |
| Podpora                              |                                                                                           | Ano       | Ano             |
|                                      | Přístup k podpoře prostřednictvím nabídky nápovědy a podporu                                             | Ano       | Ne              |

## <a name="dynamics-365-retail"></a>Dynamics 365 Retail 

Pokud chcete zobrazit seznam maloobchodních možností, které jsou k dispozici v místním nasazení, přečtěte si téma [Možnosti, které jsou k dispozici v místním nasazení maloobchodu](../../../retail/retail-onprem.md).

## <a name="dynamics-365-talent"></a>Dynamics 365 Talent 

| **Oblast**         | **Funkce**         | **Cloud** | **Místní** |
|------------------|---------------------|-----------|-----------------|
| Všechny oblasti Talent | Všechny funkce Talent | Ano       | Ne              |

## <a name="development-and-administration-features"></a>Funkce pro vývoj a správu

| **Oblast**                   | **Funkce**                               | **Cloud** | **Místní** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Sestavení a testování             |                                           | Ano       | Ano             |
| Rozšiřitelnost              |                                           | Ano       | Ano             |
| Monitorování a telemetrie   |                                           | Ano       | Ano             |
| Kompatibilita platformy     |                                           | Ano       | Ano             |
| Servis                  |                                           | Ano       | Ano             |
|                            | Upgrade v různých prostředích                    | Ano       | Žádný              |
| Trace Parser a PerfTimer |                                           | Ano       | Žádný              |
| Upgradovat                    |                                           | Ano       | Ano             |
|                            | Upgradovat                                   | Ano       | Žádný              |
|                            | Upgrade a podpora předchozích verzí | Ano       | Ne              |
| Vývoj Visual Studio  |                                           | Ano       | Ano             |

