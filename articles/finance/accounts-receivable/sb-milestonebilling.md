---
title: Šablony milníku
description: Toto téma vysvětluje, jak nastavit funkci vyúčtování po milnících ve fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 863ec55c8ba2fcc9d0e624fcca06f4491ce839ac
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462875"
---
# <a name="milestone-billing"></a>Vyúčtování po milnících

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak definovat šablony pro funkci vyúčtování po milnících ve fakturaci předplatného. U každého řádku v šabloně milníku můžete definovat procento nebo částku přidělení. Šablonu milníku pak můžete přiřadit k položkám plánu fakturace, které používají funkci vyúčtování po milnících.

## <a name="add-a-template"></a>Přidat šablonu

Chcete-li přidat šablonu milníku, postupujte takto:

1. Přejděte do nabídky **Fakturace předplatného \> Opakovaná fakturace smlouvy \> Nastavení \> Šablony milníků**.
2. Zvolte **Nové**.
3. Do pole **Šablona milníku** zadejte jedinečný identifikátor nové šablony.
4. Zadejte popis do pole **Popis**.
5. Poté vyberte metodu přidělení v poli **Metoda přidělení**.
6. Volitelné: V poli **Celková částka** zadejte celkovou částku pro šablonu.
7. Chcete-li přidat řádek, vyberte možnost **Přidat**. Poté v poli **Číslo položky** vyberte číslo položky pro nový řádek.
8. Proveďte některý z následujících kroků v závislosti na hodnotě, kterou jste vybrali v poli **Metoda přidělení**:

    - Pokud jste jako metodu přidělení vybrali **Procento**, zadejte v poli **Procento** hodnotu procenta přidělení pro každý řádek. Pokud zadáte procenta, součet procent, který se zobrazí v poli **Celkové procento**, se musí rovnat **100**.
    - Pokud jste jako metodu přidělení vybrali **Proměnlivá částka**, zadejte v poli **Částka** hodnotu částky pro každý řádek.
    - Pokud jste jako metodu přidělení vybrali **Stejnou částku**, nemusíte částku zadávat. Každý řádek bude aktualizován správným procentem a částkou na základě počtu položek, které jsou přidány do šablony.

9. Zvolte možnost **Uložit**.

## <a name="delete-a-template"></a>Odstranění šablony

Chcete-li odstranit šablonu milníku, postupujte takto:

1. Vyberte jeden nebo více řádků k odstranění a poté vyberte příkaz **Odstranit**.
2. Po zobrazení výzvy k potvrzení akce vyberte **Ano**.

## <a name="milestone-template-fields"></a>Pole šablony milníku

Stránka **Šablona milníku** obsahuje následující pole.

| Pole | Popis |
|-------|-------------| 
| Šablona milníku | Jedinečný identifikátor šablony milníku. |
| Popis | Popis šablony milníku. |
| Metoda přidělení | <p>Vyberte metodu přidělení:</p><ul><li>**Procento dokončení** – Pro každý řádek se použije kumulativní hodnota dokončení.</li><li>**Procento** – Přidělí se procentuální částka. Součet všech procent se musí rovnat 100.</li><li>**Proměnlivá částka** – Přidělí se zadaná částka. Částka přidělení je specifikována na úrovni transakce.</li><li>**Stejná částka** – Procenta přidělení se vypočítají automaticky a rovnoměrně rozdělí mezi položky v šabloně.</li></ul> |
| Celkové množství | Zadejte částku milníku pro šablonu. |
| **Řádky** | |
| Číslo položky | Vyberte číslo položky pro šablonu milníku. |
| Název produktu | Název položky. |
| Procento | <p>Zadejte procento přidělení pro řádek:</p><ul><li>Pokud je pole **Metoda přidělení** nastaveno na **Procento**, zadejte procento pro řádek.</li><li>Pokud je pole **Metoda přidělení** nastaveno na **Stejná částka**, procento se automaticky rozdělí na stejná procenta na základě počtu položek v šabloně.</li></ul><p>Součet všech procent se musí rovnat 100.</p><p>Pokud je hodnota **Celková částka** uvedena v záhlaví a vy změníte **Procento** pro řádek, aktualizuje se hodnota **Částka**. Naopak, pokud změníte hodnotu **Částka**, aktualizuje se **Procento**.</p> |
| Částka | <p>Částka přidělení pro řádek:</p><ul><li>Pokud je pole **Metoda přidělení** nastaveno na **Proměnlivá částka**, zadejte částku pro řádek.</li><li>Pokud je pole **Metoda přidělení** nastaveno na hodnotu **Stejná částka**, částka se automaticky rozdělí na stejné částky na základě počtu položek v šabloně a hodnoty **Celková částka** uvedené v záhlaví.</li></ul><p>Součet všech částek se musí rovnat hodnotě **Celková částka** uvedené v záhlaví.</p><p>Pokud je **Celková částka** uvedena v záhlaví a vy změníte hodnotu **Částka** pro řádek, aktualizuje se hodnota **Procento**. Naopak, pokud změníte hodnotu **Procento**, aktualizuje se **Částka**.</p> |
| **Součty** | |
| Celkové procento | Součet procent. Součet všech procent se musí rovnat 100. |
| Celkové množství | Součet hodnot **Částka** za všechny řádky. Tento součet se musí rovnat hodnotě **Celková částka** uvedené v záhlaví. |
| Zbývající částka | Zbývající částka. Hodnota se vypočítá jako **Celková částka** ze záhlaví mínus součet hodnot **Částka** za všechny řádky.|

## <a name="milestone-allocation"></a>Přidělení milníku

Než začnete používat funkci milníku, měli byste dokončit tyto úkoly.

1. Přidejte jednu nebo více šablon milníků.
2. Vytvořte skupinu plánu fakturace. Upřesněte **Milník** jako typ položky a vyberte šablonu.
3. Na stránce **Nastavení položky** (**Fakturace předplatného \> Opakovaná fakturace smlouvy \> Nastavení \> Položky**) vyberte vztah položky a šablonu milníku pro nastavení položky.

Po vytvoření šablon milníků, skupin plánu fakturace a položek můžete vytvořit plán fakturace, který využívá funkci milníku.

Chcete-li nastavit plán fakturace, který používá milníky, postupujte takto.

1. V seznamu **Všechny/aktivní plány fakturace** na stránce **Plány fakturace** vyberte možnost **Nový**.
2. Na stránce **Všechny plány fakturace** vytvořte nový plán fakturace a zadejte účet odběratele a počáteční datum.
3. V sekci **Řádky plánu fakturace** vyberte **Přidat řádek**. Poté přidejte číslo položky a nastavte **Typ položky** na **Milník**.

    Pokud je pro položku nastavena výchozí šablona milníku, budou události milníku automaticky přidány do řádků plánu fakturace. Data ukončení jsou v řádcích milníku prázdná.

    Pokud položka nemá nastavenu žádnou šablonu milníku, vyberte **Přidělení milníku**. Poté na stránce **Přidělení milníku** vyberte šablonu milníku a proveďte požadované aktualizace. Poté vyberte **Zavřít** a vraťte se k plánu fakturace a dokončete jeho vytváření.

4. Chcete-li vytvořit faktury pro plán fakturace, musíte aktualizovat datum ukončení pro každou událost milníku. Jde-li o jeden plán fakturace, můžete aktualizovat datum ukončení události milníku na řádcích plánu fakturace. Chcete-li aktualizovat více plánů fakturace, vyberte příkaz **Aktualizovat proces data dokončení**.
5. Po aktualizaci data dokončení můžete vytvořit fakturu. Jde-li o jeden plán fakturace, vyberte příkaz **Generovat fakturu** na stránce **Všechny plány fakturace**. Chcete-li vytvořit faktury pro více plánů fakturace, vyberte příkaz **Generovat fakturu** nebo **Generovat dávkové zpracování faktur** v sekci **Periodické úkoly**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Úprava přidělení milníku na řádku plánu fakturace

Chcete-li upravit přidělení milníku na řádku plánu fakturace, postupujte takto.

1. Na stránce **Plány účtování** > **Všechny nebo aktivní plány účtování** vyberte číslo plánu, který chcete upravit, v poli **Číslo plánu**.
2. V sekci **Řádky plánu fakturace** zadejte položku, určete **Milník** jako typ položky a vyberte **Přidělení milníku**.
3. V poli **Šablona milníku** vyberte šablonu milníku.
4. Vyberte možnost **Proces**. Řádky šablony milníku se automaticky přidají do řádků plánu fakturace.

## <a name="milestone-allocation-fields"></a>Pole přidělení milníku

Stránka **Přidělení milníku** obsahuje následující pole.

| Pole | Popis |
|-------|-------------|
| Nadřazená položka | Číslo nadřízené položky. |
| Rozšířená cena | <p>Rozšířená cena položky. Hodnota odpovídá hodnotě **Čistá částka** řádku plánu fakturace.</p></p>Pro nadřazenou položku milníku je výchozí hodnotou **Celková částka**, která je určena pro šablonu milníku. Pokud je celková částka 0 (nula), výchozí hodnotou je **Čistá částka** řádku plánu fakturace.</p> |
| Šablona milníku | Identifikátor šablony milníku pro řádkovou položku. |
| Popis šablony | Popis šablony milníku. |
| Metoda přidělení | Metoda přidělení, která se používá pro šablonu milníku. |
| **Řádky** | Výchozí hodnoty pro všechny řádky jsou založeny na vybrané šabloně milníku. Můžete je podle potřeby měnit. |
| Číslo položky | Číslo položky pro šablonu přidělení milníku. |
| Název produktu | Název produktu. |
| Procento | <p>Procento přidělení pro řádek. Součet všech procent se musí rovnat 100.</p><p>Když pro řádek změníte hodnotu **Procento**, aktualizuje se **Čistá částka**. Naopak, pokud změníte hodnotu **Čistá částka**, aktualizuje se **Procento**.</p> |
| Čistá částka | <p>Částka přidělení pro řádek. Součet čistých částek za všechny řádky se musí rovnat hodnotě **Rozšířená cena** uvedené v záhlaví.</p><p>Když pro řádek změníte hodnotu **Čistá částka**, aktualizuje se **Procento**. Naopak, pokud změníte hodnotu **Procento**, aktualizuje se **Čistá částka**.</p> |
| **Součty** | |
| Celkové procento | Součet hodnot **Procento** za všechny řádky. Tato částka se musí rovnat 100. |
| Celkové množství | Součet hodnot **Čistá částka** za všechny řádky. Tento součet se musí rovnat hodnotě **Rozšířená cena** uvedené v záhlaví. |
| Zbývající částka | Zbývající částka. Hodnota se vypočítá jako **Rozšířená cena** ze záhlaví mínus součet hodnot **Čistá částka** za všechny řádky. Konečná částka musí být 0 (nula). |
