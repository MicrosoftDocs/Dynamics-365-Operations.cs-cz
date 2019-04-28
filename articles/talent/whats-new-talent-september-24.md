---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (24. září 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 24526a5884c6c5d30d1f49077b88a24364aa4365
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "856154"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (24. září 2018)

[!include [banner](includes/banner.md)]

**Sestavení 8.1.1015.0**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.

## <a name="currency-added-to-benefits"></a>Měna přidána do zaměstnaneckých výhod

Byly aktualizovány plány zaměstnaneckých výhod, aby zahrnovaly měnu výhody. Toto nové pole je také k dispozici na registrovaných zaměstnaneckých výhodách pracovníka. Toto nové pole je součástí oprávnění zabezpečení Udržovat zaměstnanecké výhody a Zobrazit seznam zaměstnaneckých výhod.

## <a name="update-proration-process--leave-and-absence"></a>Aktualizace poměrného procesu - Pracovní volno a absence

Organizace přidělují volno odlišným způsobem na základě toho, kdy zaměstnanci nastoupili do společnosti a kdy ji opouštějí. U zaměstnanců, kteří opouštějí organizaci, mohou někteří potřebovat ukončit odměny v den ukončení, zatímco jiní se spoléhají na poslední den práce, aby zastavili proces časového rozlišení. Tyto změny umožňují organizacím zvolit, kdy má být ukončena registrace během ukončovacího procesu. Tyto nové možnosti jsou součástí oprávnění pro Ukončit poměr pracovníka a Ukončit poměr pracovníka ze samoobsluhy pro manažery. 

## <a name="other-changes"></a>Další změny

Toto vydání obsahuje několik dalších oprav chyb.

## <a name="known-issue"></a>Známý problém

-   **Problém:** Při přidání nové přílohy k pracovníkovi jsou zašedlá tlačítka **Nová** a **Upravit**. **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**. Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka příloh k dispozici. (Tento problém bude opraven v další aktualizaci Platform Update.)
