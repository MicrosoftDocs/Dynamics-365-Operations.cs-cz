---
title: Zpracování hlavního deníku
description: Toto téma popisuje možnosti v aplikaci Microsoft Dynamics 365 Finance, které usnadňují zpracování deníku hlavní knihy a které lze také použít k zaručení správnosti pořízených dat a dodržení interní kontroly.
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c067b7b6cbbcad4456df6037da8ab124776261e9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441270"
---
# <a name="general-journal-processing"></a>Zpracování hlavního deníku

[!include [banner](../includes/banner.md)]

Toto téma popisuje možnosti, které usnadňují zpracování deníku hlavní knihy a které lze také použít k zaručení správnosti pořízených dat a dodržení interní kontroly.  

## <a name="journal-names"></a>Názvy deníků

Jednou z nejdůležitějších oblastí nastavení jsou názvy deníků. Je vhodné definovat konkrétní názvy pro každý účel, například mezipodnikové, úprava časového rozlišení a opravy chyb. Můžete přizpůsobit každý název deníku pro rychlé a bezpečné zvýšení zadávání dat pro každý účel. 

Na stránce **Názvy deníků** můžete nastavit následující prvky:

-   **Schválení workflowu** – Chcete-li zlepšit interní kontrolu, definujte workflowy deníků, které stanovují limity významnosti pro kroky kontroly a schvalování na základě kritérií, jako je například celková částka na straně Má dáti. Nastavit workflowy pro hlavní deníky můžete na stránce **Workflowy hlavní knihy**.
-   **Výchozí hodnoty** – vyberte výchozí hodnoty pro protiúčty, měnu a finanční dimenze.
-   **Kontrola deníku** – lze nastavit omezení pro společnost a typ účtu a rovněž pro hodnoty segmentů. 

**Příklady**

Název deníku lze použít pouze pro úpravy. V tomto případě můžete určit, že pouze typ účtu **Hlavní kniha** je platný napříč všemi společnostmi. 

[![Typy účtů kontroly deníku](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Název deníku lze použít pouze pro konkrétní segment nebo pro rozsah u hlavních účtů. 

[![Segment kontroly deníku](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Možnost **Automatické storno** je k dispozici v hlavních denících. Například máte úpravu časového rozlišení, u které skutečný dokument dosud nebyl zpracován, jak je uvedeno v následujícím obrázku.
[![Stornování hlavního deníku](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Doplněk Microsoft Excel pro položku deníku poskytuje další úroveň automatizace a usnadňuje zadávání dat. Akce **Otevřít řádky v aplikaci Excel** je k dispozici na stránkách **Hlavní deník** a **Doklad deníku**. 

Na stránce **Periodické deníky** můžete nastavit opakující se deníky pro automatizaci zpracování deníků. 

Šablony dokladů lze použít kdykoli. Na stránce **Hlavní deníky** najdete akce **Uložit** a **Vybrat šablonu dokladu** na stránce **Doklad deníku** v oblasti **Funkce** pro řádky dokladu.

## <a name="related-setup"></a>Související nastavení
Následující nastavení není specifické pro hlavní deníky, pomůže vám však zajistit správné a snadné zadávání dat.

### <a name="main-account"></a>Hlavní účet

Nastavení hlavního účtu poskytuje mnoho možností pro zpracování hlavního deníku:

-   **Požadavek DC/CR** – tuto možnost použijte, pokud je hlavní účet omezený na transakce typu Má dáti nebo Dal. Nastavení se kontroluje při ověření nebo zaúčtování deníku.

-   **Výchozí protiúčet**
-   **Pozastaveno** – pozastaví hlavní účet pro zadávání dat napříč všemi společnostmi nebo pro určitou společnost či právnickou osobu.
-   **Nepovolit ruční zadávání** – zabrání uživatelům ručně zadat hodnotu pro účet v denících.
-   **Výchozí/ověření měny**
-   **Přepsání právnické osoby** – toto nastavení je specifické pro definovanou společnost / právnickou osobu:
    -   **Výchozí/ověření DPH**
    -   **Výchozí dimenze** – **Nestanoveno** nebo **Pevná hodnota**. **Pevná hodnota** vám pomůže zajistit, aby všechna zaúčtování pro tento hlavní účet vždy použila jakoukoli hodnotu dimenze, která je nastavena jako **Pevná**.
-   **Ověření zaúčtování**
    -   **Ověření uživatele** – tato možnost určuje, kteří uživatelé mohou účtovat do hlavního účtu.
    -   **Ověření typu zaúčtování** – tato možnost určuje, které typy zaúčtování jsou povolené pro hlavní účet.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Účetní struktury a struktury rozšířených pravidel

Účetní struktury a struktury rozšířených pravidel jsou velice důležité pro zajištění toho, aby byla data potřebná pro finanční vykazování a sledování výkonu zachycována během zpracování hlavního deníku a jakékoli dokumentace. Účetní struktury a struktury rozšířených pravidel vám umožní přizpůsobit zadávání dat. Můžete povolit zadávání dat pouze pro finanční dimenze, které jsou relevantní v každé situaci a také můžete vynutit požadavek, aby byla vždy zaznamenána povinná a přesná data.

Další informace naleznete v následujících tématech:
- [Plánování účetní osnovy](plan-chart-of-accounts.md) 
- [Vytvoření rozšířených pravidel pro deníky](tasks/create-advanced-rules-journals.md)
- [Vytvoření záznamu deníku pomocí šablony](tasks/create-journal-entry-template.md)
- [Vytváření a ověřování deníků](tasks/create-validate-journals.md)
- [Účtování periodických deníků](tasks/post-periodic-journals.md)
- [Zpracování deníku přidělení hlavní knihy](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Simulovat zaúčtování
Možnost **Simulovat zaúčtování** můžete pro většinu deníků nalézt v nabídce **Ověřit**. Při ověřování deníku pomocí funkce **Ověřit** systém otestuje deník ohledně konkrétních chybových podmínek. Pokud použijete funkci **Simulovat zaúčtování**, systém spustí všechny stejné procesy, které běží v průběhu zaúčtování bez skutečného zaúčtování deníku. Můžete poté zkontrolovat zprávy o zaúčtování, které se zobrazí, opravit nalezené chyby a poté otevřít nabídku **Zaúčtovat** pro zaúčtování deníku. 

Možnost **Simulovat zaúčtování** není k dispozici pro dávkové zpracování. Je však k dispozici kód pro simulaci zaúčtování v dávce a vývojáři mohou rozšiřovat kód pro přidání této funkcionality.  

## <a name="journal-unlock"></a>Odemknutí deníku
Na stránce deníku je k dispozici tlačítko pro odemknutí deníku, který má stav „uzamčeno systémem“ nastaven na hodnotu Ano. Tento odemčení může provádět správce systému, který analyzoval všechny spuštěné dávkové úlohy a potvrdil, že tento deník již nebude aktivně zpracováván dávkovou úlohou. Toto tlačítko je povoleno funkcí **Tlačítko odemknutí deníku** na stránce **Správa funkcí**. 

## <a name="workflow-recall"></a>Workflow odvolání 
Možnost odvolat deník v workflowu, který má stav "bez možnosti obnovy", je povolena pomocí tlačítka **Workflow** v deníku a na stránce **Historie workflowu**. To je povoleno funkcí nazvanou **Obnovení stavu workflowu pro deníky** na stránce **Správa funkcí**.

## <a name="delete-journal-lines"></a>Odstranit řádky deníku
Možnost rychlé odstranění všech řádků deníku je povolena v deníku v části **Funkce** > **Odstranit řádky deníku**. Chcete-li tuto funkci povolit, vyberte ve **Správě funkcí** možnost **Odstranit optimalizace výkonu deníku**.
