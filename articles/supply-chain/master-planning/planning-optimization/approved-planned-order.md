---
title: Prohlížení, správa a schvalování plánovaných objednávek
description: Tento článek poskytuje informace, jak zobrazovat, spravovat a schvalovat plánované objednávky.
author: t-benebo
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a4c3b6c2dd149d3fedf1dc3dc418541961ad1a73
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740951"
---
# <a name="view-manage-and-approve-planned-orders"></a>Prohlížení, správa a schvalování plánovaných objednávek

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje informace, jak zobrazovat, spravovat a schvalovat plánované objednávky.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Prohlížení a správa plánovaných objednávek

Plánované objednávky můžete zobrazit a spravovat na jakékoli stránce seznamu plánovaných objednávek. Přejděte na jedno z následujících míst v závislosti na typu plánovaných objednávek, se kterými chcete pracovat:

- Hlavní plánování \> Pracovní prostory \> Hlavní plánování
- Hlavní plánování \> Hlavní plánování \> Plánované objednávky
- Řízení výroby \> Výrobní zakázky \> Plánované výrobní zakázky
- Zásobování a zdroje \> Nákupní objednávky \> Plánované nákupní objednávky
- Správa zásob \> Příchozí objednávky \> Plánované převody
- Správa zásob \> Odchozí objednávky \> Plánované převody

## <a name="view-and-edit-the-status-of-planned-orders"></a>Zobrazení a úprava stavu plánovaných objednávek

Můžete použít pole **Stav** každé plánované objednávky, abyste mohli sledovat svůj postup nebo změnit způsob zpracování plánované objednávky. K dispozici jsou následující hodnoty **Stav**:

- **Nezpracováno** – Když hlavní plánování vytvoří naplánované objednávky, mají tento stav. Plánované objednávky s tímto stavem budou odstraněny během dalšího běhu plánování.
- **Dokončeno** – Tento stav označuje, že plánovaná objednávka byla dokončena. Když se rozhodnete plánovanou objednávku nepotvrdit, ručně změňte stav na *Dokončeno*. Mějte na paměti, že se stavy *Nezpracováno* a *Dokončeno* systém zachází stejně.
- **Schváleno** – Tento stav označuje, že plánovaná objednávka je schválena k potvrzení. Chcete-li potvrdit plánovanou objednávku, můžete její stav změnit na *Schváleno*. Chcete-li zachovat úpravy, které byly provedeny v plánované objednávce, nebo plánujete-li plánovanou objednávku potvrdit, změňte její stav na *Schváleno*. Plánované objednávky se stavem *Schváleno* jsou považovány za pevné a očekávané dodávky podle hlavního plánování. Proto se během pozdějších hlavních plánovacích běhů nemění ani neodstraní. Pro dosažení tohoto chování, logika plánování zkopíruje plánované objednávky se stavem *Schváleno* z původní verze plánu do nové verze plánu během hlavního plánování. Pamatujte si, že plánované objednávky ve stavu *Schváleno* jsou považovány za dodávky pouze v rámci konkrétního hlavního plánu.

Chcete-li změnit stav jedné plánované objednávky, [otevřete stránku se seznamem plánovaných objednávek](#view-planned-orders), otevřete objednávku a proveďte jeden z těchto kroků:

- Na rychlé kartě **Obecné** změňte hodnotu pole **Stav**.
- V podokně akcí na kartě **Plánovaná objednávka** ve skupině **Zpracovat** vyberte **Změnit stav**.
- V podokně akcí vyberte možnost **Schválit** a označte objednávku jako schválenou.

Chcete-li změnit stav několika plánovaných objednávek současně, [otevřete stránku se seznamem plánovaných objednávek](#view-planned-orders), zaškrtněte políčko u každé objednávky, kterou chcete změnit, a poté proveďte jeden z těchto kroků:

- V podokně akcí na kartě **Plánovaná objednávka** ve skupině **Zpracovat** vyberte **Změnit stav**.
- V podokně akcí vyberte možnost **Schválit** a označte objednávky jako schválené.

## <a name="approve-planned-orders"></a>Schválení plánovaných objednávek

Schválení plánovaných objednávek je volitelným krokem v procesu vytvoření potvrzené objednávky z plánované objednávky.

Následující ilustrace ukazuje, jak můžete použít hodnotu **Stav** hodnota, která je přiřazena každé plánované objednávce k implementaci pracovního toku schválení. Chcete-li implementovat proces schválení, ručně upravte hodnotu **Stav** pro každou plánovanou objednávku, jak je popsáno v předchozí části.

![Tok plánované objednávky.](media/approved-planned-orders-1.png)

> [!TIP]
> Doporučujeme vám schválit všechny upravené plánované objednávky. Jinak budou úpravy při příštím spuštění plánování ignorovány a přepsány.

## <a name="additional-resources"></a>Další prostředky

- [Potvrdit plánované objednávky](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
