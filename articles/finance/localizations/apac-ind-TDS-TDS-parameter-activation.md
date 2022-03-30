---
title: Nastavení parametrů TDS
description: Toto téma vysvětluje, jak nastavit parametry pro aktivaci funkce TDS (daň odečtená u zdroje) v zadaných transakcích. Toto je nezbytný krok k použití funkce Daň odečtená u zdroje TDS.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ca98a74753ca0de3b376cb89ef47862bc1bfb30e
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407503"
---
# <a name="set-the-tds-parameters"></a>Nastavení parametrů TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit parametry pro aktivaci funkce TDS (daň odečtená u zdroje) v zadaných transakcích. Toto je nezbytný krok k použití funkce Daň odečtená u zdroje TDS.

1. Přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Parametry hlavní knihy**.
2. Na kartě **Přímé daně** v části **Daň odečtená u zdroje** nastavte možnost **Aktivovat TDS** na **Ano** k aktivaci funkčnosti TDS a stránek a polí, která se pro ni používají.
3. Nastavte možnost **Faktura** na **Ano** k aktivaci pole, která se používají k výpočtu a odpočtu TDS na úrovni faktury.
4. Nastavte možnost **Platba** na **Ano** k aktivaci pole, která se používají k výpočtu a odpočtu TDS na úrovni platby.

    [![Karta Přímé daně.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Na kartě **Číselné řady** najděte řádek, kde je pole **Odkaz** nastaveno na **Platba srážkové daně**. V poli **Kód číselné řady** pro daný řádek vyberte kód číselné řady. Kód číselné řady se používá ke generování čísel dokladů pro periodický proces vypořádání TDS.

    > [!NOTE]
    > Chcete-li spustit periodický proces vypořádání TDS, přejděte na **Daň \> Přiznání \> Srážková daň \> Platba srážkové daně**.

    [![Karta Číselné řady.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Zavřete stránku.
