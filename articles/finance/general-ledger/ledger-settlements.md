---
title: Vyrovnání hlavní knihy
description: Tento článek vysvětluje, jak používat stránku Vyrovnání hlavní knihy k vyrovnání transakcí hlavní knihy a stornování vyrovnání.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 39fd6c6677565a4b1e9a9bf6f43a4c630cb5e07b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902480"
---
# <a name="ledger-settlements"></a>Vyrovnání hlavní knihy

[!include [banner](../includes/banner.md)]

Vyrovnání hlavní knihy je proces spárování transakce Má dáti a Dal v hlavní knize. Vyrovnání částek Má dáti a Dal se používá k odsouhlasení zůstatku účtu hlavní knihy s podrobnými transakcemi, které tvoří tento zůstatek.

Vypořádané transakce mohou být vyloučeny z dotazů a sestav. Tímto způsobem je snazší analýza transakcí otevřené knihy, které tvoří zůstatek účtu hlavní knihy.

> [!IMPORTANT] 
> Moduly Závazky (AP) a Pohledávky (AR) mají také vyrovnání faktur a plateb. Když dojde k vypořádání v dílčích knihách AR a AP, odpovídající položky hlavní knihy se automaticky nevypořádají.

## <a name="ledger-settlement-features"></a>Funkce vyrovnání hlavní knihy
V Microsoft Dynamics 365 Finance verze 10.0.21 byla možnost **Povolit pokročilá vyrovnání hlavní knihy** ze stránky **Parametry hlavní knihy** odstraněna. Pokročilé vyrovnání hlavní knihy je nyní vždy povoleno.
Ve verzi Finance 10.0.25 byla představena funkce **Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku**. Tato funkce mění základní funkčnost vyrovnání hlavní knihy i uzavření hlavní knihy na konci roku. Před povolením této funkce v pracovním prostoru **Správa funkcí** si pročtěte téma [Sledování mezi vyrovnáním hlavní knihy a uzávěrkou na konci roku](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Nastavení vypořádání hlavní knihy
Musíte vybrat hlavní účty, pro které chcete provést vyrovnání hlavní knihy. Tyto hlavní účty lze vybrat dvěma způsoby.

1. Přejděte do nabídky **Hlavní kniha** > **Nastavení hlavní knihy** > **Parametry hlavní knihy**.
2. Na kartě **Účetní vypořádání** vyberte účtové osnovy, ze kterých chcete vybrat hlavní účty.
3. Vyberte hlavní účty pro vyrovnání hlavní knihy. Protože účtové osnovy jsou globální, všechny společnosti, kterým jsou vybrané účtové osnovy přiřazeny, budou mít pro vyrovnání hlavní knihy vybrané stejné hlavní účty.

  - nebo -

1. Přejděte do nabídky **Hlavní kniha** > **Periodické úkoly** > **Vyrovnání hlavní knihy**.
2. Vyberte **Účty vypořádání hlavní knihy**.
3. V dialogovém okně vyberte účtové osnovy a hlavní účty, pro které chcete provést vyrovnání hlavní knihy. Toto dialogové okno je zkratka. Všechny hlavní účty, které sem přidáte, se projeví také na stránce **Parametry hlavní knihy**.

K odstranění hlavních účtů z vyrovnání hlavní knihy můžete kdykoli použít stejné základní postupy. Odstranění hlavního účtu nemá žádný vliv na předchozí vyrovnání hlavní knihy. Hlavní účet a transakce se však již nebudou zobrazovat na stránce **Vyrovnání hlavní knihy**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Vyrovnat transakce
Chcete-li vyrovnat transakce, postupujte takto.

1. Přejděte do nabídky **Hlavní kniha** > **Periodické úkoly** > **Vyrovnání hlavní knihy**.
2. Nastavte filtry v horní části stránky:

    - Vybrat rozsah dat Nebo můžete vybrat kód časového intervalu pro automatické vyplnění časového rozsahu. Nedoporučujeme provádět vyrovnání hlavní knihy u transakcí, které zasahují do více fiskálních roků.
    - Změňte účtovací vrstvu podle potřeby. Nemůžete vypořádat transakce, které jsou v různých účtovacích vrstvách.
    - Chcete-li zobrazit hlavní účet a dimenze zvlášť, vyberte sadu finančních dimenzí.

3. Vyberte **Zobrazit transakce** k zobrazení všech transakcí, které odpovídají nastaveným filtrům a seznamu účtů, které jste uvedli při nastavení účtové osnovy v předchozí části.

    - Pokud změníte jakýkoliv z filtrů nebo sad dimenzí, je nutné vybrat možnost **Zobrazit transakce** znovu.
    - Chcete-li vyfiltrovat transakce pro individuální hlavní účet, použijte filtr v poli **Účet hlavní knihy**. Nedoporučujeme provádět vyrovnání hlavní knihy pro transakce, které jsou zaúčtovány na různé hlavní účty.

4. Vyberte řádky pro vyrovnání. Hodnota v poli **Vybraná částka** v horní části stránky se zvyšuje nebo snižuje o celkovou částku na vybraných řádcích.
5. Po dokončení výběru transakcí vyberte **Označit vybrané**. Ve sloupci **Označené** se zobrazí zaškrtnutí pro každou vybranou transakci. Kromě toho se hodnota pole **Označená částka** nad mřížkou zvyšuje nebo snižuje o celkovou částku na označených řádcích.
6. Když je hodnota v poli **Označená částka** rovna **0** (nule), vyberte **Vyrovnat označené transakce**. Stav označených transakcí je aktualizován na **Vyrovnáno**.

    > [!IMPORTANT]
    > Všechny transakce, které jste označili k vyrovnání pro aktivní právnickou osobu, budou vyrovnány, i když nejsou aktuálně zobrazeny na stránce vypořádání hlavní knihy kvůli tomu, že jste použili filtr.

## <a name="make-transactions-easier-to-find"></a>Snadnější vyhledání transakcí
Stránka **Vyrovnání hlavní knihy** obsahuje možnosti, které usnadňují zobrazení transakcí, které potřebujete pro vyrovnání.

- Filtr **Označené** použijte k filtrování transakcí podle toho, zda je zaškrtávací políčko **Označené** pro danou položku zapnuto.
- Filtr **Stav** použijte k filtrování transakcí na základě jejich stavu.
- Vyberte možnost **Seřadit podle absolutní částky**, chcete-li seřadit částky podle absolutní hodnoty. Tímto způsobem můžete seskupit debety a kredity, které mají stejnou částku.

## <a name="reverse-a-settlement"></a>Stornování vyrovnání
Omylem provedené vyrovnání lze stornovat.

1. Postupujte podle kroků 1 až 3 v části [Vypořádat transakce](#settle-transactions) pro zobrazení transakcí, které vás zajímají.
2. Ve filtru **Stav** vyberte možnost **Vyrovnáno**.
3. Vyberte řádky pro stornování.
4. Vyberte **Stornovat označené transakce**. Stav všech transakcí, které mají stejné ID vypořádání, se aktualizuje na **Není vyřízeno**.

    > [!IMPORTANT]
    > Všechny transakce, které mají stejné ID vypořádání, budou stornovány, i když nejsou označeny. Například byly označeny a vypořádány čtyři řádky. Všechny čtyři řádky mají stejné ID vypořádání. Pokud označíte jeden z těchto čtyř řádků a poté vyberete **Stornovat označené transakce**, všechny čtyři řádky budou stornovány.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
