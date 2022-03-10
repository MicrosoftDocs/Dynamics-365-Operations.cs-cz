---
title: Výpočet TDS na fakturách pomocí deníků
description: Toto téma obsahuje kroky pro výpočet daně odečtené u zdroje (TDS) u deníků.
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
ms.openlocfilehash: fde81efed6b8a72e2149056f0196e4f9d60e59f2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345512"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>Výpočet TDS na fakturách pomocí deníků

[!include [banner](../includes/banner.md)]

Toto téma obsahuje kroky pro výpočet daně odečtené u zdroje (TDS) u deníků.

Začněte otevřením stránky **Hlavní knihy** (**Hlavní kniha > Položky deníku > Hlavní deníky**).

[![Hlavní deníky.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Vytvořte řádky deníku pomocí formulářů deníku, které jsou uvedeny v tabulce. Vyberte typ účtu a typ protiúčtu a zadejte částku za transakci. 

   > [!NOTE]
   > Na stránce **Deník schválení faktury** vyberte **Najít doklady** a vyberte faktury pro výpočet TDS. Zobrazte faktury vytvořené na stránce **Registr faktur** nebo stránce **Najít doklady**.  

2. Na kartě **Obecné** stránky **Doklad deníku** v poli **Skupiny TDS** zkontrolujte nebo změňte výchozí skupinu TDS definovanou pro dodavatele nebo zákazníka. Částka TDS, která se počítá na řádcích deníku, je založena na vzorci, který je definován pro daňové kódy TDS ve **skupině TDS**. 

   > [!NOTE]
   > Když v seznamu vyberete skupinu TDS v poli **Skupina TDS**, pole **Skupina pro srážkovou daň** a **Skupina TCS** nebudou k dispozici. Pole **Skupina pro srážkovou daň** je k dispozici pouze na stránce **Obecný deník**. TDS se počítá, pouze pokud je zaškrtnuté políčko **Vypočítat srážkovou daň** pro dodavatele nebo zákazníka na stránce **Všichni dodavatelé** nebo **Všichni zákazníci**.   

3. Vyberte kartu **Daňové údaje**. V případě potřeby vyberte alternativní adresy společnosti, které jsou nastaveny pro společnost v tomto poli. Název společnosti je zobrazen v poli **Název**, které je pod skupinou polí **Údaje o společnosti**. 

4. Ve skupině polí **Srážková daň** v poli **Povaha posuzovaného** naleznete povahu hodnocené kategorie dodavatele nebo zákazníka. V poli **Číslo daňového účtu** (**TAN**) vidíte TAN vybraného názvu společnosti, který se zobrazí.  

5. Vyberte **Srážková daň** v nabídce **Srážková daň** k otevřené stránky **Dočasné transakce srážkové daně**. V horním podokně stránky **Dočasné transakce srážkové daně** se zobrazí následující pole.

   - **Částka srážkové daně celkem** – Celková TDS, která byla vypočítána pro transakci pro skupinu TDS.

   - **Hodnota** – Celkové procento, které bylo použito k výpočtu TDS pro transakci. Celkové procento je založeno na vzorci, který je definován pro daňové kódy TDS a je připojen ke skupině TDS.

   - **Upravená částka srážkové daně celkem** – Celková upravená částka TDS pro všechny daňové kódy ve skupině TDS.

   - **TDS** – Pokud je vybráno, je k transakci připojena skupina TDS.

  Políčka na kartách **Přehled**, **Všeobecné** a **Vyrovnání** na stránce **Dočasné transakce srážkové daně** zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.

6. Vybrat **Mezní hodnota** k otevření stránky **Mezní hodnota**. Na této stránce si můžete prohlédnout mezní hodnotu a mezní hodnotu výjimky definovanou pro daňovou složku TDS připojenou ke konkrétnímu daňovému kódu TDS.

   Vyberte **Návrhář vzorců** k otevření formuláře **Návrhář vzorců**. Na této stránce si můžete prohlédnout vzorec definovaný pro konkrétní daňový kód TDS. Zavřete stránky **Návrhář vzorců** a **Dočasné transakce srážkové daně** pro návrat na stránku **Doklad deníku** .

8. Zadejte další požadované údaje. Proveďte ověření a zaúčtování deníku. Částka TDS, která se počítá z nákupních faktur, se zaúčtuje na účet závazků. Vypočítaná částka TDS, která je vypočítána na prodejních fakturách, se zaúčtuje na účet pohledávek, který je definován pro každý daňový zákon TDS ve skupině TDS. Účty závazků nebo účty pohledávek pro daňové kódy TDS jsou definovány na stránce **Kódy srážkové daně**.

9. Vyberte **Zaúčtovaná srážková daň** k otevření stránky **Transakce srážkové daně**. Pole **Hodnota** zobrazuje celkové procento, které bylo použito k výpočtu TDS pro transakci.

   Políčka na kartách **Přehled**, **Všeobecné** a **Částka** na stránce Dočasné transakce srážkové daně zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.
