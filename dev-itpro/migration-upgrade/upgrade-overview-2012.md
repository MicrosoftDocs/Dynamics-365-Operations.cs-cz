---
title: Upgrade aplikace Dynamics AX 2012 na Microsoft Dynamics 365 for Financials and Operations, Enterprise Edition
description: "Toto téma popisuje proces, který mohou využít zákazníci, kteří aktuálně používají Microsoft Dynamics AX 2012 k přesunutí dat a kódu do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: cs-cz
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Upgrade aplikace Microsoft Dynamics AX 2012 na Microsoft Dynamics 365 for Financials and Operations, Enterprise Edition

[!include[banner](../includes/banner.md)]

V aktualizaci Platform 8 poskytuje aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise edition cestu pro upgrade, kterou mohou využít zákazníci, kteří aktuálně používají Microsoft Dynamics AX 2012, k přesunutí svých dat a kódu do aplikace Finance and Operations. Proces upgradu je založen na následujících prvcích:

- Nástroje, které pomáhají uspíšit existující kód vlastní aplikace z AX 2012.
- Proces upgradu dat, který vám pomůže s přemístěním databáze. Můžete tedy upgradovat úplnou transakční historii.

## <a name="overview"></a>Přehled

Celkový proces upgradu je možné vizualizovat jako tři společné fáze: analýza, provedení a ověření.

Následující diagram znázorňuje komplexní proces upgradu a činnosti, které považujeme za součást jednotlivých fází. 

![Proces upgradování](./media/upgrade-process.png)

## <a name="analyze"></a>Analyzovat

Aktivity ve fázi nápovědy Analýza vám pomohou odhadnout úsilí potřebné pro upgrade. Dále umožňují připravit plán projektu. Tyto aktivity lze provést před zakoupením aplikace Finance and Operations. Pomohou vám učinit informované nákupní rozhodnutí tím, že poskytují datový bod o úsilí a zdrojích, které budete potřebovat.

### <a name="sign-up-for-a-public-preview-in-lcs"></a>Přihlášení k veřejnému náhledu v LCS

Aby bylo možné před zakoupením aplikace Finance and Operations provádět aktivity analýzy, můžete se přihlásit k veřejnému náhledu. Veřejný náhled umožňuje nasadit vlastní prostředí aplikace Finance and Operations. Dále poskytuje přístup k nástrojům v aplikaci Microsoft Dynamics Lifecycle Services (LCS), které se používají k vyhodnocení prostředí AX 2012 a existujícího vlastního kódu.

Pokud máte existující projekt LCS pro aplikaci AX 2012, musíte se přesto přihlásit k dalšímu novému projektu k vyhodnocení aplikace Finance and Operations.

Další informace o tom, jak získat veřejný náhled pro zákazníky, získáte na adrese https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Další informace o tom, jak získat veřejný náhled pro partnery, získáte na adrese https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Počítejte s tím, že se tento veřejný náhled liší od [30denní zkušební verze](https://aka.ms/D365OperationTrials). Třicetidenní zkušební verze obsahují nasazené instance aplikace Finance and Operations, které slouží k prohlížení a vyhodnocení aplikace. Aktivity analýzy však vyžadují úplné zkušenosti a nástroje LCS.

### <a name="select-the-upgrade-methodology"></a>Výběr metodologie upgradování
V novém projektu LCS nastavte metodologii projektu na **Upgrade AX 2012 na Dynamics 365 for Operations**. Tato metodologie je vytvořena speciálně pro zákazníky AX 2012, kteří upgradují. Podrobně popisuje tři fáze a poskytuje odkazy na veškerou podpůrnou dokumentaci týkající se procesu.

![Metodologie upgradu(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>Spuštění analyzátoru upgradu
Nástroj Analyzátor upgradu běží v prostředí AX 2012 a identifikuje úkoly, které byste měli podniknout v rámci přípravy prostředí AX 2012 na pomoc při usnadnění a zlevnění upgradu:

- **Vyčištění dat** – tento proces pomáhá identifikovat data, které lze odebrat, aniž by došlo ke ztrátě funkcí. Tento nástroj identifikuje různé typy údajů, které můžete zredukovat, spuštěním procesu čištění. Pro každý datový typ je uvedeno vysvětlení o dopadu čištění. Pak můžete rozhodnout, zda spustit proces čištění. Část nákladů na předplatné aplikace Finance and Operations je založena na velikosti databáze. Snížením velikosti proto zredukujete tuto komponentu ceny předplatného a také pomůžete zkrátit čas potřebný pro realizaci upgradu. Menší databáze pomáhá zaručit rychlejší upgrade.
- **Konfigurace SQL** – Tento proces shrnuje konfiguraci SQL a doporučí optimalizace. Zajištěním, že SQL běží optimálně, pomáhá tento proces zkrátit čas potřebný pro realizaci upgradu.
- **Funkce, které se již nepoužívají** – Tento proces identifikuje funkce, které právě používáte, ale které nejsou v aplikaci Finance and Operations k dispozici. Proto pomáhá dříve zjistit mezery funkčnosti. Také poskytuje návrhy alternativ.

Dále je v rámci tohoto kroku třeba nainstalovat článek znalostní báze KBXXXXXXX v prostředí AX 2012. Tato prava hotfix obsahuje kontrolní seznam před upgradem. V prostředí AX 2012 můžete tento kontrolní seznam použít k zadávání dat, která vyžaduje postup upgradu. Například v jednom úkolu kontrolního seznamu před upgradem zadáte přihlašovací informace služby Azure Microsoft Active Directory (Azure AD) pro aktuálního uživatele aplikace AX 2012 tak, aby se každý uživatel mohl přihlásit k aplikaci Finance and Operations.

Výstup tohoto kroku se stane tokem práce v plánu projektu upgradu pro správce systému AX 2012.

Další informace naleznete v tématu [Analýza: Použití analyzátoru upgradu k naplánování práce migrace](upgrade-analyzer-tool.md).

### <a name="run-the-code-upgrade-estimation-tools"></a>Spuštění nástrojů odhadu upgradu kódu
Tento krok převezme váš kód z aplikace AX 2012, převede ho do nového formátu a poskytne zpětnou vazbu o konfliktech, které musí vývojář vyřešit později. Tento krok je základem pro odhad nákladů na upgrade kódu.

Dokončení tohoto kroku vyžaduje export kódu aplikace AX 2012 jako export úložiště modelu a jeho nahrání do nástroje pro upgrade kódu LCS. Tento nástroj pro upgrade kódu vytvoří upgradovanou verzi kódu a sestavy o zbývajících konfliktech, které je nutné vyřešit. Vývojář pak může zkontrolovat upgradovaný kód a sestavu k určení míry úsilí, které bude vyžadováno za účelem upgradování základu kódu.

Výstup tohoto kroku představuje tok práce v plánu projektu upgradu pro vývojáře aplikace Microsoft Dynamics AX.

Další informace naleznete v tématu [Analýza: Odhad úsilí pro upgrade kódu](analyze-code-upgrade.md).

### <a name="deploy-a-demo-environment"></a>Nasazení ukázkového prostředí
Ukázková prostředí jsou výchozí prostředí, která obsahují ukázková data (nikoli vaše vlastní dat) a standardní kód (žádné přizpůsobení). Doporučujeme, abyste nasadili ukázkové prostředí pro vyhodnocení nových funkcí a k provedení základní analýzy mezer vhodnosti standardních procesů používaných v aplikaci AX 2012, ale které mohly být v aplikaci Finance and Operations změněny. Tato ukázková prostředí můžete nasadit v Azure nebo si je stáhnout jako virtuální počítač, na kterém spustíte vlastní hardware. Pokud je nasadíte na Azure, musíte poskytnout předplatné Azure, protože stále používáte projekt veřejného nákladu a dosud jste nezakoupili předplatné Finance and Operations.

Výstup tohoto kroku představuje tok práce v plánu projektu upgradu pro funkční nebo firemní uživatele.

Další informace naleznete v tématu [Analýza: Nasazení prostředí sandbox](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>Vytvoření plánu projektu
V metodologii upgradu je k dispozici šablona plánu projektu. V tomto kroku výstup z předchozích kroků fáze analýzy slouží k vyplnění plánu projektu pro projekt upgradu. Plán projektu bude obsahovat také všechny podrobnosti testování: testování upgradu dat, přelomové testování, minulé iterace funkčního testu a podrobné informace o různých přiřazeních zdrojů pro tyto úkoly.

V této fázi obsahuje plánu projektu datový bod, který vám může pomoci zjistit čas a náklady, které bude zahrnovat upgrade na aplikaci Finance and Operations.

## <a name="execute"></a>Spustit
Během fáze spouštění budete zpracovávat úlohy naplánované během fáze analýzy. Pokud chcete přejít do fáze provedení, je třeba zakoupit si aplikaci Finance and Operations. Také musíte mít k dispozici prostředky, které fungují v upgradu.

### <a name="switch-to-the-lcs-implementation-project"></a>Přechod na projekt implementace LCS
Projekt veřejného náhledu použitý pro fázi analýzy posloužil svému účelu. Můžete ho nyní zrušit. Pro zbývající kroky požadujete pouze plán projektu, který jste vytvořili v posledním kroku fáze analýzy.

Pokud zakoupíte předplatné aplikace Finance and Operations, zobrazí se podrobné informace o tom, jak se přihlásit k novému projektu LCS. Tento projekt se nazývá projekt implementace a bude představovat nový trvalý projekt LCS pro předplatné, dokud toto předplatné máte. Tento projekt se liší od veřejného náhledu projektu v tom, že ho spravuje společnost Microsoft. Proto má tento projekt tyto charakteristiky:

- Všechna prostředí projektu jsou hostovaná v Azure.
- Předplatné Azure, které je spojené s projektem, spravuje společnost Microsoft. Proto neexistuje žádná samostatná fakturace Azure nákladů. Náklady se vztahují k předplatnému aplikace Finance and Operations.
- Společnost Microsoft spravuje provozní prostředí projektu. Z toho vyplývá, že nasazení kódu, upgrady a údržbu infrastruktury provádí přímo společností Microsoft, nikoli vaši zaměstnanci. 

### <a name="perform-the-ax-2012-preparation-tasks"></a>Provádění úkolů přípravy AX 2012
Dokončete úkoly, které zjistil nástroj pro analýzu upgradu a které jsou zdokumentovány v plánu projektu upgradu. Tyto úkoly musí provést správce systému Microsoft Dynamics AX a správce databáze (DBA).

[Upgrade dat z aplikace AX 2012 na Dynamics 365 for Operations – kontrolní seznam před upgradováním v aplikaci AX 2012](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>Provedení upgradu kódu
Dokončete úkoly, které byly naplánovány v průběhu kroku odhadu upgradu kódu v rámci fáze Analýza. Tyto úlohy musí provádět vývojáři.

Od tohoto bodu by měly být změny kódu v aplikaci AX 2012 zmrazeny. V aplikaci AX 2012 by měly být povoleny pouze změny nouzových kódů. Pokud dojde ke změně, musí být ručně přenesena do nové základny kódu.

### <a name="develop-new-code"></a>Vývoj nového kódu
Proveďte úkoly z analýzy mezer, která byla provedena během kroku Nasazení ukázkového prostředí fáze Analýza. Tyto úlohy budou pravděpodobně kombinaci funkčních úkolů, které definují úkoly konfigurace a rozvoje pro vlastní nastavení, která se vztahují k novým prováděným funkcím.

### <a name="data-upgrade-development-environment"></a>Upgrade dat (vývojové prostředí)
Po dokončení úkolů upgradu kódu můžete poprvé upgradovat databázi AX 2012 pro Finance and Operations. První upgrade probíhá ve vývojovém prostředí, abyste mohli snáze napravit nebo odstranit jakékoli potíže, které se zjistí v této fázi. Ve vývojovém prostředí lze okamžitě ladit chyby, upravit kód a znovu spustit upgrade během pár minut. Větší prostředí sandbox tuto flexibilitu nenabízejí a bude třeba minimálně několik hodin ladění a nápravy problémů, aktualizace kódu, nasazení aktualizovaného kódu a opětovného spuštění upgradu.

Následující obrázek znázorňuje proces. Stačí zálohovat databázi aplikace AX 2012, odeslat ji na Azure, obnovit v prostředí Finance and Operations a spustit upgrade dat.

![Upgrade dat ve vývojovém prostředí](./media/data-upgrade-dev.png)
 
Upgrade dat se provádí prostřednictvím zvláštního typu balíčku s možností nasazení. Stejný mechanismus slouží k nasazení nového kódu aplikace Finance and Operations do jiného prostředí.

Základní soustava, která slouží pro převod dat v databázi během tohoto procesu je z velké míry stejná jako systému upgradu v aplikaci AX 2012, který je založen na dávkových úlohách X++, které mají spuštěné třídy **ReleaseUpdatexxx**.

Další informace naleznete v tématu [Upgrade dat z aplikace AX 2012 to Dynamics 365 for Operations ve vývojovém prostředí](data-upgrade-2012.md).

### <a name="data-upgrade-sandbox-environments"></a>Upgrade dat (prostředí sandbox)
Po dokončení upgradu dat ve vývojovém prostředí lze stejný postup spustit v prostředí sandbox. Prostředí sandbox je takové prostředí, kde podnikoví uživatelé a funkční členové týmu mohou testovat obchodní procesy pomocí upgradovaných data kódu aplikace AX 2012.

Následující obrázek znázorňuje proces spuštění upgradu dat v prostředí sandbox. Rozdíl spočívá v tom, že v tomto poli je použit nástroj bacpac místo tradiční zálohy SQL. Tento nástroj je požadován pro převod mezi serverem Microsoft SQL Server a databází Azure SQL. Je to standardní nástroj SQL a není specifický pro aplikaci Finance and Operations.

![Upgrade dat v prostředí sandbox](./media/data-upgrade-sandbox.png)

Další informace naleznete v tématu [Upgrade dat z aplikace AX 2012 to Dynamics 365 for Operations v prostředí sandbox](upgrade-data-sandbox.md).
 
## <a name="validate"></a>Ověřit
Když přejdete do fáze ověření, budete mít k dispozici prostředí, která zahrnují vlastní kód a upgradovaná data. Tato fáze popisuje proces ověření a testování, ve kterém upgradované prostředí funguje požadovaným způsobem. Dále popisuje proces, uvedení do praxe.

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>Testování přechodu a vytvoření plánu přechodu
Pojem _přechod_ zde slouží k popisu finálního procesu uvedení nového systému do provozu. Tento proces se skládá z úlohy vzniklé po vypnutí produktu AX 2012 a před zprovozněním aplikace Finance and Operations. 

Cílem testování je vyzkoušení procesu přechodu. Tímto způsobem můžete zaručit, že každý uživatel, který je zapojen do skutečného uvedení přechodu do provozu, má plynulé možnosti zkušenosti.

Existují dva hlavní proudy práce:

- **Technický proud práce** – Tento proud práce je proces spuštění upgradu dat. Vaše společnost vynutí limit povoleného množství prostojů. Během tohoto výpadku nebude k dispozici aplikace AX 2012 ani Finance and Operations. Technický proud práce bude nejspíš muset vyladit postup upgradování dat, aby byl splněn limit prostojů firmy. 
- **Funkční proud práce** – po upgradu dat bude zapotřebí několik konfigurací úloh v prostředí Finance and Operations. Všechny tyto úlohy musí být zdokumentované a kvantifikované a musí mít přiřazený zdroj, protože musí jít dohromady s technickými úlohami v rámci limitů prostojů společnosti.

Další informace viz 
- [Ověřování: Přechodové testování](upgrade-cutover-testing.md)
- [Ověřování: Proces ověřování aplikace](app-validation-process.md)

### <a name="functional-test-pass"></a>Úspěšný funkční test
Dokončete úplné funkční testování všech obchodních procesů. Toto testování bude představovat rozsáhlé opětovné otestování všech obchodních procesů, které se týkají aplikace Finance and Operations. Tyto obchodní procesy zahrnují i staré procesy, které byly převedeny z aplikace AX 2012, a nové procesy, které zahrnují nové funkce použité poprvé v aplikaci Finance and Operations. 

Podle kvality kódu může náprava a opětovné testování problémů vyžadovat několik iterací funkčního testování. Po vyřešení problému nezapomeňte znovu otestovat všechny zahrnuté procesy na pomoc se zajištěním, že změna neovlivní podřízené a nadřazené procesy.

Další informace naleznete v tématu [Ověření: funkční testování](upgrade-functional-validation.md).

### <a name="pre-go-live-checklist"></a>Kontrolní seznam před aktivací
Kontrolní seznam před aktivací je doporučený postup, který vám může pomoci zredukovat pravděpodobnost vzniku chyb během konečným uvedením do provozu. Týden před uvedením do provozu ukončete změny konfigurace v AX 2012 (v části \<module\>\Setup). Tato omezení změn konfigurace je čistě procedurální. Správce systému Microsoft Dynamics AX pouze odsouhlasí zablokování tohoto typu změn v daném bodě.

Doporučujeme zastavit také změny kódu v kódovém základu aplikace Finance and Operations. Neměly by být dovoleny žádné další změny, pokud nejsou vyhodnoceny a neukáže se, že uvedení do provozu neblokují.  

Po nasazení omezení konfigurace a zmrazení kódu je vhodné naposledy před přechodem spustit upgrade dat. Tímto způsobem zajistíte, že vše pracuje podle očekávání. 

Podrobnosti získáte v tématu [Ověřování: Příprava pro ostré nasazení](upgrade-go-live-prep.md)



### <a name="supported-upgrade-paths"></a>Podporované cesty upgradu
Od června 2017 je podporován upgrade na aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, verze 0617 is supported z Microsoft Dynamics AX 2012 R3. Jsou podporovány všechny kumulativní aktualizace aplikace AX 2012 R3.

Microsoft Dynamics AX 2012 R2 a Microsoft Dynamics AX 2012 RTM nejsou aktuálně podporovány. Podpora bude k dispozici později v roce 2017.

Je podporován pouze upgrade na verzi aplikace Finance and Operations nasazenou v cloudu. Upgrade na místní verzi není podporován. Podpora upgradu na místní verzi bude k dispozici později v roce 2017.

