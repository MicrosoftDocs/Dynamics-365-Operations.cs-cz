---
title: Účet za údržbu na majetku ve vlastnictví zákazníka
description: Tento článek vysvětluje, jak vytvořit, zpracovat a fakturovat údržbu, která se provádí u majetku, který vlastní vaši zákazníci.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7c2c07f3e3eb76ff20e37e8d5d485dc08232c7a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220415"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Účet za údržbu na majetku ve vlastnictví zákazníka

[!include [banner](../../includes/banner.md)]

funkce *Fakturace pracovního příkazu* umožňuje vytvářet, zpracovávat a fakturovat práce na údržbě majetku, který vlastní vaši zákazníci. Tato funkce umožňuje provádět následující úlohy:

- Připojte zákazníky k majetku, který vlastní.
- Vyberte zákazníka a při vytváření pracovního příkazu zobrazte aktiva, která zákazník vlastní.
- Nastavte nadřazený projekt pro každého zákazníka.
- Zaregistrujte hodiny, položky, výdaje a poplatky proti pracovní objednávce a poté vytvořte návrh faktury pro zákazníka později.

Kromě toho tato funkce poskytuje následující funkce:

- Smlouva o projektu z nadřazeného projektu zákazníka se automaticky zkopíruje do příslušného projektu pracovního příkazu.
- Správa majetku nyní může používat typ transakce projektu *poplatek* v prognózách pracovních objednávek i v denících pracovních objednávkách.

## <a name="turn-on-the-customer-billing-feature"></a>Zapněte funkci fakturace zákazníků:

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Správa a účtování projektu*
- **Název funkce:** *Fakturace pracovního příkazu*

## <a name="example-scenario"></a>Příklad

Pokud se chcete dozvědět, jak tato funkce funguje, projděte si následující ukázkový scénář.

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../../fin-ops-core/fin-ops/get-started/demo-data.md). Dříve než začnete, musíte vybrat právnickou osobu **USMF**.

Tento scénář můžete také použít jako vodítko pro použití této funkce při práci na produkčním systému. V takovém případě však musíte nahradit uvedené hodnoty vlastními hodnotami. Také možná budete postrádat některé typy požadovaných záznamů, jež jsou součástí standardních ukázkových dat.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>Krok 1: Vytvořte pro zákazníka novou smlouvu na projekt

1. Přejděte na **Řízení projektu a účetnictví \> Projekty \> Projektové smlouvy**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Nová projektová smlouva** nastavte následující hodnoty:

    - **Název:** *Velkoobchody Pelican*
    - **Typ financování:** *Zákazník*
    - **Zdroj financování:** *US-013* (*Velkoobchody Pelican*)

1. Vyberte **OK**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>Krok 2: Vytvořte pro zákazníka nový nadřazený projekt

Nadřazený projekt, který zde vytvoříte, se použije při vytváření pracovních příkazů pro zákazníka.

1. Přejděte na **Řízení projektu a účetnictví \> Projekty \> Všechny projekty**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Nový projekt** nastavte následující hodnoty:

    - **Typ projektu:** *Čas a materiál*
    - **Název projektu:** *Pracovní příkazy Pelican Wholesales*
    - **Skupina projektu:** *TM*
    - **ID smlouvy o projektu:** *Pelican Wholesales* (smlouva, kterou jste vytvořili dříve)
    - **Počáteční datum:** Vyberte dnešní datum.

1. Zvolte **Vytvořit projekt**.
1. Nový projekt je otevřen. Poznamenejte si hodnotu **ID projektu**. Budete ji muset zadat později.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>Krok 3: Vytvořte nový typ pracovního příkazu ve správě aktiv

1. Jděte na **Správa majetku \> Nastavení \> Pracovní příkaz \> Typy pracovních příkazů**.
1. V podokně akcí zvolte **Nový**.
1. Do mřížky je přidán nový záznam. Pro tento řádek nastavte následující hodnoty:

    - **Typ pracovního příkazu:** *Služba*
    - **Název:** *Pracovní příkazy služby*
    - **Stav životního cyklu pracovního příkazu:** *Standardní*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>Krok 4: Propojte zákaznický účet s nadřazeným projektem

Nyní musíte propojit zákaznický účet s nadřazeným projektem v nastavení projektu ve správě majetku.

1. Přejděte na **Správa majetku \> Nastavení \> Pracovní příkazy \> Nastavení projektu**.
1. Na kartě **Nadřazený projekt** vyberte možnost **Přidat** a přidejte řádek.
1. Na novém řádku nastavte následující hodnoty:

    - **Zákaznický účet:** *US-013* (*Pelican Wholesales*)
    - **ID projektu:** Zadejte ID projektu, který jste si dříve poznamenali.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>Krok 5: Propojte skupinu projektů a typ s projektem pracovního příkazu

Stále byste měli být na stránce **Nastavení projektu** (**Správa majetku \> Nastavení \> Pracovní příkazy \> Nastavení projektu**).

1. Na kartě **Skupina projektu** vyberte možnost **Přidat** a přidejte řádek.
1. Na novém řádku nastavte následující hodnoty:

    - **Typ pracovního příkazu:** *Služba* (typ pracovního příkazu, který jste vytvořili dříve)
    - **Skupina projektu:** *TM*

> [!NOTE]
> Smlouva o projektu na zakázku se vždy dědí z nadřazeného projektu.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>Krok 6: Propojte majetek s ID zákazníka

1. Přejděte na **Správa majetku \> Majetek \> Aktivní majetek**.
1. V poli **Filtr** zadejte *VE-102* a vyberte filtrování podle hodnoty **Majetek**.
1. Vyberte majetek a otevřete jeho nastavení.
1. Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-013* (*Pelican Wholesales*).

    Pole **Název** se automaticky aktualizuje na *Pelican Wholesales*.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>Krok 7: Vytvořte nový typ pracovního příkazu v majetku

1. Jděte na **Správa majetku \> Pracovní příkazy \> Aktivní pracovní příkazy**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření pracovního příkazu** nastavte následující hodnoty:

    - **Typ pracovního příkazu:** *Služba*
    - **Popis:** *Opravit nákladní auto*
    - **Zákaznický účet:** *US-013* (*Pelican Wholesales*)
    - **Majetek:** *VE-102*

        > [!NOTE]
        > Hledání zobrazuje pouze majetek, který je propojen s vybraným zákaznickým účtem.

    - **Typ úlohy údržby:** *Oprava*
    - **Obchod:** *Mechanik*
    - **Úroveň služeb:** *4*

1. Vyberte **OK**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>Krok 8: Zkontrolujte pracovní příkaz a začněte na něm pracovat

V této části budete pracovat na pracovním příkazu, který jste vytvořili v předchozí části.

1. Pomocí těchto kroků ověřte, zda je nadřazený projekt *Pracovní příkaz Pelican Wholesales*:

    1. V části **Práce údržby pracovních příkazů** vyberte řádek.
    1. Na kartě s náhledem **Podrobnosti řádku** zkontrolujte hodnotu **ID projektu**. Mělo by to být pomlčované číslo ve formuláři *\<Parent-Project-ID\>-\<Project-ID\>*. Tato hodnota je odkaz.
    1. Vyberte odkaz ID projektu a otevřete stránku, kde můžete zobrazit nadřazený projekt a názvy projektů.

1. V podokně akcí na kartě **Pracovní příkaz** ve skupině **Stav životního cyklu** vyberte **Aktualizovat stav pracovního příkazu**.
1. V dialogovém okně **Aktualizovat stav pracovního příkazu** ve sloupci **Vybrat** zaškrtněte políčko u řádku, kde je pole **Stav životního cyklu** nastaveno na *Probíhá*.
1. Vyberte **OK**.
1. V dialogovém okně **Stav životního cyklu: InProgress** vyberte **OK**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>Krok 9: Zaúčtujte hodiny, které jste strávili na pracovním příkazu, a vytvořte nový návrh faktury

V této části budete dále pracovat na pracovním příkazu, na němž jste pracovali v předchozí části.

1. V podokně akcí na kartě **Pracovní příkaz** ve skupině **Projekt** vyberte **Deníky**.

    Zobrazí se stránka **Deníky pracovních příkazů**. Zde můžete zaregistrovat čas, který jste strávili na pracovním příkazu.

1. Na kartě s náhledem **Hodiny** vyberte **Přidat řádek**.
1. Na novém řádku nastavte pole **Hodiny** na *4*.
1. V podokně akcí zvolte **Zaúčtovat deníky**.
1. Zavřete stránku **Deníky pracovních příkazů** pro návrat k pracovnímu příkazu.
1. V podokně akcí na kartě **Fakturace** zvolte **Návrh nové faktury**.
1. V dialogovém okně **Vytvořit návrh faktury** v části **Transakce projektu** zaškrtněte políčko **Vybrat** u každého řádku, který chcete fakturovat.
1. Vyberte **OK** pro zavření dialogového okna a zobrazení nového návrhu faktury.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]