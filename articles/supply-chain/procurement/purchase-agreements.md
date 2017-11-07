---
title: "Nákupní smlouvy"
description: "V tomto článku jsou informace o nákupních smlouvách. Nákupní smlouva je smlouva, která organizaci zavazuje k nákupu určitého množství nebo částky v rámci několika nákupních objednávek v průběhu času. Výměnou za tento závazek odběratel obdrží zvláštní ceny a slevy."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 029f70a995bed25b991d374608d782768b20988c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-agreements"></a>Nákupní smlouvy

[!include[banner](../includes/banner.md)]


V tomto článku jsou informace o nákupních smlouvách. Nákupní smlouva je smlouva, která organizaci zavazuje k nákupu určitého množství nebo částky v rámci několika nákupních objednávek v průběhu času. Výměnou za tento závazek odběratel obdrží zvláštní ceny a slevy. 

Nákupní smlouvy lze použít pro určitý počet produktů, částku produktu v určité měně nebo částku produktů v určité měně v kategorii zásobování. Ceny a slevy nákupní smlouvy přepíší ceny a slevy uvedené v jakýchkoli existujících obchodních smlouvách.  

Na stránce **Nákupní smlouvy** můžete vytvořit, použít a zpracovat nákupní smlouvy, které existují mezi vaší organizací a dodavateli. Například po vytvoření nákupní smlouvy z ní můžete přímo objednávat. Každá nákupní smlouva má dobu platnosti definovanou uživatelem, který vytvořil nákupní smlouvu. Datum dodání nákupu musí spadat do doby platnosti.  

Po vytvoření je nutné nákupní smlouvu aktivovat, aby se stala platnou. Aktivace nákupní smlouvy se provádí nastavením možnosti **Označit smlouvu jako platnou** na hodnotu **Ano**.

## <a name="commitment-types"></a>Typy závazků
Každý řádek nákupní smlouvy vyjadřuje závazek koupit. Může používat řádky z více nákupních objednávek (NO), abyste splnili závazek. Existují čtyři typy závazků:

-   **Závazek – množství produktu** – Kupujete určité množství produktu.
-   **Závazek – hodnota produktu** – Kupujete určitou částku v určité měně produktu.
-   **Závazek – hodnota kategorie produktu** – Kupujete určitou částku v určité měně v kategorii zásobování. Částka může být za položku katalogu nebo nekatalogovou položku.
-   **Závazek ohledně hodnoty** – Kupujete určitou částku v určité měně jakékoliv produktu v jakékoliv kategorii zásobování.

## <a name="pricing-terms-for-purchase-agreements"></a>Cenové podmínky pro nákupní smlouvy
Cenové podmínky se mohou lišit v závislosti na typu závazku. Cenové podmínky z nákupních smluv přepíší jakékoli další cenové podmínek nastavené pro obchodní smlouvy. V následující tabulce jsou popsána pole související s cenami, kterých se jednotlivé typy závazku dotýkají. Pole obsahující hodnotu **Ano** mohou být aktualizována na řádku objednávky.

| Typ závazku                   | Jednotková cena | Cenová jednotka | Procento slevy | Částka platební slevy |
|-----------------------------------|------------|------------|------------------|----------------------|
| Závazek – množství produktu       | Ano        | Ano        | Ano              | Ano                  |
| Závazek – hodnota produktu          |            |            | Ano              |                      |
| Závazek – hodnota kategorie produktu |            |            | Ano              |                      |
| Závazek ohledně hodnoty                  |            |            | Ano              |                      |

## <a name="policies-for-purchase-agreements"></a>Zásady nákupních smluv
Následující zásady mají vliv na způsob propojení mezi závazkem nákupní smlouvy a příslušnými řádky nákupní objednávky:

-   **Max je vynuceno** – Celkové množství nebo částka za všechny řádky objednávky nemůže překročit množství nebo částku, která je specifikována v souvisejícím závazku.
-   **Cena a sleva je pevná** – Cena na řádku objednávky a cena v souvisejícím závazku se musí shodovat. Pokud dojde ke změně ceny na řádku objednávky, dojde k přerušení propojení závazku. Pokud je propojení přerušeno, řádek objednávky nebude přispívat k plnění závazku.
-   **Minimální uvolněná částka a Maximální uvolněná částka** – Je-li částka zadána, zobrazí se zpráva, pokud provedete jakékoli změny na řádku objednávky, které způsobí, že řádek objednávky se bude lišit od souvisejícího závazku.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Výpočty plnění nákupní smlouvy
Množství a částky plnění se zobrazují na kartě **Plnění** na pevné záložce **Podrobnosti řádku** na stránce **Nákupní smlouvy**.  

V oblasti **Plnění** se zobrazuje zbývající částka nebo množství, které je potřeba ke splnění závazku.  

V oblasti **Smlouvy** se zobrazuje celkové množství nebo celková částka, pro kterou je řádek prodejní smlouvy platný.  

K řádkům nákupní objednávky a řádkům faktury, které přispívají k výpočtu plnění, se dostanete výběrem akce **Související informace** na řádcích nebo v záhlaví nákupní smlouvy.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Potvrzení a historie historie verzí nákupních smluv
Při potvrzení nákupní smlouvy bude aktuální verze nákupní smlouvy uložena v tabulce historie. Změníte-li nákupní smlouvu, můžete ji znovu potvrdit a uložit jinou verzi nákupní smlouvy do historie. Pokud nákupní smlouvu nepotvrdíte, je možné ji stále používat k vytvoření nákupních objednávek. Informace o historii nákupní smlouvy však nebudou uloženy. Můžete zobrazit náhled všech verzí smlouvy nebo si je vytisknout. Poté můžete sdílet revize s dodavatelem a získat schválení.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Použití nákupních smluv v procesu objednávky
Při vytváření nákupní objednávky můžete použít nákupní smlouvu. Informace ze smlouvy, jako jsou například platební podmínky, dodací podmínky nebo adresa dodání, se poté zkopírují do záhlaví nákupní objednávky. Pokud nákupní objednávka obsahuje jeden nebo více řádků pro produkty nebo kategorie, které jsou kryty smlouvou, použijí se pro tyto řádky ceny a slevy z nákupní smlouvy. Částka nebo množství v řádku objednávky přispívá k plnění závazku V nákupní smlouvě. Stejná nákupní objednávka může zahrnovat řádky, které nesouvisí s nákupní smlouvou, i řádky, které mají závazek pro nákupní smlouvu.  

Nákupní smlouvu můžete vybrat pouze, když vytváříte nákupní objednávku. Po vytvoření nákupní objednávky nelze vybrat nákupní smlouvu.  
V některých situacích, kdy jsou nákupní objednávky vytvářeny nepřímo, můžete určit, zda aplikace Finance and Operations automaticky vyhledá příslušné nákupní smlouvy. Provést to můžete například při automatickém potvrzování plánovaných nákupních objednávek nebo při vytváření nákupních objednávek, které jsou založeny na prodejních objednávkách.

## <a name="purchase-agreements-and-intercompany-trade"></a>Nákupní smlouvy a mezipodnikový obchod
Mezipodnikové obchodní vztahy lze vytvořit mezi účty dodavatele a účty zákazníků, které se u různých právnických osob liší. Po vytvoření prodejní objednávky nebo nákupní objednávky pro jednu ze stran se vytvoří mezipodnikový řetězec objednávek. V řetězci objednávek se prodejní objednávka a nákupní objednávka vytváří v příslušných právnických osobách.  

Můžete vytvořit nákupní smlouvu nebo prodejní smlouvu pro jednu mezipodnikovou obchodní stranu. Pak lze vygenerovat odpovídající prodejní smlouvu nebo nákupní smlouvu pro ostatní mezipodnikové obchodní podílníky v právnické osobě.  

Když vytvoříte mezipodnikovou nákupní objednávku používající mezipodnikovou nákupní smlouvu v jedné právnické osobě, odpovídající mezipodniková prodejní objednávka použije odpovídající mezipodnikovou prodejní smlouvu v jiné právnické osobě. Plnění závazků prodejní smlouvy a plnění nákupní smlouvy lze synchronizovat, stejně jako budou synchronizovány mezipodniková prodejní objednávka a mezipodniková nákupní objednávka.

## <a name="financial-dimensions-on-purchase-agreements"></a>Finanční dimenze nákupních smluv
Můžete kopírovat finanční dimenze do záhlaví dokladů nebo jednotlivých řádků nákupní smlouvy. Pokud změníte dimenze v záhlaví smlouvy nebo na řádku smlouvy, neovlivní tato změna žádnou z již uvolněných objednávek, ale projeví se u nových objednávek.

<a name="see-also"></a>Viz také
--------

[Vytvoření nové nákupní smlouvy (Průvodce záznamem úloh)](tasks/create-purchase-agreement.md)

[Vytvoření dílčí nákupní objednávky z nákupní smlouvy (Průvodce záznamem úloh)](tasks/create-purchase-release-order-purchase-agreement.md)




