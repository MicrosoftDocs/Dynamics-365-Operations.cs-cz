---
title: Cenové funkce v POS
description: Tento článek popisuje různé cenové a slevové funkce v aplikaci pokladního místa Microsoft Dynamics 365 Commerce (POS).
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 210798ac192ee251594ec8ff9d23dab31ec2043e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473680"
---
# <a name="pricing-functions-in-pos"></a>Cenové funkce v POS

[!include [banner](includes/banner.md)]

Tento článek popisuje různé cenové a slevové funkce v aplikaci pokladního místa Microsoft Dynamics 365 Commerce (POS).

Aplikace Dynamics 365 Commerce POS poskytuje bohaté možnosti, které umožňují pracovníkům první linie provádět operace Store Commerce. V následující tabulce jsou uvedeny cenové a slevové funkce, které jsou v aplikaci aktuálně dostupné.

| Funkce                       | Operace POS |
|--------------------------------|----------------|
| Zobrazení cen                    | [Kontrola ceny](#price-check) |
| Zobrazení slev                 | [Zobrazit všechny slevy](#view-all-discounts)<br>[Zobrazit dostupné slevy](#view-available-discounts) |
| Přepsání cen                | [Přepsání ceny](#price-override) |
| Uplatnění nebo odebrání slev      | [Částka řádkové slevy](#line-discount-amount)<br>[Procento řádkové slevy](#line-discount-percent)<br>[Částka celkové slevy](#total-discount-amount)<br>[Procento celkové slevy](#total-discount-percent)<br>[Odebrat systémové slevy z transakce](#remove-system-discounts-from-transaction)<br>[Znovu použít systémové slevy](#reapply-system-discounts) |
| Uplatnění nebo odebrání kupónů        | [Přidat kód kupónu](#add-coupon-code)<br>[Odebrat kód kupónu](#remove-coupon-code) |
| Výpočet cen a slev | [Přepočítat](#recalculate) |

Informace o tom, jak lze konfigurovat předchozí operace v aplikaci POS a zda podporují režim offline, viz [Operace online a offline pokladního místa (POS)](pos-operations.md).

## <a name="price-check"></a>Kontrola ceny

Operace **Kontrola ceny** umožňuje uživatelům POS vyhledávat předkonfigurované ceny pro konkrétní produkt.

## <a name="view-all-discounts"></a>Zobrazit všechny slevy

Operace **Zobrazit všechny slevy** umožňuje uživatelům POS vyhledat všechny platné akce, které aktuálně běží v kanálu obchodu. Konkrétně tato operace uvádí všechny slevy, které splňují některou z následujících podmínek:

- Cenová skupina slevy se shoduje s cenovou skupinou obchodu.
- Cenová skupina slevy je mapována na afilaci nebo věrnostní program.
- Cenová skupina slevy je mapována na katalog přidružený k obchodu.

V operaci **Zobrazit všechny slevy** jsou zobrazeny pouze slevy, které nejsou v rozporu s žádnými již použitými slevami. Toto chování pomáhá zajistit, že v případě, že prodávající informuje odběratele o slevě a odběratel provede požadovanou akci (například odběratel nakoupí jednu další položku pro získání 10 procent), sleva bude uplatněna na transakci. Slevy založené na kupónech jsou zobrazeny pouze v případě, že je zapnutý parametr **Použít bez kódu kupónu**.

Uvnitř operace **Zobrazit všechny slevy** uživatelé POS mohou vyhledávat slevy podle názvu a popisu a mohou slevy filtrovat podle toho, zda požadují kupon.

## <a name="view-available-discounts"></a>Zobrazit dostupné slevy

Operace **Zobrazit dostupné slevy** umožňuje uživatelům POS zobrazit všechny slevy, které se vztahují na vybraný řádek v transakci nebo na celou transakci. Slevy, které se vztahují na vybranou řadu, zahrnují slevy, které jsou již uplatněny, a slevy, které ještě nebyly uplatněny, ale lze je uplatnit (například smíšené slevy, které vyžadují další položky). Pokud je příslušná sleva spojena s kupónem, kde je parametr **Použít bez kódu kupónu** zapnutý, uživatel POS může také použít funkci **Použít kupón** uvnitř této operace pro uplatnění kupónu přímo, bez nutnosti zadávat nebo skenovat kódy kupónů nebo čárové kódy kupónů.

## <a name="price-override"></a>Přepsání ceny

Operace **Přepsání ceny** umožňuje uživatelům POS přepsat prodejní cenu produktu v transakci. Tato operace funguje pouze pro produkty, které jsou nakonfigurovány tak, aby umožňovaly přepsání ceny.

## <a name="line-discount-amount"></a>Částka řádkové slevy

Operace **Výše řádkové slevy** umožňuje uživatelům POS zadat částku slevy pro řádkovou položku v transakci. Tato operace se vztahuje pouze na zlevněné položky a respektuje hodnotu **Maximální výše slevy na řádku**, která je určena ve skupině oprávnění POS pro uživatele.

## <a name="line-discount-percent"></a>Procento řádkové slevy

Operace **Procento řádkové slevy** umožňuje uživatelům POS zadat procento slevy pro řádkovou položku v transakci. Tato operace se vztahuje pouze na zlevněné položky a respektuje hodnotu **Maximální procento slevy na řádku**, která je určena ve skupině oprávnění POS pro uživatele.

## <a name="total-discount-amount"></a>Částka celkové slevy

Operace **Celková částka slevy** umožňuje uživatelům POS zadat částku slevy pro transakci. Tato operace se vztahuje pouze na zlevněné položky a respektuje hodnotu **Maximální celková výše slevy**, která je určena ve skupině oprávnění POS pro uživatele. Pokud zadaná částka slevy překročí maximální celkovou částku slevy, operace se zablokuje a nespustí se žádný tok přepsání oprávnění. V současné době nelze celkovou částku slevy uplatnit na košík, který obsahuje kombinaci prodejních položek a vrácených položek.

## <a name="total-discount-percent"></a>Procento celkové slevy

Operace **Celkové procento slevy** umožňuje uživatelům POS zadat procento slevy pro transakci. Tato operace se vztahuje pouze na zlevněné položky a respektuje hodnotu **Maximální procento celkové slevy**, která je určena ve skupině oprávnění POS pro uživatele. Pokud zadané procento slevy překročí maximální procento celkové slevy, operace se zablokuje a nespustí se žádný tok přepsání oprávnění. V současné době nelze celkové procento slevy uplatnit na košík, který obsahuje kombinaci prodejních položek a vrácených položek.

## <a name="remove-system-discounts-from-transaction"></a>Odebrat systémové slevy z transakce

Operace **Odstranit systémové slevy z transakce** umožňuje uživatelům POS vymazat z transakce všechny uplatněné systémové slevy (včetně slev na základě kuponu). Po provedení této operace začne cenový modul vylučovat systémové slevy z rozsahu výpočtu slev. Operace **Odstranit systémové slevy z transakce** neodstraní ruční slevy.

## <a name="reapply-system-discounts"></a>Znovu použít systémové slevy

Operace **Znovu uplatnit systémové slevy** umožňuje uživatelům POS znovu použít slevy vypočítané systémem na transakci, pokud byly slevy odstraněny pomocí operace **Odstranit systémové slevy z transakce**. Po provedení této operace začne cenový modul zahrnovat všechny systémové slevy do rozsahu výpočtu slev.

## <a name="add-coupon-code"></a>Přidat kód kupónu

Operace **Přidat kód kupónu** umožňuje uživatelům POS přidat kupón k transakci zadáním kódu kupónu. Případně mohou uživatelé POS naskenovat čárový kód kupónu nebo ho zadat pomocí numerické klávesnice na obrazovce **Transakce**.

## <a name="remove-coupon-code"></a>Odebrat kód kupónu

Operace **Odstranit kód kupónu** umožňuje uživatelům POS vybrat a odstranit jeden nebo více kupónů, které jsou aktuálně aplikovány na transakci.

## <a name="recalculate"></a>Přepočítat

Operace **Přepočítat** umožňuje uživatelům POS spouštět výpočet ceny na vyžádání. Tato operace je vyžadována, když je povoleno uzamčení ceny nebo zpožděný výpočet ceny a uživatel POS chce přepočítat ceny a slevy po změně košíku nebo objednávky. Operace **Přepočítat** vždy přepočítá celou zakázku. Nedá se použít k přepočtu vybraných prodejních řádků. Chtějí-li uživatelé POS uplatnit manuální slevy na uzamčený prodejní řádek v POS, musí nejprve použít operaci **Přepočítat** k odblokování všech prodejních řádků.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
