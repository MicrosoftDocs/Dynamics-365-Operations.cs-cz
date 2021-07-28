---
title: Nastavení období vyrovnání srážkové daně pro typ daně TDS
description: Toto téma vysvětluje, jak nastavit období vypořádání pro období vypořádání daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: 12ba639ccf670997d4f16325172aa351732a5722
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348902"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a>Nastavení období vyrovnání srážkové daně pro typ daně TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit období vypořádání pro období vypořádání daně odečtené u zdroje (TDS).

1. Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Období vypořádání srážkové daně**.

    [![Stránka období vyrovnání srážkové daně.](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)

2. V poli **Typ daně** vyberte **TDS** a nastavte období vypořádání srážkové daně pro typ daně TDS.
3. Volbou možnosti **Nová položka** vytvořte řádek.
4. Do pole **Období vypořádání** zadejte název období vypořádání TDS.
5. Zadejte popis do pole **Popis**.
6. V poli **Autorita srážkové daně** vyberte autoritu TDS, pro kterou definujete období vypořádání TDS.
7. Na pevné záložce **Obecné** v poli **Interval období** vyberte typ intervalu období pro období vypořádání TDS.
8. Do pole **Počet jednotek** zadejte počet jednotek pro typ intervalu období.
9. Na pevné záložce **Období** v poli **Od data** vyberte datum zahájení období vypořádání TDS. V poli **Do data** vyberte koncové datum.
10. Chcete-li vytvořit následující období vypořádání TDS pro stávající období na základě intervalu období a jednotek období, vyberte **Nové období**.
11. Chcete-li zobrazit podrobnosti pravidelného vypořádání TDS, které se spouští pro konkrétní období vypořádání, vyberte **Platby srážkové daně** k otevření stránky **Platba srážkové daně**.

    > [!NOTE]
    > Chcete-li spustit proces periodického vypořádání TDS, přejděte na **Hlavní kniha \> Pefiodické \> Srážková daň \> Platba srážkové daně**.

    [![Stránka Platba srážkové daně.](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)

12. Zavřete stránku.
