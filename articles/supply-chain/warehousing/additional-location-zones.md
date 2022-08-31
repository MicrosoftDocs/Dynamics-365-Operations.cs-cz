---
title: Další zóny skladového místa
description: Tento článek poskytuje přehled nových zón skladového místa, jež byly přidány do systému Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336478"
---
# <a name="additional-location-zones"></a>Další zóny skladového místa

[!include [banner](../includes/banner.md)]

V programu Microsoft Dynamics 365 Supply Chain Management jsou při zadávání nové zóny k dispozici tři pole. Vedoucí skladu je mohou použít k definování dalších skladových organizací nebo rozvržení. Pole nové zóny lze nastavit buď ručně nebo pomocí průvodce **Nastavení skladového místa**. Lze je použít v jakémkoli dotazu nebo při filtrování využívajícím tabulku Skladová místa.

K použití polí zón není nutné žádné další nastavení.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Zapnutí či vypnutí funkce Další zóna skladového místa

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.25 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.29, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Další zóna skladového místa* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="use-location-zones"></a>Používání zón skladového místa

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Průvodce nastavením skladového místa**.
2. Nastavte následující hodnoty:

    - V poli **Sklad** zvolte _62_.
    - V poli **ID zóny** vyberte hodnotu _FLOOR_.
    - V poli **Další zóna 1** vyberte hodnotu _VYSKLZÓNA1_.
    - V poli **Další zóna 2** vyberte hodnotu _WEBSHOP1_.
    - V poli **ID profilu skladového místa** vyberte hodnotu _FLOOR_.

3. Vyberte řádek **Podlaha**.
4. Do pole **Od čísla** zadejte hodnotu _1_. Do pole **Do čísla** zadejte hodnotu _3_.
5. Vyberte řádek **Ulička**.
6. Do pole **Od čísla** zadejte hodnotu _1_. Do pole **Do čísla** zadejte hodnotu _5_.
7. Vyberte **Vytvořit**.
8. Obdržíte zprávy uvádějící, že byla přidána nová skladová místa. Tlačítkem **Zobrazit zprávy** tyto zprávy zobrazíte.
9. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění**. Nová skladová místa se zobrazí v seznamu a jsou k dispozici všechna pole zóny (tj. pole existující zóny i pole nové další zóny).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]