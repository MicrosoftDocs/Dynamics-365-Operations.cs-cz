---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (16. října 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460540"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (16. října 2018)

**Sestavení 8.1.1067**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.

## <a name="allow-managers-to-update-time-off-requests"></a>Povolení manažerům aktualizovat požadavky na volno

Požadavky na volno zaměstnance je třeba někdy aktualizovat po jejich schválení prostřednictvím workflow. V mnoha případech provádí manažeři tyto aktualizace jménem zaměstnance. Tato nová funkce umožňuje manažerům aktualizovat požadavky na volno nebo zrušení volna jménem zaměstnanců. Tato funkce je řízena parametrem **Práce jménem**, který lze nastavit na stránce **Parametry lidských zdrojů**. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>Povolení pro oddělení lidských zdrojů aktualizovat požadavky na volno

Podobně jako u výše uvedené funkce může být třeba, aby požadavky na volno aktualizovalo oddělení lidských zdrojů, poté, co byly schváleny prostřednictvím workflow. Tato funkce umožňuje uživatelům HR aktualizovat požadavky na volno. Možnost se povoluje v pracovním prostoru **Lidé** na stránce **Pracovník** pomocí nové možnosti s názvem **Zobrazení volna**. Na těchto stránkách mohou HR uživatelé zobrazit žádosti a aktualizovat transakce volna podobným způsobem, jako mohou tyo akce provádět manažeři.

Funkční oprávnění zabezpečení, které řídí přístup k této funkci je:
- Funkční oprávnění: Udržovat procesy pracovního volna a absence specifické pro pracovníka.
- Oprávnění: Udržovat požadavky na pracovní volno a absenci pro všechny pracovníky.

## <a name="other-changes"></a>Další změny
V této verzi byly provedeny následující aktualizace:
- Změny akcí náboru pracovníka, aby již nezůstávaly zadržení ve stavu **Workflow dokončen**.
- Záznam zaměstnání lze nyní vytvořit bez počátečního data zaměstnání.
- Datum registrace Dynamics 365 Talent pro kurz zobrazený v samoobsluze pro zaměstnance nyní uplatňuje časový posun pro datum.
- Soubory aplikace Excel lze importovat vícekrát bez chyb pomocí **Entity zaměstnance**.

## <a name="known-issue"></a>Známý problém

- **Problém**: Při přidání nové přílohy k pracovníkovi jsou tlačítka **Nová** a **Upravit** zobrazena šedě. 
- **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**. Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici. (Tento problém bude opraven v další aktualizaci Platform Update.)
