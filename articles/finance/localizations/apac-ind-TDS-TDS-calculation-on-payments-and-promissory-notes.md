---
title: Výpočet TDS u plateb a vlastních směnek
description: Toto téma poskytuje referenční informace o různých platebních transakcích, ze kterých se počítá daň odečtená u zdroje (TDS).
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
ms.openlocfilehash: 7f38a8c4b0416abb10bfdaf95c3379e964e9a41e
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726455"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>Výpočet TDS u plateb a vlastních směnek

[!include [banner](../includes/banner.md)]

Toto téma poskytuje referenční informace o různých platebních transakcích, ze kterých se počítá daň odečtená u zdroje (TDS).

| Sériové číslo | Typ transakce | Částka transakce | Název stránky a cesta | Typ účtu a typ protiúčtu |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Záloha / platba na fakturu (splatná TDS) | Má dáti nebo Dal | <ul><li>Hlavní kniha (**Hlavní kniha \> Položky deníku \> Hlavní deníky**)</li><li>Deník faktur (**Závazky \> Faktury \> Deník faktur**)</li><li>Deník plateb (**Závazky \> Platby \> Deník plateb dodavatele**)</li></ul> | Dodavatel (Dr.), Banka (Cr.) |
| 2             | Záloha / platba na fakturu (nákup od zákazníka – splatný TDS) | Má dáti nebo Dal | <ul><li>Hlavní kniha (**Hlavní kniha \> Položky deníku \> Hlavní deníky**)</li><li>Deník faktur (**Závazky \> Faktury \> Deník faktur**)</li><li>Deník plateb (**Závazky \> Platby \> Deník plateb dodavatele**)</li></ul> | Zákazník (Dr.), Banka (Cr.) |
| 3             | Vlastní směnky | Debet | Deník vlastních vystavených směnek (**Závazky \> Platby \> Vlastní směnky \> Deník vlastních vystavených směnek**) | Dodavatel (Dr.), Hlavní kniha (Cr.) |
| 4             | Různé příjmy (pohledávky TDS) | Má dáti nebo Dal | Hlavní kniha (**Hlavní kniha \> Položky deníku \> Hlavní deníky**) | Banka (Dr.), Hlavní kniha (Cr.) |
| 5             | Ostatní výdaje (splatné TDS) | Má dáti nebo Dal | Hlavní kniha (**Hlavní kniha \> Položky deníku \> Hlavní deníky**) | Banka (Dr.), Hlavní kniha (Cr.) |

Podle těchto pokynů vypočítáte TDS u plateb a směnek.

1. Na stránkách deníku vytvořte řádky deníku. Vyberte typ účtu a typ protiúčtu.
2. Vyberte **Funkce \> Vyrovnání** k otevření stránky **Otevřete úpravy transakcí**. Poté vyberte konkrétní fakturu, kterou je třeba uhradit. Pokud již byl TDS vypočítán na úrovni faktury, pole **Původ částky** zobrazuje základní částku, ze které byl TDS vypočítán. Pole **Částka TDS** zobrazuje částku TDS, která byla vypočítána pro transakci. Pole **Částka** zobrazuje čistou částku platby (tj. částka platby po odečtení TDS).

    > [!NOTE]
    > U platby provedené na základě faktury platí následující podmínky:
    >
    > - Pokud je částka platby a částka faktury stejná, TDS se nevypočítá, pokud již byla vypočítána na úrovni faktury.
    > - Pokud je částka faktury po odečtení částky TDS větší než částka platby, TDS se nepočítá.
    > - Pokud je částka faktury po odečtení částky TDS menší než částka platby, TDS se vypočítá ze částky, která přesahuje částku faktury.

3. Na stránce **Doklad deníku** na kartě **Přehled** v poli **Skupiny TDS** zkontrolujte nebo změňte výchozí skupinu TDS definovanou pro dodavatele nebo zákazníka. TDS, který se počítá na řádcích deníku, je založen na vzorci, který je definován pro daňové kódy TDS ve skupině TDS.

    > [!NOTE]
    > TDS se počítá, pouze pokud je možnost **Vypočítat srážkovou daň** je nastavena na **Ano** pro dodavatele na stránce **Dodavatelé**.

4. Na kartě **Daňové údaje** v části **Informace o společnosti** v poli **Název** můžete vybrat název společnosti pro alternativní adresy, které jsou pro společnost nastaveny.

    V části **Srážková daň** pole **Povaha posuzovaného** ukazuje povahu hodnocené kategorie dodavatele nebo zákazníka. Pole **Číslo daňového účtu (TAN)** zobrazuje číslo daňového účtu (TAN) vybrané společnosti.

5. Vyberte **Tlačítko srážkové daně \> srážková daň** k otevřené stránky **Dočasné transakce srážkové daně**. Horní část této stránky obsahuje následující pole:

    - **Částka srážkové daně celkem** – Celková TDS, která byla vypočítána pro transakci pro skupinu TDS.
    - **Hodnota** – Celkové procento, které bylo použito k výpočtu TDS pro transakci. Celkové procento je založeno na vzorci, který je definován pro daňové kódy TDS a je připojen ke skupině TDS.
    - **Upravená částka srážkové daně celkem** – Celková upravená částka TDS pro všechny daňové kódy ve skupině TDS.
    - **TDS** – Vybrané zaškrtávací políčko označuje, že je k transakci připojena skupina TDS.

    Políčka na kartách **Přehled**, **Všeobecné** a **Vyrovnání** zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.

6. Vyberte **Mezní hodnota** k otevření stránky **Práh**, kde můžete zkontrolovat mezní limit definovaný pro daňovou složku TDS, která je připojena ke konkrétnímu daňovému kódu TDS.
7. Vyberte **Návrhář vzorců** k otevření stránky **Návrhář vzorců**, kde můžete zkontrolovat vzorec definovaný pro konkrétní daňový kód TDS.
8. Zavřete stránky **Návrhář vzorců** a **Dočasné transakce srážkové daně** pro návrat na stránku **Doklad deníku** .
9. Proveďte ověření a zaúčtování deníku. Vypočítaná částka TDS se zaúčtuje na splatný účet, který je definován pro každý daňový zákon TDS ve skupině TDS. Účty pohledávek pro daňové kódy TDS jsou definovány na stránce **Kódy srážkové daně**.
10. Vyberte **Zaúčtovaná srážková daň** k otevření stránky **Transakce srážkové daně**. Pole **Hodnota** zobrazuje celkové procento, které bylo použito k výpočtu TDS pro transakci.

    Pole na kartách **Přehled**, **Všeobecné** a **Množství** zobrazují částky TDS, které byly vypočítány pro skupinu TDS, která je připojena k transakci.

11. Zkontrolujte informace o výpočtu TDS pro každý daňový kód TDS, který je připojen ke skupině TDS.

## <a name="generate-payments"></a>Generovat platby

Ke generování plateb postupujte následovně.

1. Proveďte jeden z následujících kroků:

    - Přejděte na **Pohledávky \> Platby \> Deník plateb dodavatele**.
    - Přejděte na **Pohledávky \> Platby \> Deník plateb zákazníkovi**.
    - Přejděte na **Závazky \> Platby \> Vlastní směnky \> Deník vlastních vystavených směnek**.
    - Přejděte na **Pohledávky \> Platby \> Cizí směnka \> Deník vystavení cizích směnek**.
    - Přejděte na **Pohledávky \> Platby \> Cizí směnka \> Deník opětovného vystavení cizích směnek**.

2. Vybrat **řádky**.
3. Vyberte **Funkce \> Generovat platby**.
