---
title: Změna mezipodnikových objednávek
description: Tento článek vysvětluje změnu mezipodnikových objednávek
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f139678fbb59b9132ece1ab758e141ec7cdb7a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852179"
---
# <a name="change-intercompany-orders"></a>Změna mezipodnikových objednávek

[!include [banner](../../includes/banner.md)]

Při změně mezipodnikové prodejní nebo nákupní objednávky dojde i ke změně odpovídající prodejní nebo nákupní objednávky odpovídající společnosti.

## <a name="adding-new-lines"></a>Přidání nových řádků

Do mezipodnikové prodejní objednávky a nákupní objednávky můžete přidat nové řádky, pokud je původní prodejní objednávka součástí řetězce mezipodnikových objednávek. Můžete také přidat nové řádky, pokud původní prodejní objednávka není přímou dodávkou. Pokud je původní prodejní objednávka přímou dodávkou, můžete do mezipodnikové prodejní objednávky a nákupní objednávky přidat nové řádky objednávky pouze v případě, že je vybráno pole **Povolit vytvoření nepřímé** na záložce **Mezipodniková nastavení** u původní prodejní objednávky.

## <a name="changing-prices-and-discounts"></a>Změna cen a slev

Ceny a slevy můžete změnit, pokud jsou zaškrtnuta políčka **Povolit úpravu ceny** a **Povolit úpravy slev** na stránce **Mezipodnikové**.

Při změně jednotkové ceny jednoho z existujících řádků mezipodnikové prodejní objednávky dojde také ke změně jednotkové ceny na mezipodnikové nákupní objednávce.

Při změně některého z polí slev na řádku mezipodnikové prodejní objednávky se aktualizují relevantní pole slev na mezipodnikové nákupní objednávce.

## <a name="changing-and-adding-new-charges"></a>Změna a přidání nových nákladů

Náklady můžete změnit, pokud jsou zaškrtnuta políčka **Povolit úpravu ceny** a **Povolit úpravy slev** na stránce **Mezipodnikové**.

Pokud do záhlaví mezipodnikové prodejní objednávky přidáte nový náklad a do řádku mezipodnikového prodeje také nový náklad, zkopírují se do mezipodnikové nákupní objednávky oba náklady. Mezipodniková prodejní objednávka a mezipodniková nákupní objednávka mají tedy stejnou celkovou částku. Náklady se nikdy nekopírují do původní prodejní objednávky.

## <a name="copying-a-fee"></a>Kopírování poplatku

Chcete-li zkopírovat poplatek do původní prodejní objednávky, vytvořte jej jako nový řádek prodejní objednávky, jehož typ položky je **Služba**.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Změna množství a odstraňování řádků mezipodnikových nákupních a prodejních objednávek

Změnit množství nebo odstranit řádek mezipodnikové nákupní nebo prodejní objednávky můžete pouze v případě, že daný řádek byl vytvořen přímo ve formuláři **Prodejní objednávka** nebo **Nákupní objednávka**. Tato změna učiní zdroj z mezipodnikových nákupních či prodejních objednávek, nebo ze řádků objednávek.

## <a name="origins-of-orders-and-order-lines"></a>Původy objednávek a řádků objednávek

Mezipodnikové objednávky a řádky objednávek mohou mít jeden ze dvou původů:

- **Odvozeno** – Objednávka byla automaticky vytvořena z řetězce mezipodnikových objednávek.
- **Zdroj** – Objednávka byla ručně vytvořena uživatelem.

Původ je zobrazen v záhlaví mezipodnikových nákupních a prodejních objednávek v poli **Původ**. Toto pole se nachází na záložce **Mezipodniková nastavení** na prodejní objednávce a na záložce **Nastavení** na nákupní objednávce.

Původy **Odvozeno** a **Zdroj** platí pouze pro mezipodnikové objednávky. Pole **Původ** bude tedy prázdné u všech ostatních prodejních objednávek, nákupních objednávek a řádků objednávek. Toto pole je prázdné také v původní prodejní objednávce.

## <a name="example-derived-origin"></a>Příklad: odvozený původ

Vytvoříte původní prodejní objednávku pro externího odběratele. Tato prodejní objednávka obsahuje jeden řádek objednávky. Tato původní prodejní objednávka vytvoří mezipodnikovou nákupní objednávku obsahující jeden řádek objednávky, který vytvoří mezipodnikovou prodejní objednávku obsahující jeden řádek objednávky. Záhlaví mezipodnikové nákupní objednávky a řádek objednávky jsou vytvořeny automaticky z původní prodejní objednávky.

Hodnota pole **Původ** na záložce **Nastavení** mezipodnikové nákupní objednávky a záložce **Mezipodniková nastavení** záhlaví mezipodnikové prodejní objednávky je **Odvozeno**. Hodnota pole **Původ** na kartě **Podrobnosti řádku** nákupní objednávky a řádků prodejní objednávky je také **Odvozeno**.

Pokud má řádek objednávky původ **Odvozeno**, nemůžete řádek objednávky odstranit přímo. Řádek objednávky můžete odstranit pouze ze zdroje, který řádek objednávky vytvořil. Také objednané množství můžete změnit pouze ze zdroje, který řádek objednávky vytvořil.

Pokud jsou původní prodejní objednávka a řádek původní prodejní objednávky součástí řetězce mezipodnikových objednávek, můžete změnit objednaná množství z původní prodejní objednávky a odstranit řádky objednávky z původní prodejní objednávky.

## <a name="example-source-origin"></a>Příklad: zdrojový původ

Vytvoříte nákupní objednávku pro mezipodnikového dodavatele. Mezipodniková nákupní objednávka a řádek objednávky budou mít původ **Zdroj**. Mezipodniková nákupní objednávka je tedy řídicím prvkem a automaticky vytvářená mezipodniková prodejní objednávka ve společnosti dodavatele bude mít původ **Odvozeno**.

Kromě toho nelze v mezipodnikové prodejní objednávce změnit objednané množství v řádku objednávky, který je vytvořen v mezipodnikové nákupní objednávce. Řádek objednávky lze odstranit pouze z mezipodnikové nákupní objednávky. Pokud je do mezipodnikové prodejní objednávky přidán nový řádek, má řádek mezipodnikové prodejní objednávky původ **Zdroj**.

V případě, že původní prodejní objednávka je součástí řetězce mezipodnikových objednávek, můžete vždy řídit mezipodnikové objednávky a řádky mezipodnikové objednávky z původní prodejní objednávky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
