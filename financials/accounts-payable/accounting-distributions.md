---
title: "Rozúčtování"
description: "Tento článek obsahuje informace o rozúčtování a popisuje možnosti, které jsou k dispozici k jejich zpracování. Rozúčtování se používá k přidělení peněžních částek pro zdrojový dokument konkrétním účtům hlavní knihy."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a98ce08dc115bc96cec07c2d6ced10d774785fe9
ms.openlocfilehash: b1057caae6f47e5a17e194834fbbcb9d7d731605
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-distributions"></a>Rozúčtování

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o rozúčtování a popisuje možnosti, které jsou k dispozici k jejich zpracování. Rozúčtování se používá k přidělení peněžních částek pro zdrojový dokument konkrétním účtům hlavní knihy. 

Rozúčtování je funkce dostupná v celé aplikaci, kterou používá a rozšiřuje každý zdrojový dokument, například nákupní objednávka, faktura dodavatele, sestava vyúčtování nebo volná faktura. Ve výchozím nastavení se výchozí rozúčtování generuje pro každý řádek zdrojového dokumentu a peněžní částku a jsou u něj podmíněně povoleny úpravy. 

> [!Note] 
> Některé dokumenty jsou podporovány také záhlaví dokumentu peněžní částky, například poplatky za objednávky a faktury. 

Obecné možnosti rozúčtování poskytují následující možnosti zpracování rozúčtování:

-   **Distribuovat částky** – zobrazí a upraví rozúčtování pro jednotlivá záhlaví dokumentu nebo řádek a všechny podřízené řádky, jako jsou například daně a poplatky.
    -   Pro horní distribuce peněžních částek (nadřazené distribuce) může být povoleno hlavní účet a finanční dimenze upravovat přímo v řízení segmentového zadání v mřížce. Rozšířená cena je typickým příkladem takové nadřazené distribuce.
    -   Rozúčtování částky jsou založena na podmínce měny dokumentu. Tato měna je obvykle měna transakce. Částky účetní měny a měny vykazování se generují jako součást účetnictví dílčí hlavní knihy.
    -   Distribucí zobrazují data účtování a účetní události. Obvykle je účetní událost nastavena na hodnotu **Žádná**, než se dokumentu zaúčtuje nebo zapíše do deníku. V tom okamžiku se účetní událost stane **Původní**. Po zaúčtování distribucí nelze distribuce změnit.
    -   Tlačítko **Rozdělit** je povoleno pro nadřazené distribuce. Funkce **Rozdělit** vytvoří nová rozúčtování a rozdělení může být založeno na procentech, částce nebo množství.
    -   Tlačítko **Distribuovat rovnoměrně** lze použít v kombinaci s funkcí **Rozdělit** automatickému přidělení částky rovnoměrně mezi všechna rozúčtování.
    -   Tlačítko **Smazat** může být povoleno pro nadřazené distribuce, pokud existuje více než jedna distribuce. Volba **Smazat** stornuje ruční úpravy rozdělení tím, že odstraní všechny existující distribuce a znovu vygeneruje výchozí distribuce.
    -   Podřízená distribuce, například sleva, náklady a prodejní daň, se řídí vždy nadřazenou distribucí. Můžete zobrazit vztah nadřazený podřízený v **odkaz**&gt;**nadřazené informace**.
    -   Hlavní účet a finanční dimenzi může být možné upravit i u podřízených.
    -   Finanční dimenze na rozúčtování se řídí výchozím vzorcem, který může dokument rozšířit. Další informace naleznete v souvisejících článcích.
    -   Odchylky distribuce mohou být vygenerovány v odpovídajících scénářích, například mezi dodavatelskou fakturou a nákupní objednávkou. Můžete zobrazit odpovídající vztahy mezi rozúčtování na **odkaz**&gt;**informací**.
    -   Tlačítko **Opravit** je aktivní u dokumentů, které podporují opravy. **Správné** vytvoří nové distribuce. Nejprve jsou vytvořeny rozdělení které obrátí původní distribuce. Nelze změnit tyto distribuce. Jsou vytvořeny další, nové správné rozúčtování. Tato rozúčtování lze upravit, pokud lze upravit původní rozúčtování.
    -   Tlačítko** Podrobnosti o projektu** je aktivní jako rozšíření v případě, že se řádek vztahuje k určitému projektu. Rozúčtování projektu umožňují úpravy podrobných informací, jako je například financování zdroje a vlastnost řádku.
    -   Můžete zobrazit aktuální stav účetní doklad v **odkaz**. Stav je v celém dokumentu a označuje, zda dokument je v procesu nebo dokončit.
-   ** Zobrazit rozúčtování ** – Zobrazit rozúčtování pro všechny řádky a peněžních částek v dokladu. V tomto zobrazení nelze rozúčtování upravit.


Další informace naleznete v tématu [rozúčtování a položky dílčího hlavního deníku pro volné faktury](accounting-distributions-subledger-journal-entries-vendor-invoices.md).



