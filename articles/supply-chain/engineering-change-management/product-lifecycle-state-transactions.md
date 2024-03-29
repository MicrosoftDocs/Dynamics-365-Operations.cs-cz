---
title: Stavy životního cyklu produktu a transakce
description: Tento článek vysvětluje, jak můžete ovládat, které transakce jsou povoleny pro každý stav životního cyklu, když technický produkt prochází svým životním cyklem.
author: t-benebo
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd9155f799c66e8297b93d8ffbeeced1acd14220
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867949"
---
# <a name="product-lifecycle-states-and-transactions"></a>Stavy životního cyklu produktu a transakce

[!include [banner](../includes/banner.md)]

Protože technický produkt prochází svým životním cyklem, je důležité, abyste mohli kontrolovat, které transakce jsou povoleny pro každý stav životního cyklu. Například produkty, které ještě nejsou ve vyspělém stavu, by neměly být uvedeny na prodejní objednávce. Alternativně, pokud produkt dosáhne svého stavu konce životnosti, možná budete chtít kontrolovat přírůstek tohoto produktu.

U technického produktu jsou změny stavu životního cyklu spojeny s technickými verzemi produktu. Stav životního cyklu produktu lze proto také připojit k jeho technickým verzím. Když je stav životního cyklu produktu připojen k technické verzi, můžete pomocí stavu životního cyklu určit, které transakce jsou pro technickou verzi povoleny.

## <a name="create-and-manage-product-lifecycle-states"></a>Vytvoření a správa stavů životního cyklu produktu

Chcete-li pracovat se stavy životního cyklu produktu, přejděte na **Správa technických změn \> Nastavení \> Stav životního cyklu produktu**. Potom proveďte jeden z následujících kroků.

- Chcete-li vytvořit nový stav životního cyklu, vyberte **Nový** v podokně akcí a poté nastavte pole, jak je popsáno v následujících podsekcích.
- Chcete-li upravit existující stav životního cyklu, vyberte ho v podokně seznamu, zvolte **Upravit** v podokně akcí a poté nastavte pole, jak je popsáno v následujících podsekcích.
- Chcete-li odstranit existující stav životního cyklu, vyberte ho v podokně seznamu a poté v podokně akcí vyberte **Odstranit**.

> [!NOTE]
> Technické produkty používají stejné stavy životního cyklu produktu jako standardní (netechnické) produkty. Můžete také otevřít stránku **Stav životního cyklu produktu**, která je popsána v tomto článku, přechodem na **Správa informací o produktu \> Nastavit \> Stav životního cyklu produktu**. Další informace o stavech životního cyklu produktu pro technické produkty i pro standardní produkty najdete v tématu [Přehled stavu životního cyklu produktu](../pim/product-lifecycle.md).

### <a name="header"></a>Záhlaví

V záhlaví stavu životního cyklu produktu nastavte následující pole.

| Pole | popis |
|---|---|
| Kraj | Zadejte název stavu životního cyklu produktu. |
| popis | Zadejte popis stavu životního cyklu produktu. |

### <a name="general-fasttab"></a>Záložka s náhledem Obecné

Na záložce s náhledem **Obecné** nastavte následující pole.

| Pole | popis |
|---|---|
| Výchozí hodnota při uvolnění právnické osobě | U standardních produktů nastavte tuto možnost na *Ano* pokud by měl být tento stav životního cyklu ve výchozím nastavení použit na všechny produkty při jejich prvním uvolnění. Nastavte tuto možnost na *Ne*, pokud bude tento stav životního cyklu později použit ručně.<p>Toto nastavení se nevztahuje na technické produkty. Stav životního cyklu verze technického produktu po vytvoření v technické společnosti je uveden v kategorii technické změny. Když je produkt uvolněn do provozní společnosti, zkopíruje se stav životního cyklu produktu. Jinými slovy, když je technický produkt uvolněn do provozní společnosti, má stejný stav životního cyklu, jaký měl v technické společnosti. Stav životního cyklu lze v provozní společnosti přepsat.</p> |
| Je aktivní pro plánování | Tuto možnost nastavte na *Ano* pro zahrnutí produktů, které jsou v tomto stavu životního cyklu, do výpočtů na úrovních hlavního plánování a kusovníku (BOM). Nastavte tuto možnost na *Ne* pro vyloučení produktů, které jsou v tomto stavu životního cyklu, z výpočtů. |

### <a name="enabled-business-processes-fasttab"></a>Záložka s náhledem Povolené obchodní procesy

Použijte záložku s náhledem **Povolené obchodní procesy** ke kontrole, které z dostupných podnikových procesů lze použít s produkty v aktuálním stavu životního cyklu. Procesy uvedené na této záložce s náhledem jsou automaticky nalezeny následujícím způsobem:

- Při prvním uložení nového stavu životního cyklu stránka načte obchodní procesy, které jsou aktuálně k dispozici.
- Pokud do svého systému přidáte nové obchodní procesy, můžete seznam aktualizovat na záložce s náhledem **Povolené obchodní procesy** pro existující stav životního cyklu výběrem **Kontrola aktualizací** v podokně akcí.

Následující pole jsou k dispozici pro každý proces, který je uveden na záložce s náhledem **Povolené obchodní procesy**.

| Pole | popis |
|---|---|
| Zpracovat | Toto pole jen pro čtení zobrazuje název existujícího obchodního procesu. |
| Oblast procesu | Toto pole jen pro čtení zobrazuje název oblasti existujícího procesu. |
| Zásada | Vyberte jednu z následujících hodnot, abyste určili, zda a jak bude povolen aktuální proces pro produkty, které jsou v tomto stavu životního cyklu:<ul><li>**Povoleno** - Obchodní proces je povolen.</li><li>**Blokováno** - Proces není povolen. Pokud se uživatel pokusí použít proces na produktu, který je v tomto stavu životního cyklu, systém pokus zablokuje a místo toho zobrazí chybu. Můžete například blokovat nákup produktů na konci životnosti.</li><li>**Povoleno s varováním** - Proces je povolen, ale zobrazí se varování. Můžete například chtít nasadit prototypový produkt do výrobní zakázky vytvořené oddělením výzkumu a vývoje. Ostatní oddělení by si však měla být vědoma toho, že by produkt ještě neměla vyrábět.</li></ul> |

Pokud přidáváte další pravidla stavu životního cyklu jako přizpůsobení, můžete tato pravidla zobrazit v uživatelském rozhraní výběrem možnosti **Obnovit procesy** v horním panelu. Tlačítko **Obnovit procesy** je k dispozici pouze správcům.

## <a name="lifecycle-states-for-released-products-and-product-variants"></a>Stavy životního cyklu pro vydané produkty a varianty produktů

U produktu, který má varianty (hlavní a varianty), bude mít produkt (hlavní) stav životního cyklu a každá z variant může mít také jiný stav životního cyklu.

U konkrétních procesů, pokud je blokována buď varianta, nebo produkt, bude blokován také proces. Konkrétně pro určení, zda je proces blokován, provede systém následující kontroly:

- Produkty kontrolované techniky:
  - Pokud je aktuální technická verze blokována, zablokujte proces.
  - Pokud je aktuální varianta blokována, zablokujte proces.
  - Pokud je blokován vydaný produkt, zablokujte proces.
- Pro standardní produkty:
  - Pokud je aktuální varianta blokována, zablokujte proces.
  - Pokud je blokován vydaný produkt, zablokujte proces.

Předpokládejme například, že chcete prodat pouze jednu variantu (červenou) daného produktu (tričko) a zatím blokovat prodej všech ostatních variant. Toto můžete implementovat pomocí následujícího nastavení:

- Přiřaďte produktu stav životního cyklu, který umožňuje proces. Například přiřaďte produktu trička stav životního cyklu *Prodejný*, který umožňuje obchodní proces *Zakázka odběratele*.
- Přiřaďte prodejné variantě stav životního cyklu, který umožňuje proces. Přiřaďte například také červené variantě stav životního cyklu *Prodejný*.
- Všem ostatním variantám je přiřazen jiný stav životního cyklu, kde je proces blokován. Například přiřaďte bílé variantě (a všem ostatním variantám) stav životního cyklu *Není prodejný*, který blokuje obchodní proces *Zakázka odběratele*.

## <a name="default-product-lifecycle-states"></a>Výchozí stavy životního cyklu produktu

Výchozí stav životního cyklu u technické verze je určen její technickou kategorií. Stav bude výchozí, když vytvoříte novou technickou verzi, včetně první verze nového produktu.

Když vytváříte nový produkt nebo technický produkt, můžete také nastavit výchozí stav životního cyklu tak, že jej uvedete v produktu uvolněném pomocí šablony zásady vydání přiřazené k produktu.

V tomto případě je možné, že produkt bude mít jiný stav životního cyklu než verze, když vytvoříte nový technický produkt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
