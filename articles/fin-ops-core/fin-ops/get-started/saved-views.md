---
title: Uložená zobrazení
description: V tomto tématu je popsán způsob použití funkcí uložených zobrazení.
author: jasongre
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 4b1bd7b869b68f82ce8056ac9f87a0d3bdce4102
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190872"
---
# <a name="saved-views"></a>Uložená zobrazení

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Úvod
Individuální nastavení hraje důležitou roli, která umožňuje uživatelům a organizacím optimalizovat uživatelské podmínky tak, aby vyhovovaly jejich potřebám. Další podrobnosti o individuálním nastavení najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

S tradičním individuálním nastavením mohou uživatelé používat pouze jednu sadu individuálních nastavení pro každý formulář. Uložená zobrazení se v individuálním natavení rozšiřují několika důležitými způsoby:

-    Zobrazení umožňují uživatelům používat více pojmenovaných sad individuálních nastavení pro každý formulář, které mohou rychle přepínat podle potřeby. To umožňuje uživateli vytvořit více optimalizovaných zobrazení stránky, kde každé zobrazení bylo upraveno tak, aby vyhovovalo potřebám konkrétního obchodního úkolu. 

-    Zobrazení vytvořená pro určité typy stránek mohou zahrnovat také filtry přidané uživatelem, což uživatelům umožňuje rychle se vrátit k běžně filtrovaným datovým sadám. Další informace naleznete v části [Které stránky podporují zobrazení](saved-views.md#what-pages-support-views). 

-    Zobrazení lze publikovat do rolí zabezpečení, což znamená, že každý uživatel s touto rolí bude moci přistupovat k tomuto zobrazení a používat je bez ohledu na možnost přizpůsobení. Tato schopnost publikování umožňuje organizacím definovat standardní podniková zobrazení optimalizovaná pro jejich podnikání. Další informace naleznete v části [Správa individuálních nastavení na organizační úrovni se zobrazeními](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    Na rozdíl od tradičního přizpůsobení nejsou zobrazení automaticky uložena, když uživatel provádí explicitní přizpůsobení nebo filtruje seznam. Explicitní ukládání je nutné k zajištění pružnosti při vytváření zobrazení před nebo po provedení změn souvisejících s tímto zobrazením a zajištění, že definice zobrazení nejsou neúmyslně změněny filtry nebo přizpůsobeními, které nejsou určeny pro dlouhodobé použití.  

## <a name="switching-between-views"></a>Přepínání mezi zobrazeními
Po povolení zobrazení pro prostředí bude libovolná stránka, která podporuje zobrazení, obsahovat sbalený ovládací prvek voliče zobrazení v horní části formuláře, který zobrazuje název aktuálního zobrazení.  

Výběr zobrazení obsahuje dvě varianty velikosti: 

-   **Selektory velkého zobrazení**: Stránky, které výrazně vyplní seznam, budou mít větší výběr zobrazení z několika důvodů. Nejdůležitější je, že větší selektor zobrazení označuje stránky, jejichž zobrazení může zahrnovat uživatelem definované filtry. Vzhledem k tomu, že filtry jsou zahrnuty v zobrazeních, je rovněž odůvodněna větší velikost selektoru, protože zobrazené názvy jsou často nejlepším popisem dat zobrazených na obrazovce a očekávání je, že uživatelé budou pro tyto typy stránek častěji přepínat mezi zobrazeními.  
 
-   **Selektory malého zobrazení**: všechny ostatní formuláře přes celou stránku (s výjimkou pracovních prostorů a řídicích panelů) mají menší výběr zobrazení, který se zobrazí vedle titulku stránky. Zobrazení na těchto stránkách zahrnují pouze přizpůsobení (a ne uživatelem definované filtry). Na těchto stránkách se často jedná o nejdůležitější informace v horní části formuláře. Menší velikost také odráží nižší očekávanou frekvenci přepínání zobrazení na těchto stránkách. 
 
Kliknete-li na název zobrazení, otevře se výběr zobrazení a zobrazí se seznam dostupných zobrazení pro tuto stránku.

-    **Klasické zobrazení**: klasické zobrazení je zobrazení stránky bez explicitního přizpůsobení, které jste použili.  
-    **Osobní zobrazení**: Zobrazení bez zámků představují vaše osobní zobrazení. Jedná se o zobrazení, která jste vytvořili, nebo která vám dal správce.  
-    **Zamčená zobrazení**: Některá zobrazení (jako klasické zobrazení a všechna zobrazení publikovaná v dané roli) mají ve voliči zobrazení vedle sebe visací zámek, což znamená, že tato zobrazení nelze upravovat. Implicitní vlastní nastavení, která odrážejí využití stránky, jsou však automaticky uložena, například změna šířky sloupce mřížky nebo rozbalení či sbalení pevné záložky. Můžete však vytvořit individuální zobrazení založené na uzamčeném zobrazení s použitím akce **Uložit kopii**, pokud máte oprávnění pro individuální nastavení.
-    **Nová zobrazení**: Publikovaná zobrazení, která ještě nebyla otevřena, jsou vymezena pomocí podnícení nalevo od názvu zobrazení.  

Chcete-li přepnout do jiného zobrazení, otevřete nejprve selektor zobrazení a poté vyberte zobrazení, které chcete načíst. 

## <a name="creating-and-modifying-views"></a>Vytváření a úpravy zobrazení
Na rozdíl od tradičního přizpůsobení nejsou zobrazení automaticky uložena, když uživatel provádí explicitní přizpůsobení (nebo filtruje seznam). Chcete-li uložit tyto změny do zobrazení, je nutné zadat explicitní akci. To poskytuje pružnost uživatelů při vytváření zobrazení před nebo po provedení změn souvisejících s tímto zobrazením a zajištění, že definice zobrazení nejsou neúmyslně změněny jednorázovými filtry nebo přizpůsobeními, které nejsou určeny pro dlouhodobé použití. Všimněte si, že implicitní vlastní nastavení (jako rozbalení nebo sbalení pevné záložky nebo změna šířky sloupce mřížky) jsou automaticky uložena do aktuálního zobrazení i u uzamčených zobrazení. 

Chcete-li zajistit, aby byl znám aktuální stav zobrazení, při zahájení provádění změn zobrazení pomocí explicitního přizpůsobení nebo filtrování se vedle aktuálního názvu zobrazení zobrazí hvězdička, která označuje, že prohlížíte neuloženou, upravenou verzi tomto zobrazení.

Chcete-li tyto změny uložit, postupujte podle následujících kroků.
1.  Chcete-li otevřít selektor zobrazení, vyberte název zobrazení.
2.  Změna stávajícího zobrazení:
     1. Zvolte **Uložit**. Všimněte si, že tato akce nebude povolena pro zamčená zobrazení. 
3.  Vytvoření nového zobrazení:
     1.    Vyberte **Uložit kopii**. 
     2.    Zadejte název (a volitelně) popis zobrazení.
     3.    Zvolte **Uložit**.

## <a name="changing-the-default-view"></a>Změna výchozího zobrazení
Výchozí zobrazení je zobrazení, které se systém pokusí otevřít při prvním přechodu na stránku. Tato možnost by měla být nastavena na zobrazení, které budete pravděpodobně používat nejčastěji.  

Pokud chcete změnit výchozí zobrazení stránky, postupujte takto: 
1.  Přepněte na zobrazení, které používáte jako výchozí. 
2.  Chcete-li otevřít selektor zobrazení, vyberte název zobrazení. 
3.  Vyberte **Více** a potom **Připnout jako výchozí**.  

Případně můžete při vytváření nového zobrazení (pomocí akce **Uložit kopii**) nastavit toto nové zobrazení jako výchozí nastavením možnosti **Připnout jako výchozí** před uložením zobrazení.  

Všimněte si, že v některých případech se dotaz přidružený k výchozímu zobrazení nespustí při prvním přechodu na stránku. Pokud například přejdete v dlaždici na stránku, bude dotaz dlaždice proveden bez ohledu na dotaz přidružený k výchozímu zobrazení. Pokud také přejdete na stránku, jejíž klasické zobrazení již má definovaný dotaz, bude původní dotaz proveden místo dotazu výchozího zobrazení. Pokud k tomu dojde, zobrazí se při načítání zobrazení výstražná informační zpráva. Přepnutí zobrazení po načtení stránky by umožnilo spuštění dotazu zobrazení očekávaným způsobem.

## <a name="managing-personal-views"></a>Správa osobních zobrazení 
Dialogové okno **Spravovat moje zobrazení** poskytuje základní funkce pro správu osobních zobrazení a pořadí zobrazení v selektoru zobrazení. Chcete-li otevřít tuto stránku, kliknutím na název zobrazení otevřete rozevírací nabídku selektoru zobrazení, vyberte **Více** a poté vyberte možnost **Spravovat moje zobrazení**.  

Chcete-li zobrazit seznam dostupných zobrazení pro tuto stránku, je k dispozici následující soubor akcí.  
-    **Změna výchozího zobrazení**: Použijte akci **Připnout jako výchozí**, aby se aktuálně zvýrazněné zobrazení nastavilo pro tuto stránku jako výchozí.  
-    **Změnit pořadí zobrazení**: Pomocí akce **Přesunout nahoru** a **Přesunout dolů** změňte pořadí zobrazení na konkrétní pořadí.  
-    **Přejmenovat zobrazení**: Pomocí akce **Přejmenovat** změňte název aktuálně zvýrazněného osobního zobrazení. Tato akce je pro zamčená zobrazení vypnuta. 
-    **Odstranění zobrazení**: pomocí akce **odebrat** trvale odstraníte aktuálně zvýrazněné zobrazení ze stránky. Po odebrání nelze zobrazení nijak obnovit.  

Změny provedené v tomto dialogovém okně se projeví po výběru tlačítka **Uložit**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Správa individuálních nastavení na organizační úrovni se zobrazeními
Chcete-li porozumět zlepšení správy osobních nastavení na úrovni organizace, podívejme se nejprve, jak Správa přizpůsobení pro vlastní nastavení fungovala před zobrazením.  

Bez zobrazení mohli správci pro stránku použít sadu individuálních nastavení pro uživatele nebo skupinu uživatelů pomocí stránky pro individuální nastavení. Pokud mají tito uživatelé práva pro individuální nastavení, používalo se na této stránce individuální nastavení. Nebylo však možné zabránit uživatelům v další personalizaci stránky, což znamenalo, že organizace nemohla uživatelům zajistit konzistentní uživatelské rozhraní. Pokud některý z těchto uživatelů neměl práva pro individuální nastavení, nebyla zavedena individuální nastavení, která jim byla přidělena správcem. Když navíc byli do určité organizace zařazeni noví uživatelé, bylo nutné, aby správci ručně načetli sadu individuálních nastavení pro daného uživatele. Neexistoval žádný automatický mechanismus pro určení, že určitá sada individuálních nastavení by měla být dostupná pro uživatele v dané roli.

Pomocí funkce uložená zobrazení je Správa organizace individuálního nastavení podstatně snadnější, především kvůli možnosti publikování zobrazení rolím zabezpečení. Po publikování zobrazení bude každý uživatel s touto rolí moci přistupovat k tomuto zobrazení a používat je bez ohledu na možnost přizpůsobení. Zatímco má každý uživatel kopii v publikovaném zobrazení, v němž je použito automatické přizpůsobení stránky (implicitní individuální nastavení), nemůže žádný uživatel uložit explicitní přizpůsobení nebo aktualizace dotazu do publikovaného zobrazení (tj. publikovaná zobrazení jsou uzamčena). Pokud navíc novému uživateli byla přidělena role, do kterého bylo zobrazení publikováno, budou automaticky zobrazena zobrazení přidružená k jejich rolím bez zásahu správce. Podobně pokud uživatel změní role v organizaci, zobrazení přidružená k původní roli již nebudou dostupná, a to ani bez zásahu správce. Aktualizace publikovaného zobrazení lze uživatelům snadno distribuovat tím, že zobrazení znovu publikujete do příslušných rolí zabezpečení.

Tato schopnost publikování umožňuje organizacím definovat standardní podniková zobrazení optimalizovaná pro jejich podnikání zaměřené na uživatele s konkrétními rolemi zabezpečení.  

## <a name="publishing-views"></a>Publikování zobrazení
Během procesu publikování lze zobrazení přiřadit k jedné nebo více rolím zabezpečení, což znamená, že každý uživatel s touto rolí bude moci přistupovat k tomuto zobrazení a používat je, ale nemůže upravit zobrazení. V současné době mají v rozevírací nabídce selektoru práva k akci **Publikování** pouze správci systému, ale v budoucí aktualizaci bude k dispozici nová role zabezpečení, která poskytne práva pro publikování jiným důvěryhodným uživatelům.  

Zobrazení publikujete takto. 
1.  Vytvořte a uložte osobní kopii zobrazení, kterou chcete publikovat. 
2.  V zobrazení, které je aktuálně načteno, vyberte název zobrazení pro otevření rozevírací nabídky selektoru zobrazení. 
3.  Vyberte tlačítko **Další** a potom **Publikovat**. Otevře se dialogové okno Publikovat.  
4.  Zadejte název a (volitelně) popis zobrazení. Toto jméno se zobrazí uživatelům, kteří toto zobrazení obdrží, v jejich selektorech zobrazení. Na stránce nejsou povoleny žádné duplicitní názvy pro publikovaná zobrazení, a to ani v případě, že se seznam rolí, které se používají, liší.  
5.  Přidejte všechny role zabezpečení, které odpovídají uživatelům, kteří budou moci zobrazit toto zobrazení.  
6.  Zvolte **Publikovat**.

Všimněte si, že v některých prostředích může tato doba trvat dlouho (až hodinu), než uživatelé uvidí publikované zobrazení.

## <a name="modifying-a-published-view"></a>Úprava publikovaného zobrazení
Po publikování zobrazení můžete zjistit, že chcete provést změny v publikovaném zobrazení. Ačkoli v publikovaném zobrazení nelze provádět změny přímo, protože jsou tato zobrazení uzamčena pro úpravy pro všechny uživatele (včetně vydavatelů), můžete zobrazení aktualizovat opětovným publikováním.  

Pokud změny, které chcete provést v publikovaném zobrazení, zahrnují pouze parametry publikování (název a popis zobrazení nebo role zabezpečení, ve kterých je zobrazení publikováno), proveďte následující akce: 
1.  Přepněte do zobrazení Publikováno pro parametry, které chcete aktualizovat. 
2.  V rozevírací nabídce selektoru zobrazení vyberte **Publikovat**. 
3.  Pokud chcete aktualizovat existující zobrazení, vyberte **Ano** (nebo vyberte **Ne**, pokud je chcete publikovat s jiným názvem).
4.  Aktualizujte název, popis nebo role zabezpečení zobrazení. 
5.  Zvolte **Publikovat**. 
6.  Pokud jste aktualizovali název publikovaného zobrazení, bude také nutné odstranit publikované zobrazení s původním názvem (Další informace naleznete v části **Správa publikovaných zobrazení**). 

Pokud změny provedené v publikovaném zobrazení zahrnují úpravy přizpůsobení nebo filtrů spojených se zobrazením, postupujte následujícím způsobem: 
1.  Přepněte do publikovaného zobrazení pro parametry, které chcete změnit. 
2.  Uložte kopii publikovaného zobrazení a vytvořte místní koncept publikovaného zobrazení. 
3.  Upravte místní koncept o potřebné změny.
4.  Publikujte zobrazení s původním názvem. 

## <a name="managing-published-views"></a>Správa publikovaných zobrazení
Podobně jako správa osobních zobrazení poskytuje dialogové okno **Správa mých zobrazení** uživatelům s oprávněním k publikování základní možnosti správy nad publikovanými zobrazeními dané stránky (kromě vlastních osobních zobrazení). Chcete-li otevřít tuto stránku, výběrem názvu zobrazení otevřete rozevírací nabídku selektoru zobrazení, vyberte **Více** a poté vyberte možnost **Spravovat moje zobrazení**.

Zatímco všichni uživatelé vidí kartu **Moje zobrazení** s osobními zobrazeními, uživatelům s oprávněním k publikování se zobrazí také karta **Publikováno**, která zobrazuje všechna publikovaná zobrazení pro danou stránku. Vzhledem k tomu, že zobrazení může publikovat několik uživatelů, je důležité mít možnost spravovat úplný seznam publikovaných zobrazení bez ohledu na to, zda jste uživatelem, který zobrazení skutečně publikoval.

Chcete-li zobrazit seznam všech dostupných zobrazení pro tuto stránku, je k dispozici následující soubor akcí. 

-    **Publikování**: chcete-li znovu publikovat zobrazení s upravenými parametry publikování (název, popis, role zabezpečení), použijte akci **Publikování**.  
-    **Odebrat**: k trvalému odstranění publikovaného zobrazení použijte akci **odebrat**. Tato akce odebere zobrazení pro všechny uživatele v systému.  
 
Změny provedené v tomto dialogovém okně se projeví až po výběru tlačítka **Uložit**.

## <a name="frequently-asked-questions"></a>Časté dotazy
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Jak povolím uložená zobrazení v mém prostředí? 
Chcete-li povolit uložená zobrazení, když je tato funkce v náhledu, postupujte podle následujících kroků: 

1.  **Povolit let**: spustit následující příkaz SQL: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Obnovit IIS** pro vyprázdnění statickou mezipaměť testovací verze. 

3.  **Najít funkci**: přejděte do pracovního prostoru **Správa funkcí**. Pokud se **Uložená zobrazení** v seznamu neobjeví, vyberte **Vyhledat aktualizace**.   

4.  **Povolit funkci**: vyhledejte funkci **Uložená zobrazení** v seznamu funkcí a v podokně podrobností vyberte **Povolit nyní**.

Všechny následující uživatelské relace budou začínat uloženým zobrazením.  

Všimněte si, že pokud je individuální nastavení pro dané prostředí vypnuto, zobrazení budou zakázána i v případě, že provedete výše uvedené kroky. Důvodem je, že funkce zobrazení je postavena na podsystému individuálního nastavení.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Co se stane se stávajícími individuálními nastaveními, když jsou povolena zobrazení? 
Jsou-li povolena zobrazení, budou všechna existující individuální nastavení pro uživatele a formulář uložena do nového zobrazení s názvem **Moje zobrazení**, které je automaticky nastaveno jako výchozí zobrazení. To je určeno k zajištění konzistentního uživatelského prostředí před a po povolení zobrazení, kromě toho, že se na formulářích zobrazí ovládací prvek selektoru.  

### <a name="what-pages-support-views"></a>Které stránky podporují zobrazení? 
Zobrazení jsou k dispozici ve většině, ale ne na všech stránkách. Zobrazení jsou aktuálně k dispozici na všech stránkách na celé obrazovce s výjimkou řídicích panelů a pracovních prostorů. Neúplné stránky obrazovky, které obsahují dialogová okna, rozevírací dialogová okna, vyhledávání, rozšířené náhledy, aktuálně nepodporují zobrazení. Zobrazení podpory pro další typy stránek, jako jsou například pracovní prostory a dialogová okna, může být vzato v úvahu pro budoucí aktualizaci.   

### <a name="who-is-allowed-to-publish-views"></a>Kdo smí publikovat zobrazení?
V současné době představují správci systému jediné uživatele, kteří mají práva k publikování v zobrazeních.  V budoucí aktualizaci je plánována nová role zabezpečení, která poskytne zákazníkům větší flexibilitu, jakou mohou publikovat.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Proč nemohu uložit filtry s tímto zobrazením? 
Existuje několik důvodů, proč se filtr nemusí zobrazit pro uložení se zobrazením: 

- Stránka pravděpodobně nepodporuje ukládání filtrů v rámci definice zobrazení. Všimněte si, že pouze stránky s vybranými velkými zobrazeními umožňují přizpůsobení a úpravy dotazů, které mají být uloženy jako zobrazení. Další informace naleznete v části Přepínání zobrazení. 

- Pokud je zobrazení výchozím zobrazením a navigační cesta na stránce obsahuje dotaz, dotaz na zobrazení nebude pravděpodobně použit jako počáteční. Jedná se o dva primární scénáře, které jsou následující: 
     - Pokud například přejdete v dlaždici na stránku, bude dotaz dlaždice proveden bez ohledu na dotaz přidružený k výchozímu zobrazení. 
     - Pokud také přejdete na stránku, jejíž vstupní bod obsahuje dotaz, bude původní dotaz proveden místo dotazu výchozího zobrazení. 
     
  Na tyto situace by vás měla upozornit výstražná informační zpráva. Můžete také potvrdit přepnutí do tohoto zobrazení po načtení stránky, což by mělo umožnit spuštění dotazu zobrazení.  

- Je možné, že daná stránka nebude správně podporovat zobrazení, protože může zcela ignorovat zobrazení dotazu nebo může pracovat s dočasnou tabulkou, jejíž data nejsou trvalá. 
