---
title: Srovnání funkcí cloudu a on-premises
description: Toto téma popisuje funkce, které jsou podporovány v cloudu a instalaci on-premises.
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
ms.openlocfilehash: e2126983fef2b59af5c8082a6495f808afeb5f9c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744044"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Srovnání funkcí cloudu a on-premises

[!include [banner](../includes/banner.md)]

V tomto tématu je uvedeno porovnání funkcí dostupných v cloudu a místně pro následující aplikace:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Jsou zde také [uvedeny informace o funkcích vývoje a správy](cloud-prem-comparison.md#development-and-administration-features).

Následující tabulka uvádí oblasti aplikace. Podpora cloudu a instalace on-premise je uvedena pro funkci jako celek. Tam, kde se konkrétní funkce liší od celkové oblasti, jsou funkce uvedeny na odděleném řádku ve sloupci Funkce.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Oblast**             | **Funkce**                | **Cloud** | **Místní** |
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
|                                      | ER: Používá místní systém souborů jako úložiště konfigurací ER přístupné z úložišť ER | Žádný        | Ano             |
|                                      | Integrace s PowerBI.com                                                              | Ano       | Žádný              |
|                                      | Integrace s PowerBI Desktop                                                          | Žádný        | Ano             |
|                                      | Analytické pracovní prostory                                                                     | Ano       | Žádný              |
|                                      | Inteligentní obchodní proces: doporučení                                             | Ano       | Žádný              |
|                                      | Vytváření sestav Power BI s OData pomocí pracovní plochy Power BI nebo nástroje PowerQuery aplikace Excel    | Ano       | Žádný              |
|                                      | Služba SQL Server Reporting Services podporuje rozšiřování                                 | Ano       | Ano             |
|                                      | Telemetrie je přenesena do cloudu                                                   | Ano       | Žádný              |
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
| Správa majetku                     |                                                                                           | Ano       | Žádný              |
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
|                                      | Povolení exportu přírůstkových aktualizací datových entit                                 | Ano       | Ano             |
|                                      | Integrace dat                                                                         | Ano       | Ano             |
| Správa dokumentů                  |                                                                                           | Ano       | Ano             |
| Nápověda                                 |                                                                                           | Ano       | Ne              |
| Intelligence                         |                                                                                           | Ano       | Ano             |
|                                      | Elektronické výkaznictví (EV)                                                                 | Ano       | Ano             |
|                                      | ER: Integrace s LCS                                                                  | Ano       | Ne              |
|                                      | ER: Integrace se službou SharePoint                                                           | Ano       | Ne              |
|                                      | ER: Integrace se službou Regulatory Configuration Services (RCS)                              | Ano       | Ne              |
|                                      | ER: Používá místní systém souborů jako úložiště konfigurací ER přístupné z úložišť ER | Žádný        | Ano             |
|                                      | Integrace s PowerBI.com                                                              | Ano       | Žádný              |
|                                      | Integrace s PowerBI Desktop                                                          | Žádný        | Ano             |
|                                      | Analytické pracovní prostory                                                                     | Ano       | Žádný              |
|                                      | Inteligentní obchodní proces: doporučení                                             | Ano       | Žádný              |
|                                      | Vytváření sestav Power BI s OData pomocí pracovní plochy Power BI nebo nástroje PowerQuery aplikace Excel    | Ano       | Žádný              |
|                                      | Služba SQL Server Reporting Services podporuje rozšiřování                                 | Ano       | Ano             |
|                                      | Telemetrie je přenesena do cloudu                                                   | Ano       | Žádný              |
| Řízení zásob                 |                                                                                           | Ano       | Ano             |
| Lifecycle Services                   |                                                                                           | Ano       | Ano             |
|                                      | Konfigurovatelné obchodní procesy                                                           | Ano       | Ne              |
| Lokalizace                        |                                                                                           | Ano       | Ano             |
| Výroba                        |                                                                                           | Ano       | Ano             |
| Hlavní plánování a prognóza      |                                                                                           | Ano       | Ano             |
| Optimalizace plánování                |                                                                                           | Ano       | Žádný              |
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

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Pokud chcete zobrazit seznam možností, které jsou k dispozici v místním nasazení, přečtěte si téma [Možnosti Commerce, které jsou k dispozici v místním nasazení](../../../retail/retail-onprem.md).

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
|                            | Upgrade v různých prostředích                    | Ano       | Žádný              |
| Trace Parser               |                                           | Ano       | Ano             |
| PerfTimer                  |                                           | Ano       | Ano\*           |
| Upgrade                    |                                           | Ano       | Ano             |
|                            | Upgrade                                   | Ano       | Žádný              |
|                            | Upgrade a podpora předchozích verzí | Ano       | Žádný              |
| Vývoj Visual Studio  |                                           | Ano       | Ano             |

\* V místních prostředích zobrazuje PerfTimer pouze výsledky pro klienta.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]