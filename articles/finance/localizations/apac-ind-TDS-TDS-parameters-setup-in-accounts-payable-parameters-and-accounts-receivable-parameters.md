---
title: Nastavení parametrů TDS v závazcích a pohledávkách
description: Tento článek vysvětluje, jak nastavit parametry v závazcích a pohledávkách na podporu odpočtů daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: e547b92f9f7e0ccc5b92df4cd991ce402369b568
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883143"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Nastavení parametrů TDS v závazcích a pohledávkách

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak nastavit parametry v závazcích a pohledávkách na podporu odpočtů daně odečtené u zdroje (TDS).

1. Přejděte do **Daň \> Nastavení \> Parametry \> Parametry pohledávek**.
2. Na kartě **Aktualizace** vyberte **Aktualizovat řádky objednávky** k otevření dialogového okna **Aktualizovat řádky objednávky**.
3. V části **Skupina TDS** v poli **Aktualizace skupiny TDS** zadejte metodu, která se má použít k aktualizaci skupiny TDS na úrovni řádku. Toto nastavení se používá, když je skupina TDS aktualizována v záhlaví objednávky. Existují tyto možnosti:

    - **Nikdy** – Skupina TDS není aktualizována na řádcích objednávky, když je aktualizována v záhlaví objednávky.
    - **Vždy** – Skupina TDS je automaticky aktualizována na řádcích objednávky, když je aktualizována v záhlaví objednávky.
    - **Výzva** – Uživatelé obdrží zprávu, která je vyzve k aktualizaci skupiny TDS na řádcích objednávky.
4. Vyberte **OK**.

    [![Dialogové okno Aktualizovat řádky objednávky.](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Přejděte do **Daň \> Nastavení \> Parametry \> Parametry zakázek**.
6. Na kartě **Všeobecné** na pevné záložce **Rozdělit na základě informací o doručení** nastavte možnost **Příjem produktu** na **Ano** k zaúčtování a rozdělení příjemky produktu, která má různé doručovací adresy a čísla daňových účtů (TAN). Pokud je tato možnost nastavena na **Ne**, nemůžete zaúčtovat nákupní dodací list, který má různé dodací adresy a TAN.
7. Nastavte možnost **Faktura** na **Ano** k zaúčtování a rozdělení nákupní fakturu, která má různé dodací adresy a čísla TAN.

    [![Pevná záložka Rozdělit na základě informací o doručení.](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Zavřete stránku.
