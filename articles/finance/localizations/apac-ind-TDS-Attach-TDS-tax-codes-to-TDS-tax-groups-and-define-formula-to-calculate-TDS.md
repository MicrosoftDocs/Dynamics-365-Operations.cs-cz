---
title: Připojení daňových kódů TDS k daňovým skupinám TDS a definování vzorce pro výpočet TDS
description: Toto téma vysvětluje, jak nastavit daňové skupiny odečtené u zdroje (TDS) a připojit daňové kódy TDS k daňovým skupinám TDS. Chcete-li vypočítat TDS pro daňovou skupinu TDS, musíte definovat vzorec pro daňové kódy TDS, který je k ní připojen.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023097"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>Připojení daňových kódů TDS k daňovým skupinám TDS a definování vzorce pro výpočet TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit daňové skupiny odečtené u zdroje (TDS) a připojit daňové kódy TDS k daňovým skupinám TDS. Chcete-li vypočítat TDS pro daňovou skupinu TDS, musíte definovat vzorec pro daňové kódy TDS, který je k ní připojen.

Pomocí těchto kroků můžete nastavit daňovou skupinu TDS, připojit k ní daňové kódy TDS a definovat vzorec pro výpočet TDS.

1. Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Skupiny srážkové daně**.

    [![Stránka Skupiny srážkové daně](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. V podokně akcí vyberte **Nový** pro vytvoření skupiny srážkové daně pro TDS a zadejte požadované podrobnosti.
3. V poli **Typ daně** vyberte **TDS**.
4. Na pevné záložce **Nastavení** výběrem tlačítka **Přidat** vytvořte nový řádek.
5. V poli **Kód srážkové daně** vyberte kód daně TDS pro skupinu daní TDS. Pole **Název srážkové daně** zobrazuje název daňového kódu TDS a pole **Hodnota** zobrazuje hodnotu.
6. Chcete-li ignorovat mezní limit a mezní limit výjimky, které jsou definovány pro daňovou složku TDS, která je připojena k daňovému zákonu TDS v transakcích TDS, zaškrtněte políčko **Přehlédnout prahovou hodnotu**.
7. Aby se zabránilo výpočtu této daňové skupiny v transakcích, zaškrtněte políčko **Vyloučit**.
8. V podokně Akce vyberte **Návrhář** k otevření návrháře vzorců, abyste mohli definovat vzorec pro výpočet TDS pro daňovou skupinu TDS. Na stránce **Návrhář** karta **Daně** zobrazuje daňové kódy TDS, které byly vybrány pro daňovou skupinu TDS.

    [![Stránka návrháře](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Na kartě **Výpočet** vyberte **Alt + N** k vytvoření čáry. Pole **ID** zobrazuje automaticky generované ID priority pro výpočet TDS.
10. V poli **Kód daně** vyberte kód daně TDS, pro kterou se má vzorec definovat. V tomto poli jsou k dispozici pro výběr všechny daňové kódy TDS, které byly vybrány pro daňovou skupinu TDS.
11. V poli **Zdanitelný základ** vyberte základ pro výpočet TDS:

    - **Hrubá částka** – Vypočítat TDS na základě hrubé částky transakce (tj. částky faktury) pomocí výrazu výpočtu, který je definován pro daňový zákon.
    - **Bez hrubé částky** – Výpočet TDS na základě výrazu výpočtu, který je definován pro daňový zákon.

    > [!NOTE]
    > Pole **Zdanitelný základ** nelze nastavit na **Bez hrubé částky** pro daňový zákon TDS, který má ID priority **1**.

12. Výpočet TDS je založen na vzorci, který je definován v poli **Výpočetní výraz** pro každý daňový kód, který je připojen k daňové skupině TDS. Vyberte tlačítko plus (**+**), znaménko minus (**-**), znak násobení (**\**_) nebo znak dělení (_*/**) pro zadání výrazu výpočtu pro vybraný daňový kód TDS v poli **Výpočetní výraz**.

    > [!NOTE]
    > Pro daňový kód TDS, který má ID priority **1**, nelze definovat žádný výpočetní výraz.

13. Chcete-li definovat výraz výpočtu pro daňový kód TDS v poli **Výpočetní výraz**, přidejte daňové kódy TDS, které jsou k dispozici na kartě **Daně**. Chcete-li přidat daňové kódy TDS do pole **Výpočetní výraz**, můžete použít některou z následujících metod:

    - Přetáhněte požadovaný daňový kód z karty **Daně** do pole **Výpočetní výraz**.
    - Dvakrát klepněte (nebo dvakrát klikněte) na požadovaný daňový zákon na kartě **Daně**.
    - Podržte (nebo klikněte pravým tlačítkem) požadovaný daňový kód na kartě **Daně** a poté vyberte **Přidat daňový kód**.

    > [!NOTE]
    > Před každý daňový zákon TDS vložte výpočetní výraz. Daňové kódy TDS, které byly přidány do výrazu výpočtu, se zobrazí v závorkách (\[ ...\]).

14. Chcete-li vymazat výpočetní výraz, který je definován pro daňový zákon v poli **Výpočetní výraz**, vyberte tlačítko **C**.
15. Odstranění záznamu na serveru kartě **Výpočet**, vyberte **Odstranit**.
16. Zavřete stránku.
