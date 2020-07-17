---
title: Další zóny skladového místa
description: Toto téma poskytuje přehled nových zón skladového místa, jež byly přidány do systému Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9727187ad555f9e3d09beed3f3447a22c29ed22a
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530160"
---
# <a name="additional-location-zones"></a>Další zóny skladového místa

[!include [banner](../includes/banner.md)]

V programu Microsoft Dynamics 365 Supply Chain Management jsou při zadávání nové zóny k dispozici tři pole. Vedoucí skladu je mohou použít k definování dalších skladových organizací nebo rozvržení. Pole nové zóny lze nastavit buď ručně nebo pomocí průvodce **Nastavení skladového místa**. Lze je použít v jakémkoli dotazu nebo při filtrování využívajícím tabulku Skladová místa.

K použití polí zón není nutné žádné další nastavení.

## <a name="turn-on-the-additional-location-zone-feature"></a>Zapnutí funkce Další zóna skladového místa

Než můžete použít funkci *Další zóna skladového místa*, musíte ji v systému zapnout. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Další zóna skladového místa*

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
