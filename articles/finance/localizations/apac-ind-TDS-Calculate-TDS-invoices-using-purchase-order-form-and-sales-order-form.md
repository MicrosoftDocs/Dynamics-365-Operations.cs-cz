---
title: Výpočet faktur TDS pomocí formuláře nákupní objednávky a formuláře prodejní objednávky
description: Toto téma obsahuje kroky pro výpočet daně odečtené u zdroje (TDS) u různých typů faktur.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023078"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Výpočet faktur TDS pomocí formuláře nákupní objednávky a formuláře prodejní objednávky

[!include [banner](../includes/banner.md)]

Toto téma obsahuje kroky pro výpočet daně odečtené u zdroje (TDS) u různých typů faktur pomocí stránek **Nákupní objednávka**, **Deník nákupů**, **Paušální objednávka** a **Prodejní objednávka**.

1. Pomocí uvedené stránky vytvoříte nákupní objednávku, deník nákupu, paušální nákupní objednávku nebo prodejní objednávku. Zadejte požadované údaje.

2. Vyberte kartu **Nastavení** pro zobrazení povahy hodnotitele dodavatele nebo zákazníka. Tyto informace jsou uvedeny v poli **Povaha posuzovaného** pod skupinou poli **Skupina pro srážkovou daň**.

3. V poli **Skupina TDS** zobrazte nebo upravte výchozí skupinu TDS definovanou pro dodavatele nebo zákazníka.

   > [!NOTE]
   > Pole **Skupina TCS** není k dispozici, když vyberete skupinu TDS v poli **Skupina TDS**. TDS se počítá, pouze pokud je zaškrtnuté políčko **Vypočítat srážkovou daň** pro dodavatele nebo zákazníka na stránce **Všichni dodavatelé** nebo **Všichni zákazníci**.  

4. Vytvořte řádky položek na kartě **Řádky** a zadejte požadované údaje.

5. Vyberte kartu **Nastavení** (na úrovni řádku) pro zobrazení nebo změnu skupiny TDS definované na úrovni záhlaví. Skupina TDS je zobrazena v poli **Skupina TDS**, které je pod skupinou polí **Skupina pro srážkovou daň**.

6. Vyberte kartu **Daňové údaje** a vyberte alternativní adresy, které jsou nastaveny pro název společnosti, který se zobrazuje v tomto poli. Název společnosti je zobrazen v poli **Název**, které je pod skupinou polí **Údaje o společnosti**. 

   TAN vybraného názvu společnosti se zobrazí v poli **Číslo daňového účtu** (**TAN**) pod skupinou polí **Srážková daň**. 

7. Vyberte **Srážková daň** k otevření stránky **Dočasné transakce srážkové daně**. Zobrazte následující pole v horním podokně stránky **Dočasné transakce srážkové daně**.

   - **Částka** **srážkové** **daně** **celkem** – Celková TDS, která byla vypočítána pro transakci pro skupinu TDS.

   - **Hodnota** – Celkové procento, které bylo použito k výpočtu TDS pro transakci. Celkové procento je založeno na vzorci, který je definován pro daňové kódy TDS a je připojen ke skupině TDS.

   - **Upravená částka srážkové daně celkem** – Celková upravená částka TDS pro všechny daňové kódy ve skupině TDS.

   - **TDS** – Pokud je vybráno, je k transakci připojena skupina TDS.

Políčka na kartách **Přehled**, **Všeobecné** a **Vyrovnání** na stránce **Dočasné transakce srážkové daně** zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.

8. Vybrat **Mezní hodnota** k otevření stránky **Mezní hodnota**. Na této stránce si můžete prohlédnout mezní hodnotu definovanou pro daňovou složku TDS připojenou ke konkrétnímu daňovému kódu TDS.

9. Vyberte **Návrhář vzorců** k otevření stránky **Návrhář vzorců**. Na této stránce si můžete prohlédnout vzorec definovaný pro konkrétní daňový kód TDS. 

10. Zaúčtujte fakturu. Částka TDS vypočtená z nákupních faktur se zaúčtuje na účet závazků a částka TDS vypočítaná z prodejních faktur se zaúčtuje na účet pohledávek, který je definován pro každý daňový kód TDS ve skupině TDS. Účty závazků nebo účty pohledávek pro daňové kódy TDS jsou definovány na stránce **Kódy srážkové daně**.

11. Vyberte tlačítko **Dotaz** **> Faktura > Zaúčtovaná srážková daň** k otevření stránky **Transakce srážkové daně**. Pole **Hodnota** zobrazuje celkové procento, které bylo použito k výpočtu TDS pro transakci.

Pole na kartách **Přehled**, **Všeobecné** a **Částka** na stránce **Transakce srážkové daně** zobrazuje informace TDS vypočítané pro transakci. Zkontrolujte informace o výpočtu TDS pro každý daňový kód TDS, který je připojen ke skupině TDS.
