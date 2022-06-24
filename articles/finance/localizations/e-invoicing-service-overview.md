---
title: Přehled elektronické fakturace
description: Tento článek poskytuje přehled elektronické fakturace v Microsoft Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 4ce5776216855fc664b9beba68036d41920ae602
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861289"
---
# <a name="electronic-invoicing-overview"></a>Přehled elektronické fakturace

[!include [banner](../includes/banner.md)]

Elektronická fakturace pro Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management je hyperškálovatelná multiklientová služba, která umožňuje konfigurovatelné zpracování elektronických faktur a konfigurovatelnou elektronickou výměnu dokumentů. Pravidla zpracování a integrace jsou plně konfigurovatelná a logika je spuštěna mimo Finance a Supply Chain Management. Služba je zaměřena především na zpracování elektronických fakturačních dokladů ve scénářích business-to-government. Lze jej však uživatelsky nakonfigurovat pro jiné účely, jako jsou scénáře business-to-business pro různé typy dokumentů.

Elektronická fakturace vám pomůže dosáhnout následujících cílů:

- Rychlé a snadné přijetí požadavků konkrétních zemí / regionů
- Standardizované implementace řešení elektronické fakturace
- Vylepšená sledovatelnost historie dokumentů
- Kratší implementační cyklus
- Snížené celkové náklady na vlastnictví (TCO)
- Snadno nastavitelné konfigurace, které nevyžadují změny kódu
- Zjednodušené konfigurační balení
- Integrovaný export, import a integrace a snadná rozšiřitelnost při zpracování dokumentů elektronických faktur
- Snadné opětovné použití stejné konfigurace exportu, importu a integrace napříč společnostmi

## <a name="service-availability"></a>Dostupnost služby

V současné době je pro zákazníky Finance a Supply Chain Management k dispozici funkce elektronické fakturace. Další informace naleznete v licenčních podmínkách pro vaši aplikaci.

Protože funkce, která řeší požadavky specifické pro zemi / region, mohou být v různých fázích vydání omezené, měli byste vždy zkontrolovat nejaktuálnější dokumentaci, která zdůrazňuje pokrytí a rozsah podporovaných řešení pro konkrétní zemi / region.

Elektronická fakturace je nasazena v následujících geografických oblastech Azure:

- Spojené státy
- Evropa
- Asie

> [!NOTE]
> Elektronická fakturace nepodporuje místní nasazení.

## <a name="feature-highlights"></a>Zvýrazněné funkce

- Dodávaná integrace s Finance a Supply Chain Management
- Konzistentní uživatelské prostředí pro konfiguraci a sledování procesu elektronické faktury pro všechny země a regiony
- Rychlejší, snazší a levnější přijetí řešení elektronické fakturace v nových zemích nebo regionech
- Konfigurace služby prostřednictvím nastavení funkcí Regulatory Configuration Service (RCS) a globalizace
- Transformace obchodních dat do více formátů elektronických faktur (XML, JavaScript Object Notation \[JSON\], TXT a hodnoty oddělené čárkami \[CSV\]) pomocí konfigurací definovaných v RCS:

    - Formáty elektronických sestav (ER), které jsou k dispozici pro země a oblasti, kde není k dispozici konfigurovatelnost pro transformaci e-faktur

- Konfigurovatelné odesílání elektronických faktur externím webovým službám, včetně zpracování certifikace prostřednictvím digitálních podpisů:

    - Integrovaná, snadno rozšiřitelná a konfigurovatelná integrace s dalším obsahem pro několik zemí a oblastí

- Zpracování odpovědí z webových služeb, včetně konfigurovatelného zpracování zpráv o výjimkách
- Podpora elektronických podpisů (například pomocí elektronických podpisů, které používají podpisový algoritmus XMLDSig)
- Schopnost odesílat dokumenty na e-maily a ukládat je v SharePoint
- Hromadné zpracování zpráv elektronické faktury
- Konfigurovatelná transformace příchozích dokumentů a zpracování těchto dokumentů ve Finance a Supply Chain Management
- Schopnost přijímat příchozí dokumenty z kanálů, jako je e-mail a SharePoint

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Aktivace a používání elektronické fakturace může vyžadovat odesílání omezeného objemu dat. Tato data zahrnují identifikační daňové identifikační číslo organizace. Tato data budou předána agenturám třetích stran oprávněným daňovými úřady pro účely zasílání elektronických faktur v předdefinovaných formátech požadovaných pro integraci s webovými službami těchto vlád. Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132). Další informace najdete v sekci Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země/oblasti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
