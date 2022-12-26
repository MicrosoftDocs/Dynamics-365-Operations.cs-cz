---
title: Dotaz na vyrovnání hlavní knihy
description: Tento článek popisuje okno s dotazem na vyrovnání hlavní knihy
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ae49d9503c0a83bda7e0093ab6ef69fb4aef0a
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853117"
---
# <a name="ledger-settlement-inquiry"></a>Dotaz na vyrovnání hlavní knihy

[!include [banner](../includes/banner.md)]

Tento článek popisuje okno **Dotaz na vyrovnání hlavní knihy**, které lze použít k zobrazení vyrovnaných, nevyrovnaných nebo vyrovnaných i nevyrovnaných transakcí hlavní knihy za fiskální období.

## <a name="view-ledger-settlement-transactions"></a>Zobrazení transakcí vyrovnání hlavní knihy
1.  Přejděte do části **Hlavní kniha > Dotazy a sestavy > Dotaz na vyrovnání hlavní knihy**.
2.  Pomocí polí **Od data** a **Do data** nebo **Časový interval** zadejte rozsah dat. Pokud jde o předvahu, časové období musí spadat do jednoho fiskálního roku.
3.  V poli **Hlavní účty** vyberte jeden nebo více hlavních účtů, pro které chcete zobrazit transakce hlavní knihy. Rozevírací seznam zobrazuje pouze hlavní účty, které jsou nastaveny pro vyrovnání hlavní knihy na stránce **Parametry hlavní knihy**.
4.  Pomocí pole **Sada finančních dimenzí** zobrazíte finanční dimenze v mřížce. Protože je vyžadován hlavní účet, hodnota pole **Hlavní účet** bude vždy zobrazena jako první sloupec, i když vyberete sadu finančních dimenzí, která nezahrnuje hlavní účet.
5.  V poli **Stav** vyberte možnost:
-   **Vše** pro zobrazení vyrovnaných i nevyrovnaných transakcí
-   **Nevyrovnáno** pro zobrazení pouze nevyrovnaných transakcí 
-   **Vyrovnáno** pro zobrazení pouze vyrovnaných transakcí
6.  Vyberte **Zobrazit transakce**. Transakce hlavní knihy se zobrazí v mřížce na základě kritérií, která jste zadali. Výsledky dotazu můžete exportovat do Microsoft Excel pro další analýzu. Vyberte a podržte (nebo klikněte pravým tlačítkem myši) na mřížce.

### <a name="column-details"></a>Podrobnosti sloupce
Mřížka na stránce **Dotaz na vyrovnání hlavní knihy** obsahuje následující sloupce:
-   **Hlavní účet**– Toto pole je povinné a zobrazuje se vždy.
-   **Finanční dimenze** – Finanční dimenze se zobrazují na základě vybrané sady finančních dimenzí.
-   **Datum transakce** – Datum zaúčtování transakce hlavní knihy.
-   **Původní datum transakce**– Pokud byla spuštěna uzávěrka na konci roku a vyrovnání hlavní knihy je nastaveno tak, že uchovává podrobnosti o hlavním účtu, nevyrovnané transakce jsou podrobně převedeny na počáteční zůstatek. Původní datum zaúčtování transakce hlavní knihy je zachováno v poli **Původní datum transakce**.
-   **Stáří transakce**– Hodnota je 0 (nula) pro všechny vyrovnané transakce. U nevyrovnaných transakcí se hodnota vypočítá jako počet dní od původního data transakce nebo od data transakce do data, kdy je dotaz spuštěn.
Například transakce hlavní knihy má datum transakce 1. ledna 2022 (1. 1. 2022) a původní datum transakce 30. prosince 2021 (30. 12. 2021). Pokud je dotaz pro fiskální rok 2022 spuštěn 2. ledna 2022 (1/2/2022), **Stáří transakce** bude mít hodnotu 4. Tato hodnota se vypočítá jako počet dní mezi původním datem transakce (30. 12. 2021) a 2. 1. 2022.

Pokud neexistuje původní datum transakce, použije se místo toho datum transakce.
-   **(Další informace o transakcích)**– Další sloupce zobrazují informace, jako je číslo dokladu, popis a debetní a kreditní částky ve všech třech měnách (transakce, účetnictví a výkaznictví).
-   **Stav** – Tato hodnota je buď **Vyrovnáno** nebo **Nevyrovnáno**.
-   **ID vyrovnání** – ID, které je přiřazeno vyrovnaným transakcím.

[![Stránka s dotazem na vyrovnání hlavní knihy](./media/Inquiry1.png)](./media/Inquiry1.png)

 
Součty lze zobrazit pod mřížkou.
1.  Vyberte tři tečky (…) napravo od mřížky a poté vyberte **Zobrazit zápatí**.
2.  Vyberte a podržte (nebo klikněte pravým tlačítkem) v každém sloupci a poté výběrem **Seskupit podle tohoto sloupce** zobrazíte součty. Součty jsou zobrazeny v zápatí. Pokud je dotaz filtrován tak, že zobrazuje pouze nevyrovnané transakce, můžete použít součty k odsouhlasení částek s předvahou.







