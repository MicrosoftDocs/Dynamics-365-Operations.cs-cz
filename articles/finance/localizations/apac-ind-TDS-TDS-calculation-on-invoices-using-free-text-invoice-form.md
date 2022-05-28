---
title: Výpočet TDS na fakturách ze stránky faktury ve volném textu
description: Toto téma vysvětluje, jak vypočítat daň odečtenou u zdroje (TDS) na fakturách pomocí stránky faktury s volným textem.
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
ms.openlocfilehash: 5a1960974dff90ef5f0cc8eab018351a9e412858
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725170"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>Výpočet TDS na fakturách ze stránky faktury ve volném textu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vypočítat daň odečtenou u zdroje (TDS) na fakturách pomocí stránky **Faktura s volným textem**.

1. Přejděte na **Pohledávky \> Faktury \> Všechny volné faktury**.

    [![Stránka Volná faktura.](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Vybráním možnosti **Nové** vytvořte fakturu s volným textem a poté zadejte požadované informace.
3. Vyberte kartu **Faktura**. V části **Skupina srážkové daně** pole **Povaha posuzovaného** ukazuje povahu hodnocené kategorie zákazníka.
4. V poli **Skupina TDS** zobrazte nebo upravte výchozí skupinu TDS definovanou pro zákazníka.

    > [!NOTE]
    > Když vyberete hodnotu v poli **Skupina TDS**, pole **Skupina TCS** není k dispozici. TDS se počítá, pouze pokud je možnost **Vypočítat srážkovou daň** je nastavena na **Ano** pro zákazníka na stránce **Všichni zákazníci**.

5. Na kartě **Daňové údaje** v části **Informace o společnosti** v poli **Název** můžete vybrat název společnosti pro alternativní adresu, která je pro společnost nastavena.

    V části **Srážková daň** pole **Číslo daňového účtu (TAN)** zobrazuje číslo daňového účtu (TAN) pro vybranou společnost.

6. Na kartě **Řádky faktury** vytvořte řádky faktury a zadejte požadované údaje.

    V části **Skupina pro srážkovou daň** pole **Číslo daňového účtu (TAN)** ukazuje TAN a pole **Skupina TDS** pole zobrazuje skupinu TDS.

7. Vyberte **Srážková daň** k otevření stránky **Dočasné transakce srážkové daně**. Horní část této stránky obsahuje následující pole:

    - **Částka srážkové daně celkem** – Celková TDS, která byla vypočítána pro transakci pro skupinu TDS.
    - **Hodnota** – Celkové procento, které bylo použito k výpočtu TDS pro transakci. Celkové procento je založeno na vzorci, který je definován pro daňové kódy TDS a je připojen ke skupině TDS.
    - **Upravená částka srážkové daně celkem** – Celková upravená částka TDS pro všechny daňové kódy ve skupině TDS.
    - **TDS** – Vybrané zaškrtávací políčko označuje, že je k transakci připojena skupina TDS.

    Políčka na kartách **Přehled**, **Všeobecné** a **Vyrovnání** zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.

8. Vyberte **Mezní hodnota** k otevření stránky **Práh**, kde můžete zkontrolovat mezní limit definovaný pro daňovou složku TDS, která je připojena ke konkrétnímu daňovému kódu TDS.
9. Vyberte **Návrhář vzorců** k otevření stránky **Návrhář vzorců**, kde můžete zkontrolovat vzorec definovaný pro konkrétní daňový kód TDS.
10. Zaúčtujte fakturu s volným textem. Vypočítaná částka TDS, která je vypočítána pro fakturu s volným textem, se zaúčtuje na účet pohledávek, který je definován pro každý daňový zákon TDS ve skupině TDS. Účty pohledávek pro daňové kódy TDS jsou definovány na stránce **Kódy srážkové daně**.
11. Vyberte **Zaúčtovaná srážková daň** k otevření stránky **Transakce srážkové daně**. Pole **Hodnota** zobrazuje celkové procento, které bylo použito k výpočtu TDS pro transakci.

    Pole na kartách **Přehled**, **Všeobecné** a **Množství** zobrazují částky TDS, které byly vypočítány na řádcích faktury.

12. Zkontrolujte informace o výpočtu TDS pro každý daňový kód TDS, který je připojen ke skupině TDS.
