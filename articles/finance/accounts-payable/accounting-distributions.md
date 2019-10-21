---
title: Rozúčtování
description: Tento článek obsahuje informace o rozúčtování a popisuje možnosti, které jsou k dispozici k jejich zpracování. Rozúčtování se používá k přidělení peněžních částek pro zdrojový dokument konkrétním účtům hlavní knihy.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f7d98d7ab9b375bfeb8784596753ca956f96e36
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189722"
---
# <a name="accounting-distributions"></a>Rozúčtování

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o rozúčtování a popisuje možnosti, které jsou k dispozici k jejich zpracování. Rozúčtování se používá k přidělení peněžních částek pro zdrojový dokument konkrétním účtům hlavní knihy. 

Rozúčtování je funkce dostupná v celé aplikaci, kterou používá a rozšiřuje každý zdrojový dokument, například nákupní objednávka, faktura dodavatele, sestava vyúčtování nebo volná faktura. Ve výchozím nastavení se výchozí rozúčtování generuje pro každý řádek zdrojového dokumentu a peněžní částku a jsou u něj podmíněně povoleny úpravy. 

> [!Note] 
> Některé dokumenty podporují také peněžní částky záhlaví dokumentu, například poplatky za objednávky a faktury. 

Obecné možnosti rozúčtování poskytují následující možnosti zpracování rozúčtování:

-   **Distribuovat částky** – zobrazí a upraví rozúčtování pro jednotlivá záhlaví dokumentu nebo řádek a všechny podřízené řádky, jako jsou například daně a poplatky.
    -   Pro horní distribuce peněžních částek (nadřazené distribuce) může být povoleno hlavní účet a finanční dimenze upravovat přímo v řízení segmentového zadání v mřížce. Rozšířená cena je typickým příkladem takové nadřazené distribuce.
    -   Rozúčtování částky jsou založena na podmínce měny dokumentu. Tato měna je obvykle měna transakce. Částky účetní měny a měny vykazování se generují jako součást účetnictví dílčí hlavní knihy.
    -   Distribucí zobrazují data účtování a účetní události. Obvykle je účetní událost nastavena na hodnotu **Žádná**, než se dokumentu zaúčtuje nebo zapíše do deníku. V tom okamžiku se účetní událost stane **Původní**. Po zaúčtování distribucí nelze distribuce změnit.
    -   Tlačítko **Rozdělit** je povoleno pro nadřazené distribuce. Funkce **Rozdělit** vytvoří nová rozúčtování a rozdělení může být založeno na procentech, částce nebo množství.
    -   Tlačítko **Distribuovat rovnoměrně** lze použít v kombinaci s funkcí **Rozdělit** automatickému přidělení částky rovnoměrně mezi všechna rozúčtování.
    -   Tlačítko **Smazat** může být povoleno pro nadřazené distribuce, pokud existuje více než jedna distribuce. Volba **Smazat** stornuje ruční úpravy rozdělení tím, že odstraní všechny existující distribuce a znovu vygeneruje výchozí distribuce.
    -   Podřízená distribuce, například sleva, náklady a prodejní daň, se řídí vždy nadřazenou distribucí. Pomocí volby **Odkaz** &gt; **Nadřazená informace** lze zobrazit vztah mezi nadřazenými a podřízenými.
    -   Hlavní účet a finanční dimenzi může být možné upravit i u podřízených.
    -   Finanční dimenze na rozúčtování se řídí výchozím vzorcem, který může dokument rozšířit. Další informace naleznete v souvisejících článcích.
    -   Odchylky distribuce mohou být vygenerovány v odpovídajících scénářích, například mezi dodavatelskou fakturou a nákupní objednávkou. Pomocí volby **Odkaz** &gt; **Informace o dokumentu** můžete zobrazit odpovídající vztahy mezi rozúčtováním.
    -   Tlačítko **Opravit** je aktivní u dokumentů, které podporují opravy. **Opravit** vytvoří nové distribuce. Nejprve jsou vytvořeny distribuce, které stornují původní distribuce. Tyto distribuce nelze změnit. Dále se vytvoří nová správná rozúčtování. Tato rozúčtování lze upravit, pokud lze upravit původní rozúčtování.
    -   Tlačítko**Podrobnosti o projektu** je aktivní jako rozšíření v případě, že se řádek vztahuje k určitému projektu. Rozúčtování projektu umožňují úpravy podrobných informací, jako je například financování zdroje a vlastnost řádku.
    -   Můžete zobrazit účetní stav aktuálního dokumentu v položce **Odkaz**. Stav se týká celého dokumentu a určuje, zda je dokument nedokončený nebo dokončený.
-   **Zobrazit distribuce** – zobrazení rozúčtování pro všechny řádky a peněžní částky v dokumentu. V tomto zobrazení nelze rozúčtování upravit.


Více informací naleznete v části [Rozúčtování a záznamy v dílčí hlavní knize pro volné faktury](accounting-distributions-subledger-journal-entries-vendor-invoices.md)


