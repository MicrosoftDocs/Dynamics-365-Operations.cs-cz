---
title: Pracovní prostor uzavření finančního období
description: V tomto článku je přehled pracovního prostoru Uzavření finančního období a příslušné konfigurace.
author: ShylaThompson
ms.date: 11/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 157d7e7503a3153f74e705c20b4afac76a81229e807ae6f39b52fc05c733487b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739947"
---
# <a name="financial-period-close-workspace"></a>Pracovní prostor uzavření finančního období

[!include [banner](../includes/banner.md)]

V tomto článku je přehled pracovního prostoru Uzavření finančního období a příslušné konfigurace.

Pracovní prostor uzavření finančního období

Pracovní prostor **Uzavření finančního období** umožňuje sledování procesů finanční uzávěrky různých společností, oblastí a lidí. V závislosti na zobrazení pracovního prostoru **Uzavření finančního období** se zobrazí buď všechny úkoly a stavy pro uzavření plánu nebo pouze úkoly, které vám byly přiřazeny. 

Nejprve je nutné vybrat plán uzávěrky v horní části pracovního prostoru. Všechna data, která jsou zobrazena v pracovním prostoru, jsou pak filtrována podle vybraného plánu uzávěrky.

### <a name="summary-tiles"></a>Dlaždice souhrnu

Dlaždice **Souhrn** poskytují přehled procesu a ukazatele vám pomohou udržovat uzávěrku podle plánu. Můžete zobrazovat úlohy, které jsou po termínu, zbývající úlohy pro dnešní den, jejichž termín je dnes, ale jsou blokovány kvůli závislostem, a všechny zbývající úlohy procesu. Tyto informace jsou pro všechny společnosti, které jsou zahrnuté do vybraného plánu uzávěrky.

### <a name="tasks-and-status-section"></a>Úkoly a výběr stavu

V části **Úkoly a stav** je stav celkového plánu uzávěrky členěn různými způsoby: stav podle společnosti, podle oblasti, stavu a stav podle zodpovědné osoby. Můžete zobrazit stav pro všechny úkoly v plánu uzávěrky, pouze pro úkoly, které mají být splněny dnes, nebo úkoly, které jsou po splatnosti, změnou filtru v horní části seznamu karet. Můžete také vybrat filtr společnosti k zobrazení stavu pro konkrétní firmu. Každá karta stavu uvádí členění podle procenta, které bylo dokončeno a počtu úkolů, které zůstávají. Klepněte na kartu, nebo akci **Zobrazit podrobnosti** k filtrování seznamu podrobných úkolů podle vybrané karty. 

Poslední karta je určená pro seznam podrobných úkolů. Tento seznam zobrazuje celý seznam úkolů a lze ho filtrovat, aby se zobrazily pouze úkoly, které vás zajímají. Můžete filtrovat seznam úkolů v několika způsoby. Můžete například filtrovat podle termínu splnění úkolu, přidružené společnosti a přidružené oblasti. Můžete také vybrat, zda chcete zobrazit nebo skrýt dokončené úkoly v seznamu úkolů. 

Pro úkoly se používají dva indikátory:

-   Ikona vykřičníku označuje, že úkol je po splatnosti. Pro úkoly, které jsou po splatnosti, je datum splatnosti červeně zvýrazněno.
-   Ikona visacího zámku označuje, že úkol závisí na jiných úkolech, které ještě nejsou dokončeny. Úkol, který je blokováno závislostmi, nelze označit jako dokončený. Závislosti úkolu lze nastavit pomocí akce **Nastavit závislost**.

Název úkolu je hypertextový odkaz na stránku nebo jinou webovou stránku, kam uživatel musí přejít k dokončení práce. Tento hypertextový odkaz můžete nastavit pomocí pole **Odkaz na úkol** při úpravě nebo vytvoření úkolu. 

Soubory, poznámky, obrázky a adresy URL můžete připojit k úkolu pomocí akce **Přílohy**. Můžete například označit čísla deníků, které jsou používány jako součást úkolu, přidat komentáře týkající se určitého úkolu nebo připojit soubor sestavy, který byl vytištěn pro úkol. Ikona se zobrazí ve sloupci **Přílohy** pro úkol, pokud je příloha k dispozici. 

Možnost **Dokončení úkolu** musí být vybrána ručně po dokončení úkolu. Pokud je úkol označen jako dokončený, pole **Datum dokončení** je automaticky aktualizováno na aktuální datum a čas. Indikátory závislosti jsou také aktualizovány podle potřeby.

## <a name="all-financial-period-close-tasks-list-page"></a>Stránka seznamu Všechny úkoly uzavření finančního období
Můžete zobrazit všechny úkoly pro aktuální a předchozí období uzavření ze stránky se seznamem **Všechny úkoly uzavření finančního období**. Tato stránka se seznamem je nejvhodnější pro historickou analýzu procesu uzavření, protože obsahuje informace o plánovaném datu splatnosti, datu skutečného dokončení a osobě, která úlohu dokončila. Informace na této stránce se seznamem můžete snadno exportovat do aplikace Microsoft Excel pro vytváření sestav a účely auditování.

## <a name="financial-period-close-configuration-page"></a>Stránka Konfigurace uzavření finančního období
Než bude možné použít pracovní prostor **Uzavření finančního období**, je nutné nastavit proces pomocí stránky **Konfigurace uzavření finančního období**. (Klikněte na tlačítko **Hlavní kniha** &gt; **Závěrka období** &gt; **Konfigurace uzavření finančního období**.)

### <a name="resources"></a>Zdroje

Na kartě **Prostředky** definujte osoby, které se podílejí na procesu uzávěrky. Zde musí být nejprve přiřazen jakýkoli zaměstnanec, který odpovídá za úkol uzávěrky. Musíte také zadat zobrazení pro zaměstnance v pracovním prostoru. Existují tyto možnosti:

-   **Pouze přiřazené úkoly** – budou zobrazeny pouze úlohy, které jsou uživateli přiřazeny.
-   **Všechny úlohy a stav** – budou zobrazeny všechny úlohy uzávěrky a stav celého procesu.

Uživatelé, kteří mají oprávnění pouze zobrazit přiřazené úkoly, nebudou moci přidat úkoly k seznamu úkolů, upravit koly nebo odebrat úkoly ze seznamu.

### <a name="task-areas"></a>Oblasti úkolů

Pomocí oblastí úkolů seřaďte úkoly uzávěrky do logických skupin vlastnictví ve vaší organizaci. Například závazky, pohledávky a hlavní kniha mohou být použity jako oblasti úkolu.

### <a name="calendars"></a>Kalendáře

Vytvořte a upravte kalendáře finanční uzávěrky pomocí karty Kalendáře. Zde můžete definovat pracovní dny pro procesy uzávěrky a můžete je také použít k plánování úkolů uzávěrky.  Vytvořte nový kalendář a určete pracovní dny používané k plánování úloh.  Doporučujeme vytvořit kalendář na dlouhou dobu, například na rok nebo více let, protože jej lze po vytvoření upravit.  Po vytvoření kalendáře klepněte na tlačítko Upravit, aby se aktualizoval kalendář pro konkrétní dny, například svátky.  Úkoly uzávěrky budou naplánovány na dny, kdy je hodnota Řízení nastavena na Otevřeno.  Pokud úkoly uzávěrky nelze naplánovat na konkrétní den, měla by na tento den být hodnota ovládacího prvku nastavena na Uzavřeno.

### <a name="templates"></a>Šablony

Pomocí šablony finanční uzávěrky definujte všechny úkoly, které jsou součástí procesu uzávěrky. Úkol uzávěrky je opakované pracovní úsilí, které je přiřazeno jednotlivci k dokončení v rámci každého procesu uzávěrky. V šabloně musí být definováno relativní datum splatnosti definován pro každý úkol uzávěrky. Relativní datum splatnosti je počet dní před nebo po definovaném koncovém datu období, ke kterému bude úkol v každém období splatný. Jednotlivým úkolům je přiřazen také čas splatnosti. Čas splatnosti je nastaven pomocí kontextu vašeho časového pásma a bude převeden na časové pásmo pro každého uživatele. 

Úkol v šabloně můžete přiřadit jedné nebo více společnostem, na které se vztahuje tento úkol. Pokud je jiná osoba je přiřazena k dokončení tohoto pracovního úsilí v každé společnosti, může být užitečné vytvořit více úkolů pro stejné pracovní úsilí. Vytvořte jeden úkol pro každou společnost. 

Položka nabídky **Odkaz na úkol** je spojena s pracovním úsilím úkolu a lze ji použít k přechodu přímo na příslušnou stránku z odkazu na úkol v pracovním prostoru. Například úkol uzávěrky spuštění procesu přecenění měny závazků lze propojit s příslušnou stránkou **Přecenění cizí měny**. Můžete také odkazovat na externí adresu URL. 

> [!TIP]
> Pokud chcete odkázat konkrétní sestavu aplikace Management Reporter na úkol uzávěrky finančního období, můžete použít adresu URL sestavy. Chcete-li přistupovat k adrese URL sestavy, otevřete sestavu v Návrháři sestav a klikněte na možnost **Soubor** &gt; **Zobrazit sestavu**, aby se sestava otevřela v prohlížeči. Můžete zkopírovat adresu URL v řádku adresa v prohlížeči a vložit ji do pole **Odkaz na úkol** **URL**. 

Závislosti mezi úkoly můžete definovat v šabloně. Pokud byl úkol nastaven, aby závisel na jedné nebo více úlohách, nelze jej označit jako dokončený až do dokončení všech závislosti. 

Je možné vytvořit více šablon finanční uzávěrky. Potom můžete pomocí různých šablon sledovat procesy uzávěrky pro různé typy období, například konec měsíce konec nebo konec roku nebo ke sledování společností, které používají různé procesy uzávěrky. Po vytvoření šablony ji můžete zkopírovat do nové šablony a provést požadované změny. Jednotlivým plánům uzávěrky můžete přiřadit pouze jednu šablonu.

### <a name="closing-schedules"></a>Plány uzávěrky

Pomocí plánu uzavírací přiřadit šablonu finanční uzávěrky konkrétnímu finančnímu období, které musí být uzavřeno. Úkoly ze šablony jsou pak automaticky generovány pro zadané období a nový plán uzávěrky je přidán do pracovního prostoru. Při vytváření nového plánu uzávěrky je pole **Koncové datum období** použito k určení skutečných dat plnění úkolů uzávěrky na základě relativního data splatnosti, které je přiřazeno v šabloně finanční uzávěrky. 

Přiřaďte kalendář, který je vhodný pro plán uzávěrky, k určení pracovních dní, které se použijí pro plánování úloh. Pokud nedefinujete konkrétní kalendář, data plnění úkolu budou používat všechny dny v týdnu. 

Je nutné definovat také společnosti, které budou přidruženy k plánu uzávěrky. Pokud jsou šablony úlohy jsou přiřazeny k více společnostem, pro každou společnost, která je v plánu uzávěrky, bude vytvořen plán uzávěrky, který bude přiřazen k úkolu šablony. 

Po dokončení plánu uzávěrky pro něho vyberte možnost **Uzavřeno**. Historie úloh bude stále k dispozici ze stránky se seznamem **Všechny úkoly uzavření finančního období**, ale plán uzávěrky bude odebrán z pracovního prostoru. Po označení plánu uzávěrky jako **Uzavřeno** nebudete moci přidat upravit nebo zrušit úlohy v tomto plánu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]