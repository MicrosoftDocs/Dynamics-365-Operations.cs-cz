---
title: Omnikanálové rozšířené automatické náklady
description: Toto téma popisuje funkce pro správu dalších nákladů objednávky pro objednávky velkoobchodní sítě pomocí funkcí rozšířených automatických nákladů.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: 826c955b7c99073ff41c8a5ed75254c824359925
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175147"
---
# <a name="omni-channel-advanced-auto-charges"></a>Omnikanálové rozšířené automatické náklady

[!include [banner](includes/banner.md)]

Toto téma obsahuje informace o konfiguraci a nasazení funkce rozšířených automatických nákladů, které jsou k dispozici v aplikaci Dynamics 365 for Retail verze 10.0.

Pokud jsou funkce rozšířených automatických nákladů povoleny, objednávky vytvořené v libovolném podporovaném kanálu Commerce (pokladní místo (POS), kontaktní středisko a online) mohou využít konfigurací [automatických nákladů](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) definovaných v aplikaci ERP pro související náklady záhlaví a úrovně řádku.

Ve verzích předcházejících aplikaci 10.0 bývaly konfigurace [automatických nákladů](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) přístupné pouze pro objednávky vytvořené v kanálech e-Commerce a kontaktního střediska. Ve verzi 10.0 a novějších mohou objednávky vytvořené v POS využít konfigurace automatických nákladů. Tímto způsobem další vedlejší náklady mohou být systematicky přidány do prodejních transakcí.

Používáte-li verze starší než je verze 10.0, uživatel POS je vyzván k ručnímu zadání dopravného během vytváření transakcí POS „expedovat vše“ nebo „expedovat vybrané“. Zatímco funkce vedlejších nákladů v aplikaci se používají s ohledem na to, jak jsou náklady zapsány do objednávky, není poskytován systematický výpočet - výpočet se opírá o vstup uživatele, který určuje hodnotu nákladů. Náklady lze přidat pouze jako jeden kód nákladů souvisejících s expedicí a nelze je snadno upravit ani změnit v POS po jejich vytvoření.

Použití ruční výzvy k přidání nákladů na expedici je stále k dispozici ve verzi 10.0 a starších. Pokud organizace nepovolí parametr **rozšířené automatické náklady**, výzvy POS k ručnímu zadání nákladů zůstanou stejné.

Díky funkci rozšířených automatických nákladů mohou mít uživatelé POS systematické výpočty pro všechny definované vedlejší náklady založené na tabulkách nastavení automatických nákladů. Navíc uživatelé budou mít možnost přidávat nebo upravovat neomezené množství dodatečných nákladů a poplatků do jakékoli prodejní transakci POS na záhlaví nebo na úrovni řádku (pro „cash and carry“ nebo objednávku odběratele).

## <a name="enabling-advanced-auto-charges"></a>Povolení rozšířených automatických nákladů

Na stránce **Maloobchod a velkoobchod \> Nastavení centrály \> Parametry \> Parametry velkoobchodu** přejděte na kartu **Objednávky odběratele**. Na záložce s náhledem **Náklady** nastavte možnost **Použít rozšířené automatické náklady** na **Ano**.

![Parametr rozšířených automatických nákladů](media/advancedchargesparameter.png)

Když jsou povoleny rozšířené automatické náklady, uživatelé nejsou nadále vyzýváni k ručnímu zadání nákladů na terminálu POS při vytváření objednávky odběratele expedovat vše a expedovat vybrané. Náklady objednávky POS jsou systematicky vypočítávány a přidávány k transakci POS (pokud je nalezena odpovídající tabulka automatických nákladů, která odpovídá kritériu vytvářené objednávky). Uživatelé mohou přidávat nebo udržovat náklady záhlaví nebo na úrovni řádku ručně prostřednictvím nově přidaných operací POS, které lze přidat do rozvržení obrazovky POS.

Pokud jsou povoleny rozšířené automatické náklady, existující **Parametry velkoobchodu** pro **Kód dopravného** a **Refundovat dopravné** se již nepoužívají. Tyto parametry jsou použitelné pouze tehdy, když je parametr **Použít rozšířené automatické náklady** nastaven na **Ne**.

Než povolíte tuto funkci, ujistěte se, že jste vyzkoušeli a vyškolili své zaměstnance, protože to změní tok obchodních procesů výpočtu dopravného a jiných nákladů a přidání do prodejních objednávek POS. Ujistěte se, že rozumíte dopadu toku procesu na vytváření transakcí z POS. Pro objednávky kontaktního střediska a e-Commerce je dopad povolení rozšířených automatických nákladů minimální. Aplikace kontaktního střediska a e-Commerce budou mít nadále stejné chování, které měly v minulosti, v souvislosti s tabulkami automatických nákladů pro výpočet dalších nákladů objednávky. Uživatelé kanálu kontaktního střediska budou nadále mít možnost ručně upravit veškeré automatické náklady vypočítané systémem v záhlaví nebo na úrovni řádku, nebo ručně přidat další vedlejší náklady na záhlaví nebo úrovni řádku.

## <a name="additional-pos-operations"></a>Další operace POS

Aby rozšířené automatické náklady fungovaly správně v prostředí vaší aplikace POS, byly přidány nové operace POS. Tyto operace musí být přidány do vašeho [rozvržení obrazovky POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) a nasazeny na zařízení POS při nasazení rozšířených automatických nákladů. Pokud tyto operace nebudou přidány, uživatelé nebudou schopni spravovat nebo udržovat vedlejší náklady na transakcích POS a nebudou mít žádný způsob, jak upravit nebo změnit hodnoty nákladů, které jsou systematicky vypočítávány na základě konfigurace automatických nákladů. Minimálně navrhujeme nasadit operaci **Spravovat náklady** do vašeho rozvržení POS.

Nové operace jsou následující.

- **142 – Spravovat náklady** – Tuto operaci použijte k tomu, aby uživatelé POS mohli zobrazit a upravovat vedlejší náklady pro transakci POS, které byly buď přidány ručně nebo systematicky pomocí výpočtů automatických nákladů.
- **141 - Přidat náklady záhlaví** – Tuto operaci použijte k tomu, abyste uživateli umožnili ručně přidat vedlejší náklady na úrovni záhlaví do jakékoliv prodejní transakce POS (a vybrat kód nákladů, který se má použít).
- **140 - Přidat náklady řádku** – Tuto operaci použijte k tomu, abyste uživateli umožnili ručně přidat vedlejší náklady na úrovni řádku do jakéhokoliv řádku prodejní transakce POS (a vybrat kód nákladů, který se má použít).
- **143 - Přepočítat náklady** – Použijte tuto operaci k provedení úplného přepočítání nákladů pro prodejní transakci. Veškeré dříve uživatelem přepsané automatické náklady budou přepočítány na základě aktuální konfigurace košíku.

Jako u všech operací POS lze provést konfigurace zabezpečení, aby bylo požadováno schválení manažerem za účelem provedení operace.

Je důležité poznamenat, že výše uvedené operace POS lze také přidat k rozvržení POS, i v případě, když je parametr **Použít rozšířené automatické náklady** zakázán. V tomto scénáři budou organizace stále přidávat další výhody v tom, že budou moci zobrazit manuálně přidané náklady a upravovat je pomocí operace **Spravovat náklady**. Uživatel může rovněž použít operace **Přidat náklady záhlaví** a **Přidat náklady řádku** pro POS transakce, i když je parametr **Použít rozšířené automatické náklady** zakázán. Operace **Přepočítat náklady** má nižší funkci, je-li použita při zákazu možnosti **Použít rozšířené automatické náklady**. V tomto scénáři by nebylo nic přepočítáno a veškeré náklady ručně přidané do transakce by se pouze resetovaly na 0,00 USD.

## <a name="use-case-examples"></a>Použití příkladů případu

V této části jsou uvedeny ukázkové příklady použití, které vám pomohou porozumět konfiguraci a použití automatických nákladů a vedlejších nákladů v kontextu objednávek kanálu. Tyto příklady ilustrují chování aplikace při povolení parametru **Použít automatické rozšířené náklady**.

### <a name="auto-charges-header-charges-example"></a>Příklad nákladů záhlaví automatických nákladů

#### <a name="use-case-scenario"></a>Příklad použití

Maloobchodní prodejce chce automaticky přidávat náklady za dopravné při vytváření transakcí v jakémkoli velkoobchodním kanálu, který vyžaduje dodávku produktů zákazníkovi. Prodejce nabízí dva způsoby dodání: po zemi a letecky. Pokud zákazník zvolí dodání po zemi a hodnota objednávky je menší než 100 USD, prodejce chce zpoplatnit odběratele za dopravné částkou 10 USD. Pokud je objednávka vyšší než 100 USD a zákazník si zvolí pozemní dopravu, zákazníkovi nebudou účtovány žádné dodatečné poplatky za dopravu. Pokud si zákazník zvolí způsob dodávky letecky pro všechny objednávky, bez ohledu na jejich celkovou hodnotu, bude účtován poplatek za dopravu ve výši 20 USD.

#### <a name="setup-and-configuration"></a>Instalace a konfigurace

Tento scénář vyžaduje konfiguraci dvou tabulek s automatickými náklady.

Přejděte na **Pohledávky \> Nastavení nákladů \> Automatické náklady**.

Nakonfigurujte dva druhy různých automatických nákladů na úrovni záhlaví. Nakonfigurujte jeden pro doručení po zemi a druhý pro doručení letecky. V tomto scénáři je nakonfigurujte tak, aby se používaly pro všechny odběratele.

U nákladů za pozemní doručení definujte v části řádků stránky **Automatické náklady** náklad 10 USD, který bude použit pro objednávky mezi 0,01 a 100 USD. Vytvořte jiný řádek nákladů pro označení, že objednávky nad 100,01 USD nebudou mít žádné náklady.

![Příklad automatických nákladů](media/headerchargesexample.png)

U nákladů za letecké doručení definujte v části řádků formuláře automatických nákladů náklad 20 USD, který bude použit na všechny objednávky (mezi 0,01 a 9 999 999 USD).

Odešlete změny do databáze Commerce Scale Unit/kanál, aby je mohlo POS použít spuštěním úlohy **1040 plán distribuce**.

#### <a name="sales-processing-for-this-scenario"></a>Zpracování prodeje pro tento scénář

Po dokončení výše uvedených konfiguračních kroků a použití změn databáze kanálu použije každá objednávka odběratele nebo prodejní transakce vytvořená v kanálech POS, kontaktního střediska nebo e-Commerce se způsobem doručení po zemi nebo letecky nastaveným na úrovní řádku tyto náklady a automaticky je aplikuje na prodej.

V tuto chvíli se náklady budou vztahovat na všechny prodejní transakce vytvořené v rámci právnické osoby, která používá tyto způsoby doručení, protože neexistuje žádná funkce, která by označovala, že konfigurace automatických nákladů bude platit pouze pro konkrétní prodejní kanál.

Protože není jasně definované záhlaví na těchto objednávkách, náklady na úrovni řádků se pro scénáře POS a e-Commerce použijí pouze tehdy, když všechny řádky prodeje na transakci jsou nastaveny na expedici se stejným způsobem dodání. Jestliže existují smíšené způsoby plnění na transakcích vytvořených pomocí POS nebo e-Commerce, budou zvažovány a použity pouze automatické náklady na úrovni řádku.

Ve scénářích kontaktního střediska má uživatel kontrolu nad nastavením způsobu dodání na záhlaví objednávky. Proto se náklady na úrovni záhlaví použijí pro tyto objednávky i v případě, že některé řádky prodeje byly nakonfigurovány pro použití jiného způsobu dodání. Náklady na úrovni záhlaví pro objednávky kontaktního střediska budou vždy založeny na způsobu dodání, který je definován na úrovni záhlaví prodejní objednávky.

### <a name="auto-charges-line-charges-example"></a>Příklad nákladů řádku automatických nákladů

#### <a name="use-case-scenario"></a>Příklad použití 

Maloobchodní prodejce chce přidat další náklady odběrateli za instalační poplatky v případě, kdy odběratel zakoupí určitý model počítače. Tento počítač vyžaduje další nevolitelné instalační akce, které je prodejce provede pro odběratele. Prodejce informoval odběratele, že za tuto instalaci bude účtovat další poplatek. Maloobchodní prodejce preferuje správu nákladů spojených s tímto poplatkem odděleně od prodejní ceny produktu pro účely finančního výkaznictví. Instalační poplatek 19,99 USD bude odběrateli účtován při koupi tohoto konkrétní počítače v libovolném kanálu.

#### <a name="setup-and-configuration"></a>Instalace a konfigurace

Tento scénář vyžaduje konfiguraci jedné tabulky s automatickými náklady na úrovni řádku.

Přejděte na **Pohledávky \> Nastavení nákladů \> Automatické náklady**.

Nastavte rozevírací nabídku **Úroveň** na **Řádek** a vytvořte nový záznam automatických nákladů pro všechny odběratele a pro konkrétní produkt nebo skupinu produktů, u kterých bud účtován instalační poplatek.

![Příklad automatických nákladů](media/linechargesexample.png)

Odešlete poplatky do databáze Commerce Scale Unit/kanál, aby je mohlo POS použít spuštěním úlohy **1040 plán distribuce**.

#### <a name="sales-processing-for-this-scenario"></a>Zpracování prodeje pro tento scénář

Po dokončení výše uvedených konfiguračních kroků a použití změn databáze kanálu spustí každá objednávka odběratele nebo prodejní transakce vytvořená v kanálech POS, kontaktního střediska nebo e-Commerce s touto položkou na objednávce náklady na úrovni řádku, které budou systematicky přidány k celkové objednávce.

V tuto chvíli se náklady budou vztahovat na všechny řádky prodeje, které se shodují s konfigurací automatických nákladů na úrovni řádku v rámci právnické osoby, protože neexistuje žádná funkce pro konfiguraci automatických nákladů, která platí pouze pro konkrétní prodejní kanál.

### <a name="manual-header-charges-example"></a>Příklad ručních nákladů záhlaví

#### <a name="use-case-scenario-description"></a>Popis příkladu použití

Maloobchodní prodejce uděluje výjimku z typických procesů tím, že nabízí speciální dodávku produktů domů zákazníkům, kteří objednávají produkty v obchodě. Prodejce a zákazník se dohodli, že zákazník za tuto službu zaplatí další manipulační poplatek ve výši 25 USD. Osoba přebírající objednávku musí přidat tento dodatečný poplatek k transakci. Vzhledem k tomu, že poplatek je paušální a nesouvisí s žádným konkrétním produktem na objednávce, bude použit náklad záhlaví.

#### <a name="setup-and-configuration"></a>Instalace a konfigurace

Ujistěte se, že kód nákladů, který bude použit v tomto scénáři, byl správně nakonfigurovaný přechodem na **Pohledávky \> Nastavení nákladů \> Náklady** pro definování příslušného kódu nákladů pro tento scénář.

![Příklad nákladů](media/chargesexample.png)

Pokud by poplatek měl být považován za náklad související s přepravou pro účel slevy nebo propagace související s přepravou, nastavte **Dopravné** na kódu nákladů na **Ano**. Pokud je rovněž možné tento poplatek systematicky refundovat během procesu transakce vrácení v aplikaci POS, nastavte **Vratný** na **Ano**. Příznak **Vratný** lze použít pouze tehdy, když je parametr **Použít rozšířené automatickyé náklady** nastaven na hodnotu **Ano**.

Odešlete poplatky do databáze Commerce Scale Unit/kanál, aby je mohlo POS použít spuštěním úlohy **1040 plán distribuce**.

Operace **Přidat náklady záhlaví** musí být nakonfigurována ve vašem [rozvržení obrazovky POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) tak, aby tlačítko, které je dostupné pro uživatele z POS, mohlo volat tuto operaci (operaci 141). Změny rozvržení obrazovky musí být distribuovány do kanálu, stejně jako prostřednictvím funkce plánu distribuce.

#### <a name="sales-processing-of-manual-header-charges"></a>Zpracování prodeje ručních nákladů záhlaví

Pro provedení scénáře v aplikaci POS uživatel POS vytvoří obvyklou prodejní transakci a do prodeje přidá produkty a další konfigurace. Před inkasováním platby by měl uživatel provést operaci platbu **Přidat náklady záhlaví**, která vyzve uživatele k výběru kódu nákladů a zadání hodnoty nákladů. Jakmile uživatel dokončí proces, náklad bude přidán do prodejní objednávky jako náklad na úrovni záhlaví.

Tento proces lze použít v kontaktním středisku pomocí stávající funkce **Náklady**, která se nalézá na kartě **Prodej** na panelu nástrojů. Na stránce **Spravovat náklady** může uživatel přidat nový řádek nákladů do záhlaví objednávky.

### <a name="manual-line-charges-example"></a>Příklad ručních řádků záhlaví

#### <a name="use-case-scenario"></a>Příklad použití

Odběratel požádal, aby dvě z pěti položek na jeho prodejní objednávce byly dárkově zabaleny. Prodejce poskytuje tuto volitelnou službu za poplatek 2 USD za položku. Osoba přebírající objednávku bude muset přidat tyto poplatky ke konkrétním položkám, které mají být dárkově zabaleny.

#### <a name="setup-and-configuration"></a>Instalace a konfigurace

Ujistěte se, že kód nákladů, který bude použit v tomto scénáři, byl správně nakonfigurovaný přechodem na **Pohledávky \> Nastavení nákladů \> Náklady** pro definování příslušného kódu nákladů pro tento scénář.

Pokud by poplatek měl být považován za náklad související s přepravou pro účel slevy nebo propagace související s přepravou, nastavte **Dopravné** na kódu nákladů na **Ano**. Pokud je rovněž možné tento poplatek systematicky refundovat během procesu transakce vrácení v aplikaci POS, nastavte **Vratný** na **Ano**. Příznak **Vratný** lze použít pouze tehdy, když je parametr **Použít rozšířené automatickyé náklady** nastaven na hodnotu **Ano**.

Odešlete poplatky do databáze Commerce Scale Unit/kanál, aby je mohlo POS použít spuštěním úlohy **1040 plán distribuce**.

Operace **Přidat náklady řádku** musí být nakonfigurována ve vašem [rozvržení obrazovky POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) tak, aby tlačítko, které je dostupné pro uživatele z POS, mohlo volat tuto operaci (operaci 140). Změny rozvržení obrazovky musí být distribuovány do kanálu, stejně jako prostřednictvím funkce plánu distribuce.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Zpracování prodeje ručních nákladů řádku

Pro provedení scénáře v aplikaci POS uživatel POS vytvoří obvyklou prodejní transakci a do prodeje přidá produkty a další konfigurace. Před inkasováním platby by měl uživatel vybrat konkrétní řádek, kde se použijí náklady ze zobrazení seznamu položek POS, a provést operaci **Přidat náklady** řádku. Uživatel bude vyzván ke zvolení kódu nákladů a zadání hodnoty nákladů. Jakmile uživatel dokončí proces, náklad bude propojen na řádek a přidán k součtu objednávky jako náklad na úrovni řádku. Uživatel může opakovat proces pro přidání dalších nákladů řádku k dalším řádkům položek na transakci v případě potřeby.

Stejný proces lze použít v kontaktním středisku pomocí funkce Udržovat náklady, která se nalézá pod rozevírací nabídkou **Finance** v části **Řádky prodejní objednávky** na stránce **Prodejní objednávka**. Tím se otevře stránka **Udržovat náklady**, kde může uživatel přidat nový náklad specifický pro řádek k transakci.

## <a name="additional-features"></a>Další funkce

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Úprava nákladů na prodejní transakci POS

Operace **Správa nákladů** (142) by měla být přidána do [rozvržení obrazovky POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) tak, aby uživatel mohl zobrazit a upravit nebo přepsat jakékoli systémem vypočítané nebo ručně vytvořené náklady na úrovni řádku nebo záhlaví. Není-li operace přidána, uživatelé nebudou moci upravit hodnotu nákladů na transakci POS, ani nebudou schopni zobrazit podrobnosti o nákladech, jako je typ kódu nákladů navázaný na náklad.

Na stránce **Spravovat náklady** v POS může uživatel zobrazit podrobnosti nákladů na úrovni záhlaví a řádku. Uživatel může použít funkci **Upravit** dostupnou na této stránce pro provedení změn částky účtované na konkrétní řádek nákladů. Jakmile je řádek nákladů ručně přepisován, nebude systematicky přepočítáván, pokud uživatel neinicializuje operaci **Přepočítat náklady**.

Pokud byl **Kód důvodu přepsání nákladů** nakonfigurován na stránce nastavení **Parametry velkoobchodu**, uživatel bude vyzván k zadání kódu důvodu, když byly upraveny náklady v aplikaci POS.

Pokud byly kódy důvodů zaznamenány pro přepsané náklady, přepsán, bude k dispozic též nová sestava pro kontrolu a audit těchto přepsání. Sestava se nalézá v možnostech **Maloobchod a velkoobchod \> Dotazy a sestavy \> Historie přepsání nákladů**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Refundace nákladů na transakci vrácení POS

Pokud je parametr **Použít rozšířené automatické náklady** nastaven na hodnotu **Ano**, existující parametr velkoobchodu pro možnost **Refundovat dopravné** již není k dispozici. Chcete-li uvést, které poplatky by měly být zákazníkovi systematicky refundovány při použití rozšířených automatických nákladů, zkontrolujte, zda je příslušný kód nákladů nakonfigurován **Vratný** na stránce nastavení **Kód nákladů**. Ujistěte se, že nastavení byla synchronizována do databází velkoobchodní sítě prostřednictvím zpracování plánu distribuce.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Refundace nákladů na transakci vratky

Náklady nejsou systematicky refundovány do **vratek** vytvořených v aplikaci Commerce. Uživatelé musí vybrat možnost **kopírovat náklady** při vytvoření **vratky**. Pokud není možnost **Kopírovat náklady** zvolena, náklady z původní prodejní transakce nebudou automaticky refundovány. Pokud je možnost **Kopírovat náklady** zvolena, všechny náklady se zkopírují do vratky a uživatel může ručně upravovat nebo odebrat veškeré náklady, které nechce mít refundované. Proces vratky kontaktního střediska aktuálně nepřipouští příznak **Vratný** v nastavení **Kód nákladů**.

### <a name="configuring-pos-receipts-to-show-charges"></a>Konfigurace příjemek POS pro zobrazení nákladů

Následující prvky příjemky byly přidány na řádek a zápatí příjemky pro podporu funkce rozšířených automatických nákladů.

- **Náklady expedice řádku** - Tento prvek na úrovni řádku lze použít k souhrnu kódů konkrétních nákladů, které byly použity na řádek prodeje. Pouze kódy nákladů, které byly označeny příznakem jako náklady **Expedice** na stránce **Kód nákladů** se zobrazí na tomto místě.
- **Jiné náklady řádku** - Tento prvek na úrovni řádku lze použít k souhrnu kódů konkrétních neexpedičních nákladů, které byly použity na řádek prodeje. Jedná se o kódy nákladů, kde příznak **Expedice** na stránce **Kód nákladů** nebyl povolen.
- **Podrobnosti dopravného objednávky** - Tento prvek na úrovni zápatí zobrazí popisy kódů nákladů, které jsou použity na objednávku s příznakem nákladů **Expedice** na stránce nastavení **Kód nákladů**.
- **Dopravné objednávky** - Tento prvek na úrovni zápatí zobrazuje peněžní hodnotu nákladů souvisejících s expedicí.
- **Podrobnosti jiných nákladů objednávky** - Tento prvek na úrovni zápatí zobrazí popis kódů nákladů, které jsou použity na objednávku bez příznaku nákladů souvisejících s expedicí.
- **Jiné náklady objednávky** - Tento prvek na úrovni zápatí zobrazuje peněžní hodnotu jiných nákladů nesouvisejících s expedicí.

Doporučujeme, aby organizace rovněž přidala volná textová pole do zápatí příjemky za účelem definování oblastí, kde budou náklady shrnuty.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Zabránění výpočtu nákladů do dokončení objednávky POS

Některé organizace mohou chtít počkat, než uživatel dokončí přidání všech prodejních řádků k transakci POS před výpočtem nákladů. Chcete-li zabránit výpočtu nákladů, když se k transakci POS přidávají položky, zapněte parametr **Ruční výpočet nákladů** ve **funkčním profilu** používaném obchodem. Povolení tohoto parametru vyžaduje, aby uživatel POS použil operaci **Vypočítat součty** po dokončení přidání produktů k transakci POS. Operace **Vypočítat součty** poté spustí výpočet jakýchkoliv automatických nákladů pro záhlaví nebo řádky objednávky podle potřeby.

### <a name="charges-override-reports"></a>Sestavy přepsání nákladů

Pokud uživatelé ručně přepíší vypočtené náklady nebo přidají ruční náklady do transakce, budou tato data dostupná pro audit v sestavě **Historie přespání nákladů**. K sestavě lze získat přístup z: **Maloobchod a velkoobchod \> Dotazy a sestavy \> Historie přepsání nákladů**. Je důležité poznamenat, že data potřebná pro tuto sestavu se importují z databáze maloobchodní sítě do HQ prostřednictvím úloh plánování distribuce "P". Informace o přepsáních právě provedených v POS proto nemusí být okamžitě k dispozici v této sestavě, dokud tato úloha nenahraje data transakce obchodu do HQ.

## <a name="additional-resources"></a>Další prostředky

[Povolení a konfigurace automatických nákladů podle kanálu](auto-charges-by-channel.md)

[Poměrné rozdělení nákladů záhlaví na odpovídající řádky prodeje](pro-rate-charges-matching-lines.md)

