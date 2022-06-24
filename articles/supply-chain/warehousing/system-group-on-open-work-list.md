---
title: Systémové seskupení na otevřeném seznamu úkolů
description: Tento článek popisuje, jak filtrovat seznam otevřené práce u mobilního zařízení.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42e5862392cff57886c36bcbe138e13a8ce7ef23
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849090"
---
# <a name="system-grouping-on-an-open-work-list"></a>Systémové seskupení na otevřeném seznamu úkolů

[!include [banner](../includes/banner.md)]

Pomocí pole seskupení systému můžete filtrovat seznam otevřené práci bez nutnosti upravovat položku nabídky mobilního zařízení.
V příslušných případech funguje seskupování systému k filtrování pracovního seznamu u jednoho pole záhlaví práce. Systémové seskupení nelze použít k filtrování na úrovni polí řádku.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Nastavení systémového seskupení v otevřeném seznamu úkolů
Tyto kroky slouží k nastavení systémového seskupení v otevřeném seznamu úkolů.

-   Z položky nabídky mobilního zařízení vyberte **Režim: Nepřímý** a **Kód aktivity: Zobrazit otevřený pracovní seznam**. K dispozici jsou následující možnosti. Tyto možnosti jsou požadovány pro systémové seskupení v otevřeném pracovním seznamu. 

|        Parametr         |                                                                                                                                                                                                                                                                         popis                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Povolit seskupení systému |                                                                                                                                                                                                                                                 Umožňuje seskupení systému pro vybranou položku pracovního seznamu.                                                                                                                                                                                                                                                  |
| Pole systémového seskupení | K dispozici pouze v případě, že je možnost <strong>Povolit systémovou práci</strong> nastavena na hodnotu <strong>Ano</strong>. Vyberte pole, které určuje způsob seskupení práce pro pracovníky. Pokud například vyberete pole <strong>ShipmentId</strong>, pracovník naskenuje ID dodávky pro seskupení práce výdeje. Všechna práce pro dodávku bude přiřazena pracovníkovi. Toto pole vyžaduje, abyste vytvořili položku nabídky pro stávající práci, která je seskupena podle systému. Pole <strong>Popisek systémového seskupení</strong> použijte k informování pracovníka, co kontrolovat. |
| Popisek systémového seskupení |                       K dispozici pouze v případě, že je možnost <strong>Povolit systémovou práci</strong> nastavena na hodnotu <strong>Ano</strong>. Zadejte informace pro pracovníka o tom, co kontrolovat při seskupení práce vyskladnění v aplikaci . Používáte-li například pole <strong>ShipmentId</strong> pro seskupení práce výdeje podle dodávky, měli byste do pole zadat ID dodávky. Toto pole vyžaduje, abyste vytvořili položku nabídky pro stávající práci, která je seskupena podle systému. Je nutné zaškrtnout pole definující seskupení v poli <strong>systémové seskupení</strong>.                       |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]