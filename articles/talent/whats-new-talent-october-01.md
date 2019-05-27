---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (1. října 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 15b5fd7095a62aa9b7b79ebfcada667959b756aa
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517550"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (1. října 2018)

[!include [banner](includes/banner.md)]

**Sestavení 8.1.1035.0**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.

## <a name="turn-off-electronic-payment-validation"></a>Vypnutí ověření elektronické platby

K ověření informací o elektronické platbě dochází, pokud nastavíte úhrady pro přímý vklad buď prostřednictvím pracovního prostoru **Samoobsluha pro zaměstnance** nebo přímo na formuláři zaměstnance. Tato volba poskytuje možnost odebrat takové ověření, pokud nevyžadujete kontroly ověření pro částky a hodnoty zůstatku. Tato funkce je užitečná v případě, kdy provádíte integraci s externím mzdovým systémem, který má jiné požadavky.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Samoobsluha pro manažery - Přidání cílů pro členy týmu prostřednictvím dlaždice Cíle výkonnosti týmu

Před touto verzí manažeři mohou přidat cíle svým zaměstnancům jednotlivě prostřednictvím cílů výkonnosti přidružených ke každému zaměstnanci. Od této aktualizace mají manažeři přístup k dlaždici **Cíle výkonnosti týmu** a mohou vytvořit nové cíle volbou jakéhokoliv ze svých přímých podřízených.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Samoobsluha pro manažery - Přidání kontrol pro členy týmu prostřednictvím dlaždice Kontroly výkonnosti týmu

Před touto verzí manažeři mohou přidat kontroly svým zaměstnancům jednotlivě prostřednictvím kontrol výkonnosti přidružených ke každému zaměstnanci. Od této aktualizace mají manažeři přístup k dlaždici **Kontroly výkonnosti týmu** a mohou vytvořit nové kontroly volbou jakéhokoliv ze svých přímých podřízených.

## <a name="configure-proration-options-by-leave-plan"></a>Konfigurace poměrných možností podle plánu pracovního volna

Organizace přidělují volno odlišným způsobem na základě toho, kdy zaměstnanci nastoupili do společnosti a kdy ji opouštějí. U některých organizací dostanou zaměstnanci v datum svého nástupu své úplné přidělení, zatímco jiné organizace přidělí pouze poměrnou část. Nové možnosti jsou k dispozici v této verzi k výběru způsobu poměrného rozdělení volna a časovému rozlišení pro nastupující a odcházející zaměstnance v organizaci. Možnosti zahrnují: Poměrné, Úplné časové rozlišení a Bez časového rozlišení.

## <a name="other-changes"></a>Další změny

-   Entita zaměstnance byla aktualizována - Dlaždici **Osobní** lze nyní aktualizovat pomocí doplňku aplikace Excel / správy dat.

-   Změna zabezpečení pro povolení odstranění tlačítek **Odstranit** a **Deaktivovat** v samoobsluze zaměstnance pro informace o platbě.

## <a name="known-issue"></a>Známý problém

-   **Problém:** Při přidání nové přílohy k pracovníkovi jsou zašedlá tlačítka **Nová** a **Upravit**. **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**. Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka **Přílohy** k dispozici. (Tento problém bude opraven v další aktualizaci Platform Update.)
