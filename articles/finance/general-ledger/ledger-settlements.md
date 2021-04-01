---
title: Vyrovnání hlavní knihy
description: Toto téma vysvětluje, jak používat stránku Vyrovnání hlavní knihy k vyrovnání transakcí hlavní knihy a stornování vyrovnání.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 7704c38f878784647b44e81922b7679c0fedfbb2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248872"
---
# <a name="ledger-settlements"></a>Vyrovnání hlavní knihy

[!include [banner](../includes/banner.md)]

Vyrovnání hlavní knihy vám umožňují spárovat transakce Má dáti a Dal v hlavní knize, a označit je jako vyrovnané. Tímto způsobem můžete zajistit, že související transakce budou vyrovnány. Pokud byla provedena omylem, můžete také vyrovnání stornovat.

## <a name="enable-advanced-ledger-settlements"></a>Povolit pokročilá vyrovnání hlavní knihy

Stránka pokročilých vyrovnání hlavní knihy poskytuje další možnosti filtrování a výběru transakcí. Chcete-li povolit pokročilá vyrovnání hlavní knihy, postupujte takto.

1. Zvolte **Hlavní kniha** \> **Nastavení hlavní knihy** \> **Parametry hlavní knihy**. 
2. Na kartě **Vyrovnání hlavní knihy** nastavte možnost **Rozšířené vyrovnání hlavní knihy** na **Ano**, čímž zapnete funkci rozšířeného vyrovnání hlavní knihy Stránka **Pokročilé vyrovnání hlavní knihy** se použije tehdy, když zvolíte **Vyrovnání hlavní knihy** v možnosti **Periodické úlohy**. 
3. Je nutné zadat seznam účtů, které se použijí pro vyrovnání hlavní knihy pro každou účtovou osnovu. Tento seznam slouží k filtrování seznamu transakcí, které se zobrazí na stránce **Vyrovnání hlavní knihy**. V seznamu **Účtové osnovy** vyberte účtovou osnovu a poté vyberte **Nový** pro přidání nových účtů do seznamu.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Vyrovnání transakcí pomocí stránky pokročilého vyrovnání hlavní knihy

Chcete-li vyrovnat transakce, postupujte takto.

1. Zvolte **Hlavní kniha** \> **Periodické úlohy** \> **Vyrovnání hlavní knihy**.
2. Nastavte filtry v horní části stránky:

    - Vyberte rozsah dat nebo zvolte **Kód časového intervalu** pro automatické vyplnění časového rozsahu.
    - Změňte účtovací vrstvu podle potřeby.
    - Chcete-li zobrazit hlavní knihu a dimenze zvlášť, vyberte sadu finančních dimenzí.

3. Vyberte **Zobrazit transakce** k zobrazení všech transakcí, které odpovídají nastaveným filtrům a seznamu účtů, které jste uvedli při nastavení účtové osnovy v předchozí části. Pokud změníte jakýkoliv z filtrů nebo sad dimenzí, je nutné vybrat možnost **Zobrazit transakce** znovu.
4. Vyberte jeden nebo více řádků, které máte v plánu vyrovnat. Hodnota pole **Vybraná částka** v horní části stránky se zvyšuje nebo snižuje o celkovou částku na vybraných řádcích.
5. Po dokončení výběru transakcí vyberte **Označit vybrané**. Ve sloupci **Označené** se zobrazí zaškrtnutí pro každou vybranou transakci. Kromě toho se hodnota pole **Označená částka** nad mřížkou zvyšuje nebo snižuje o celkovou částku na označených řádcích.
6. Když je hodnota **Označené částka** rovna **0** (nule), vyberte **Vyrovnat označené transakce**. Stav označených transakcí je aktualizován na **Vyrovnáno**.

## <a name="make-transactions-easier-to-find"></a>Snadnější vyhledání transakcí

Stránka **Vyrovnání hlavní knihy** obsahuje možnosti, které usnadňují zobrazení transakcí, které potřebujete pro vyrovnání.

- Tlačítko **Zrušit označení vybraných** vymaže pole **Označené** pro všechny řádky, které jsou vybrány.
- Filtr **Označené** vám umožňuje filtrovat transakce podle toho, zda je pole **Označené** pro danou položku vybráno nebo odznačeno.
- Filtr **Stav** vám umožňuje filtrovat transakce podle toho, zda je jejich stav **Vyrovnáno** nebo **Nevyrovnáno**.
- Tlačítko **Třídit podle absolutní částky** umožňuje seřadit částky podle absolutní hodnoty, abyste mohli seskupit dohromady položky Má dáti a Dal, které mají stejnou částku.

## <a name="reverse-a-settlement"></a>Stornování vyrovnání

Omylem provedené vyrovnání lze stornovat.

1. Proveďte kroky 1 až 3 v části „Vyrovnání transakcí pomocí stránky pokročilých vyrovnání hlavní knihy“ k zobrazení transakcí, které hledáte.
2. Ve filtru **Stav** vyberte možnost **Vyrovnáno**.
3. Vyberte jeden nebo více řádků, které máte v plánu stornovat. Hodnota pole **Vybraná částka** v horní části stránky se zvyšuje nebo snižuje o celkovou částku na vybraných řádcích.
4. Po dokončení výběru transakcí vyberte **Označit vybrané**. Ve sloupci **Označené** se zobrazí zaškrtnutí pro každou vybranou transakci. Kromě toho se hodnota pole **Označená částka** v horní části stránky zvyšuje nebo snižuje o celkovou částku na označených řádcích.
5. Když je hodnota **Označené částka** rovna **0** (nule), vyberte **Stornovat označené transakce**. Stav označených transakcí je aktualizován na **Nevyrovnáno**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Aktualizace seznamů účtů, které jsou zahrnuty v seznamu transakcí

Vyberte **Účty vyrovnání hlavní knihy** pro otevření dialogového okna, ve kterém můžete upravit účty zahrnuté v seznamu transakcí. Zvolte **Nový** pro přidání nových účtů do seznamu. Tento seznam slouží k filtrování seznamu transakcí, které se zobrazí na stránce **Vyrovnání hlavní knihy**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]