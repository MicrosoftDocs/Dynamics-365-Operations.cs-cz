---
title: Seskupování řádků vyskladnění
description: Toto téma poskytuje přehled seskupení řádků výdeje.
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e70244d46ec2787fefdb097d0354af7910b55e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989711"
---
# <a name="pick-line-grouping"></a>Seskupování řádků vyskladnění

[!include [banner](../includes/banner.md)]

V seskupování řádků výdeje lze kombinovat více řádků práce, které mají stejné zboží a umístění, do jednoho výdeje, které se uživateli zobrazí v mobilním zařízení. Pracovníci skladu tedy mohou získat nejúčinnější pokyny, které jsou možné, ale je zachováno i povinné oddělení pracovních řádků v systému (například pro různé kontejnery a objednávky).

## <a name="turn-on-the-pick-line-grouping-feature"></a>Zapnutí funkce seskupení řádků práce výdeje

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou použít pracovní prostor [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zkontrolovat stav této funkce a zapnout ji, je-li to potřeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Seskupení řádků vyskladnění*

## <a name="set-up-pick-line-grouping"></a>Nastavit seskupování řádků výdeje

### <a name="create-a-mobile-device-menu-item"></a>Vytvoření položky nabídky mobilních zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně akcí zvolte **Nový**.
1. V poli **Název položky nabídky** zadejte *Vyskladnění řádků skupiny prodejů*.
1. V poli **Nadpis** zadejte *Vyskladnění řádků skupiny prodejů*. Tento název se zobrazí v nabídce mobilního zařízení.
1. V poli **Režim** vyberte *Práce*.
1. Nastavte hodnotu možnosti **Použít stávající práci** na *Ano*.
1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - V poli **Řídí** nastavte *Řízeno uživatelem*.
    - Nastavte volbu **Generovat registrační značku vozidla** na *Ano*.
    - Nastavte možnost **Výdej skupiny** na *Ano*.
    - Potvrďte výchozí hodnoty ve všech zbývajících možnostech.

1. Nakonfigurujte pomocí následujícího postupu platné třídy práce pro položku nabídky mobilního zařízení:

    1. Na kartě s náhledem **Pracovní třídy** vyberte **Nová**.
    2. V poli **ID pracovní třídy** můžete vybrat *Prodej* nebo *Výdej PO* v závislosti na skladu, který budete používat. V tomto scénáři vyberte *Výdej PO*.

        Pole **Typ pracovního příkazu** je automaticky nastaveno na *Prodejní objednávky*.

### <a name="set-up-a-mobile-device-menu"></a>Vytvořit nabídku mobilního zařízení

Pomocí těchto kroků přidejte do nabídky položku, kterou jste právě vytvořili, do nabídky **Odchozí**.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. V podokně akcí vyberte **Upravit**.
1. V podokně seznamu jsou zobrazeny všechny nabídky mobilních zařízení. V seznamu vyberte *Odchozí*.
1. V mřížce **Dostupné nabídky a položky nabídky** najděte a vyberte položku nabídky *Vyzvednutí řádku prodejní položky*, kterou jste právě vytvořili.
1. Stisknutím tlačítka se šipkou doprava přesuňte položku nabídky *Výběr řádku skupiny prodeje* do seznamu **Struktura nabídky**.
1. Pomocí šipky nahoru nebo tlačítek šipky dolů přesuňte položku nabídky na požadované místo ve struktuře nabídky.
1. V podokně akcí vyberte **Uložit**.

### <a name="set-up-a-work-template"></a>Nastavit šablonu práce

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.
1. V mřížce **Přehled** vyhledejte a vyberte pracovní šablonu, která by měla být použita s touto funkcí. V tomto scénáři vyberte šablonu *51 vybrat pro fázi*.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazu na kartě **Třídění** přidejte tlačítkem **Přidat** řádek a pak nastavte následující hodnoty pro nový řádek:

    - Ve sloupci **Tabulka** vyberte *Dočasné pracovní transakce*.
    - Ve sloupci **Odvozená tabulka** vyberte *Dočasné pracovní transakce*.
    - Ve sloupci **Pole** zvolte *Číslo položky*.
    - Ve sloupci **Směr vyhledávání** vyberte *Vzestupně*.

1. Volbou **OK** uložte svá nastavení a zavřete dialogové okno.
1. Může se zobrazit následující zpráva: „Seskupení bude resetováno, pokračovat?“ Pokračujte výběrem tlačítka **Ano**.

> [!IMPORTANT]
> Aby funkce seskupování řádků vyskladnění fungovala, musí být pracovní řádky seřazeny podle ID položky. Pokud řádky se stejnými položkami nejsou seřazeny jeden po druhém, nebudou seskupeny.

## <a name="example"></a>Příklad

### <a name="create-picking-work"></a>Vytvořit práci výdeje

Dříve než můžete nastavit seskupování řádků vyskladnění, musíte vytvořit nějakou způsobilou výstupní práci.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.
1. V poli **Účet odběratele** vyberte *US-004*.
1. Na pevné záložce **Obecné** v poli **Sklad** vyberte *51*.
1. Vyberte **OK**.
1. Na kartě s náhledem **Řádky prodejní objednávky** přidejte následujících šest řádků:

    - **Řádek 1:** v poli **Číslo položky** vyberte *M9200*. Do pole **Množství** zadejte *3*.
    - **Řádek 2:** v poli **Číslo položky** vyberte *M9201*. Do pole **Množství** zadejte *3*.
    - **Řádek 3:** v poli **Číslo položky** vyberte *M9202*. Do pole **Množství** zadejte *2*.
    - **Řádek 4:** v poli **Číslo položky** vyberte *M9200*. Do pole **Množství** zadejte *1*.
    - **Řádek 5:** v poli **Číslo položky** vyberte *M9200*. Do pole **Množství** zadejte *3*.
    - **Řádek 6:** v poli **Číslo položky** vyberte *M9202*. Do pole **Množství** zadejte *7*.

    Zde je souhrn celkových množství pro každou položku:

    - **Položka M9200:** *7* ks
    - **Položka M9201:** *3* ks
    - **Položka M9202:** *9* ks

1. Před vydáním objednávek do skladu je třeba zajistit, aby skladová místa pro vyskladnění měla dostatečné množství zásob pro všechny položky ve všech objednávkách. Zkontrolujte nastavení **Směrnice skladového místa** pro určení, která výdejní skladová místa se použijí pro výdej prodejní objednávky. Pokud používáte prostředí ukázkových dat Contoso pro sklad *51*, potvrďte, že jsou k dispozici zásoby.

    Nyní musíte rezervovat zásoby pro každý řádek.

1. Na kartě s náhledem **Řádky prodejní objednávky** vyberte jeden z řádků, které je třeba rezervovat.
1. V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** k použití rezervace. Poté stránku zavřete.
1. Opakujte kroky 8 až 10 pro zbývající řádky, které je třeba rezervovat.

    Nyní musíte vydat prodejní objednávku do skladu.

1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Zobrazí se zpráva s oznámením, že byla vytvořena zásilka a vlna a že vlna byla odeslána k dávkovému spuštění.

    Po dokončení vlny a všech následných úloh se vytvoří ID práce pro práci, která má šest řádků. Řádky jsou seřazeny podle čísla položky.

1. Přejděte na **Řízení skladu \> Práce \> Všechna práce** k zobrazení práce, která byla vytvořena. Poznamenejte si hodnotu **ID práce**, protože ji budete potřebovat v dalším postupu.

### <a name="initiate-picking-from-the-mobile-device"></a>Zahájení výběru z mobilního zařízení

1. Přihlaste se do mobilního zařízení jako uživatel, který je nastaven pro sklad *51*.
1. V mobilním zařízení vyberte nabídku obsahující novou položku nabídky mobilního zařízení. V tomto scénáři vyberte **Odchozí**.
1. Vyberte položku nabídky **Vyskladnění skupiny řádku prodeje** a zahajte vyskladnění.
1. Zadejte hodnotu **ID práce**, kterou jste si poznamenali v předchozím postupu.

    Měli byste vidět krok výběru, kde jsou všechny řádky pro výběr položky *M9200* seskupeny a měli byste obdržet pokyn k výběru *7* ks položky *M9200*.

    > [!IMPORTANT]
    > Na mobilním zařízení byla vychystávací práce pro tři vychystávací pracovní linky agregována do jednoho vychystávacího kroku pro uživatele.

1. Potvrďte krok vyskladnění.
1. Přejděte na stránku práce pro ID práce a všimněte si, že všechny tři řádky vyskladnění pro položku *M9200* byly uzavřeny současně.
1. Vraťte se do mobilního zařízení a pokračujte ve výběru. Měl být předložen pracovní řádek 4 pro položku *M9201*. Protože na objednávce byl pouze jeden řádek práce, není co agregovat.
1. Potvrďte krok vyskladnění.
1. Poslední krok vyskladnění na mobilním zařízení agreguje poslední dva řádky vyskladnění z pracovní objednávky.
1. Dokončete krok vyskladnění pro *9* kusů položky *M9202*.
1. Pro dokončení práce potvrďte krok vložení a dalších párů vyskladnění/vložení.

> [!IMPORTANT]
>
> - Řádky práce lze seskupit pouze v případě, že jdou po sobě.
> - Následující funkce není podporována:
>
>   - Položky se skutečnou hmotností
>
>    Pokud je v práci nějaké zboží se skutečnou hmotností, zobrazí se před začátkem vyskladnění chybová zpráva.
>
>   - Výdej kusů
>   - Řádky práce s nedokončenou doplňovací prací
>   - Naměrné vyskladnění
>   - Opakované přidělení zboží při krátkodobém vyskladnění
