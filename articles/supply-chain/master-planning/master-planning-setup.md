---
title: Nastavit hlavní plány
description: Tento článek popisuje různé důležité strategie a parametry, které se používají k nastavení hlavních plánů.
author: t-benebo
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 150e02916e056946016155d1b4969e99fbd47af5
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740650"
---
# <a name="set-up-master-plans"></a>Nastavit hlavní plány

[!include [banner](../includes/banner.md)]

Tento článek popisuje různé důležité strategie a parametry, které se používají k nastavení hlavního plánování. Obsahuje přehled typů plánů, které jsou používány hlavním plánováním, a vysvětluje, jakou strategii plánování byste měli použít v závislosti na obchodních požadavcích. Popisuje také hlavní parametry ovlivňující plán a vysvětluje, jak tyto parametry ovlivňují navrhované plánované objednávky.

## <a name="types-of-master-plans"></a>Typy hlavních plánů

Hlavní plánování má dva typy plánů: statický a dynamický. Každý typ je navržen pro jiné použití. Chcete-li dosáhnout nejlepšího výkonu, doporučujeme použít příslušný plán pro váš scénář.

### <a name="static-plan"></a>Statický plán

Statický plán zůstane nezměněn bez ohledu na případné změny v nabídce a poptávce až do dalšího spuštění hlavního plánování.

Statický plán se používá ke schválení a potvrzení navrhovaných objednávek. Jedná se o operační plán, který může používat různý personál společnosti (například nákupčí nebo plánovač výroby) a zakládat na něm svá rozhodnutí a provádět každodenní úkoly a činnosti.

Statický plán také podporuje regeneraci. Zcela nový optimalizovaný plán je vypočten pokaždé, když je spuštěno hlavní plánování, a stávající objednávky, které nebyly schváleny, budou odstraněny.

### <a name="dynamic-plan"></a>Dynamický plán

Dynamický plán obvykle začíná jako kopie statického plánu, ale lze jej aktualizovat vždy, když se změní hlavní data. Pokud se například změní data, vytvoří se nová prodejní objednávka.

Dynamický plán se používá pro plánování ad hoc. To umožní společnosti sledovat síť změnových příkazů dostupnost položky bez narušení statického plánu, který používají ostatní pracovníci pro své pracovní procesy. Používá se zejména pro příslib na základě ověření dostupné kapacity. Dynamický plán je výchozím plánem při otevření čistých požadavků ze stránek objednávek (jako jsou například stránky prodejní objednávky, nákupní objednávky nebo výrobní zakázky).

Dynamický plán používá čistou změnu. Proto pomáhá zaručit rychlejší běh.

## <a name="strategies-for-using-master-plans"></a>Strategie používání hlavních plánů

V hlavním plánování můžete použít buď jeden plán, nebo dva plány. Použitá strategie závisí na obchodních požadavcích.

### <a name="one-plan-strategy"></a>Strategie s jedním plánem

Pro strategii s jedním plánem použijete stejný hlavní plán pro statický plán a dynamický plán. Tato strategie se používá pro scénáře vytváření zásob, kde obvykle nemusíte simulovat plán, který objednávku splňuje.

Strategie jednoho plánu se obvykle používá v maloobchodních a distribučních odvětvích nebo v případech, kdy jsou data dodání potvrzena na základě smluv o úrovni služeb (SLAs) nebo doby realizace. Pro plán lze kontrolu data dodání použít bez CTP.

Pokud je nutné provést simulaci, plán lze znovu spustit pro položky, které vyžadují simulaci. Plánované objednávky, které simulace objednávky produkuje, jsou obvykle potvrzeny.

### <a name="two-plan-strategy"></a>Strategie s dvěma plány

Pro strategii se dvěma plány použijete statický plán a jiný dynamický plán. Strategie dvou plánů se obvykle používá pro scénáře konfigurace na zakázku a pro vytváření objednávek, kde je nutné provést simulace prodejních objednávek a vypočítat přesná data dodání pro prodejní objednávky, ale výpočty nesmí mít vliv na každodenní operace. Tyto simulace se vždy provádějí v dynamickém plánu. Strategie s dvěma plány je užitečná například v automobilovém průmyslu a u výrobců OEM.

Pro strategii s dvěma plány lze kontrolu data dodání použít s CTP. Při použití CTP se automaticky zahájí spuštění v dynamickém plánu.

### <a name="setting-up-the-plans"></a>Nastavení plánů

Plány můžete vytvářet na stránce **Hlavní plány** (**Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**).

Můžete určit, které plány budou použity pro statický plán a dynamický plán nastavením polí **Aktuální statický hlavní plán** a **Aktuální dynamický hlavní plán** na stránce **Parametry hlavního plánování** (**Hlavní plánování \> Nastavení \> Parametry hlavního plánování**). Chcete-li použít strategii s jedním plánem, vyberte stejný plán v polích **Aktuální statický hlavní plán** a **Aktuální dynamický hlavní plán**.

## <a name="types-of-planning-methods"></a>Typy metod plánování

Ke spuštění hlavního plánování lze použít tři metody výpočtu: regeneraci a čistou změnu. Každá metoda vytváří při spuštění jiný plán.

Metodu plánování lze zadat v dialogovém okně **Spuštění hlavního plánování**. Chcete-li otevřít toto dialogové okno, přejděte na **Hlavní plánování \> Hlavní plánování \> Spuštění \> Hlavní plánování** nebo vyberte **Spustit** v pracovním prostoru **Hlavní plánování**.

### <a name="regeneration"></a>Obnovení

Metoda plánování regenerace odstraní existující plánované objednávky, pokud nejsou potvrzeny. Generuje nové plánované objednávky na základě všech požadavků. Regenerace je jediná metoda plánování, která je k dispozici pro statické plány.

- Změny v dodávce se vezmou v úvahu. Tyto změny zahrnují změny v prognóze.
- Tato metoda respektuje kód disponibility **období**.
- Tato metoda podporuje funkci náhradního produktu (PI).

### <a name="net-change"></a>Čistá změna

Metoda plánování čisté změny generuje plánované objednávky za účelem pokrytí požadavků, které byly vytvořeny nebo změněny od posledního spuštění hlavního plánování. Při spuštění této metody nejsou změny v dodávce zvažovány. Systém nebere v úvahu žádné nové zásoby a dříve vytvořené plánované objednávky nejsou odstraněny, pokud již nejsou vyžadovány. Metoda plánování čisté změny běží rychleji než metoda regenerace. Je k dispozici pouze pro dynamické plány.

- Data akcí a termíny budou aktualizovány pro všechny požadavky.
- Tato metoda nerespektuje kód disponibility **období**.
- Tato metoda nesplňuje prognózu, a to ani v případě, že je vybrána v plánu.
- Tato metoda nepodporuje funkci náhradního produktu (PI).

### <a name="net-change-minimized"></a>Minimalizovaná čistá změna

Minimalizovaná metoda plánování čisté změny generuje plánované objednávky za účelem pokrytí pouze těch požadavků, které byly vytvořeny nebo změněny od posledního spuštění hlavního plánování. Na rozdíl od metody čisté změny se data akce a data termínů aktualizují pouze pro nové nebo změněné požadavky. Tato metoda plánování je k dispozici pouze pro dynamické plány.

## <a name="types-of-scheduling-methods"></a>Typy metod plánování

U každého plánu na záložce s náhledem **Obecné** stránky **Hlavní plány** (**Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**) je nutné vybrat metodu plánování, která se použije pro výrobní zakázky. Můžete naplánovat výrobu na úrovni operací a pracovního zařazení.

### <a name="operations-scheduling"></a>Plánování operací

Plánování operací můžete použít, když je třeba získat obecný odhad výrobního procesu v čase. Plánování operací nerozšiřuje na operace pro výrobní postup úloh. Další informace o plánování operací naleznete v tématu [Plánování operací](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Plánování úlohy

Plánování práce je podrobnější metodou plánování, kde každá operace je rozdělena na jednotlivé úkoly nebo práce. Plánování práce zahrnuje informace o kapacitě. Obvykle se používá k plánováním jednotlivých úloh v dílně a obvykle je prováděno v krátkodobém až střednědobém časovém horizontu. Další informace o plánování práce naleznete v tématu [Plánování práce](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Ochranné doby ve dnech

Pro každý plán můžete vybrat, jak daleko v budoucnosti musí být různé požadavky a další ohledy vypočítány podle hlavního plánování. Období je označováno jako *ochranná doba*. Chcete-li dosáhnout nejlepšího výkonu v hlavním plánování, doporučujeme upravit různá ochranná období tak, aby vyhovovala vašim obchodním požadavkům. Pro každý plán můžete na záložce s náhledem **Ochranná doba v dnech** na stránce **Hlavní plány** (**Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**) najít ochranné doby.

> [!NOTE]
> Ochranné doby určují, jak daleko v budoucnosti jsou vypočteny hlavním plánováním různé požadavky a další ohledy. Ochranná doba vybraná na této stránce přepíše ochrannou dobu definovanou ve skupině disponibility. To znamená, že nastavení možnosti ochranné doby na Ano a definování dnů přepíše ochrannou dobu definovanou ve skupině disponibility. Při nastavení na Ne se ochranná doba definuje ve skupině disponibility. Pokud nechcete nebo nepotřebujete použít možnost (například nechcete používat zprávy akcí), nastavte ji na hodnotu **Ano** a nastavte ochrannou dobu na **0** (nula) dní.

### <a name="coverage"></a>Pokrytí

Ochranná doba disponibility reprezentuje období plánování nebo to, jak dlouho má být poptávka zahrnuta. Jinými slovy, označuje plánovací horizont.

Nastavením možnosti **Disponibilita** na **Ano** můžete přepsat ochrannou dobu disponibility definovanou pro položku během hlavního plánování. V tomto případě zadejte počet dní, během nichž bude výpočet hlavního plánování pokrývat požadavky. Ochranná doba disponibility se počítá od aktuálního data. Požadavky, které se objevují před aktuálním datem, jsou vždy zpracovány.

> [!NOTE]
> Chcete-li dosáhnout nejlepšího výkonu v hlavním plánování, doporučujeme upravit ochrannou dobu disponibility pro svůj plánovací horizont.

### <a name="freeze"></a>Zablokovat

Ochranná doba zablokování představuje období, po které se při spuštění nového hlavního plánu nezmění existující plánované objednávky. Plánované objednávky jsou zablokovány nebudou navrhovány žádné nové objednávky.

Nastavením možnosti **Zablokovat** na **Ano** můžete přepsat ochrannou dobu zablokování definovanou pro položku během hlavního plánování. V tomto případě zadejte počet dní, během nichž by měla být aktivita plánování zablokována. Pamatujte, že během tohoto období nebudou generovány žádné nové plánované objednávky a existující plánované objednávky nelze změnit.

### <a name="firming"></a>Potvrzení

Ochranná doba potvrzení označuje časový horizont, ve kterém jsou plánované objednávky automaticky převedeny na nákupní objednávky a výrobní zakázky. Tento proces se také nazývá *automatické potvrzení plánovaných objednávek*.

Nastavením možnosti **Potvrzení** na **Ano** můžete přepsat ochrannou dobu potvrzení definovanou pro položku během hlavního plánování. V tomto případě, zadejte počet dní, po kterých budou plánované nákupní objednávky a výrobní zakázky automaticky potvrzeny. Ochranná doba potvrzení se počítá od data hlavního plánování. K automatickému potvrzení plánované nákupní objednávky může dojít pouze tehdy, pokud je položka přidružena k dodavateli.

### <a name="forecast-plan"></a>Plán prognóz

Ochranná doba plánu prognózy udává, jak daleko v budoucnu hlavní plánování vytváří plánované objednávky pro položky s prognózou poptávky.

Nastavením možnosti **Plán prognóz** na **Ano** můžete přepsat ochrannou dobu plánu prognózy definovanou pro položku během hlavního plánování. V tomto případě zadejte počet dní, po kterých by měla být prodejní prognóza z plánu prognózy zahrnuta do hlavního plánování.

### <a name="capacity"></a>Kapacita

Ochranná doba kapacity udává, jak daleko v budoucnosti systém zvažuje maximální kapacitu vašich zdrojů při plánování objednávek. Jinými slovy, plán plánuje výrobní zakázky pomocí výrobního postupu pro položky a zohledňuje zdroje výrobního postupu a maximální kapacitu jednotlivých zdrojů.

Nastavením možnosti **Kapacita** na **Ano** můžete přepsat ochrannou dobu kapacity definovanou pro položku během hlavního plánování. V tomto případě zadejte počet dní, po kterých by měla být kapacita plánována pro plánované výrobní zakázky. Hlavní plánování použije aktivní postup výroby položky a plánuje zpětně od data požadavku. Pokud datum požadavku plánované výrobní zakázky spadá mimo ochrannou dobu kapacity, bude doba realizace určena na základě času dodání položky. Ochranná doba kapacity se počítá od aktuálního data.

### <a name="action-message"></a>Zpráva akce

Zprávy akce navrhují změny, které lze provést u existující objednávky dodávky za účelem optimalizace plánu dodávek. Mohou například doporučit, abyste přesunuli na dřívější datum nebo odložili objednávky, nebo zvýšili nebo snížili množství objednávky.

Nastavením možnosti **Zpráva akce** na **Ano** můžete přepsat ochrannou dobu zprávy akce definovanou pro položku během hlavního plánování. V tomto případě zadejte počet dní, během nichž by mělo hlavní plánování generovat zprávy akce pro požadavky. Ochranná doba zprávy akce se počítá od aktuálního data.

Další informace o zprávách akce naleznete v tématu [Zprávy akce](/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Výpočet zpráv akce má za následek delší operační dobu hlavního plánování. Nejsou-li zprávy akce pravidelně analyzovány a použity (denně, týdně atd.), zvažte při spuštění hlavního plánování vypnutí výpočtu. Chcete-li vypnout výpočet, na stránce **Hlavní plány** nastavte ochrannou dobu **Zprávy akce** na **0** (nula) fpro hlavní plán, který spouštíte. Rovněž zkontrolujte, zda je nastavení **Zprávy akce** vypnuto pro všechny skupiny disponibility.

### <a name="calculated-delays"></a>Vypočtená zpoždění

Můžete určit, jak daleko v budoucnu budou zjištěna a vykazována možná zpoždění v plánovaných objednávkách. Tímto způsobem můžete naplánovat možná (opožděná) data dodání.

Pokud nemůže být plánovaná objednávka pro požadované datum splněna, je naplánována na nejdřívější datum plnění pro transakci na základě doby realizace a dostupnosti materiálu a kapacity.

### <a name="approved-requisitions-time-fence"></a>Ochranná doba schválených žádanek

Chcete-li vytvořit plánované objednávky pro poptávku žádanky, můžete nastavit hlavní plánování. Nastavte možnost **Zahrnout žádanky** na **Ano** na záložce s náhledem **Obecné** stránky **Hlavní plány**. Poté, když je účelem schválené žádanky doplnění, hlavní plánování vytvoří automaticky odpovídající plánovanou objednávku, která ho splní. Ke stanovení metody doplnění slouží zásady dodávek, které byly nastaveny pro položky ve vaší organizaci. Po vytvoření a schválení žádanky o doplnění nejsou vyžadovány žádné další akce.

Nastavením možnosti **Ochranná doba schválené žádanky** na **Ano** na záložce s náhledem dny **Ochranné doby ve dnech** můžete přepsat ochrannou dobu schválených žádanek, které je definováno pro položku během hlavního plánování. V tomto případě zadejte počet dnů v minulosti, po které má být poptávka ze schválených žádanek s účelem doplnění zahrnuta v hlavním plánování. Například můžete určit, aby byly uvažovány a plánovány pouze nesplněné poptávky po termínu ze schválených žádanek, které byly vytvořeny za posledních 10 dnů.

### <a name="sequencing"></a>Klasifikace

Klasifikace umožňuje uspořádat plánované objednávky na základě atributů klasifikace, které jsou přidruženy k dokončenému produktu. Často se používá k přípravě výrobních zakázek pro balení. Lze jej například použít k balení krabic v určitém pořadí na základě barvy a velikosti.

Nastavením možnosti **Klasifikace** na hodnotu **Ano** můžete určit, jak daleko v budoucnu mají být operace nebo úlohy seřazeny. Mějte na paměti, že čím větší je ochranná doba, tím déle bude trvat i hlavní plánování.

### <a name="calculated-delays"></a>Vypočtená zpoždění

Možnosti zpoždění pomáhají zaručit, že objednávky mají proveditelná plánovaná data. Na záložce s náhledem **Vypočtená zpoždění** stránky **Hlavní plány** jsou k dispozici následující možnosti:

- **Zajistiti, aby plánované objednávky nebyly vytvořeny před datem spuštění hlavního plánování.** – tuto možnost nastavte na **Ano**, chcete-li zaručit, aby objednávky nebylo možné plánovat pro data v minulosti.
- **Přidat vypočtené zpoždění k požadovanému datu** (v rámci **plánovaných nákupních objednávek**) – tuto možnost nastavte na **Ano**, chcete-li do požadavků přidat vypočítané zpoždění.
- **Přidat vypočtené zpoždění k požadovanému datu** (v rámci **plánovaných výrobních zakázek**) – tuto možnost nastavte na **Ano**, chcete-li do požadavků přidat vypočítané zpoždění.
- **Přidat vypočtené zpoždění k požadovanému datu** (v rámci **plánovaných převodů**) – tuto možnost nastavte na **Ano**, chcete-li do požadavků přidat vypočítané zpoždění.
- **Přidat vypočtené zpoždění k požadovanému datu** (v rámci **plánovaných kanbanů**) – tuto možnost nastavte na **Ano**, chcete-li do požadavků přidat vypočítané zpoždění.

Nastavíte-li možnost **Přidat vypočtené zpoždění k požadovanému datu** na **Ano** pro přidání zpoždění k požadavkům, bude systém zohledňovat kapacitu zdrojů a vytvoří proveditelné plánované objednávky. Přepočet dat plánované objednávky zvýší čas spuštění hlavního plánování. Pokud tedy nepotřebujete používat zpoždění, nastavte možnosti na **Ne**.

## <a name="positive-and-negative-days"></a>Kladné a záporné dny

Kladné a záporné dny ovlivňují způsob, jakým hlavní plánování navrhuje plánované objednávky a akce. Kladné a záporné dny se nastavují na skupině disponibility položky pro danou položku. Můžete definovat různé skupiny disponibility a nastavit jejich parametry na stránce **Skupiny disponibility** (**Hlavní plánování \> Nastavení \> Disponibilita \> Skupiny disponibility**).

### <a name="positive-days"></a>Kladné dny

Kladné dny naznačují, jak daleko v budoucnu hlavní plánování zvažuje aktuální zásoby nebo příjmy ke splnění budoucí poptávky. Jsou-li například kladné dny nastaveny na **100**, lze aktuální zásoby použít k plnění poptávky v příštích 100 dnech. Pokud existuje objednávka 150 dní od aktuálního data, hlavní plánování vytvoří plánovanou objednávku pro splnění poptávky, i když množství na skladě pro položku může objednávku splnit. U položek s rychlým pohybem, které mají krátkou dobu realizace, pravděpodobně nebudete chtít použít množství na skladě pro objednávku, která je daleko v budoucnosti. V tomto rychlém případě bude aktuální množství na skladě rychle pryč a další objednávky lze provést do budoucna, aby splnily budoucí poptávku včas. což by bylo možné kvůli krátké době realizace položky.

Kladné dny také ovlivní zprávy akce. Systém může například doporučit, abyste zvýšili plánovanou nákupní objednávku tak, aby zahrnovala poptávku, která spadá do počtu kladných dnů v budoucnosti. Pokud jsou kladné dny nastaveny na **100** a pokud pro položku existuje poptávka za 30 dní od aktuálního data, systém vytvoří plánovanou objednávku, která splní danou poptávku. Pokud existuje poptávka pro stejnou položku za 90 dnů od aktuálního data, systém doporučí, abyste zvýšili množství objednávky za 30 dnů od aktuálního data, takže objednávka též pokryje požadavek za 90 dnů. Pokud však existuje poptávka pro položku za 150 dní od aktuálního data, systém nedoporučí, abyste zvýšili množství objednávky, které bylo již naplánováno. Namísto toho bude vytvořena nová plánovaná objednávka.

Jako pravidlo jsou kladné dny nastaveny na číslo, které je mezi nejdelší dobou realizace položek a ochrannou dobou disponibility. Doporučujeme vám přiřazovat položky, které jsou pravidelně pořízeny nebo vyráběny do skupiny disponibility, kde kladné dny odpovídají době realizace položky.

### <a name="negative-days"></a>Dny zpoždění

Záporné dny označují, jak budou povoleny opožděné příjmy položek. Představují počet dní, které jste ochotni čekat před objednáním nového doplnění v případě záporného množství zásob nebo nedostatku zásob. Záporné dny odpovídají na otázku: Máme vytvořit novou nákupní objednávku pro položku nebo máme použít existující nákup, přestože víme, že položka bude opožděná?

Například máte prodejní objednávku pro položku 15 dní od aktuálního data. Máte také nákupní objednávku pro stejnou položku. Tato nákupní objednávka bude přijata za 20 dnů od aktuálního data. Chcete, aby systém vytvořil nákupní objednávku pro tuto prodejní objednávku nebo chcete použít existující objednávku, i když nemůžete splnit prodejní objednávku včas? Pokud jsou záporné dny nastaveny na méně než **5**, což znamená, že položka může být zpožděna maximálně o pět dní, systém vytvoří novou plánovanou nákupní objednávku pro splnění prodejní objednávky. Jsou-li záporné dny nastaveny na hodnotu vyšší než **5**, systém použije pro danou položku stávající objednávku.

Záporné dny také ovlivňují výkon hlavního plánování. Pokud jsou záporné dny nastaveny na vysoké číslo, bude vygenerováno mnoho zpráv akce.

Doporučujeme nastavit záporné dny na číslo, které je menší než doba realizace položky.

### <a name="dynamic-negative-days"></a>Dynamické záporné dny

Dynamické záporné dny zvažují dobu realizace položky a dny, které jste zadali. Systém vytvoří novou plánovanou nákupní objednávku na základě ochranné doby záporných dnů, která je vypočtena pomocí následujícího vzorce:

Doba realizace + záporné dny + aktuální datum – datum požadavku

Systém používá pouze plánované objednávky dodávek, které jsou v této ochranné době, a vytváří novou plánovanou objednávku mimo ni. Výhodou dynamických negativních dnů je, že bude zahrnuta doba realizace jednotlivého produktu pro opětovné použití existujících objednávek a pro zamezení vytváření nových plánovaných objednávek, které budou ukončeny později v důsledku zpoždění způsobených dobou realizace. 

Další informace naleznete v tématu [Záporné dny a dynamické záporné dny](/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]