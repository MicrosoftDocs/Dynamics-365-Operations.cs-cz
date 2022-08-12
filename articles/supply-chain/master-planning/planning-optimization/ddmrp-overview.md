---
title: Plánování materiálových požadavků řízené poptávkou (DDMRP) – přehled
description: Tento článek poskytuje informace o plánování materiálových požadavků řízené poptávkou (DDMRP), metodologii plánování, která je založena na oddělení nabídky a poptávky.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: d894b83afe822e013c0c4375e5cfe5e7e8ac8d1d
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186657"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Plánování materiálových požadavků řízené poptávkou (DDMRP) – přehled

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Společnosti po léta používají plánování materiálových požadavků (MRP) jako systém pro výpočet materiálů a komponentů, které jsou nutné k výrobě produktu. Dodavatelské řetězce se však nyní změnily. Díly mají delší dodací lhůty, protože stále častěji pocházejí ze zámoří. Mnoho společností proto hlásilo, že dochází k vyprodání zásob nebo přeplnění zásob, protože nevědí, kolik zásob mají naskladnit. Dochází také k většímu kolísání trhu (někdy nepřesně předpovídané) a zákazníci požadují produkty v krátké dodací lhůtě. Po celém světě proto existuje nedostatek v dodavatelském řetězce. Nástroje MRP navíc často dávají plánovačům k dispozici tisíce akcí. Proto je těžké vědět, na co se zaměřit. Často je řešením mnoha z těchto problémů přechod na plánování materiálových požadavků řízené poptávkou (DDMRP).

DDMRP je metodika plánování, která je založena na oddělení nabídky a poptávky. Tohoto oddělení se dosáhne nastavením položek bodů oddělení. U těchto položek jsou udržovány vyrovnávací zásoby, aby bylo zajištěno, že bude udržováno správné množství zásob. Oddělení nabídky a poptávky pomáhá předcházet „efektu biče“, protože variabilita neprochází řetězcem. (*Efekt biče* označuje, jak malé výkyvy v poptávce na maloobchodní úrovni mohou způsobit progresivně větší výkyvy v poptávce na úrovni velkoobchodu, distributora, výrobce a dodavatele surovin.) Každá rezerva je určena k pokrytí průměrného využití dílu a lze ji také upravit k pokrytí špiček poptávky.

DDMRP se osvědčilo jako cenná metodologie plánování pro proměnná prostředí, kde jsou doby tolerance zákazníků kratší než kumulativní dodací lhůty.

## <a name="the-five-components-of-ddmrp"></a>Pět složek DDMRP

DDMRP má pět po sobě jdoucích komponent (kroků). První tři komponenty v podstatě definují počáteční a vyvíjející se konfiguraci poptávkového modelu plánování požadavků na materiál. Poslední dvě složky definují každodenní fungování metodiky.

1. **[Strategické umístění zásob](ddmrp-inventory-positioning.md)** – Identifikujte body oddělení v síti dodavatelského řetězce. Body oddělení jsou konkrétní body vašeho dodavatelského řetězce, kam umístíte vyrovnávací zásoby, které budete monitorovat a doplňovat.
2. **[Profily a úrovně vyrovnávacích zásob](ddmrp-buffer-profile-and-levels.md)** – U každého oddělovacího bodu identifikujte velikosti vyrovnávacích zásob (minimální množství, maximální množství a bod objednání) a objednací množství.
3. **[Dynamická vyrovnání vyrovnávacích zásob](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – Upravte úrovně vyrovnávacích zásob na základě měnících se provozních parametrů nebo plánovaných budoucích událostí.
4. **[Plánování řízené poptávkou](ddmrp-planning.md)** – Generujte objednávky dodávek podle potřeby. Tyto objednávky dodávek zahrnují výrobní objednávky, nákupní objednávky a objednávky na převod skladu
5. **[Vysoce spolupracující a viditelné provedení](ddmrp-visual-and-collaborative-execution.md)** – Spusťte objednávky dodávek pomocí vizualizace.

DDMRP obvykle používají výrobci, kteří mají víceúrovňový kusovník (BOM). Lze jej však aplikovat i na distribuční a maloobchodní sítě.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP v Dynamics 365 Supply Chain Management

DDMRP je součástí Microsoft Dynamics 365 Supply Chain Management a nevyžaduje žádné další licenční poplatky. V Supply Chain Management byla přidána funkce DDMRP ke stávajícímu modulu **Hlavní plánování**. Vyžaduje však, abyste používali doplněk Optimalizace plánování. 

DDMRP je integrován se stávajícími nastaveními plánování v Supply Chain Management a používá se společně s těmito nastaveními k dosažení správné konfigurace plánování pro vaši firmu. Řídí se novým kódem pokrytí, který je zcela odlišný od období, min/max, požadavku a tak dále. Nejedná se o nový modul a nenahrazuje stávající funkce plánování. Poskytuje vám však více funkcí.
