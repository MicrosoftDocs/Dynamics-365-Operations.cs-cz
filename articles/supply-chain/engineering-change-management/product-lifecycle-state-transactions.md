---
title: Stavy životního cyklu produktu a transakce
description: Toto téma vysvětluje, jak můžete ovládat, které transakce jsou povoleny pro každý stav životního cyklu, když technický produkt prochází svým životním cyklem.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 421fae6eab20eea50b9ce677a1ae7993add6cb93
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842050"
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
> Technické produkty používají stejné stavy životního cyklu produktu jako standardní (netechnické) produkty. Můžete také otevřít stránku **Stav životního cyklu produktu**, která je popsána v tomto tématu, přechodem na **Správa informací o produktu \> Nastavit \> Stav životního cyklu produktu**. Další informace o stavech životního cyklu produktu pro technické produkty i pro standardní produkty najdete v tématu [Přehled stavu životního cyklu produktu](../pim/product-lifecycle.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]