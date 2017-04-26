---
title: "Pracovní prostor uzavření finančního období"
description: "V tomto článku je přehled pracovního prostoru Uzavření finančního období a příslušné konfigurace."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Pracovní prostor uzavření finančního období

[!include[banner](../includes/banner.md)]


V tomto článku je přehled pracovního prostoru Uzavření finančního období a příslušné konfigurace.

Pracovní prostor uzavření finančního období

**Finančního období blízko** prostoru umožňuje sledování procesů finanční uzávěrky různých společností, oblastí a lidé. V závislosti na zobrazení **finančního období blízko** prostoru, zobrazí se buď všechny úkoly a stavy pro uzavření plánu nebo pouze úkoly, které vám byly přiřazeny. 

Nejprve je nutné vybrat plán uzávěrky v horní části pracovního prostoru. Všechna data, která je zobrazena v pracovním prostoru je pak filtrovány podle plánu vybraná uzávěrka.

### <a name="summary-tiles"></a>Dlaždice souhrnu

Dlaždice **Souhrn** poskytují přehled procesu a ukazatele, které vám pomohou udržet proces uzávěrky podle plánu. Zobrazí úkoly, které jsou po splatnosti zbývající úkoly dnes, úkoly, které mají být splněny dnes, ale jsou blokovány z důvodu závislostí a všechny zbývající úkoly pro proces. Tyto informace jsou pro všechny společnosti, které jsou součástí plánu vybraná uzávěrka.

### <a name="tasks-and-status-section"></a>Úkoly a výběr stavu

V **úlohy a stav** část celkového stavu plánu uzávěrky se člení různými způsoby: stav společnosti, podle oblasti, stavu a stavu osobou, která je zodpovědná. Můžete zobrazit stav pro všechny úkoly v uzavírací naplánovat pouze úkoly, které mají být splněny dnes, nebo úkoly, které jsou po splatnosti změnou filtru v horní části seznamu karet. Můžete také vybrat filtr společnosti k zobrazení stavu pro konkrétní firmu. Každá karta stav poskytuje členění podle procenta, která byla dokončena a počet úkolů, které zůstávají. Klepněte na kartu, nebo **podrobnosti** akce, které chcete filtrovat seznam podrobných úkolů podle vybrané karty. 

Seznam podrobných úkolů je na poslední kartu. Tento seznam zobrazuje seznam úloh úplné a mohou být filtrovány, aby se zobrazil pouze úkoly, které vás zajímají. Můžete filtrovat seznam úkolů v několika způsoby. Můžete například filtrovat podle úkol termín splnění, přidružené společnosti a přidružené oblasti. Můžete také vybrat Zobrazit nebo skrýt dokončené úkoly v seznamu úkolů. 

Pro úkoly se používají dva indikátory:

-   Ikonu vykřičník označuje, že úkol je po splatnosti. Pro úlohy, které jsou po splatnosti datum splatnosti je červeně zvýrazněno.
-   Ikona visacího zámku indikuje, že úkol závisí na jiných úkolech, které ještě nejsou dokončeny. Úkol, který je blokováno závislostmi nelze označit jako dokončený. Závislostí úkolu lze nastavit pomocí **nastavit závislost** akce.

Název úkolu je hypertextový odkaz 365 Microsoft Dynamics pro operace stránky nebo jiné webové stránky, kde uživatel musí přejít k dokončení práce. Tento hypertextový odkaz můžete nastavit pomocí **vazby úkolu** při úpravě nebo vytvoření úkolu. 

Soubory, poznámky, obrázky a adresy URL můžete připojit k úkolu pomocí **přílohy** akce. Můžete například označení čísel deníků, které jsou používány jako součást úkolu přidat komentáře týkající se určitého úkolu nebo připojit soubor sestavy, který byl vytištěn úkolu. Ikona se zobrazí v **přílohy** sloupec pro úkol, pokud příloha je k dispozici. 

**Dokončení úkolu** možnost musí být vybrána ručně po dokončení úkolu. Pokud je úkol označen jako dokončený, **dokončení datum** pole je automaticky aktualizován na aktuální datum a čas. Závislost indikátory jsou také aktualizovány podle potřeby.

## <a name="all-financial-period-close-tasks-list-page"></a>Stránka seznamu Všechny úkoly uzavření finančního období
Můžete zobrazit všechny aktuální a předchozí období uzavřít úkoly z **všechny finanční období uzavřít úkoly** stránku seznamu. Tato stránka se seznamem je nejvhodnější pro historické analýzy procesu zavírání, protože obsahuje informace o plánované datum splatnosti, datum skutečného dokončení a osoba, která byla dokončena úloha. Informace na této stránce seznamu můžete snadno exportovat do aplikace Excel pro vytváření sestav a účely auditování.

## <a name="financial-period-close-configuration-page"></a>Stránka Konfigurace uzavření finančního období
Před použitím **finančního období blízko** prostoru, je nutné nakonfigurovat procesu 365 Microsoft Dynamics pro operace s použitím **finanční období Zavřít konfigurační** stránky. (Klepněte na tlačítko **financí**&gt;**zavřít období**&gt;**finanční období Zavřít konfigurační**.)

### <a name="resources"></a>Zdroje

Na **prostředky** kartu, definování osob, které se podílejí na procesu uzávěrky. Zaměstnanec odpovídá za úkol uzávěrky musí být přiřazena sem. Musíte také zadat zobrazení pro zaměstnance v pracovním prostoru. Existují tyto možnosti:

-   **Pouze přiřazené úkoly** – budou zobrazeny pouze úlohy, které jsou mu přiřazeny.
-   **Všechny úlohy a stav** – budou zobrazeny všechny úlohy uzávěrky a stav celého procesu.

Uživatelé, kteří mají oprávnění pouze zobrazit přiřazené úkoly, nebudou moci přidat úkoly k seznamu úkolů, upravit koly nebo odebrat úkoly ze seznamu.

### <a name="task-areas"></a>Oblasti úkolů

Pomocí oblastí úkolů seřaďte úkoly uzávěrky do logických skupin vlastnictví ve vaší organizaci. Například závazky, pohledávky a hlavní kniha mohou být použity jako oblasti úkolu.

### <a name="calendars"></a>Kalendáře

Vytvořit a upravit na kartě kalendářů kalendáře finanční uzávěrky.  To je, kde bude definovat pracovní dny pro uzávěrky a bude použit pro plánování úkolů uzávěrky.  Vytvoření nového kalendáře a určit pracovní dny pro plánování úloh.  Doporučujeme vytvořit kalendář pro dlouhou dobu, například rok nebo více let, protože jej lze upravit po vytvoření.  Po vytvoření kalendáře, klepněte na tlačítko Upravit a aktualizovat kalendář pro konkrétní dny, například svátky.  Ukončení úlohy bude naplánována na dny, pokud je hodnota ovládacího prvku nastavena na otevřeno.  Pokud ukončení úlohy nemůže být plán v určitý den, v tento den by měl mít hodnota ovládacího prvku nastavena na Uzavřeno.

### <a name="templates"></a>Šablony

Pomocí finanční zavřít šablony definovat všechny úkoly, které jsou součástí procesu zavírání. Uzavření úkolu je opakované pracovní úsilí, které je přiřazen k dokončení každého procesu uzávěrky jednotlivce. V šabloně relativní splatnosti datum musí být definovány pro každý úkol uzávěrky. Termín relativní datum se počet dní před nebo po konci definovaného období datum úkolu budou splatné každé období. Každý úkol přiřazen také čas potřeby. Doba splatnosti je nastavena pomocí kontextu časové pásmo a budou převedeny na časové pásmo pro každého uživatele. 

Jedna nebo více společností, které se vztahuje tento úkol můžete přiřadit úkol v šabloně. Pokud jinou osobu je přiřazen k dokončení této práce úsilí v každé společnosti, mohou být užitečné vytvořit více úkolů pro stejné pracovní úsilí. Vytvořte jeden úkol pro každou společnost. 

**Vazby úkolu** nabídka je spojena s úsilím práce úkolu a lze přejít přímo na příslušnou stránku z odkazu úkolu v pracovním prostoru. Například úkol uzávěrky spustit proces přecenění měny závazků lze propojit s příslušnými **přecenění cizí měny** stránky v 365 Microsoft Dynamics pro operace. Můžete také odkazovat na externí adresu URL. 

> [! Tip] Pokud chcete propojit konkrétní sestavu Management Reporter finanční období uzavření úkolu, můžete použít adresu URL sestavy. Pro přístup k adrese URL sestavy, otevřete sestavu v nástroji Návrhář sestavy a potom klepněte na tlačítko **souboru**&gt;**zobrazit sestavu** Chcete-li otevřít sestavu ve webovém prohlížeči. Můžete zkopírovat adresu URL v řádku adresa v prohlížeči a vložit ji do pole **Odkaz na úkol** **URL**. 

Závislosti mezi úkoly můžete definovat v šabloně. Pokud úkol nastavena závisí na jeden nebo více úkolů, tento úkol nelze označit jako dokončenou, dokud byly dokončeny všechny závislosti. 

Můžete vytvořit více šablon finančního uzavření. Potom můžete různých šablon lze sledovat procesy uzávěrky pro různé typy období, například měsíce konec nebo konec roku nebo společnostem, které používají různé uzávěrky postupy pro sledování. Po vytvoření šablon můžete zkopírovat do nové šablony a proveďte požadované změny. Každý plán uzávěrky můžete přiřadit pouze jednu šablonu.

### <a name="closing-schedules"></a>Plány uzávěrky

Pomocí plánu uzavírací přiřadit šablonu finančního uzavření na určité finanční období uzavřen. Úkoly ze šablony jsou pak automaticky generovány pro zadané období a nový plán uzávěrky je přidán do pracovního prostoru. Při vytváření plánu nové uzavírací **koncové datum období** pole se používá k určení skutečné splnění data úkolů uzávěrky, relativní náležitý datum, kdy je přiřazena v šabloně finančního uzavření. 

Přiřazení kalendáře, které jsou vhodné pro uzavření plán určit pracovní dny se použije pro plánování úloh. Pokud nedefinujete konkrétní kalendář, data dokončení úkolu budou používat všechny dny v týdnu. 

Je nutné definovat také společnosti, které budou přidruženy k uzavření plánu. Pokud šablona úlohy jsou přiřazeny k více společnostem, vytvoří se pro každou společnost, která je v plánu uzávěrky a přiřazených k úkolu šablony samostatné úkoly. 

Po dokončení uzávěrky plán vyberte **uzavřeno** pro tuto možnost. Historie úloh stále k dispozici **všechny finanční období uzavřít úkoly** stránku seznamu, ale plán uzávěrky budou odebrány z pracovního prostoru. Po uzavření plánu byla označena jako **uzavřeno**, nebudete moci přidat úkoly, úkoly upravit nebo zrušit úlohy.




