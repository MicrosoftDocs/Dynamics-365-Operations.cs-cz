---
title: Seskupování řádků vyskladnění
description: Toto téma poskytuje přehled seskupení řádků výdeje.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424147"
---
# <a name="pick-line-grouping"></a>Seskupování řádků vyskladnění

[!include [banner](../includes/banner.md)]

V seskupování řádků výdeje lze kombinovat více řádků práce, které mají stejné zboží a umístění, do jednoho výeje, které se uživateli zobrazí v mobilním zařízení. Pracovníci skladu tedy mohou získat nejúčinnější pokyny, které jsou možné, ale je zachováno i povinné oddělení pracovních řádků v systému (například pro různé kontejnery a objednávky).

## <a name="set-up-pick-line-grouping"></a>Nastavit seskupování řádků výdeje

### <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní řařízení \> Položky nabídky mobilního zařízení** a vytvořte novou položku nabídky nazvanou **Výdej řádku prodejní skupiny – Řízeno uživatelem**.
2. V nabídce **Položky nabídky mobilního zařízení** nastavtenásledující hodnoty:

    - V poli **Název položky nabídky** zadejte **Vyskladňování prodeje - řádek skupiny**.
    - V poli **Nadpis** zadejte **Vyskladňování prodeje - řádek skupiny**.
    - V poli **Režim** vyberte **Práce**.
    - Nastavte hodnotu možnosti **Použít stávající práci** na **Ano**.

3. Na pevné záložce **Obecné** můžete nastavit následující hodnoty:

    - V poli **Řídí** nastavte **Řízeno uživatelem**.
    - Nastavte volbu **Generovat registrační značku vozidla** na **Ano**.
    - Nastavte možnost **Výdej skupiny** na **Ano**.

4. Na pevné záložce **Pracovní třídy** nakonfigurujte pomocí následujícího postupu platné třídy práce pro položku nabídky mobilního zařízení:

    1. Zvolte **Nové**.
    2. V poli **ID pracovní třídy** vyberte **Prodej** nebo **Výdej PO** v závislosti na skladu, který budete používat.
    3. V poli **Typ pracovního příkazu** vyberte možnost **Prodejní objednávky**.

### <a name="set-up-a-mobile-device-menu"></a>Vytvořit nabídku mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**. 
1. Přidejte položku nabídky, kterou jste právě vytvořili, do požadované nabídky.

### <a name="set-up-a-work-template"></a>Nastavit šablonu práce

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. Najděte šablonu práce, která má být použita s touto funkcí. V tomto příkladu vyberte šablonu pro práci Contoso **51 výdej ddo fáze**.
1. V nabídce vyberte příkaz **Upravit dotaz**.
1. Na kartě **Řazení** vyberte možnost **Přidat** a nastavte následující hodnoty:

    - V poli **Tabulka** vyberte **Dočasné pracovní transakce**.
    - V poli **Odvozená tabulka** vyberte **Dočasné pracovní transakce**.
    - V poli **Pole** zvolte **Číslo položky**.
    - V poli **Směr vyhledávání** vyberte **Vzestupně**.

> [!NOTE]
> Aby funkce seskupování řádků vyskladnění fungovala, musí být pracovní řádky seřazeny podle ID položky. Pokud řádky se stejnými položkami nejsou seřazeny jeden po druhém, nebudou seskupeny.

## <a name="example"></a>Příklad

### <a name="create-picking-work"></a>Vytvořit práci výdeje

Dříve než můžete nastavit seskupování řádků vyskladnění, musíte vytvořit nějakou způsobilou výstupní práci.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
2. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku. 
3. V poli **Účet odběratele** vyberte libovolného zákazníka. 
4. Na pevné záložce **Obecné** v poli **Sklad** vyberte **51**. Pak vyberte **OK**.
5. Do volby **Řádky prodejní objednávky** přidejte následujících šest řádků:

    - **Řádek 1:** v poli **Číslo položky** vyberte **M9200**. Do pole **Množství** zadejte **3**.
    - **Řádek 2:** v poli **Číslo položky** vyberte **M9201**. Do pole **Množství** zadejte **3**. 
    - **Řádek 3:** v poli **Číslo položky** vyberte **M9202**. Do pole **Množství** zadejte **2**. 
    - **Řádek 4:** v poli **Číslo položky** vyberte **M9200**. Do pole **Množství** zadejte **1**. 
    - **Řádek 5:** v poli **Číslo položky** vyberte **M9200**. Do pole **Množství** zadejte **3**.
    - **Řádek 6:** v poli **Číslo položky** vyberte **M9202**. Do pole **Množství** zadejte **7**. 

    Zde je souhrn celkových množství pro každou položku:

    - **Položka M9200:** každá 7
    - **Položka M9201:** každá 3
    - **Položka M9202:** každá 9

6. Před vydáním objednávek do skladu je třeba zajistit, aby skladová místa pro vyskladnění měla dostatečné množství zásob pro všechny položky ve všech objednávkách. Zkontrolujte nastavení **Směrnice skladového místa** pro určení, která výdejní skladová místa se použijí pro výdej prodejní objednávky.
7. Rezervace zásob a jejich uvolnění do skladu. Je vytvořeno ID práce, které má šest řádků. Řádky jsou seřazeny podle čísla položky.

### <a name="run-the-mobile-device-flow"></a>Spustit tok mobilního zařízení

1. V mobilním zařízení vyberte nabídku obsahující novou položku nabídky mobilního zařízení.
1. Vyberte položku nabídky **Vyskladnění prodeje – řádek skupiny** a zahajte vyskladnění.

    Po výběru nabídky a zadání ID práce se zobrazí krok vyskladnění, ve kterém jsou seskupeny všechny řádky vyskladnění pro položku M9200. Obdržíte pokyn k vyzvednutí 7 jednotlivých položek M9200.

1. Potvrďte krok vyskladnění. 
1. Přejděte na obrazovku klienta probíhající práce a všimněte si, že všechny tři řádky vyskladnění pro položku M9200 byly uzavřeny současně.

    Uveden je řádek práce 4.

1. Potvrďte krok vyskladnění.

    Poslední krok vyskladnění na mobilním zařízení agreguje poslední dva řádky vyskladnění z pracovní objednávky.

1. Dokončete krok vyskladnění pro 9 kusů položky M9202.
1. Pro dokončení práce potvrďte krok vložení a dalších párů vyskladnění/vložení.

> [!NOTE]
> - Řádky práce lze seskupit pouze v případě, že jdou po sobě.
> - Následující funkce není podporována:
>
>    - Položka se skutečnou hmotností. Pokud je v práci nějaké zboží se skutečnou hmotností, zobrazí se před začátkem vyskladnění chybová zpráva.
>    - Výdej kusů.
>    - Řádky práce s nedokončenou doplňovací prací.
>    - Naměrné vyskladnění.
>    - Opakované přidělení zboží při krátkodobém vyskladnění


[!INCLUDE[footer-include](../../includes/footer-banner.md)]