---
title: Konfigurace rozhraní pro provádění výrobního provozu
description: Toto téma popisuje, jak vytvořit jednu nebo více konfigurací rozhraní pro provádění výrobního provozu. Když otevřete rozhraní pro provádění výrobního provozu, automaticky načte vybranou konfiguraci a filtr úloh, které jsou specifické pro prohlížeč a zařízení. V konfiguraci nastavíte zásady, které musí být použitelné pro konkrétní použití.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84d845055e175e6f4b8078fabeb3307ee96826f2
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115016"
---
# <a name="configure-the-production-floor-execution-interface"></a>Konfigurace rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Pracovníci v dílně používají rozhraní pro provádění výrobního provozu pro registraci denní práce, například když zahajují práci, poskytnutí zpětné vazby k úlohám, registraci nepřímých aktivit a hlášení nepřítomnosti. Tyto registrace jsou základem pro sledování průběhu a nákladů výrobních zakázek a pro výpočet základu pro odměny pracovníků.

Když otevřete rozhraní pro provádění výrobního provozu, automaticky načte vybranou konfiguraci a filtr úloh, které jsou specifické pro prohlížeč a zařízení. V konfiguraci nastavíte zásady, které musí být použitelné pro konkrétní použití. Několik příkladů využití:

- Na zařízení ve firemní hale zaměstnanci registrují příchod, když přicházejí do kanceláře, a registrují odchod při odchodu.
- Na zařízení v dílně se operátoři strojů zaregistrují, když zahájí a dokončí práci. Rovněž registrují přestávky a nepřímé aktivity.

Tohle téma popisuje různé možnosti konfigurace zařízení úkolového lístku.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Zapněte rozhraní pro provádění výrobního provozu a související volitelné funkce

Samotné rozhraní pro provádění výrobního provozu a několik volitelných nastavení, která jsou popsána v tomto tématu, musí být ve vašem systému zapnutá, než je budete moci používat. Použijte stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), chcete-li podle potřeby zapnout některou nebo všechny funkce popsané v následujících podkapitolách,

### <a name="the-production-floor-execution-interface"></a>Rozhraní pro provádění výrobního provozu

Toto je primární funkce popsaná v tomto tématu. Přidává rozhraní pro provádění výrobního provozu do vašeho systému. Chcete-li ji povolit, zapněte následující funkci ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Provádění výrobního provozu

### <a name="generate-license-plates"></a>Generování registračních značek

Tyto funkce zpřístupňují funkčnost registrační značky pro rozhraní provádění výrobního provozu. Chcete-li tyto funkce použít, zapněte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v tomto pořadí):

1. Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku
1. Povolit automatické generování čísla registrační značky při vykazování jako dokončeno v zařízení úkolového lístku

### <a name="print-labels"></a>Tisknout štítky

Tyto funkce zpřístupňují funkčnost tisku štítku pro rozhraní provádění výrobního provozu. Chcete-li tyto funkce použít, zapněte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v tomto pořadí):

1. Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku
1. Vytisknout štítek ze zařízení úkolového lístku

### <a name="allow-locking-the-touch-screen"></a>Povolení uzamčení dotykové obrazovky

Tato funkce přidává tlačítko do rozhraní provádění výrobního provozu, které umožňuje pracovníkům dezinfikovat dotykovou obrazovku. Chcete-li ho použít, zapněte následující funkci ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Funkce pro uzamčení zařízení úkolového lístku a terminálu úkolových lístků za účelem dezinfekce

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Funkce správy majetku pro rozhraní provádění výrobního provozu

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Tato funkce přidává kartu správy majetku do rozhraní pro spuštění výrobního provozu. Pracovníci mohou na této kartě vybrat majetek, který je připojen ke zdroji stroje, který je ve vybraném filtru seznamu úloh. U vybraného majetku stroje může pracovník zobrazit stav a stav majetek z hodnot čítače až pro čtyři vybrané čítače. Chcete-li tuto funkci použít, zapněte následující funkci ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Funkce správy majetku pro rozhraní provádění výrobního provozu

### <a name="enable-job-search"></a>Povolit hledání úloh

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Tato funkce umožňuje přidat vyhledávací pole do seznamu úloh. Pracovníci mohou najít konkrétní práci zadáním ID úlohy nebo vyhledat všechny úlohy pro konkrétní objednávku zadáním ID objednávky. Pracovníci mohou zadat ID pomocí klávesnice nebo naskenováním čárového kódu. Chcete-li ho použít, zapněte následující funkci ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Vyhledávání práce pro rozhraní ke spuštění výrobního provozu

## <a name="work-with-production-floor-execution-configurations"></a>Práce s konfiguracemi rozhraní pro provádění výrobního provozu

Chcete-li vytvořit a udržovat konfigurace zařízení, přejděte na **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurace provádění výrobního provozu**. Na stránce **Konfigurace provádění výrobního provozu** se nachází seznam existujících konfigurací. Na této stránce můžete provést následující akce:

- Výběrem libovolné konfigurace výrobního provozu uvedené v levém sloupci ji zobrazíte a upravíte.
- Volbou **Nové** v podokně akcí přidejte novou konfiguraci zařízení do seznamu. Poté do pole **Konfigurace** zadejte název, dle kterého identifikujete novou konfiguraci. Zadaný název musí být ve všech konfiguracích zařízení jedinečný a později jej nebudete moci upravit.

Dále nakonfigurujte různá nastavení pro vybranou konfiguraci zařízení. K dispozici jsou následující pole:

- **Pouze označení příchodu a odchodu** - Nastavte tuto možnost na *Ano* k vytvoření zjednodušeného rozhraní, které poskytuje pouze funkci označení příchodu a odchodu. Tím se deaktivuje většina ostatních možností na této stránce. Než tuto možnost povolíte, musíte odstranit všechny řádky ze záložky s náhledem **Výběr karty**.
- **Povolit vyhledávání** - Nastavte tuto možnost na *Ano*. chcete-li zahrnout vyhledávací pole do seznamu úloh. Pracovníci mohou najít konkrétní práci zadáním ID úlohy nebo vyhledat všechny úlohy pro konkrétní objednávku zadáním ID objednávky. Pracovníci mohou zadat ID pomocí klávesnice nebo naskenováním čárového kódu.
- **Hlášení množství při odchodu** – Nastavením možnosti na *Ano* vyzvete pracovníky, aby nahlásili zpětnou vazbu o probíhajících úlohách při odchodu. Při nastavení na *Ne* k tomu pracovníci nebudou vyzváni.
- **Zamknout zaměstnance** – Když je tato možnost nastavena na *Ne*, pracovníci budou odhlášeni ihned po provedení registrace (například nové úlohy). Zařízení se poté vrátí na přihlašovací stránku. Pokud je tato možnost nastavena na *Ano*, pracovníci zůstanou přihlášení k zařízení úkolového lístku. Pracovník se však může ručně odhlásit, aby se mohl jiný pracovník přihlásit, zatímco zařízení úkolového lístku nadále běží pod stejným uživatelským účtem systému. Další informace o těchto typech účtů naleznete v tématu [Přiřazení uživatelé](config-job-card-device.md#assigned-users).
- **Použít skutečný čas registrace** – Nastavením na *Ano* nastavíte pro každou novou registraci přesný čas, kdy se pracovník registroval. Když je tato možnost nastavena na *Ne*, místo toho se použije čas přihlášení. Tuto možnost budete obvykle chtít nastavit na *Ano*, pokud možnosti **Zamknout zaměstnance** a/nebo **Jeden pracovník** nastavili na *Ano*, kde pracovníci často zůstávají přihlášeni delší dobu.
- **Jeden pracovník** – Nastavte tuto možnost na *Ano*, pouze pokud jeden pracovník používá každé zařízení úkolového lístku, kde je tato konfigurace aktivní. Pokud je tato možnost nastavena na *Ano*, možnost **Zamknout zaměstnance** je automaticky nastavena na *Ano*. Tohle nastavení navíc odebere požadavek (a schopnost) pracovníka přihlásit se pomocí ID znaku (nebo jiného podobného ID). Místo toho se pracovník přihlásí do Microsoft Dynamics 365 Supply Chain Management pomocí systémového uživatelského účtu propojeného s účtem *časově registrovaný pracovník* (z tabulky *pracovníci*) a současně se přihlásí k zařízení úkolového lístku jako tento pracovník.
- **Povolit uzamčení dotykové obrazovky** – Nastavte tuto možnost na *Ano*, aby pracovníci mohli zamknout dotykovou obrazovku zařízení úkolového lístku, aby ji mohli dezinfikovat. Když je tato možnost nastavena na *Ano*, na přihlasovací stránku zařízení je přidáno tlačítko **Zamknout obrazovku kvůli dezinfekci**. Když pracovník vybere toto tlačítko, dotykový displej se dočasně zamkne, aby se zabránilo neúmyslnému zadání. Zobrazí se také odpočítávání. Pracovník může nyní bezpečně vyčistit zařízení a obrazovku. Po skončení odpočítávání se dotykový displej automaticky odemkne.
- **Doba trvání uzamčení obrazovky** – Když je možnost **Povolit uzamčení dotykové obrazovky** nastavena na *Ano*, použijte tuto možnost pro zadání počtu sekund, po které by měla být dotyková obrazovka uzamčena pro dezinfekci. Doba trvání musí být mezi 5 a 120 sekundami.
- **Generovat registrační značku** – Nastavením této možnosti na *Ano* vygenerujete novou registrační značku pokaždé, když pracovník použije zařízení úkolového lístku k vykázání dokončené práce. Registrační značka vozidla je generována z číselné posloupnosti nastavené na stránce **Parametry řízení skladu**. Při nastavení této možnosti na *Ne* musí pracovníci při vykazování dokončené práce uvést existující registrační značku.
- **Tisk etikety** – Nastavte tuto možnost na *Ano* k vytištění etikety poznávací značky, když pracovník používá zařízení úkolového lístku k nahlášení dokončené práce. Konfigurace etikety je nastavena ve směrování dokumentu, jak je popsáno v [Rozvržení směrování dokumentu pro popisky registrační značky](../warehousing/document-routing-layout-for-license-plates.md).
- **Výběr karty** - Pomocí nastavení v této části zvolte, které karty by se měly zobrazit rozhraním provádění výrobního provozu, když je aktivní aktuální konfigurace. Můžete navrhnout tolik karet, kolik potřebujete, a poté je zde podle potřeby přidat a uspořádat. Podrobnosti o tom, jak zde navrhovat karty a pracovat s nastavením, najdete v části [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Konfigurace úloh čištění

Když supervizor dílny nastaví rozhraní pro provádění výrobního provozu, vybere konfiguraci a filtr úloh. Tyto výběry jsou uloženy v referenční tabulce v Supply Chain Management a prohlížeč používá ID, které je uloženo v místním souboru cookie, aby našel správný řádek v této tabulce. Tabulka také zaznamenává datum a čas, kdy se pracovník naposledy přihlásil ke každému zařízení.

Dávková úloha pravidelně čistí položky v referenční tabulce pro zařízení, která za posledních 60 dní nezaznamenala žádnou aktivitu. Pomocí těchto kroků můžete také položky kdykoli ručně vyčistit.

1. Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurace provádění výrobního provozu**.
1. V podokně Akce vyberte **Vyčištění konfigurací klienta**.
1. V dialogovém okně **Vyčištění konfigurace klienta** nastavte pole **Počet dní** na počet dní (zpětně), které je třeba zvážit. Odeberete všechny konfigurace a záznamy přihlášení pro zařízení, která nebyla během této doby aktivní.
1. Volbou **OK** vyčistíte příslušné konfigurace na základě nastavení **Počet dní**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
