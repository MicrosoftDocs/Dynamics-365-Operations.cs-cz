---
title: Porovnat sestavu úložiště cen položek
description: Naučte se generovat sestavu porovnávacího úložiště cen položek a poté procházet a exportovat výsledek.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c6373679299b68413d75236ca8cc18ceba03e091
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334978"
---
# <a name="compare-item-prices-storage-report"></a>Porovnat sestavu úložiště cen položek

[!include [banner](../includes/banner.md)]

V tomto článku je vysvětleno, jak spustit sestavu **Porovnání úložiště cen položek** a zpřístupnit výstup digitálně, a to buď jako interaktivní stránku v Dynamics 365 Supply Chain Management nebo jako exportovaný dokument v některém z několika formátů.

Pokud zobrazíte sestavu ve svém prohlížeči, sloupce a agregované zůstatky jsou v závislosti na konfigurovaném rozvržení dynamicky upravovány. Výsledky můžete řadit, filtrovat, přecházet k podrobnostem atd.

Výsledky sestavy jsou uloženy v datové entitě **Porovnat ceny položek**, což umožňuje filtrovat a exportovat výsledky do formátu, jako je například CSV nebo Microsoft Excel.

Sestava **Porovnání úložiště cen položek** je užitečná v případech, kdy výstup obsahuje mnoho řádků. Výstup bude obsahovat například mnoho řádků v případě, že máte více než 40 000 položek, které mají v nákladové verzi pozastavenou cenu položky.

## <a name="turn-the-compare-item-prices-storage-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce Úložiště porovnání cen zboží

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.29, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Úložiště porovnání cen zboží* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="generate-a-compare-item-prices-storage-report"></a>Generovat sestavu s porovnáním cen položek

Chcete-li vytvořit a uložit sestavu **Porovnat sestavu úložiště cen položek**, postupujte takto:

1. Přejděte na **Řízení nákladů > Dotazy a sestavy > Předem stanovené sestavy nákladů > Porovnání úložiště cen položek**.

1. Výběrem **Nový** otevřete podokno **Porovnat ceny položek**. Chcete-li definovat ceny, které mají být porovnány v sestavě, nastavte následující volby:

    - Na pevné záložce **Parametry** zadejte jedinečný **Název** sestavy a použijte pole v sekcích **Nevyřízené ceny pro porovnání** a **Ceny použité pro porovnání** a definujte, které ceny a kalendářní data chcete porovnat.
    - Na pevné záložce **Záznamy, které mají být zahrnuty** nastavte filtry a omezení, která definují, která data mají být do sestavy zahrnuta.
    - Na pevné záložce **Spustit na pozadí** nastavte, jak, kdy a jak často chcete sestavu generovat.
    > [!NOTE]
    > Tato sestava se vždy spustí jako součást dávkové úlohy.

1. Vyberte **OK**, pokud chcete použít své nastavení a zavřete podokno.

1. Po dokončení dávkové úlohy bude tato úloha uvedena na stránce **Porovnat úložiště cen položek**. Možná budete muset stránku obnovit pro zobrazení sestavy.

## <a name="explore-the-compare-item-prices-storage-report"></a>Prozkoumejte sestavu Porovnat úložiště cen položek

Po vygenerování sestavy ji můžete kdykoli zobrazit a prozkoumat následujícím způsobem:

1. Přejděte na **Řízení nákladů > Dotazy a sestavy > Předem stanovené sestavy nákladů > Porovnání úložiště cen položek**.

1. Vyberte sestavu ze seznamu.

1. Proveďte některou z následujících akcí:

    - Vyberte **Přehled**, chcete-li získat přehled výsledků sestavy.
    - Vyberte **Zobrazit podrobnosti**, chcete-li získat podrobnější zobrazení sestavy

1. Po otevření vybraného zobrazení můžete provést následující:

    - Vyberte téměř libovolné záhlaví sloupce, chcete-li tabulku seřadit nebo filtrovat podle hodnot v tomto sloupci, stejně jako u většiny standardních formulářů v Supply Chain Management. Poznámka: není možné třídit nebo filtrovat sloupec **Čistá změna ceny v %**, protože se jedná o počítané pole.
    - Výběrem možnosti **Zobrazení dimenze** otevřete podokno, ve kterém můžete vybrat sloupec dimenze, který má být zahrnut ve formuláři. Nastavte **Uložit nastavení** na **Ano**, pokud chcete nastavení uložit, aby byla při příštím otevření sestavy zachována. Vyberte **OK**, pokud chcete použít své nastavení a zavřete.
    - Vyberte libovolný řádek ve formuláři a pak výběrem možnosti **Zobrazit podrobnosti** zobrazte další informace o vybrané položce. Z tohoto místa budete moci přejít k datům.
    - Vyberte libovolný řádek ve formuláři a pak výběrem možnosti **Zobrazit srovnávací graf** zobrazte interaktivní grafické znázornění výsledků, které se vztahují k vybrané položce. Tyto výsledky můžete prozkoumat výběrem různých grafických prvků v tabulce a legendě grafu.
    - Vyberte libovolný řádek ve formuláři a pak výběrem možnosti **Zobrazit podrobnosti výpočtu** zobrazte další informace o výpočtech vztahujících se k vybrané položce. Z tohoto místa budete moci přejít k datům.

## <a name="export-the-compare-item-prices-storage-report"></a>Exportujte sestavu Porovnat úložiště cen položek

Každá generovaná sestava je uložena v datové entitě **Porovnat ceny položek**. Pomocí standardních funkcí Supply Chain Management můžete exportovat data z této entity do libovolného podporovaného formátu dat, včetně formátu CSV nebo Microsoft Excel.

Následuje příklad exportu sestavy **Porovnání úložiště cen položek**:

1. Přejděte do nabídky **Správa systému > Pracovní prostory > Správa dat**.

1. Vyberte tlačítko **Export** v části **Správa dat**.

1. Otevře se stránka **Export**, kterou použijete k nastavení úlohy exportu. Začněte tím, že své úloze zadáte **Název skupiny**.

1. V části **Vybrané entity** vyberte možnost **Přidat entitu** a otevřete dialogové okno, ve kterém můžete nastavit následující možnosti:

    - **Název entity** – vyberte **Porovnat ceny položek**.
    - **Formát cílových dat** – vyberte formát, do kterého chcete exportovat.

1. Vyberte **Přidat**, chcete-li přidat nový řádek a vyberte **Zavřít** pro zavření dialogového okna.

1. Obvykle exportujete vždy jednu sestavu. Provedete to tak, že nastavíte **Filtr** pro řádek, který jste právě přidali do podokna **Dotaz**. To vám umožní definovat sestavy z entity **Porovnat ceny položek**, kterou chcete zahrnout do exportu. Chcete-li exportovat jednu sestavu, nastavte následující možnosti filtrování:

    - Na kartě **Rozsah** vyberte možnost **Přidat** a přidejte nový řádek.
    - Nastavte **Tabulku** pro **Porovnání cen položek**.
    - Nastavte **Odvozenou tabulku** pro **Porovnání cen položek**.
    - Nastavte **Pole** na pole, podle kterého chcete filtrovat. Obvykle použijete **Název provedení** nebo **Čas provedení**.
    - Nastavte **Kritéria** na hodnotu z vybraného pole, které chcete vyhledat (buď název sestavy, nebo čas vygenerování sestavy).
    - V případě potřeby přidejte do tabulky **Rozsah** další řádky, dokud neurčíte jedinečnou sestavu, kterou hledáte.

1. Vyberte **OK**, pokud chcete uložit své nastavení a zavřít.

1. Nastavení exportu uložíte výběrem možnosti **Uložit**.

1. Otevřete kartu **Možnosti exportu** a výběrem volby **Exportovat nyní** vygenerujte exportovaný soubor.

1. Otevře se stránka **Souhrn spuštění**, v níž se zobrazí stav úlohy exportu a seznam exportovaných entit. Vyberte entitu **Porovnat ceny zboží**, která je uvedena v oblasti **Stav zpracování entity** a poté vyberte **Stáhnout soubor** pro stažení dat exportovaných z této entity.

Další informace o tom, jak používat správu dat k exportu dat, naleznete v tématu [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]