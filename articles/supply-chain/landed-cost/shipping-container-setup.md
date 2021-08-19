---
title: Přepravní kontejnery
description: Toto téma popisuje, jak nastavit přepravní kontejnery pro modul nákladů za doručení.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c13102ac1c852aabd25c54e4b51d2f14548290a3d6b90090425aa37e5bde110b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727887"
---
# <a name="shipping-container-setup"></a>Nastavení přepravního kontejneru

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak nastavit přepravní kontejnery pro modul **Náklady za doručení**.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Nastavení typů přepravních kontejnerů

Typy přepravních kontejnerů definují typy přepravních kontejnerů, které jsou k dispozici pro použití během přepravy a plavby.

Chcete-li pracovat s typy přepravních kontejnerů, přejděte na **Náklady na doručení \> Nastavení kontejnerů \> Typy přepravních kontejnerů**. Zde můžete prohlížet, přidávat a odebírat záznamy o vašich typech kontejnerů. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Typ přepravního kontejneru | Zadejte jedinečný identifikační název/číslo přepravního kontejneru. |
| popis | Zadejte popis skupiny typů nákladů přepravních kontejnerů. |
| Objem | Zadejte maximální povolený objem v přepravních kontejnerech tohoto typu. |
| Váha | Zadejte maximální povolenou hmotnost v přepravních kontejnerech tohoto typu. |
| Vratný | Určete, zda lze přepravní kontejnery tohoto typu vrátit prodejci po jejich použití během plavby. Pokud je tato možnost nastavena na *Ano*, mohou se na vrácení přepravních kontejnerů tohoto typu do přístavu původu vztahovat další náklady. |

## <a name="set-up-shipping-containers"></a>Nastavení přepravních kontejnerů

Záznamy přepravních kontejnerů slouží k identifikaci každého kontejneru, který používáte během plavby. Když vytvoříte cestu, můžete pro ni vybrat konkrétní kontejner v seznamu všech záznamů přepravního kontejneru, které jste zde definovali. Tato funkce je obzvláště užitečná, pokud má vaše společnost vlastní přepravní kontejnery.

U přepravních kontejnerů, které budou použity pouze jednou, nemusíte zadávat čísla přepravních kontejnerů. Místo toho můžete při vytváření cesty přidat číslo přepravního kontejneru.

Záznamy přepravního kontejneru se používají pouze v nákladech za doručení. Nejsou k dispozici ve standardním modulu **Správa přepravy** (TMS).

Chcete-li pracovat s přepravními kontejnery, přejděte na **Náklady na doručení \> Nastavení kontejnerů \> Přepravní kontejnery**. Zde můžete prohlížet, přidávat a odebírat záznamy o vašich přepravních kontejnerech. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Přepravní kontejner | Zadejte jedinečný identifikační název/číslo přepravního kontejneru. |
| Typ přepravního kontejneru | Vyberte typ přepravního kontejneru. Další informace naleznete v části [Nastavení typů přepravních kontejnerů](#shipping-container-types) dříve v tomto tématu. |

> [!NOTE]
> - Nastavení přepravního kontejneru je volitelné. Obvykle jej použijete, pouze pokud má vaše společnost vlastní přepravní kontejnery nebo často znovu používá stejné přepravní kontejnery.
> - Pro čísla přepravních kontejnerů se nepočítají žádné kontrolní číslice.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Nastavení typů jednotky

Typy jednotek vytvářejí další seskupení a způsoby identifikace přepravních kontejnerů. Typ jednotky se obvykle používá k identifikaci typu kontejneru, do kterého je zboží zabaleno, jako jsou palety nebo sudy. Při nastavování typu kontejneru na stránce **všechny přepravní kontejnery** můžete vybrat typ jednotky.

Typy jednotek se používají pouze v ceně nákladů za doručení. Nejsou k dispozici v TMS.

Chcete-li pracovat s typy jednotky, přejděte na **Náklady na doručení \> Nastavení kontejnerů \> Typy jednotky**. Zde můžete prohlížet, přidávat a odebírat záznamy o vašich typech jednotky. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Typ jednotky | Zadejte jedinečný identifikační název/číslo typu jednotky. |
| popis | Zadejte popis typu jednotky. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Nastavení typů chlazení

Typy chlazení nastavují další metody seskupení a identifikace pro dopravní kontejnery (obvykle chlazené kontejnery). Při nastavování typu kontejneru na stránce **všechny přepravní kontejnery** můžete vybrat typ chlazení.

Chcete-li pracovat s typy chlazení, přejděte na **Náklady na doručení \> Nastavení kontejnerů \> Typy chlazení**. Zde můžete prohlížet, přidávat a odebírat záznamy o vašich typech chlazení. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Typ chlazení | Zadejte jedinečný identifikační název/číslo typu chlazení. |
| popis | Zadejte stručný popis typu chlazení. |
