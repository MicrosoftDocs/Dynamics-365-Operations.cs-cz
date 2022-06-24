---
title: Další zóny skladového místa
description: Tento článek poskytuje přehled nových zón skladového místa, jež byly přidány do systému Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 07/01/2020
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
ms.openlocfilehash: c20225cfb3c44fff955d0ad4e96c7fecf0ddf715
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900644"
---
# <a name="additional-location-zones"></a>Další zóny skladového místa

[!include [banner](../includes/banner.md)]

V programu Microsoft Dynamics 365 Supply Chain Management jsou při zadávání nové zóny k dispozici tři pole. Vedoucí skladu je mohou použít k definování dalších skladových organizací nebo rozvržení. Pole nové zóny lze nastavit buď ručně nebo pomocí průvodce **Nastavení skladového místa**. Lze je použít v jakémkoli dotazu nebo při filtrování využívajícím tabulku Skladová místa.

K použití polí zón není nutné žádné další nastavení.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Zapnutí či vypnutí funkce Další zóna skladového místa

Od verze Supply Chain Management 10.0.25 je tato funkce ve výchozím nastavení zapnuta. Správci mohou tuto funkci zapnout nebo vypnout vyhledáním funkce *Další zóna skladového místa* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

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