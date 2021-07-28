---
title: Spuštění periodického procesu vypořádání TDS
description: Toto téma vysvětluje, jak vypořádat pravidelné daně odečtené u zdroje (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: bfa7dc9c2a86b5bd8783327c0e7cfa6b8b9ddd4c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358331"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Spuštění periodického procesu vypořádání TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vypořádat pravidelné daně odečtené u zdroje (TDS).

1. Přejděte do nabídky **Daň \> Přiznání \> Srážková daň \> Platba srážkové daně**.

    [![Dialogové okno Platba srážkové daně.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. V dialogovém okně **Platba srážkové daně** v poli **Typ daně** vyberte **TDS**.
3. V poli **Číslo daňového účtu (TAN)** vyberte číslo daňového účtu (TAN), pro které chcete spustit proces vypořádání.
4. V poli **Skupina složek srážkové daně** vyberte skupinu složek TDS, pro kterou chcete spustit proces vypořádání.
5. V poli **Zúčtovací období** vyberte období vypořádání TDS, pro které chcete spustit proces vypořádání.

    > [!NOTE]
    > Proces vypořádání TDS je spuštěn pro všechna období, která jsou nastavena pro období vypořádání TDS na kartě **Období** stránky **Období zúčtování srážkové daně** (**Daň \> Nepřímé daně \> Srážková daň \> Období zúčtování srážkové daně**).

6. V poli **Od data** vyberte datum zahájení, od kterého se má spustit proces vypořádání TDS.

    Pro konkrétní období v rámci období vypořádání se počáteční datum, které je definováno pro toto období, považuje za datum „od“. Například období vypořádání TDS má dvě období: 1. dubna až 30. dubna 2009 a 1. května až 31. května 2009. Pokud vyberete **06/04/2009** (6. dubna 2009) jako datum zahájení v poli **Od data**, proces vypořádání bude běžet od 1. dubna 2009.

    Pokud zadáte pozdější období do pole **Od data**, ale bez vyrovnání předchozího období v rámci zúčtovacího období, nedojde k vyrovnání za žádná předchozí období. Například období vypořádání TDS má tři období: 1. dubna až 30. dubna 2009, 1. května až 31. května 2009 a 1. června až 30. června 2009. Pokud vyberete **01/05/2009** (1. května 2009) jako datum zahájení v poli **Od data**, bude proces vypořádání probíhat pouze od 1. května do 31. května 2009. K vypořádání nedojde od 1. dubna do 30. dubna 2009.

7. V poli **Datum transakce** vyberte datum zaúčtování transakce vypořádání TDS.
8. V poli **Verze platby srážkové daně** vyberte typ vypořádání TDS:

     - **Originál** – Tuto možnost použijte k prvnímu spuštění procesu vypořádání TDS. Původní verze platby se používá pouze jednou ke spuštění procesu vypořádání TDS pro kombinaci TAN, skupiny složek srážkové daně a období zúčtování srážkové daně.
    - **Nejnovější verze** -–Tuto možnost použijte, pokud byl proces vypořádání TDS již spuštěn po zadané období. Zahrňte transakce se zpětným datem, které byly zaúčtovány poté, co byl pro dané období dříve spuštěn proces vypořádání. Tuto možnost můžete použít ke spuštění procesu vypořádání několikolikrát.

9. Zaškrtnutím políčka **Aktualizovat** spustíte procesu vypořádání TDS a zaúčtování částek na účty hlavní knihy. Pokud toto políčko není zaškrtnuto, proces vypořádání nebude spuštěn a nebudou vygenerovány finanční položky.
10. Vyberte **OK** ke spuštění procesu vypořádání TDS a vygenerování přehledu plateb srážkové daně. Stav transakcí TDS, které jsou zahrnuty do procesu vypořádání, se zobrazuje jako **Vypořádáno** na stránce **Vyrovnání** (přejděte na **Závazky \> Platby \> Deník plateb dodavatele**, vyberte **Řádky**, vyberte **Funkce** a potom vyberte **Vypořádání**).

### <a name="important-points"></a>Důležité body

- Pokud během procesu vypořádání není vybrána skupina složek srážkové daně, dojde k vyrovnání pro všechny skupiny složek srážkové daně pro vybrané TAN a období vypořádání. Pro každou skupinu složek srážkové daně na stránce **Otevřené úpravy transakcí** se vytvoří samostatný řádek.
- Proces vypořádání je založen na povaze kategorie posuzovaného pro období vypořádání. Transakce, kde je povaha kategorie posuzovaného **Společnost**, jsou vypořádány a zobrazeny jako jeden řádek na stránce **Otevřené úpravy transakcí**. Transakce, kde je povaha kategorie posuzovaného něco jiného než **Společnost**, jsou vypořádány a zobrazeny jako jeden řádek na stránce **Otevřené úpravy transakcí**.
- Datum splatnosti pro vypořádané řádky transakcí TDS na stránce **Otevřené úpravy transakcí** je založena na platebních podmínkách, které jsou definovány pro dodavatele autorit TDS na stránce **Dodavatelé**. Pokud u dodavatele autorit TDS nejsou definovány platební podmínky, jako datum splatnosti se zobrazí poslední den zúčtovacího období.
