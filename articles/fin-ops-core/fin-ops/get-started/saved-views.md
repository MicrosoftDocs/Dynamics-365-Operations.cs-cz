---
title: Uložená zobrazení
description: V tomto článku je popsán způsob použití funkcí uložených zobrazení.
author: jasongre
ms.date: 07/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 6faf71ec5d14584034f9107c33ccce1cd1d393c7
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220325"
---
# <a name="saved-views"></a>Uložená zobrazení

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

[!INCLUDE [PEAP](../../../includes/peap-1.md)]

## <a name="introduction"></a>Úvod

Individuální nastavení hraje důležitou roli, která umožňuje uživatelům a organizacím optimalizovat uživatelské podmínky tak, aby vyhovovaly jejich potřebám. Další podrobnosti o individuálním nastavení najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

Tradiční individuální nastavení umožňuje uživatelům používat pouze jednu sadu individuálních nastavení na stránku. Funkce **Uložená zobrazení** se v individuálním nastavení rozšiřují několika důležitými způsoby:

- Zobrazení umožňují uživatelům používat více pojmenovaných sad individuálních nastavení pro každý formulář, které mohou rychle přepínat podle potřeby. To umožňuje uživateli vytvořit více optimalizovaných zobrazení stránky, kde každé zobrazení bylo upraveno tak, aby vyhovovalo potřebám konkrétního obchodního úkolu. 
- Zobrazení vytvořená pro určité typy stránek mohou zahrnovat také filtry přidané uživatelem, což uživatelům umožňuje rychle se vrátit k běžně filtrovaným datovým sadám. Další informace naleznete v části [Které stránky podporují zobrazení](saved-views.md#what-pages-support-views). 
- Zobrazení mohou být publikována uživatelům v určitých rolích zabezpečení a konkrétních právnických osob. Proto může libovolný uživatel, který má zadanou roli a přístup do zadané právnické osoby, přistupovat k tomuto zobrazení a používat ho, i když tento uživatel nemusí mít oprávnění jej přizpůsobit. Tato schopnost publikování umožňuje organizacím definovat standardní podniková zobrazení optimalizovaná pro jejich podnikání. Další informace naleznete v části [Správa individuálních nastavení na organizační úrovni se zobrazeními](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- Na rozdíl od tradičního přizpůsobení nejsou zobrazení automaticky uložena, když uživatel provádí přizpůsobení nebo filtruje seznam. Explicitní uložení jsou vyžadována, aby uživatelům poskytla flexibilitu k vytvoření zobrazení před nebo po provedení změn souvisejících s tímto zobrazením. Tento požadavek také zajišťuje, aby definice zobrazení nebyly neúmyslně změněny filtry, nebo personalizace, které nejsou určeny k dlouhodobému použití. Položky, které systém automaticky ukládá jako součást typického využití stránky (například šířky sloupců nebo rozbalený nebo sbalený stav sekcí), se uloží na jedno zobrazení.
- Zobrazení lze přidat do pracovních prostorů jako dlaždice, seznamy nebo odkazy. Filtrovanou datovou sadu je tedy možné rozdělit do pracovního prostoru a uživatelé mohou přidružit sadu individuálních nastavení, která jsou relevantní pro danou datovou sadu s dlaždicí nebo propojením.

## <a name="switching-between-views"></a>Přepínání mezi zobrazeními

Po zpřístupnění zobrazení pro prostředí bude horní část libovolné stránky, která podporuje zobrazení, obsahovat sbalený ovládací prvek voliče zobrazení v horní části formuláře, který zobrazuje název aktuálního zobrazení.

Výběr zobrazení obsahuje dvě varianty velikosti: 

- **Selektory velkého zobrazení** - Stránky, které výrazně vyplní seznam, budou mít větší výběr zobrazení z několika důvodů. Nejdůležitější je, že větší selektor zobrazení označuje stránky, jejichž zobrazení může zahrnovat uživatelem definované filtry a řazení. Vzhledem k tomu, že filtry a řazení jsou zahrnuty v zobrazeních, je rovněž odůvodněna větší velikost selektoru, protože zobrazené názvy jsou často nejlepším popisem dat zobrazených na obrazovce a očekávání je, že uživatelé budou pro tyto typy stránek častěji přepínat mezi zobrazeními. Seskupení v mřížce lze také uložit do zobrazení na stránce s výběrem velkých zobrazení. 
    
    [![Velký výběr zobrazení, který podporuje úpravy dotazů v zobrazení.](./media/views-largeViewSelector.png)](./media/views-largeViewSelector.png)

- **Selektory malého zobrazení** - všechny ostatní stránky přes celou obrazovku (s výjimkou pracovních prostorů a řídicích panelů) mají menší výběr zobrazení, který se zobrazí vedle titulku stránky. Zobrazení na těchto stránkách zahrnují pouze přizpůsobení a ne uživatelem definované filtry. Na těchto stránkách se často jedná o nejdůležitější informace v horní části stránky. Menší velikost selektoru zobrazení také odráží nižší očekávanou frekvenci přepínání zobrazení na těchto stránkách. 
    
    [![Malý výběr zobrazení, který nepodporuje úpravy dotazů v zobrazení.](./media/views-smallViewSelector.png)](./media/views-smallViewSelector.png)
 
Vyberte-li název zobrazení, otevře se výběr zobrazení a zobrazí se seznam dostupných zobrazení pro tuto stránku.

**Verze 10.0.21 nebo novější:** Pokud je zapnutá funkce **Vylepšená podpora právnických osob pro uložená zobrazení**, volič zobrazení zobrazuje dostupná zobrazení ve dvou sekcích. První část zobrazuje všechna zobrazení, která jsou specifická pro aktuální právnickou osobu, a druhá ukazuje pohledy, které jsou k dispozici všem právnickým osobám. První část je viditelná pouze v případě, že pro stránku existují pohledy specifické pro právnické osoby.

- **Standardní zobrazení**: **Standardní** zobrazení je zobrazení stránky bez explicitního přizpůsobení, které jste použili.
- **Osobní zobrazení** - Zobrazení bez zámků představují vaše osobní zobrazení. Jedná se o zobrazení, která jste vytvořili, nebo která vám dal správce.
- **Uzamknutá zobrazení** - Některá zobrazení (například **Standardní** zobrazení a všechna zobrazení publikovaná u vaší role) mají vedle sebe v selektoru zobrazení symbol zámku. Tento symbol označuje, že tato zobrazení nelze upravit. Změny, které odrážejí využití stránky, jsou však automaticky uloženy. Tyto změny zahrnují změny šířky sloupce mřížky a změny rozšířeného nebo sbaleného stavu pevné záložky. Pokud však máte oprávnění pro individuální nastavení, můžete pomocí akce **Uložit jako** vytvořit osobní zobrazení založené na uzamknutém zobrazení.
- **Nová zobrazení** - Publikovaná zobrazení, která ještě nebyla otevřena, jsou vymezena symbolem blesku nalevo od názvu zobrazení.

Chcete-li přepnout do jiného zobrazení, otevřete nejprve selektor zobrazení a poté vyberte zobrazení, které chcete načíst. 

## <a name="creating-and-modifying-views"></a>Vytváření a úpravy zobrazení

Na rozdíl od tradičního přizpůsobení se zobrazení automaticky neuloží, když uživatel přizpůsobí stránku nebo použije filtr na seznam nebo seřadí. Chcete-li uložit tyto změny do zobrazení, je nutné zadat explicitní akci. Tento požadavek uživatelům poskytuje flexibilitu k vytvoření zobrazení před nebo po provedení změn souvisejících s tímto zobrazením. Rovněž zajišťuje, aby definice zobrazení nebyly neúmyslně změněny jednorázovými filtry nebo personalizacemi. Všimněte si, že položky typického využití stránky (například šířky sloupců nebo rozbalený nebo sbalený stav sekcí) se automaticky uloží v současném zobrazení, a to i u zamčených zobrazení.

Chcete-li zajistit, aby byl znám aktuální stav zobrazení, když začnete měnit zobrazení personalizací nebo filtrováním, vedle aktuálního názvu zobrazení se zobrazí hvězdička (\*). Tento symbol označuje, že se díváte na neuloženou, upravenou verzi tohoto zobrazení.

[![Neuložené změny v zobrazení.](./media/views-unsavedChanges.png)](./media/views-unsavedChanges.png)

Chcete-li tyto změny uložit, postupujte podle následujících kroků.

1. Chcete-li otevřít selektor zobrazení, vyberte název zobrazení.
2. Chcete-li změnit stávající zobrazení, vyberte **Uložit**. Tato akce není k dispozici pro uzamčená zobrazení. 
3. Vytvoření nového zobrazení:

    1. Zvolte **Uložit jako**. 
    2. V podokně **Uložit zobrazení jako** zadejte název a volitelně popis pohledu.
    3. Pokud chcete, aby toto zobrazení bylo vaším výchozím zobrazením, vyberte **Připnout jako výchozí**. Další informace o výchozích zobrazeních naleznete v následující sekci [Změna výchozího zobrazení](#changing-the-default-view). 
    4. **Verze 10.0.21 nebo novější:** Pokud je zapnutá funkce **Vylepšená podpora právnických osob pro uložená zobrazení**, můžete si vybrat, zda chcete, aby bylo toto zobrazení dostupné pro všechny právnické osoby nebo jen pro jejich podmnožinu.
    5. Zvolte možnost **Uložit**.

## <a name="changing-the-default-view"></a>Změna výchozího zobrazení

Výchozí zobrazení je zobrazení, které se systém pokusí otevřít, když poprvé otevřete stránku. Měli byste nastavit výchozí zobrazení, které budete pravděpodobně používat nejčastěji. 

> [!NOTE]
> - V základní funkci **Uložená zobrazení** existuje jediné, globální výchozí zobrazení napříč právnickými osobami. Pokud změníte výchozí zobrazení, otevře se toto zobrazení ve výchozím nastavení bez ohledu na právnickou osobu, ve které se právě nacházíte.
> - **Verze 10.0.21 nebo novější:** Když je zapnutá funkce **Vylepšená podpora právnických osob pro uložená zobrazení**, každá právnická osoba může mít své vlastní výchozí zobrazení na stránku.

Pokud chcete změnit výchozí zobrazení stránky, postupujte takto:

1. Přepněte na zobrazení, které používáte jako výchozí. 
2. Chcete-li otevřít selektor zobrazení, vyberte název zobrazení. 
3. Vyberte **Více** a potom **Připnout jako výchozí**.

Případně můžete při vytváření nového zobrazení (pomocí akce **Uložit jako**) nastavit toto nové zobrazení jako výchozí nastavením možnosti **Připnout jako výchozí** před uložením zobrazení.

> [!WARNING]
> V některých případech se dotaz přidružený k výchozímu zobrazení nespustí, dokud neuložíte stránku. Pokud například otevřete stránku skrze dlaždici, dotaz dlaždice se spustí bez ohledu na dotaz přidružený k výchozímu zobrazení. Pokud dále otevřete stránku, jejíž **standardní** zobrazení již má definovaný dotaz, bude původní dotaz proveden místo dotazu výchozího zobrazení. V takovém případě obdržíte při načtení zobrazení informační zprávu. Pokud přepnete zobrazení po načtení stránky, mělo by být dotaz na zobrazení možné spustit podle očekávání. Počínaje verzí 10.0.10 bude informační zpráva, kterou obdržíte, obsahovat vloženou akci, která umožní přímé načtení dotazu výchozího zobrazení.

## <a name="managing-personal-views"></a>Správa osobních zobrazení

Dialogové okno **Spravovat moje zobrazení** poskytuje základní funkce pro správu osobních zobrazení a pořadí zobrazení v selektoru zobrazení. Chcete-li otevřít tuto stránku, výběrem názvu zobrazení otevřete rozevírací nabídku selektoru zobrazení, vyberte **Více** a poté vyberte možnost **Spravovat moje zobrazení**.

**Verze 10.0.21 nebo novější:** Pokud je zapnutá funkce **Vylepšená podpora právnických osob pro uložená zobrazení**, sekce **Moje zobrazení** v dialogovém okně **Spravovat má zobrazení** se zobrazí dostupná zobrazení stránky v sekcích. Jakákoli zobrazení, která jsou specifická pro aktuální právnickou osobu, jsou uvedena v jejich vlastní sekci. Sekce **Globální zobrazení** je vždy zobrazena, takže můžete spravovat zobrazení, která jsou pro stránku k dispozici u všech právnických osob. 

Chcete-li zobrazit seznam dostupných zobrazení pro tuto stránku, je k dispozici následující soubor akcí.

- **Změna výchozího zobrazení**: Použijte akci **Připnout jako výchozí**, aby se aktuálně vybrané zobrazení nastavilo pro tuto stránku jako výchozí. Pokud je zapnutá funkce **Importovat podporu právnických osob pro uložená zobrazení**, sekce **Globální zobrazení** vám umožňuje nastavit zobrazení jako výchozí zobrazení buď pro aktuální právnickou osobu, nebo pro všechny právnické osoby.
- **Změnit pořadí zobrazení**: Pomocí akce **Přesunout nahoru** a **Přesunout dolů** změňte pořadí zobrazení na konkrétní pořadí.
- **Přejmenovat zobrazení**: Pomocí akce **Přejmenovat** změňte název aktuálně vybraného osobního zobrazení. Tato akce je pro zamčená zobrazení vypnuta. 
- **Odstranění zobrazení**: pomocí akce **Odstranit** trvale odstraníte aktuálně vybrané zobrazení ze stránky. Po odebrání nelze zobrazení nijak obnovit.

Změny provedené v tomto dialogovém okně se projeví po výběru tlačítka **Aktualizovat**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Správa individuálních nastavení na organizační úrovni se zobrazeními

Na pomoc s pochopením, jak uložená zobrazení pomáhají zlepšit správu vlastních nastavení na organizační úrovni, popisuje tato část určité rozdíly ve správě individuálního nastavení s funkcí **uloženého** zobrazení a bez ní.

Bez zobrazení mohli správci pro stránku použít sadu individuálních nastavení pro uživatele nebo skupinu uživatelů pomocí stránky pro individuální nastavení. Pokud mají tito uživatelé práva pro individuální nastavení, používalo se na této stránce individuální nastavení. Nebylo však možné zabránit uživatelům v další personalizaci stránky, což znamenalo, že organizace nemohla uživatelům zajistit konzistentní uživatelské rozhraní. Pokud některý z těchto uživatelů neměl práva pro individuální nastavení, nebyla zavedena individuální nastavení, která jim byla přidělena správcem. Když navíc byli do určité organizace zařazeni noví uživatelé, bylo nutné, aby správci ručně načetli sadu individuálních nastavení pro daného uživatele. Neexistoval žádný automatický mechanismus pro určení, že určitá sada individuálních nastavení by měla být dostupná pro uživatele v dané roli.

Pomocí funkce **uložená zobrazení** je správa organizace individuálního nastavení mnohem jednodušší, především díky možnosti publikování zobrazení rolím zabezpečení. Po publikování zobrazení budou mít všichni uživatelé, kteří mají jednu z definovaných rolí zabezpečení a mají přístup k zadaným právnickým osobám, budou moci zobrazit a používat zobrazení i přesto, že tento uživatel nemá přístup k individuálnímu nastavení. Zatímco má každý uživatel kopii v publikovaném zobrazení, v němž je použito automatické přizpůsobení stránky, nemůže žádný uživatel uložit explicitní přizpůsobení nebo aktualizace dotazu do publikovaného zobrazení. Jinými slovy, publikovaná zobrazení jsou uzamčena. Pokud jsou navíc novým uživatelům přiřazeny role v právnických osobách, do nichž byla publikována zobrazení, budou automaticky zobrazena zobrazení přidružená k jejich rolím a právnickým osobám. Od správce se nevyžaduje žádná další akce. Podobně platí, že pokud uživatelé změní role v organizaci nebo mají přístup k různým právnickým osobám, může se stát, že již nebudou moci získat přístup k zobrazením, která byla k nim dříve publikována. Znovu není potřeba žádná akce správce.

Aktualizace publikovaného zobrazení lze uživatelům snadno distribuovat tím, že zobrazení znovu publikujete do příslušných rolí zabezpečení a právnických osob.

Tato schopnost publikování umožňuje organizacím definovat standardní podniková zobrazení optimalizovaná pro jejich podnikání zaměřené na uživatele s konkrétními rolemi zabezpečení.

## <a name="publishing-views"></a>Publikování zobrazení

Během publikování lze zobrazení přiřadit k jedné nebo více rolím zabezpečení pro jednu nebo více právnických osob. Z toho vyplývá, že každý uživatel, který má přístup k právnické osobě a který je přiřazen k jedné z těchto rolí, má přístup k zobrazení a k jejich používání. Uživatel však nemůže zobrazení upravovat. V současné době mají práva k akci **publikovat** v rozevírací nabídce zobrazení výběru ve výchozím nastavení správci systému. Ostatní důvěryhodní uživatelé ve vaší organizaci však mohou mít také přístup k zobrazení publikování pomocí nové role **Správce uložených zobrazení**.

Zobrazení publikujete takto.

1. Vytvořte a uložte osobní kopii zobrazení, kterou chcete publikovat. 
2. V zobrazení, které je aktuálně načteno, vyberte název zobrazení pro otevření rozevírací nabídky selektoru zobrazení. 
3. Vyberte tlačítko **Další** a potom **Publikovat**. Otevře se dialogové okno Publikovat.
4. Zadejte název zobrazení. Jméno, které zadáte, se zobrazí uživatelům, kteří toto zobrazení obdrží, v jejich selektorech zobrazení. Názvy publikovaných zobrazení pro stránku musí být jedinečné. Na stránce nejsou povoleny žádné duplicitní názvy, a to ani v případě, že se seznam rolí nebo právnických osob, na něž jsou zobrazení aplikována, liší.
5. **Aktualizace 10.0.17 nebo novější:** Pokud je zapnutá funkce **(Náhled) Podpora překladů pro organizační zobrazení**, můžete přidat překlady pro název vašeho zobrazení v tolika jazycích, kolik vyžaduje vaše organizace, výběrem tlačítka **Překlady** vedle pole **Název**. Název zobrazení se poté ukáže uživatelům v jejich aktuálním jazyce. Můžete také nastavit výchozí jazyk a určit překlad, který se zobrazí uživatelům, kteří používají jazyky, pro které není definován žádný překlad.
5. Volitelné: Zadejte popis zobrazení, aby uživatelé, kteří obdrží toto zobrazení, lépe porozuměli jeho účelu. 
6. Určete, zda má být zobrazení publikováno jako výchozí zobrazení pro vybrané uživatele. Když zobrazení nastavíte jako výchozí, zobrazí se uživatelům při dalším otevření cílové stránky. Jednotné globální výchozí zobrazení každého cílového uživatele se změní. Po publikování však uživatelé mohou změnit své výchozí zobrazení.

    > [!NOTE]
    > Při publikování zobrazení jako výchozího zobrazení mějte na paměti následující chování:
    >
    > - Pokud publikujete zobrazení jako výchozí zobrazení pro některé nebo všechny právnické osoby, dojde k následujícímu chování:
    >
    >    - Pokud je zapnutá pouze základní funkce **Uložená zobrazení**, změní se u každého cíleného uživatele jednotné globální výchozí zobrazení. 
    >    - **Verze 10.0.21 nebo novější:** Pokud je zapnutá funkce **Vylepšená podpora právnických osob pro uložená zobrazení** a publikujete pohled na podmnožinu právnických osob, výchozí zobrazení pro tyto právnické osoby se změní pro každého cíleného uživatele.
    >
    > - Pokud má uživatel role, ve kterých je jako výchozí zobrazení publikováno více zobrazení, použije se jako výchozí zobrazení uživatele poslední publikované zobrazení. 

8. Přidejte role zabezpečení, které odpovídají uživatelům, na něž je toto zobrazení zaměřeno. 
9. Zjistěte, zda chcete publikovat zobrazení do podřízených rolí každé vybrané role zabezpečení. Pokud tak učiníte, zaškrtněte políčko **Zahrnout podřízené role** v řádku pro příslušné role zabezpečení. Toto políčko není k dispozici pro role, které nemají podřízené role.
10. Přidejte právnické osoby, pro které má být toto zobrazení k dispozici. 

    > [!NOTE]
    > Při publikování zobrazení konkrétní právnické osobě, ale ne jako výchozí zobrazení vezměte v potaz následující chování:
    >
    > - Pokud je zapnutá pouze základní funkce **Uložená zobrazení**, volič zobrazení uživatele na stránce zpočátku zobrazuje zobrazení pouze pro zadané právnické osoby. Po prvním načtení zobrazení ji však volič zobrazení stránky vždy zobrazí bez ohledu na právnickou osobu.
    > - **Verze 10.0.21 nebo novější:** Pokud je zapnutá funkce **Vylepšená podpora právnických osob pro uložená zobrazení**, volič zobrazení vždy zobrazí pouze zobrazení pro konkrétní právnické osoby.

11. Zvolte **Publikovat**.

Všimněte si, že v některých prostředích může tato doba trvat dlouho (až hodinu), než uživatelé uvidí publikované zobrazení.

## <a name="modifying-a-published-view"></a>Úprava publikovaného zobrazení

Po publikování zobrazení můžete zjistit, že jej chcete změnit. I když v publikovaném zobrazení nelze provádět změny přímo, protože jsou tato zobrazení uzamčena pro úpravy pro všechny uživatele (včetně vydavatelů), můžete zobrazení aktualizovat opětovným publikováním.

Pokud změny, které chcete provést v publikovaném zobrazení, zahrnují pouze parametry publikování (název a popis zobrazení nebo role zabezpečení, ve kterých je zobrazení publikováno), proveďte následující akce:

1. Přepněte do zobrazení Publikováno pro parametry, které chcete aktualizovat. 
2. V rozevírací nabídce selektoru zobrazení vyberte **Znovu publikovat**. Pokud používáte verzi 10.0.12 nebo starší, musíte vybrat **Publikovat** a pak **Ano** pro aktualizaci stávajícího zobrazení.
3. Aktualizujte název, popis nebo role zabezpečení a právnické osoby pro zobrazení. 
4. Zvolte **Publikovat**. Pokud jste původně vybrali toto publikované zobrazení jako výchozí zobrazení, bude to po publikování pro uživatele znovu výchozí zobrazení. 

Pokud změny provedené v publikovaném zobrazení zahrnují úpravy přizpůsobení nebo filtrů spojených se zobrazením, postupujte následujícím způsobem.

1. Načtěte publikované zobrazení pro parametry, které chcete změnit. 
2. Proveďte požadované změny místního konceptu.
3. V rozevírací nabídce selektoru zobrazení vyberte **Znovu publikovat**.
4. Vyberte **Ano** k indikaci, že chcete zobrazení spolu s neuloženými změnami. 
5. Upravte všechny parametry publikování, které vyžadují úpravu, a poté vyberte **Publikovat**. 

## <a name="managing-published-views"></a>Správa publikovaných zobrazení

Podobně jako správa osobních zobrazení poskytuje dialogové okno **Správa mých zobrazení** uživatelům s oprávněním k publikování základní možnosti správy nad publikovanými zobrazeními dané stránky (kromě vlastních osobních zobrazení). Chcete-li otevřít tuto stránku, výběrem názvu zobrazení otevřete rozevírací nabídku selektoru zobrazení, vyberte **Více** a poté vyberte možnost **Spravovat moje zobrazení**.

Zatímco všichni uživatelé vidí kartu **Moje zobrazení** s osobními zobrazeními, uživatelé, kteří mají oprávnění pro publikování, mají také kartu **Publikováno**, na níž se zobrazují všechna publikovaná a nepublikovaná zobrazení pro danou stránku. Vzhledem k tomu, že zobrazení může publikovat několik uživatelů, je důležité mít možnost spravovat úplný seznam publikovaných zobrazení bez ohledu na to, zda jste uživatelem, který zobrazení skutečně publikoval.

Chcete-li zobrazit seznam všech dostupných zobrazení pro tuto stránku, je k dispozici následující soubor akcí. 

- **Znovu publikovat** – Použijte akci **Znovu publikovat**, pokud chcete znovu publikovat zobrazení s upravenými parametry publikování (název, popis, role zabezpečení).
- **Publikovat** - Použijte akci **Publikovat** k publikování aktuálně nepublikovaného zobrazení. 
- **Zrušit publikování** - Použijte akci **Zrušit publikování** k deaktivaci zobrazení. Zobrazení bude stále k dispozici v systému, ale uživatelé jej neuvidí ve výběru zobrazení, dokud nebude znovu publikováno.
- **Uložit jako osobní** – Použijte akci **Uložit jako osobní** k vytvoření osobní rámcové kopie publikovaného zobrazení. Tato funkce vám může pomoci pochopit obsah zobrazení, který pro vás nebyl publikován nebo který ještě nebyl publikován. Můžete jej také použít k úpravě a opětovnému publikování zobrazení.
- **Odstranit** – k trvalému odstranění publikovaného nebo nepublikovaného zobrazení použijte akci **Odstranit**. Tato akce odebere zobrazení také pro všechny uživatele v systému. Odebrání publikovaných zobrazení se projeví po výběru tlačítka **Uložit**. Po odstranění nelze zobrazení obnovit. 

## <a name="managing-views-globally"></a>Globální správa zobrazení

Přestože jsou na každé stránce zobrazeny některé funkce správy, jak je uvedeno v tomto článku, **správci systému** a **správci uložených zobrazení** mohou spravovat pohledy holističtěji pro systém prostřednictvím stránky **Individuální nastavení**. Tato stránka obsahuje zejména následující oddíly a možnosti: 

- **Publikovaná zobrazení** - V této části jsou uvedena všechna zobrazení, která byla publikována pro vaši organizaci. Odsud můžete zobrazení znovu upravit poté, co upravíte role zabezpečení nebo právnické osoby, na které je zobrazení zaměřeno. Tato zobrazení můžete také exportovat, odstranit nebo můžete zrušit jeho publikování. Pomocí akce **Uložit jako osobní** můžete vytvořit k vytvoření osobní kopii zobrazení, abyste mohli zobrazení aktualizovat nebo získat lepší přehled o jeho obsahu. 
- **Nepublikovaná zobrazení** - V této části jsou uvedena všechna zobrazení organizace ve vašem systému, která momentálně nejsou publikována. Tato zobrazení nejčastěji přicházejí do systému pomocí funkce importu. Tato zobrazení můžete publikovat, exportovat nebo odstranit. Akce **Rychlé publikování**, která byla přidána ve verzi 10.0.12, umožňuje publikovat více zobrazení z této sekce v jedné akci pomocí stávající konfigurace zabezpečení a konfigurace právnických osob. Pomocí akce **Uložit jako osobní** můžete vytvořit k osobní kopie těchto zobrazení, abyste mohli lépe pochopit obsah zobrazení.
- **Osobní zobrazení** – v této části jsou uvedena všechna zobrazení, která byla vytvořena uživateli v systému. Odsud můžete publikovat osobní zobrazení do organizace nebo zkopírovat jedno či více těchto zobrazení pro jiné uživatele. Tato zobrazení můžete také exportovat nebo odstranit podle potřeby.
- **Uživatelské nastavení** - Vyberte uživatele, kterého chcete zobrazit, nebo upravte jeho schopnost používat personalizaci pro celý systém nebo pro konkrétní stránky, které uživatel navštívil. Můžete si prohlížet a pracovat s personalizacemi uživatele v systému. Můžete také odstranit všechny personalizace pro daného uživatele nebo popisek funkcí pro uživatele. Pokud jsou obnoveny popisky funkce, všechna překryvná okna, která zavedla nové funkce a která uživatel předtím odstranil se znovu zobrazí při příštím výskytu těchto funkcí uživatelem.
- **Nastavení systému:** – Zde můžete dočasně vypnout přizpůsobení v systému pro všechny uživatele. V tomto případě budou všechna individuální nastavení použita pro všechny uživatele a všechny stránky budou obnoveny do výchozího stavu. Pokud později zapnete přizpůsobení znovu, veškerá přizpůsobení budou znovu použita. Můžete trvale odstranit veškerá přizpůsobení v systému pro všechny uživatele. Neexistuje žádný způsob obnovení individuálního nastavení, které bylo odstraněno. Proto se před provedením tohoto úkolu ujistěte, že jste exportovali všechna individuální nastavení, která můžete chtít později.

Uživatelé, kteří mají přístup na stránku **Individuální nastavení**, mohou také importovat osobní zobrazení nebo zobrazení organizace pomocí tlačítka **Importovat zobrazení** v podokně akcí. Pro zobrazení organizace můžete vybrat **Publikovat okamžitě** ke zpřístupnění výběrů uživatelům bez dalšího explicitního publikování.

## <a name="known-issues"></a>Známé problémy

Seznam známých problémů s uloženými zobrazeními naleznete na stránce [Vytváření formulářů, které plně využívají uložená zobrazení](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Jak povolím uložená zobrazení v mém prostředí?

> [!NOTE]
> Funkce **Uložená zobrazení** vyžaduje povolení systému přizpůsobení ve finančních a provozních aplikacích. Pokud je individuální nastavení pro celé prostředí vypnuto, zobrazení budou zakázána i v případě, že provedete níže uvedené kroky. 

Můžete zapínat a vypínat funkci **Uložená zobrazení** prostřednictvím správy funkcí v libovolném prostředí. Po zapnutí budou uložená zobrazení povolena ve všech následujících relacích uživatele.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Co se stane se stávajícími individuálními nastaveními, když jsou povolena zobrazení? 

Jsou-li povolena zobrazení, budou všechna existující individuální nastavení pro uživatele a formulář uložena do nového zobrazení s názvem **Moje zobrazení**, které je automaticky nastaveno jako výchozí zobrazení. To je určeno k zajištění konzistentního uživatelského prostředí před a po povolení zobrazení, kromě toho, že se na formulářích zobrazí ovládací prvek selektoru.

### <a name="what-pages-support-views"></a>Které stránky podporují zobrazení? 

Zobrazení jsou k dispozici ve většině, ale ne na všech stránkách. Zobrazení jsou aktuálně k dispozici na všech stránkách na celé obrazovce s výjimkou řídicích panelů. Podpora zobrazení pro pracovní prostory je k dispozici prostřednictvím funkce **Podpora uložených pohledů pro pracovní prostory**. Většina stránek, které nejsou na celou obrazovku, které obsahují rozevírací dialogová okna, vyhledávání a rozšířené náhledy, v současné době nepodporují zobrazení. Podpora zobrazení pro dialogové okna je k dispozici prostřednictvím funkce **Podpora uložených pohledů pro dialogová okna**.

### <a name="who-is-allowed-to-publish-views"></a>Kdo smí publikovat zobrazení?

Pouze správci a uživatelé, kteří byli přiřazeni k roli **Správce uložených zobrazení**, mají práva pro publikování. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Proč nemohu uložit filtry s tímto zobrazením? 

Existuje několik důvodů, proč se filtr nemusí zobrazit pro uložení se zobrazením: 

- Stránka pravděpodobně nepodporuje ukládání filtrů v rámci definice zobrazení. Všimněte si, že pouze stránky s vybranými velkými zobrazeními umožňují přizpůsobení a úpravy dotazů, které mají být uloženy jako zobrazení. Další informace naleznete v části **Přepínání zobrazení**. 
- Je možné, že daná stránka nebude správně podporovat zobrazení, protože může zcela ignorovat zobrazení dotazu nebo může pracovat s dočasnou tabulkou, jejíž data nejsou trvalá. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Jaká data se zobrazí při návštěvě stránky?

U stránek s malými selektory zobrazení (do zobrazení lze uložit pouze individuální nastavení) se zobrazí stejná data, jaká byste měli vždy po návštěvě stránky. 

U stránek s vybranými velkými zobrazeními (přizpůsobení a dotazy lze ukládat do zobrazení) se běžně zobrazí data propojená s dotazem přidruženým k výchozímu zobrazení. Existují dvě hlavní výjimky:

- Pokud například přejdete v dlaždici na stránku, bude dotaz dlaždice proveden bez ohledu na dotaz přidružený k výchozímu zobrazení. Pokud jste vytvořili tuto dlaždici po povolení zobrazení, výběrem dlaždice se otevře stránka se zobrazením přidruženým k této dlaždici.
- Pokud také přejdete na stránku, jejíž vstupní bod obsahuje dotaz, bude původní dotaz proveden místo dotazu výchozího zobrazení. Měli byste věnovat pozornost, pokud k tomu dojde prostřednictvím informační zprávy při načítání zobrazení. Můžete také potvrdit přepnutí do tohoto zobrazení po načtení stránky, což by mělo umožnit spuštění dotazu zobrazení.

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>Proč je pohled, který byl publikován pro konkrétní právnickou osobu, viditelný u všech právnických osob?

Při publikování zobrazení konkrétní právnické osobě, ale ne jako výchozí zobrazení se projeví následující chování:

- Pokud je zapnutá pouze základní funkce **Uložená zobrazení**, volič zobrazení uživatele na stránce zpočátku zobrazuje zobrazení pouze pro zadané právnické osoby. Po prvním načtení zobrazení ji však volič zobrazení stránky vždy zobrazí bez ohledu na právnickou osobu. K tomuto chování dochází, protože uživatelé po načtení získají vlastní osobní kopii publikovaného zobrazení a osobní zobrazení jsou globální.
- **Verze 10.0.21 nebo novější:** Pokud je zapnutá funkce **Vylepšená podpora právnických osob pro uložená zobrazení**, volič zobrazení vždy zobrazí pouze zobrazení pro konkrétní právnické osoby. K tomuto chování dochází, protože funkce umožňuje propojení zobrazení (včetně osobních pohledů) s konkrétními právnickými osobami.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

