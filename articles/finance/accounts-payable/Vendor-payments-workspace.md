---
title: Pracovní prostor plateb dodavatelů
description: Tento článek obsahuje informace o pracovním prostoru Platby dodavatele. Pracovní prostor Platby dodavatele zobrazuje informace související se zpracováním dodavatelských plateb.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.assetid: ''
ms.search.form: VendPaymentWorkspace
ms.openlocfilehash: 13d86c037dccf23725bc8bdce268ed9fada3c5cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288594"
---
# <a name="vendor-payments-workspace"></a>Pracovní prostor plateb dodavatelů

[!include [banner](../includes/banner.md)]

Pracovní prostor **Platby dodavatele** zobrazuje informace související se zpracováním dodavatelských plateb. Tento pracovní prostor obsahuje zobrazení **Moje práce** a stránku **Analýzy**. Zobrazení **Moje práce** zobrazuje souhrnné dlaždice, mřížky transakce dodavatele a související informace o dodavateli. Stránka **Analýza** používá funkce Microsoft Power BI k zobrazení vizuálů, které se vztahují k platbám dodavatelům.

## <a name="setup-needed-to-view-power-bi-content"></a>Zobrazení obsahu Power BI vyžaduje instalační programu

Následující nastavení je nutné dokončit, aby bylo možné zobrazit data ve vizuálech Power BI **Platby dodavatele**.
1. Přejděte na **Správa systému > Nastavení > Systémové parametry** a nastavte hodnoty **Měna systému** a **Směnný kurz systému**.
2. Přejděte na **Hlavní kniha > Kalendáře > Fiskální kalendáře** k ověření dat fiskálního kalendáře přiřazených k aktivnímu časovému období.
3. Přejděte na **Hlavní kniha > Nastavení > Účetní kniha** k nastavení **Měna účtování** a **Typ směnného kurzu**. 
4. Definujte směnné kurzy mezi měnami transakcí a zúčtovací měnou a mezi zúčtovací měnou a systémovou měnou. Postup: Přejděte na: **Hlavní kniha > Měny > Směnné kurzy měn**.
5. Přejděte na **Správa systému > Nastavení > Úložiště Entit**, pokud chcete aktualizovat agregované měření **VendPaymentBIMeasureV2**.

## <a name="my-work-view"></a>Zobrazení Moje práce

### <a name="summary-tiles"></a>Dlaždice souhrnu

Dlaždice v oddílu **Souhrn** oddílu poskytují přehled o stavu platební informace. Můžete zobrazit platební deníky, které dosud nebyly zaúčtovány, faktury, které jsou po splatnosti, všechny dodavatele a dodavatele, kteří jsou blokováni. Z oddílu **Souhrn** můžete vytvořit nové spuštění mezd.

Informace v oddílu **Souhrn** jsou určeny pro společnost, pode kterou jste přihlášeni.

### <a name="vendor-transactions-grids"></a>Mřížky Transakce dodavatele

Oddíl **Transakce dodavatele** obsahuje mřížky, které zobrazují faktury, které jsou po splatnosti, a platby, které nebyly dosud uhrazeny. Z mřížky **Faktury po splatnosti** můžete zobrazit historii vyrovnání pro vybranou fakturu. Z mřížky **Nevyrovnané platby** můžete zobrazit historii vyrovnání pro vybranou fakturu a vyrovnat fakturu.

Úředníci pro centralizované platby mohou používat filtr, který se zobrazí v horní části každé mřížky, k výběru společnosti. Mřížka je pak filtrována tak, aby se zobrazily pouze společnosti, které jsou definované v organizační hierarchii centralizované platby, kterou má úředník pro centralizované platby oprávnění zobrazit.

Karta **Najít transakce** v oddílu **transakce dodavatele** umožňuje vyhledávat transakce dodavatele.

### <a name="related-information"></a>Související informace

Můžete zobrazit sestavu **Sledování splatnosti dodavatele** a **Souhrn plateb podle data** pomocí odkazů v části pracovního prostoru **související informace**.

## <a name="analytics-page"></a>Stránka Analytika

Stránka **Analytika** uvádí důležitou metriku, například faktury dodavatele po splatnosti a faktury dodavatele splatné v budoucnosti. Tato stránka obsahuje devět stránek sestavy. Jedna stránka obsahuje přehled a dalších osm stránek poskytuje podrobné informace o metrikách plateb závazků.

V následující tabulce jsou uvedeny vizualizace dostupné na stránkách sestav.


|            Stránka sestavy            |                                                                                                                                                                                Vizualizace                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Přehled plateb dodavatele      | <ul><li>Faktury po splatnosti</li><li>Faktury splatné k dnešnímu dni</li><li>Slevy pořízené u ztrát slev</li><li>Faktury splatné v budoucnosti podle data hotovostní slevy</li><li>Faktury splatné v budoucnosti podle data splatnosti</li><li>Faktury zaplacené později vůči fakturám zaplaceným včas</li><li>Přiřazení workflow platby</li><li>Zůstatek dodavatele vůči odběrateli</li><li>Otevřené faktury s blokováním platby</li></ul> |
|         Faktury po splatnosti         |                                                                                             <ul><li>Faktury po splatnosti</li><li>Podrobnosti o fakturách po splatnosti</li><li>Celkem otevřených faktur:</li><li>Faktury po splatnosti podle skupiny dodavatelů</li><li>Faktury po splatnosti podle společnosti</li></ul>                                                                                              |
|        Faktury splatné k dnešnímu dni         |                                                                                                         <ul><li>Faktury splatné k dnešnímu dni</li><li>Podrobnosti o fakturách splatných k dnešnímu dni</li><li>Faktury splatné k dnešnímu dni podle společnosti</li><li>Faktury splatné k dnešnímu dni podle skupiny dodavatelů</li></ul>                                                                                                          |
| Slevy pořízené u ztrát slev |                                                                             <ul><li>Slevy pořízené vůči ztrátám slev</li><li>Slevy pořízené vůči ztrátám slev – podrobnosti</li><li>Slevy pořízené vůči ztrátám slev – podle společnosti</li><li>Slevy pořízené vůči ztrátám slev – podle skupiny dodavatelů</li></ul>                                                                              |
|      Faktury splatné v budoucnosti       |                                                 <ul><li>Faktury splatné v budoucnosti</li><li>Faktury splatné v budoucnosti – detaily</li><li>Faktury splatné v budoucnosti podle společnosti</li><li>Faktury splatné v budoucnosti podle skupiny dodavatelů</li><li>Faktury splatné v budoucnosti podle data hotovostní slevy</li><li>Faktury splatné v budoucnosti podle data splatnosti</li></ul>                                                  |
|        Pozdě zaplacené faktury         |                                                         <ul><li>Faktury zaplacené po datu splatnosti</li><li>Faktury zaplacené po datu splatnosti – detaily</li><li>Faktury zaplacené po datu splatnosti – podle společnosti</li><li>Faktury zaplacené po datu splatnosti – podle skupiny dodavatelů</li><li>Faktury zaplacené pozdě vůči fakturám zaplaceným včas</li></ul>                                                          |
|         Workflow platby          |                                                                                <ul><li>Instance workflowu platby dodavatele</li><li>Instance workflowu platby podle schvalujícího</li><li>Instance workflowu platby podle společnosti</li><li>Průměrný počet dnů ve workflowu podle schvalujícího</li></ul>                                                                                |
|    Zůstatek dodavatele vůči odběrateli     |                                                                                                                   <ul><li>Zůstatek dodavatele vůči odběrateli</li><li>Zůstatek dodavatele vůči na společnost</li><li>Zůstatek dodavatele vůči odběrateli – detaily</li></ul>                                                                                                                    |
|    Faktury s blokováním platby     |                                                                                         <ul><li>Faktury s blokováním platby</li><li>Faktury s blokováním platby – detaily</li><li>Faktury s blokováním platby podle společnosti</li><li>Faktury s blokováním platby podle skupiny dodavatelů</li></ul>                                                                                          |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
