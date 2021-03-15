---
title: Rozúčtování
description: Toto téma obsahuje informace o rozúčtování a popisuje možnosti, které jsou k dispozici k jejich zpracování.
author: ShylaThompson
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3901fb61c1c8f9a9fd13b8ea558877daf884f3ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972224"
---
# <a name="accounting-distributions"></a>Rozúčtování

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o rozúčtování a popisuje možnosti, které jsou k dispozici k jejich zpracování. Rozúčtování se používá k přidělení peněžních částek pro zdrojový dokument konkrétním účtům hlavní knihy. 

Rozúčtování je funkce dostupná v celé aplikaci, kterou používá a rozšiřuje každý zdrojový dokument, například nákupní objednávka, faktura dodavatele, sestava vyúčtování nebo volná faktura. Ve výchozím nastavení se výchozí rozúčtování generuje pro každý řádek zdrojového dokumentu a peněžní částku a jsou u něj podmíněně povoleny úpravy. 

> [!NOTE] 
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
    -   Finanční dimenze na rozúčtování se řídí výchozím vzorcem, který může dokument rozšířit.
    -   Odchylky distribuce mohou být vygenerovány v odpovídajících scénářích, například mezi dodavatelskou fakturou a nákupní objednávkou. Pomocí volby **Odkaz** &gt; **Informace o dokumentu** můžete zobrazit odpovídající vztahy mezi rozúčtováním.
    -   Tlačítko **Opravit** je aktivní u dokumentů, které podporují opravy. **Opravit** vytvoří nové distribuce. Nejprve jsou vytvořeny distribuce, které stornují původní distribuce. Tyto distribuce nelze změnit. Dále se vytvoří nová správná rozúčtování. Tato rozúčtování lze upravit, pokud lze upravit původní rozúčtování.
    -   Tlačítko **Podrobnosti o projektu** je aktivní jako rozšíření v případě, že se řádek vztahuje k určitému projektu. Rozúčtování projektu umožňují úpravy podrobných informací, jako je například financování zdroje a vlastnost řádku.
    -   Můžete zobrazit účetní stav aktuálního dokumentu v položce **Odkaz**. Stav se týká celého dokumentu a určuje, zda je dokument nedokončený nebo dokončený.
-   **Zobrazit distribuce** – zobrazení rozúčtování pro všechny řádky a peněžní částky v dokumentu. V tomto zobrazení nelze rozúčtování upravit.

Ve verzi 10.0.13 byla přidána funkce, která ověřuje distribuční tabulku účetnictví, aby bylo zajištěno, že jsou nová pole správně nastavena. Tato funkce se nazývá **Povolit další ověření dat pro dokumenty pomocí rámce účetnictví zdrojových dokumentů**. Chcete-li tuto funkci používat, musíte ji povolit pomocí pracovního prostoru **Správa funkcí**. Chcete-li funkci povolit, vyhledejte její název v poli **Vyhledávání** na stránce **Správa funkcí** a poté vyberte **Povolit hned**.

Více informací naleznete v části [Rozúčtování a záznamy v dílčí hlavní knize pro faktury dodavatele](accounting-distributions-subledger-journal-entries-vendor-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]