---
title: Nastavení parametrů TDS
description: Tento článek vysvětluje, jak nastavit parametry pro aktivaci funkce TDS (daň odečtená u zdroje) v zadaných transakcích. Toto je nezbytný krok k použití funkce Daň odečtená u zdroje TDS.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 3390cad6979858fbff73769d0d25132ba18a2157
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865606"
---
# <a name="set-the-tds-parameters"></a>Nastavení parametrů TDS

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit parametry pro aktivaci funkce TDS (daň odečtená u zdroje) v zadaných transakcích. Toto je nezbytný krok k použití funkce Daň odečtená u zdroje TDS.

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
