---
title: Konfigurace rozhraní pro provádění výrobního provozu
description: Tento článek popisuje, jak vytvořit jednu nebo více konfigurací rozhraní pro provádění výrobního provozu. Když otevřete rozhraní pro provádění výrobního provozu, automaticky načte vybranou konfiguraci a filtr úloh, které jsou specifické pro prohlížeč a zařízení. V konfiguraci nastavíte zásady, které musí být použitelné pro konkrétní použití.
author: johanhoffmann
ms.date: 11/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 641b293617df608bc07b97c077dbcd05664f8e2a
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748679"
---
# <a name="configure-the-production-floor-execution-interface"></a>Konfigurace rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Pracovníci v dílně používají rozhraní pro provádění výrobního provozu pro registraci denní práce, například když zahajují práci, poskytnutí zpětné vazby k úlohám, registraci nepřímých aktivit a hlášení nepřítomnosti. Tyto registrace jsou základem pro sledování průběhu a nákladů výrobních zakázek a pro výpočet základu pro odměny pracovníků.

Když otevřete rozhraní pro provádění výrobního provozu, automaticky načte vybranou konfiguraci a filtr úloh, které jsou specifické pro prohlížeč a zařízení. V konfiguraci nastavíte zásady, které musí být použitelné pro konkrétní použití. Několik příkladů využití:

- Na zařízení ve firemní hale zaměstnanci registrují příchod, když přicházejí do kanceláře, a registrují odchod při odchodu.
- Na zařízení v dílně se operátoři strojů zaregistrují, když zahájí a dokončí práci. Rovněž registrují přestávky a nepřímé aktivity.

Tento článek popisuje různé možnosti konfigurace rozhraní provedení výrobního provozu pro každé zařízení používané na vašem pracovišti.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Zapněte rozhraní pro provádění výrobního provozu a související volitelné funkce

Samotné rozhraní pro provádění výrobního provozu a několik volitelných nastavení, která jsou popsána v tomto článku, musí být ve vašem systému zapnutá, než je budete moci používat. Použijte stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), chcete-li podle potřeby zapnout některou nebo všechny funkce popsané v následujících podkapitolách,

### <a name="the-production-floor-execution-interface"></a>Rozhraní pro provádění výrobního provozu

Toto je primární funkce popsaná v tomto článku a je nezbytným předpokladem pro všechny ostatní funkce uvedené v této části. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Provedení výrobního provozu* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="generate-license-plates"></a>Generování registračních značek

Tyto funkce zpřístupňují funkčnost registrační značky pro rozhraní provádění výrobního provozu. Chcete-li tyto funkce použít, zapněte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v tomto pořadí):

1. *Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku*<br>(Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.25 je tato funkce povinná.)
1. *Povolit automatické generování čísla registrační značky při vykazování jako dokončeno v zařízení úkolového lístku*<br>(Od verze Supply Chain Management 10.0.25 je tato funkce povinná.)

### <a name="print-labels"></a>Tisknout štítky

Tyto funkce zpřístupňují funkčnost tisku štítku pro rozhraní provádění výrobního provozu. Chcete-li tyto funkce použít, zapněte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v tomto pořadí):

1. *Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku*<br>(Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.25 je tato funkce povinná.)
1. *Vytisknout štítek ze zařízení úkolového lístku*<br>(Od verze Supply Chain Management 10.0.25 je tato funkce povinná.)

### <a name="allow-locking-the-touch-screen"></a>Povolení uzamčení dotykové obrazovky

Tato funkce umožňuje pracovníkům zamknout dotykovou obrazovku, aby ji mohli dezinfikovat.

Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním *Funkce pro uzamčení zařízení úkolového lístku a terminálu úkolových lístků za účelem dezinfekce* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Funkce správy majetku pro rozhraní provádění výrobního provozu

Tato funkce přidává kartu správy majetku do rozhraní pro spuštění výrobního provozu. Pracovníci mohou na této kartě vybrat majetek, který je připojen ke zdroji stroje, který je ve vybraném filtru seznamu úloh. U vybraného majetku stroje může pracovník zobrazit stav a stav majetek z hodnot čítače až pro čtyři vybrané čítače.

Od verze Supply Chain Management 10.0.25 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.29, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Funkce správy majetku pro rozhraní provádění výrobního provozu* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="job-search"></a>Hledání úloh

Tato funkce umožňuje přidat vyhledávací pole do seznamu úloh. Pracovníci mohou najít konkrétní práci zadáním ID úlohy nebo vyhledat všechny úlohy pro konkrétní objednávku zadáním ID objednávky. Pracovníci mohou zadat ID pomocí klávesnice nebo naskenováním čárového kódu.

Od verze Supply Chain Management 10.0.25 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.29, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Vyhledávání práce pro rozhraní ke spuštění výrobního provozu* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="report-on-co-products-and-by-products"></a>Hlášení koproduktů a vedlejších produktů

Tato funkce umožňuje pracovníkům používat rozhraní provádění produkčního podlaží k hlášení průběhu dávkových objednávek. Toto hlášení zahrnuje hlášení o koproduktech a vedlejších produktech.

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce ve výchozím nastavení zapnuta. Správci mohou tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Zpráva o vedlejších a souběžných produktech z rozhraní pro provádění výrobního provozu* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>Zbrazení úplných sériových čísel, čísel šarží a registračních čísel vozidel

Tato funkce poskytuje vylepšené prostředí k prohlížení seznamů sériových, dávkových a registračních čísel v rozhraní pro provádění výrobního provozu. Zobrazení se změní ze zobrazení karty s omezeným počtem znaků na zobrazení seznamu, ve kterém je dostatek prostoru pro zobrazení celých hodnot. Seznam také poskytuje možnost vyhledávat konkrétní čísla.

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.25 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud spouštíte verzi starší než 10.0.29, správci mohou tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Zobrazit úplná čísla série, dávky a registrační značky vozidla v produkčním rozhraní výrobního provozu* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Od verze Supply Chain Management 10.0.25 je tato funkce ve výchozím nastavení zapnuta. Správci mohou tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Zobrazit úplná čísla série, dávky a registrační značky vozidla v produkčním rozhraní výrobního provozu* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="register-material-consumption"></a>Zaregistrovat spotřebu materiálu

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Tato funkce umožňuje pracovníkům používat rozhraní k provádění výrobního provozu k registraci spotřeby materiálu, čísel šarží a sériových čísel. Někteří výrobci, zejména výrobci ve zpracovatelském průmyslu, potřebují explicitně registrovat množství spotřebovaného materiálu pro každou dávku nebo výrobní zakázku. Pracovníci mohou například používat váhu k vážení množství spotřebovaného materiálu při práci. Aby byla zajištěna úplná sledovatelnost materiálu, organizace musí také registrovat, která čísla šarží byla spotřebována při výrobě každého produktu.

Tato funkce existuje ve dvou verzích. Jedna podporuje pouze položky, které *nemají* povoleno používat procesy řízení skladu (WMS). Druhý podporuje položky, které *mají* povoleno používat WMS. Chcete-li použít tuto funkci, zapněte jednu nebo obě z následujících funkcí v části [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v tomto pořadí), v závislosti na tom, zda máte položky, které jsou povoleny pro WMS:

- *Registrace spotřeby materiálu na rozhraní pro provádění výrobního provozu (mimo WMS)*
- *(Preview) Registrace spotřeby materiálu na rozhraní pro provádění výrobního provozu (s povoleným WMS)*

> [!IMPORTANT]
> Funkci mimo WMS můžete používat samostatně. Pokud však používáte WMS, musíte povolit obě funkce.

### <a name="report-on-catch-weight-items"></a>Vykazování položek se skutečnou hmotností

Pracovníci mohou používat rozhraní provádění produkčního podlaží k hlášení průběhu dávkových objednávek pro položky skutečné hmotnosti. Dávkové příkazy se vytvářejí ze vzorců, které lze definovat tak, aby měly položky skutečné hmotnosti jako položky vzorce, koprodukty a vedlejší produkty. Vzorec lze také definovat tak, aby obsahoval řádky vzorce pro přísady, které jsou definovány pro skutečnou hmotnost. Položky skutečné hmotnosti používají ke sledování inventáře dvě měrné jednotky: množství skutečné hmotnosti a množství inventáře. Například v potravinářském průmyslu lze maso v krabicích definovat jako položku skutečné hmotnosti, kde se množství skutečné hmotnosti používá ke sledování počtu krabic a množství v inventáři se používá ke sledování hmotnosti krabic.

Chcete-li tuto funkci používat, zapněte následující funkci ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Sestava položek skutečné hmotnosti z rozhraní provádění výrobního provozu*

### <a name="the-my-day-dialog"></a>Dialogové okno „Můj den“

Dialogové ono **Můj den** poskytuje pracovníkům přehled jejich denních registracích a aktuálních zůstatcích za placenou dobu, placené přesčasy, nepřítomnost a placenou nepřítomnost.

Pokud chcete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce ve výchozím nastavení zapnuta. Správci mohou tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Zobrazení Můj den pro rozhraní pro provádění výrobního provozu* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="teams"></a>Týmy

Když je ke stejné výrobní úloze přiděleno více pracovníků, mohou vytvořit tým. Tým může nominovat jednoho pracovníka jako pilota. Zbývající pracovníci se pak automaticky stanou asistenty tohoto pilota. Pro výsledný tým musí stav úlohy zaregistrovat pouze pilot. Časové záznamy platí pro všechny členy týmu.

Chcete-li tuto funkci používat, zapněte následující funkci ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Produkční týmy v rozhraní pro provádění výrobního provozu*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Další konfigurace v rozhraní pro provádění výrobního provozu

Tato funkce přidává nastavení pro následující funkce na stránce **Konfigurace provádění výrobního provozu**:

- Automatické otevření dialogového okna **Zahájení úlohy** po dokončení vyhledávání.
- Automatické otevření dialogového okna **Průběh sestavy** po dokončení vyhledávání.
- Předvyplnění zbývajícího množství v dialogovém okně **Průběh sestavy**.
- Povolení úprav spotřeby materiálu v dialogovém okně **Průběh sestavy**. (Tato funkce vyžaduje také funkci *Registrace spotřeby materiálu na rozhraní pro provádění výrobního provozu (mimo WMS)*.)
- Povolení vyhledávání podle ID projektu.

Informace o použití těchto nastavení jsou uvedeny dále v tomto článku.

Chcete-li tuto funkci používat, zapněte následující funkci ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Další konfigurace v rozhraní pro provádění výrobního provozu*

### <a name="enable-the-my-jobs-tab"></a>Povolte kartu Moje úlohy

Karta **Moje úlohy** umožňuje pracovníkům snadno zobrazit všechny nezahájené a nedokončené úlohy, které jsou jim specificky přiřazeny. Je to užitečné ve společnostech, kde jsou úkoly někdy nebo vždy přiděleny konkrétním pracovníkům (lidské zdroje) namísto jiných typů zdrojů (jako jsou stroje).

Chcete-li tuto funkci používat, zapněte následující funkci ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Karta Moje úlohy v rozhraní pro provádění výrobního provozu*

### <a name="enable-use-of-a-numpad-on-the-sign-in-page"></a>Povolení používání numerické klávesnice na přihlašovací stránce

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

Tato stránka umožní správcům přidat ovládací prvek číselné klávesnice na přihlašovací stránku pro rozhraní provádění výrobního provozu. Pracovníci se pak mohou přihlásit pomocí numerické klávesnice a zadat své identifikační číslo nebo osobní číslo.

Chcete-li tuto funkci používat, zapněte následující funkci ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- *Povolení používání numerické klávesnice na přihlašovací stránce*

## <a name="work-with-production-floor-execution-configurations"></a>Práce s konfiguracemi rozhraní pro provádění výrobního provozu

Chcete-li vytvořit a udržovat konfigurace provedení výrobního provozu, přejděte na **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurace provádění výrobního provozu**. Na stránce **Konfigurace provádění výrobního provozu** se nachází seznam existujících konfigurací. Na této stránce můžete provést následující akce:

- Výběrem libovolné konfigurace výrobního provozu uvedené v levém sloupci ji zobrazíte a upravíte.
- Volbou **Nová** v podokně akcí přidáte novou konfiguraci do seznamu. Poté do pole **Konfigurace** zadejte název, dle kterého identifikujete novou konfiguraci. Zadaný název musí být ve všech konfiguracích jedinečný a později jej nebudete moci upravit. Do pole **Popis** volitelně zadejte popis konfigurace.

Dále nakonfigurujte různá nastavení pro vybranou konfiguraci, jak je popsáno v následujících podsekcích.

### <a name="the-general-fasttab"></a>Záložka s náhledem Obecné

Na záložce s náhledem **Obecné** jsou k dispozici následující nastavení:

- **Pouze označení příchodu a odchodu** – Nastavte tuto možnost na *Ano* k vytvoření zjednodušeného rozhraní, které poskytuje pouze funkci označení příchodu a odchodu. Toto nastavení deaktivuje většinu ostatních možností na této stránce. Než tuto možnost povolíte, musíte odstranit všechny řádky ze záložky s náhledem **Výběr karty**.
- **Povolit vyhledávání** – Nastavte tuto možnost na *Ano*. chcete-li zahrnout vyhledávací pole do seznamu úloh. Pracovníci mohou najít konkrétní práci zadáním ID úlohy nebo vyhledat všechny úlohy pro konkrétní objednávku zadáním ID objednávky. Pracovníci mohou zadat ID pomocí klávesnice nebo naskenováním čárového kódu.
- **Povolit vyhledávání podle ID projektu** – Nastavením této možnosti na *Ano* umožníte pracovníkům vyhledávat podle ID projektu (kromě ID úlohy a ID objednávky) ve vyhledávacím poli v rozhraní pro provádění výrobního provozu. U této možnosti můžete nastavit hodnotu *Ano*, pouze když je možnost **Povolit vyhledávání** nastavena na *Ano*.
- **Automatické otevření dialogového okna spuštění** – Pokud je tato možnost nastavena na *Ano*, když pracovníci použijí vyhledávací panel k nalezení úlohy, automaticky se otevře dialogové okno **Zahájení úlohy**.
- **Automatické otevření dialogového okna průběhu vykazování** – Pokud je tato možnost nastavena na *Ano*, když pracovníci použijí vyhledávací panel k nalezení úlohy, automaticky se otevře dialogové okno **Průběh sestavy**.
- **Povolit úpravu materiálu** – Nastavením této možnosti na *Ano* povolíte tlačítko **Upravit materiál** v dialogovém okně **Průběh sestavy**. Pracovníci mohou vybrat toto tlačítko, aby upravili spotřebu materiálu pro úlohu.
- **Hlášení množství při odchodu** – Nastavením možnosti na *Ano* vyzvete pracovníky, aby nahlásili zpětnou vazbu o probíhajících úlohách při odchodu. Při nastavení na *Ne* k tomu pracovníci nebudou vyzváni.
- **Zamknout zaměstnance** – Když je tato možnost nastavena na *Ne*, pracovníci budou odhlášeni ihned po provedení registrace (například nové úlohy). Rozhraní se poté vrátí na přihlašovací stránku. Pokud je tato možnost nastavena na *Ano*, pracovníci zůstanou přihlášení k rozhraní provedení výrobního provozu. Pracovník se však může ručně odhlásit, aby se mohl jiný pracovník přihlásit, zatímco rozhraní provedení výrobního provozu nadále běží pod stejným uživatelským účtem systému. Další informace o těchto typech účtů naleznete v tématu [Přiřazení uživatelé](config-job-card-device.md#assigned-users).
- **Použít skutečný čas registrace** – Nastavením na *Ano* nastavíte pro každou novou registraci přesný čas, kdy se pracovník registroval. Když je tato možnost nastavena na *Ne*, místo toho se použije čas přihlášení. Tuto možnost budete obvykle chtít nastavit na *Ano*, pokud možnosti **Zamknout zaměstnance** a/nebo **Jeden pracovník** nastavili na *Ano*, kde pracovníci často zůstávají přihlášeni delší dobu.
- **Jeden pracovník** – Nastavte tuto možnost na *Ano*, pouze pokud jeden pracovník používá každé rozhraní provedení výrobního provozu, kde je tato konfigurace aktivní. Pokud je tato možnost nastavena na *Ano*, možnost **Zamknout zaměstnance** je automaticky nastavena na *Ano*. Tohle nastavení navíc odebere požadavek (a schopnost) pracovníka přihlásit se pomocí ID znaku (nebo jiného podobného ID). Místo toho se pracovník přihlásí do Microsoft Dynamics 365 Supply Chain Management pomocí systémového uživatelského účtu propojeného s účtem *časově registrovaný pracovník* (z tabulky *pracovníci*) a současně se přihlásí k rozhraní provedení výrobního provozu jako tento pracovník.
- **Povolit numerickou klávesnici** – Nastavte tuto možnost na *Ano* pro přidání numerické klávesnice na přihlašovací obrazovku, která umožňuje pracovníkům zadat své identifikační číslo nebo osobní číslo pomocí numerické klávesnice na dotykové obrazovce. Tuto možnost nastavte na *Ne*, chcete-li skrýt číselnou klávesnici.
- **Povolit uzamčení dotykové obrazovky** – Nastavte tuto možnost na *Ano*, aby pracovníci mohli zamknout dotykovou obrazovku rozhraní provedení výrobního provozu, aby ji mohli dezinfikovat. Když je tato možnost nastavena na *Ano*, na přihlašovací stránku je přidáno tlačítko **Zamknout obrazovku kvůli dezinfekci**. Když pracovník vybere toto tlačítko, dotykový displej se dočasně zamkne, aby se zabránilo neúmyslnému zadání. Zobrazí se také odpočítávání. Pracovník může nyní bezpečně vyčistit zařízení a obrazovku. Po skončení odpočítávání se dotykový displej automaticky odemkne.
- **Doba trvání uzamčení obrazovky** – Když je možnost **Povolit uzamčení dotykové obrazovky** nastavena na *Ano*, použijte tuto možnost pro zadání počtu sekund, po které by měla být dotyková obrazovka uzamčena pro dezinfekci. Doba trvání musí být mezi 5 a 120 sekundami.
- **Generovat registrační značku** – Nastavením této možnosti na *Ano* vygenerujete novou registrační značku pokaždé, když pracovník použije rozhraní provedení výrobního provozu k vykázání dokončené práce. Registrační značka vozidla je generována z číselné posloupnosti nastavené na stránce **Parametry řízení skladu**. Při nastavení této možnosti na *Ne* musí pracovníci při vykazování dokončené práce uvést existující registrační značku.
- **Tisk etikety** – Nastavte tuto možnost na *Ano* k vytištění etikety poznávací značky, když pracovník používá rozhraní provedení výrobního provozu k nahlášení dokončené práce. Konfigurace etikety je nastavena ve směrování dokumentu, jak je popsáno v [Rozvržení popisků směrování dokumentu](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Záložka s náhledem Výběr karty

Pomocí nastavení na záložce s náhledem **Výběr karty** zvolte, které karty provádění výrobního provozu se mají zobrazit, když je aktivní aktuální konfigurace. Můžete navrhnout tolik karet, kolik potřebujete, a poté je přidat a uspořádat podle potřeby pomocí tlačítek na panelu nástrojů záložky s náhledem. Informace, jak zde navrhovat karty a pracovat s nastavením, najdete v části [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Záložka s náhledem Průběh sestavy

Na záložce s náhledem **Průběh sestavy** jsou k dispozici následující nastavení:

- **Povolit úpravu materiálu** – Nastavením této možnosti na *Ano* přidáte tlačítko **Upravit materiál** v dialogovém okně **Průběh sestavy**. Pracovníci mohou vybrat toto tlačítko, aby upravili spotřebu materiálu pro úlohu.
- **Výchozí zbývající množství** – Nastavením této možnost na *Ano* dojde k předvyplnění očekávaného zbývajícího množství výrobní úlohy v dialogovém okně **Průběh sestavy**.

## <a name="clean-up-job-configurations"></a>Konfigurace úloh čištění

Když supervizor dílny nastaví rozhraní pro provádění výrobního provozu, vybere konfiguraci a filtr úloh. Tyto výběry jsou uloženy v referenční tabulce v Supply Chain Management a prohlížeč používá ID, které je uloženo v místním souboru cookie, aby našel správný řádek v této tabulce. Tabulka také zaznamenává datum a čas, kdy se pracovník naposledy přihlásil ke každému zařízení.

Dávková úloha pravidelně čistí položky v referenční tabulce pro zařízení, která za posledních 60 dní nezaznamenala žádnou aktivitu. Pomocí těchto kroků můžete také položky kdykoli ručně vyčistit.

1. Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurace provádění výrobního provozu**.
1. V podokně Akce vyberte **Vyčištění konfigurací klienta**.
1. V dialogovém okně **Vyčištění konfigurace klienta** nastavte pole **Počet dní** na počet dní (zpětně), které je třeba zvážit. Odeberete všechny konfigurace a záznamy přihlášení pro zařízení, která nebyla během této doby aktivní.
1. Volbou **OK** vyčistíte příslušné konfigurace na základě nastavení **Počet dní**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
