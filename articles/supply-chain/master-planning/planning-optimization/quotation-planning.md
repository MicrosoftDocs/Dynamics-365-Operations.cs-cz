---
title: Plány založené na nabídkách a RFQ
description: Tento článek popisuje, jak nastavit hlavní plánování, aby při generování plánovaných objednávek zvažovalo nabídky a požadavky na nabídku (RFQ).
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690081"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Plán založený na nabídkách a RFQ

[!include [banner](../../includes/banner.md)]

Nabídky a žádosti o nabídky (RFQ) představují možné nebo dokonce pravděpodobné budoucí objednávky. Proto má smysl je brát v úvahu během hlavního plánování, aby bylo možné naplánovat další dodávky na základě existujících RFQ a pravděpodobnosti, že se každá nabídka stane skutečnou objednávkou. Tento článek popisuje, jak nastavit hlavní plánování, aby při generování plánovaných objednávek zvažovalo nabídky a RFQ.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Nastavte hlavní plánování pro zvážení prodejních nabídek a/nebo RFQ

Následující postup použijte k nastavení hlavního plánování pro zvážení prodejních nabídek a/nebo RFQ.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte existující plán v podokně seznamu nebo vyberte **Nový** v podokně akcí a vytvořte nový.
1. Na pevné záložce **Obecné** zadejte následující pole:

    - **Zahrnout prodejní nabídky** – Nastavte tuto možnost na *Ano*, chcete-li zvážit prodejní nabídky při spuštění aktuálního plánu. Nastavte na *Ne* pro jejich ignorování.
    - **Pravděpodobnost %** – Nastavte minimální úroveň spolehlivosti, která je vyžadována pro zahrnutí nabídky do hlavního plánování. Výpočet hlavního plánování bude zahrnovat všechny nabídky, které byly vytvořeny z příležitostí, které mají toto procento pravděpodobnosti nebo vyšší. Chcete-li zahrnout všechny nabídky, včetně nabídek, kterým není přiřazena žádná pravděpodobnost nebo s nimi není spojena žádná příležitost, nastavte toto pole na *0* (nula). Další informace o pravděpodobnostech nabídek najdete v další části.
    - **Zahrnout požadavky na nabídky** – Nastavte tuto možnost na *Ano*, chcete-li posoudit RFQ při spuštění aktuálního plánu. Nastavte na *Ne* pro jejich ignorování. Pokud se rozhodnete zvážit RFQ, systém pro ně vytvoří plánované nákupní objednávky, ale nebude specifikovat dodavatele, dokud nebude RFQ vyřešen. Plánované nákupní objednávky, které jsou vytvořeny pro RFQ, mohou ovlivnit množství jiných plánovaných objednávek.

1. Pokračujte v nastavování hlavního plánu obvyklým způsobem.

## <a name="assign-and-view-probabilities-for-quotations"></a>Přiřaďte a zobrazte pravděpodobnosti nabídek

Jak bylo zmíněno v předchozí části, hlavní plán bude posuzovat pouze nabídky, které splňují nebo překračují práh pravděpodobnosti, který je pro plán definován (pokud je práh definován). Pravděpodobnost však není nastavena přímo u každé nabídky. Místo toho je zděděno z příležitosti, která byla použita k vytvoření nabídky. Proto nabídky, které jsou vytvořeny přímo na stránce **Všechny nabídky**, nebudou mít přiřazenu pravděpodobnost nebo s nimi spojenou příležitost a nebudou nikdy brány v úvahu při hlavním plánování (pokud je pole **Pravděpodobnost %** nastaveno na *0* \[nula\]). Aby k tomu byla přiřazena pravděpodobnost, musí být z příležitosti vygenerována nabídka.

### <a name="create-a-quotation-from-an-opportunity"></a>Vytvořit nabídku z příležitosti

Následující postup použijte k přiřazení pravděpodobnosti příležitosti a poté k vytvoření nabídky z této příležitosti.

1. Přejděte na **Prodej a marketing \> Vztahy \> Příležitosti \> Všechny příležitosti**.
1. Vyberte existující příležitost nebo vyberte **Nová** v podokně akcí a vytvořte novou.
1. Vyplňte stránku příležitosti a identifikujte příležitost, jak chcete. Nezapomeňte nastavit pole **Pravděpodobnost** na vhodnou hodnotu. Pouze hlavní plány, které jsou nastaveny tak, aby hledaly pravděpodobnosti této hodnoty nebo vyšší, budou brát v úvahu nabídky, které jsou vygenerovány z této příležitosti.
1. V podokně akcí vyberte **Uložit**.
1. V podokně akcí na kartě **Příležitost**, ve skupině **Nový** vyberte **Prodejní nabídka** nebo **Nabídka projektu** v závislosti na typu nabídky, kterou chcete vytvořit.
1. V dialogovém okně **Vytvořit nabídku** nastavte pole dle potřeby a poté vyberte **OK**.
1. Je vytvořena a otevřena nová nabídka. Na pevné záložce **Řádky** použijte panel nástrojů k přidání prodejních řádků nebo projektových řádků podle potřeby k definování obsahu nabídky.
1. V podokně akcí vyberte **Uložit**. Poté nabídku zavřete.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Zobrazit pravděpodobnost, která je přiřazena k nabídce

Jediným způsobem, jak zobrazit pravděpodobnost přiřazenou k nabídce, je otevřít příležitost, která byla použita k vytvoření této nabídky, jak je popsáno v následujícím postupu.

1. Přejděte na **Prodej a marketing \> Prodejní nabídky \> Všechny nabídky**.
1. Pokud se soupec **ID příležitosti** nezobrazuje (ve výchozí instalaci je skrytý), dočasně jej zobrazíte podle následujících kroků. (Případně pro zachování dostupnosti sloupce **ID příležitosti** vytvořte [uložené zobrazení](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json), které jej zahrnuje.)

    1. Vyberte a podržte (nebo klikněte pravým tlačítkem) v mřížce a poté vyberte **Vložit sloupce**.
    1. V dialogovém okně **Vložit sloupce** najděte řádek, kde je pole **Pole** nastaveno na *Příležitost* a vyberte zaškrtávací pole **Vybrat** pro daný řádek.
    1. Vyberte **Aktualizace** pro přidání vybraného sloupce na stránku **Všechny nabídky**.

1. V mřížce najděte řádek pro příslušnou nabídku. Poté ve sloupci **ID příležitosti** vyberte hodnotu pro tento řádek.

    > [!NOTE]
    > Pokud hledáte cenovou nabídku projektu, možná budete muset vybrat záhlaví sloupce **Typ nabídky** a vymazat jeho filtr. Ve výchozí instalaci je tento filtr nastaven tak, aby se zobrazovaly pouze prodejní nabídky.

1. Otevře se související příležitost. Nyní můžete prohlížet a upravovat hodnotu **Pravděpodobnost** dle potřeby.
