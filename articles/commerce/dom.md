---
title: Distribuovaná správa objednávek (DOM)
description: Tento článek popisuje funkcionalitu distribuované správy objednávek v aplikaci Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/16/2022
ms.topic: index-page
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.openlocfilehash: cfb89544580141ed397d27886f51fd0f1ac138d2
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785173"
---
# <a name="distributed-order-management-dom"></a>Distribuovaná správa objednávek (DOM)

[!include [banner](includes/banner.md)]

Tento článek popisuje funkcionalitu distribuované správy objednávek v aplikaci Microsoft Dynamics 365 Commerce.

Distribuovaná správa objednávek je omnikanálové řešení, které optimalizuje a maximalizuje vyřizování objednávek v síti dodavatelského řetězce. Díky distribuované správě objednávek budou vašim zákazníkům dodány produkty ve správném množství, ze správných zdrojů a ve správný čas. Mimo to vám distribuovaná správa objednávek pomůže maximalizovat zisky, minimalizovat náklady a plnit požadavky na úrovni služeb.

Optimalizace probíhá na úrovni dávek i jednotlivých objednávek, přičemž obojí využívá smíšené celočíselné programování (MIP) a modely prediktivní analýzy. Maloobchodníci tak mohou definovat pravidla vyvažující řadu možných konfliktních bodů při plnění objednávky. V moderní dodavatelské síti, kde jsou produkty distribuovány přes více kanálů, musí být organizace schopna flexibilně řešit změny objednávek, problémy s dostupností dodavatelů nebo prudké nárůsty poptávky. Distribuovaná správa objednávek pomáhá maximalizovat plnění objednávek a hledat správné zdroje pro dodání produktů na základě obchodních omezení a cílů. Pokud chcete například minimalizovat náklady, objednávku odbaví nejbližší zdroje. Při optimalizaci plnění objednávek se bere v úvahu vzdálenost mezi místem distribuce a místem doručení, definované nákladové faktory, jako jsou cíle optimalizace, a pravidla definovaná jako omezení, například zásoby v distribučních uzlech. Distribuovaná správa objednávek umožňuje podnikům definovat různé profily aplikující různé optimalizační strategie dle typu podnikání nebo spotřebitelského segmentu. 

Následující příklad ilustruje životní cyklus prodejní objednávky v systému distribuované správy objednávek.

![Životní cyklus prodejní objednávky v kontextu distribuované správy objednávek](./media/flow.png "Životní cyklus prodejní objednávky v kontextu distribuované správy objednávek")

Následující video poskytuje přehled funkcí distribuované správy objednávek v aplikaci Dynamics 365 Commerce.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bRYl]

## <a name="set-up-dom"></a>Nastavit distribuovanou správu objednávek

1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.
2. Na kartě **Konfigurační klíče** rozbalte uzel **Commerce** a poté vyberte zaškrtávací políčko **Distribuovaná správa objednávek**.
3. Přejděte na **Retail a Commerce \> Distribuovaná správa objednávek \> Nastavení \> Parametry distribuované správy objednávek**.
4. Na kartě **Obecné** natavte následující hodnoty:

    - **Povolit distribuovanou správu objednávek** – Nastavte tuto možnost **Ano**.
    - **Potvrdit použití map Bing pro distribuovanou správu objednávek** – Nastavte tuto možnost na **Ano**.

        > [!NOTE]
        > Tuto možnost můžete nastavit na **Ano** pouze tehdy, pokud je na stránce **Sdílené parametry Commerce** (**Retail a Commerce \> Nastavení centrály \> Parametry \> Sdílené parametry Commerce**) na kartě **Mapy Bing** nastavena možnost **Povolit mapy Bing** také na **Ano** a pokud byl zadán platný klíč do pole **Klíč map Bing**.
        >
        > Portál [Bing Maps Dev Center](https://www.bingmapsportal.com/) umožňuje omezit přístup k vašim klíčům rozhraní API pro mapy Bing na sadu domén, které zadáte. Tato funkce umožňuje odběratelům definovat striktní sadu hodnot odkazujícího nebo rozsahů IP adres, podle kterých bude klíč ověřen. Žádosti ze seznamu povolených položek budou normálně zpracovány, zatímco žádosti mimo seznam vrátí odpověď Přístup odepřen. Přidání zabezpečení domény do klíče rozhraní API je volitelné a klíče ponechané v původním stavu budou i nadále funkční. Seznam povolených položek pro klíč je nezávislý na všech ostatních klíčích, takže pro každý z vašich klíčů můžete stanovit odlišná pravidla. Distribuovaná správa objednávek nepodporuje nastavení vlastností odkazujících na doménu.

    - **Doba uchovávání ve dnech** – Určete, jak dlouho budou v systému uchovány plány, které jsou generovány spuštěním distribuované správy objednávek. Dávková úloha **Nastavení úlohy odstranění dat plnění DOM** odstraní všechny plány plnění, které jsou starší než počet dní, které zde zadáte.
    - **Období zamítnutí (v dnech)** – Určete, kolik musí uplynout času, než může být přiřazen zamítnutý řádek objednávky ke stejnému místu.

5. Na kartě **Řešitel** natavte následující hodnoty:

    - **Maximální počet pokusů automatického plnění** – Určete, kolikrát se modul distribuované správy objednávek pokusí zprostředkovat řádek objednávky do místa. Pokud nemůže modul distribuované správy objednávek zprostředkovat řádek objednávky do místa v určeném množství pokusů, označí řádek objednávky jako výjimku. Poté přeskočí tento řádek při dalších spuštěních, dokud nebude stav resetován ručně.
    - **Rádius oblasti místního obchodu** – Zadejte hodnotu. Toto pole pomáhá určit, jakým způsobem jsou místa seskupena a považována za stejná, pokud jde o vzdálenost. Pokud například zadáte **100**, každý obchod nebo distribuční centrum v okruhu 100 km adresy plnění bude považován za rovnocenný, co se týká vzdálenosti.
    - **Typ řešitele** - Vyberte typ hodnoty. S aplikací Commerce jsou vydány dva typy řešitelů: **Řešitel výroby** a **Zjednodušitelný řešitel**. Pro všechna zařízení, která budou spouštět distribuovanou správu objednávek (to znamená všechny servery, které jsou součástí skupiny DOMBatch), musí být zvolen **Řešitel výroby**. Řešitel výroby vyžaduje speciální licenční klíč, který je ve výchozím nastavení licencován a nasazen v provozních prostředích. V novějších prostředích úrovně 2+ již bude řešitel výroby povolen. U neprovozních prostředí je třeba tento licenční klíč nasadit ručně. Pokud chcete nasadit licenční klíč ručně, postupujte takto:

        1. Ve službě Microsoft Dynamics Lifecycle Services otevřete knihovnu sdíleného majetku, zvolte **Model** jako typ majetku a stáhněte soubor **DOM license**.
        1. Spusťte správce internetové informační služby společnosti Microsoft, klikněte pravým tlačítkem na **Web AOSService** a poté zvolte **Prozkoumat**. Otevře se okno průzkumníka Windows na **\<AOS service root\>\\webroot**. Poznamenejte si cestu \<AOS Service root\>, protože ji budete muset použít v dalším kroku.
        1. Zkopírujte konfigurační soubor do adresáře **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Přejděte do klienta Headquarters a otevřete stránku **Parametry distribuované správy objednávek**. Na kartě **Řešitel** v poli **Typ řešitele** zvolte **Řešitel výroby** a potvrďte, že se nezobrazily žádné chybové zprávy.

        > [!NOTE]
        > Zjednodušený řešitel je poskytnut proto, aby maloobchodníci mohli vyzkoušet funkci distribuované správy objednávek bez nasazení speciální licence. Organizace by neměly používat zjednodušeného řešitele v provozních prostředích.
        >
        > Řešitel výroby zlepšuje výkon (například počet objednávek a řádků objednávek, které lze zpracovat při jednom spuštění) a konvergenci výsledků (jelikož dávka objednávek nemusí v některých scénářích vytěžit nejlepší výsledky). Pravidlo **Dílčí objednávky** vyžaduje Řešitele výroby.

6. Přejděte zpět na **Maloobchod a obchod \> Distribuovaná správa objednávek \> Nastavení \> Parametry DOM**.
7. Na kartě **Číselné řady** přiřaďte požadované číselné řady různým entitám distribuované správy objednávek.

    > [!NOTE]
    > Než mohou být číselné řady přiřazené entitám, musí být definovány na stránce **Číselné řady** (**Správa organizace \> Číselné řady \> Číselné řady**).

8. Funkce distribuované správy objednávek podporuje definici různé typy pravidel distribuované správy objednávek a organizace mohou konfigurovat mnoho pravidel, v závislosti na svých obchodních potřebách. Pravidla distribuované správy objednávek lze definovat pro skupinu míst nebo individuální místa, a pro specifickou kategorii produktu, produkt nebo variantu. Chcete-li vytvořit seskupení míst, která se musí použít pro pravidla distribuované správy objednávek, postupujte podle těchto kroků:

    1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Skupiny plnění**.
    2. Zvolte **Nová** a zadejte název a popis nové skupiny.
    3. Zvolte **Uložit**.
    4. Zvolte **Přidat řádek** a přidejte ke skupině jedno místo. Popřípadě zvolte **Přidat řádky** a přidejte více míst.

    > [!NOTE]
    > Ve verzi Commerce 10.0.12 musí být v pracovním prostoru **Správa funkcí** povolena volba **Možnost specifikovat místa jako „Expedice“ nebo „Výdej“ povolena ve skupině plnění**.
    >
    > Tato funkce přidává nové konfigurace na stránce **Skupina plnění**, takže můžete definovat, zda lze sklad použít pro expedici, nebo zda lze kombinaci sklad/obchod použít pro expedici, výdej nebo obojí. 
    >
    > Pokud tuto funkci povolíte, možnosti dostupné pro výběr umístění při vytváření objednávek výdeje nebo expedice v POS budou aktualizovány.
    >
    > Povolení funkce také vede k aktualizaci stránek v POS, když jsou vybrány operace „expedovat vše“ nebo „expedovat vybrané“.

9. Chcete-li definovat pravidla, přejděte na **Retail a Commerce \> Distribuovaná správa objednávek \> Nastavení \> Spravovat pravidla**. Jsou podporována následující pravidla distribuované správy objednávek:

    - **Pravidlo skladového minima** – Tento typ pravidla umožňuje organizacím vyčlenit konkrétní množství produktu pro účely jiné než plnění objednávky. Například organizace nemusí chtít, aby distribuovaná správa objednávek zvažovala všechny zásoby dostupné v obchodě pro plnění objednávek. Místo toho mohou chtít rezervovat některé zásoby pro příchozí zákazníky. Při použití tohoto typu pravidla můžete pro kategorii produktů, samostatný produkt nebo jeho variantu definovat minimální zásoby, které mají být zachovány, na základě místa nebo skupiny míst. Minimální zásoby můžete definovat také pomocí doplňkové hierarchie kategorií. Pokud produkt spadá do více kategorií, ve všech pravidlech používajících kategorie má nejvyšší důležitost doplňková kategorie.
    - **Pravidlo priority místa plnění** – Tento typ pravidla umožňuje organizacím definovat hierarchii míst vytyčující priority, podle kterých se řídí modul distribuované správy objednávek při identifikaci distribučních míst pro konkrétní produkty. Platný rozsah priorit je 1 až 10, kde 1 je nejvyšší prioritou a 10 je nejnižší priorita. Místa, která mají vyšší prioritu, jsou zvažována dříve než místa s nižší prioritou. Pokud je pravidlo definováno jako vážné omezení, objednávky jsou zprostředkovány pouze pro místa s definovanými prioritami. Distribuovaná správa objednávek preferuje kompletní expedici objednávek z jednoho místa. Pokud tedy celá objednávka a její řádky nejsou dostupné z místa s prioritou 1, distribuovaná správa objednávek se ji pokusí odbavit z místa s prioritou 2.
    - **Pravidlo částečných objednávek** – Ve verzi 10.0.5 aplikace Retail byl změněn parametr **Plnění objednávky pouze z jednoho místa** na **Maximální počet míst plnění**. Starý parametr umožňoval uživatelům konfigurovat, zda lze objednávky odbavit pouze z jednoho místa nebo z co nejvíce míst. Nový parametr umožňuje uživatelům určit, zda lze objednávku odbavit z určité sady míst (maximálně pět) nebo z co největšího počtu míst. Ve všech případech mimo odbavení z jednoho místa pak distribuovaná správa objednávek rozdělí řádek, protože zpracování objednávky probíhá po řádcích. Toto pravidlo platí pouze pro řešitele výroby.
    - **Pravidlo místa plnění offline** – Toto pravidlo umožňuje organizacím označit místo nebo skupinu míst jako offline nebo nedostupnou pro distribuovanou správu objednávek, takže objednávky není možné plnit přiřazením k těmto místům.
    - **Pravidlo maximálního počtu zamítnutí** – Toto pravidlo umožňuje organizacím určit prahovou hodnotu zamítnutí. Když je dosažena prahová hodnota, procesor distribuované správy objednávek označí objednávku nebo řádek objednávky jako výjimku a vyloučí je z dalšího zpracování. Aby nedocházelo ke snížení výkonu, distribuovaná správa objednávek nebere v potaz historii všech zamítnutí. 

        Po přiřazení řádků objednávky k místu je může dané místo zamítnout, protože je z nějakých důvodů nemůže plnit. Zamítnuté řádky jsou označené jako výjimka a vrácené zpět do skupiny pro zpracování v dalším spuštění. Během dalšího spuštění se distribuovaná správa objednávek pokusí přiřadit zamítnutý řádek k jinému místu. Nové místo může rovněž zamítnout přiřazený řádek objednávky. Tento cyklus přiřazení a zamítnutí se může přihodit několikrát. Když počet zamítnutí dosáhne definované prahové hodnoty, distribuovaná správa objednávek označí řádek objednávky jako stálou výjimku a již znovu nevybere řádek pro přirazení. Distribuovaná správa objednávek bude zvažovat řádek objednávky znovu pro opětovné přiřazení pouze tehdy, když uživatel ručně resetuje stav řádku objednávky.

    - **Pravidlo maximální vzdálenosti** – Toto pravidlo umožňuje organizacím určit maximální vzdálenost, do které může být místo nebo skupina míst pro plnění objednávky. Pokud jsou pro místo definována překrývající se pravidla maximální vzdálenosti. distribuovaná správa objednávek použije nejnižší maximální vzdálenost definovanou pro toto místo.
    - **Pravidlo maximální počtu objednávek** – Toto pravidlo umožňuje organizacím určit maximální počet objednávek, který může místo nebo skupina míst zpracovat. Během procesu optimalizace systém posoudí objednávky, které nebyly expedovány z těchto míst. Tato kontrola probíhá napříč profily. Pokud je tedy v profilech definován překrývající se maximální počet objednávek pro stejné místo, systém vezme v úvahu maximální počet objednávek definovaný ve všech profilech. 

    Zde je několik společných atributů, které lze definovat pro všechny předchozí typy pravidel:

    - **Počáteční datum** a **Koncové datum** – Tato pole určují datum účinnosti jednotlivých pravidel.
    - **Zakázáno** – Distribuovaná správa objednávek bere v potaz pouze pravidla, u nichž je hodnota tohoto pole **Ne**.
    - **Vážné omezení** – Pravidlo lze definovat buď jako vážné omezení, nebo bez vážného omezení. Každé spuštění distribuované správy objednávek prochází dvěma iteracemi. V první iteraci je každé pravidlo považováno jako pravidlo s vážným omezením, bez ohledu na nastavení tohoto pole. Jinými slovy, je použito každé pravidlo. Jedinou výjimkou je pravidlo **Priorita místa**. V druhé iteraci jsou pravidla, která nebyla definována jako pravidla s vážným omezením, odstraněna, a objednávka nebo řádky objednávky nepřiřazené k místům, když byla použita všechna pravidla, jsou přiřazeny k místům.

10. Profily plnění se použijí k seskupení kolekce pravidel, právnických osob, původů prodejní objednávky a způsobů dodání. Každé spuštění distribuované správy objednávek je pro konkrétní profil plnění. Tímto způsobem organizace mohou určit a spustit sadu pravidel pro sadu právnických osob na objednávkách, které mají specifické původy prodejní objednávky a způsoby dodání. Proto když musí být spuštěna různá sada pravidel na různé sady původů prodejní objednávky nebo způsoby dodání, profily plnění lze definovat odpovídajícím způsobem. Chcete-li nastavit profily plnění, postupujte následujícím způsobem:  

    1. Přejděte na **Retail a Commerce \> Distribuovaná správa objednávek \> Nastavení \> Profily plnění**.
    2. Zvolte **Nové**.
    3. Zadejte hodnoty do polí **Profil** a **Popis**.
    4. Nastavte možnost **Automaticky použít výsledek**. Pokud nastavíte tuto možnost na **Ano**, výsledky spuštění distribuované správy objednávek pro profil budou automaticky použity na řádky prodejní objednávky. Pokud ji nastavíte na hodnotu **Ne**, lze zobrazit výsledky pouze v plánu plnění. Nebudou použity na řádky prodejní objednávky.
    5. Pokud chcete, aby byl profil distribuované správy objednávek spuštěn pro objednávky, které mají původ u každé prodejní objednávky, včetně objednávek bez určeného původu prodejní objednávky, nastavte možnost **Zpracovat objednávky s prázdným původem prodeje** na **Ano**. Chcete-li spustit profil jen pro několik původů prodejní objednávky, můžete je definovat na stránce **Původy prodeje**, jak bude vysvětleno později.

        > [!NOTE]
        > Ve verzi Commerce 10.0.12 a vyšší musí být v pracovním prostoru **Správa funkcí** povolena funkce **Možnost přiřadit skupinu plnění k profilu plnění**. Tato funkce umožňuje zadat seznam skladů, které má distribuovaná správa objednávek posoudit při spuštění optimalizace s profilem plnění. Pokud není seznam skladů zadán, distribuovaná správa objednávek vyhodnotí všechny sklady právnických osob, které jsou definovány v profilu.
        >
        > Tato funkce přidá na stránku **Profil plnění** novou konfiguraci, kterou lze přiřadit k jedné skupině plnění. 
        >
        > Pokud vyberete skupinu plnění, budou pravidla distribuované správy objednávek pro tento profil plnění efektivně probíhat proti skladům expedice zahrnutým do skupiny plnění. 
        > 
        > Chcete-li tuto funkci efektivně využít, zajistěte, aby existovala jedna skupina plnění, která obsahuje všechny expediční sklady, a poté tuto skupinu plnění přiřaďte k profilu plnění.

    6. Na záložce s náhledem **Právnické osoby** zvolte **Přidat** a potom zvolte právnickou osobu.
    7. Na pevné záložce **Pravidla** zvolte **Přidat** a potom zvolte pravidlo, které navážete na profil.
    8. Opakujte předchozí dva kroky, dokud nejsou všechna požadovaná pravidla přiřazena k profilu.
    9. Zvolte **Uložit**.
    10. V podokně akcí na kartě **Nastavení** zvolte **Způsoby dodání**.
    11. Na stránce **Způsoby dodání** zvolte **Nový**.
    12. V poli **Společnost** zvolte právnickou osobu. Seznam společností je omezen na právnické osoby, které jste přidali dříve.
    13. V poli **Způsob dodání** zvolte způsob dodání, který má být přiřazen k tomuto profilu. Způsob dodání nelze přiřadit k více aktivním profilům.
    14. Opakujte předchozí dva kroky, dokud nejsou všechny požadované způsoby dodání přiřazeny k profilu.
    15. Zavřete stránku **Způsoby dodání**.
    16. V podokně akcí na kartě **Nastavení** zvolte **Původy prodejní objednávky**.
    17. Na stránce **Původy prodeje** zvolte **Nový**.
    18. V poli **Společnost** zvolte právnickou osobu. Seznam společností je omezen na právnické osoby, které jste přidali dříve.
    19. V poli **Původ prodeje** zvolte původ prodeje, který má být přiřazen k tomuto profilu. Původ prodeje nelze přiřadit k více aktivním profilům.
    20. Opakujte předchozí dva kroky, dokud nejsou všechny požadované původy prodeje přiřazeny k profilu.
    21. Zavřete stránku **Původy prodeje**.
    22. Nastavte možnost **Povolit profil** na **Ano**. Při dojde při nastavení k jakýmkoliv chybám, obdržíte zprávu s upozorněním.

## <a name="dom-processing"></a>Zpracování distribuované správy objednávek

Distribuovaná správa objednávek se spustí pouze v dávkové úloze. Chcete-li konfigurovat dávkovou úlohu pro spuštění distribuované správy objednávek, postupujte takto.

1. Přejděte zpět na **Retail a Commerce \> Distribuovaná správa objednávek \> Dávkové zpracování \> Nastavení procesoru úlohy DOM**.
1. Na pevné záložce **Parametry** v poli **Profil plnění** zvolte profil, pro který musí být spuštěna distribuovaná správa objednávek.
1. Na pevné záložce **Spustit na pozadí** v poli **Skupina dávek** zvolte nakonfigurovanou skupinu dávek.
1. V poli **Popis úlohy** zadejte název dávkové úlohy.
1. Zvolte **Opakování** a nadefinujte opakování dávkové úlohy.
1. Vyberte **OK**.

V průběhu zpracování bude distribuovaná správa objednávek zvažovat objednávku a řádky objednávky níže popsaným způsobem:

- Řádky objednávek, které splňují kritéria pro původy prodejní objednávky, způsoby dodání a právnické osoby, jak jsou definována v profilu distribuované správy objednávek, a které rovněž splňují některá z těchto kritérií:

    - Jsou vytvořeny z obchodní sítě.
    - Nikdy nebyly zprostředkovány distribuovanou správou objednávek.
    - Dříve byly zprostředkovány distribuovanou správou objednávek, ale jsou označeny jako výjimky a jsou pod maximální prahovou hodnotou počtu pokusů.
    - Způsob dodání není výdej nebo elektronické dodání.
    - Nejsou označeny pro dodání.
    - Nejsou ručně vyloučeny.

- Objednávky, které nejsou blokované

Když distribuovaná správa objednávek použije pravidla, omezení zásob a optimalizaci, následně vybere místo, které je nejblíže dodací adrese zákazníka. Distribuovaná správa objednávek převede adresy typu **Doručení** na hodnoty zeměpisné šířky a délky. Poté převede dodací adresu na prodejní objednávce na hodnoty zeměpisné šířky a délky a aktualizuje hodnoty zeměpisné šířky a délky adresy pro budoucí použití. Distribuovaná správa objednávek určuje přesné hodnoty zeměpisné šířky a délky na základě adresy, města a PSČ získaných z Map Bing.

Distribuovaná správa objednávek počítá vzdušné nebo silniční vzdálenosti prostřednictvím rozhraní API Map Bing v závislosti na nastavení. Tyto informace pak použije ke stanovení nákladů na dopravu. Model optimalizace upřednostňuje odbavení kompletní zakázky z jednoho místa. I když je část objednávky dostupná ve stejném městě nebo na stejném PSČ, model je optimalizován ke snížení počtu dodávek. 

Distribuovaná správa objednávek vyhledá dostupné zásoby zobrazením jejich aktuálního množství v entitách V2 skladu. Během každého běhu dávky jsou objednávky rozděleny do dávek podle hodnoty parametru **Procesor DOM** u úloh definovaných v profilu. Výchozí hodnota tohoto parametru je **2000**. Jestliže je tedy při běhu optimalizováno 10 000 řádků objednávky a parametr **Procesor DOM** je nastaven na výchozí hodnotu **2000**, distribuovaná správa objednávek vytvoří pět dávek, které jsou zpracovány současně. Plány plnění jsou pak převzaty z optimalizátoru a použity na řádek. Pokud musí být řádek objednávky rozdělen mezi dvě místa, distribuovaná správa objednávek zajistí, aby byly v řádcích patřičně rozloženy ceny a daně.

![Kritéria prodejních objednávek.](./media/ordercriteria.png "Kritéria prodejních objednávek")

## <a name="results-of-dom-runs"></a>Výsledky spuštění distribuované správy objednávek

Pokud je profil plnění nastaven jako **Automaticky použít**, výsledky spuštění se automaticky použijí na řádky prodejní objednávky a plán plnění lze samostatně zobrazit. Pokud však profil plnění není nastaven na **Automaticky použít**, výsledky spuštění lze zobrazit pouze ze zobrazení plánu plnění. 

Chcete-li zobrazit vygenerované plány plnění, postupujte podle těchto kroků.

1. Přejděte na **Retail a Commerce \> Distribuovaná správa objednávek \> Distribuovaná správa objednávek**.
2. V pracovním prostoru **Distribuovaná správa objednávek** zvolte dlaždici **Plány plnění**.
3. Zvolte ID příslušného plánu plnění objednávek pro zobrazení plánu plnění.

    Část podrobností objednávek plánu plnění zobrazuje řádky původní prodejní objednávky, které byly součástí spuštění. Kromě standardních polí řádků prodejní objednávky zahrnuje část podrobností objednávky také následující tři pole související s distribuovanou správou objednávek:

    - **Typ plnění** – Toto pole označuje, zda je řádek prodejní objednávky plně zprostředkován, částečně zprostředkován nebo zcela nezprostředkován do místa.
    - **Rozdělit** – Toto pole označuje, zda byl jeden řádek prodejní objednávky rozdělen a zprostředkován do různých míst.
    - **Počet míst plnění** – Toto pole označuje, kolik řádků plnění bylo vytvořeno pro jeden řádek prodejní objednávky (na základě počtu míst, do kterých byl původní řádek prodejní objednávky zprostředkován).

    Část podrobností plnění objednávek zobrazuje přiřazení řádků původní prodejní objednávky do různých míst, spolu s jejich množstvím.

## <a name="order-line-actions-and-statuses"></a>Akce a stavy řádku objednávky

Následující část popisuje nastavení na řádku objednávky. Chcete-li otevřít řádek objednávky, přejděte na **Retail a Commerce \> Zákazníci \> Všechny prodejní objednávky**.

- Pokud nastavíte možnost **Vyloučit ze zpracování DOM** na kartě **Obecné** řádku prodejní objednávky na **Ano**, objednávka nebo řádek objednávky budou vyloučeny ze zpracování distribuované správy objednávek.
- Pole **Stav DOM** na kartě **Obecné** řádku prodejní objednávky lze nastavit na jednu z následujících hodnot:

    - **Žádný** -Řádek objednávky nebyl nikdy zprostředkován.
    - **Dokončeno** – Řádek objednávky byl úspěšně zprostředkován a přiřazen k místu.
    - **Výjimka** – Řádek objednávky byl zprostředkován, ale nemůže být přiřazen k místu. Výjimky mají několik dílčích typů, které lze zobrazit z pracovního prostoru distribuované zprávy objednávek:

        - **Žádné dostupné množství** – Neexistují žádné dostupné zásoby, ke kterým mají být přiřazeny objednávky v místech.
        - **Maximální počet zamítnutí** – Řádek objednávky dosáhl maximální prahové hodnoty pro zamítnutí.
        - **Konflikt úpravy dat** – Řádek prodejní objednávky byl změněn od doby, kdy byla zprostředkována objednávka. Proto nelze použít plán plnění na objednávku.
        - **Výjimka specifická pro řádek objednávky** – Na řádku objednávky existuje mnoho výjimek.

- Během zadání prodejní objednávky lze spustit distribuovanou správu objednávek v interaktivním režimu. Když zadáváte řádek objednávky, můžete po určení produktu a množství zvolit možnost **Aktualizovat řádek** a poté v části **DOM** zvolit **Navrhnout místo plnění**. Poté uvidíte seznam míst, založený na pravidlech distribuované správy objednávek, která mohou plnit množství na řádku objednávky. Tento seznam je roztříděn podle vzdálenosti. Zvolte místo pro nastavení příslušného pracoviště a skladu na řádku prodejního objednávky. Aby tato funkce fungovala, musí existovat aktivní profil plnění, který odpovídá původu prodeje a způsobu doručení na řádku prodeje.
- Chcete-li zobrazit protokoly spuštění distribuované správy objednávek pro řádek prodejní objednávky, zvolte **Řádek prodejní objednávky** a poté v části **DOM** zvolte **Zobrazit protokoly DOM**. Protokoly DOM zobrazují všechny události a protokoly, které byly vygenerovány spuštěním distribuované správy objednávek. Protokoly vám pomohou pochopit, proč bylo specifické místo přiřazeno k řádku objednávky a jaká pravidla a omezení byla zvažována jako součást tohoto přiřazení. Na kartě **Spravovat** jsou rovněž k dispozici protokoly distribuované správy objednávek na úrovni záhlaví prodejní objednávky.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Spuštění úlohy pro vyčištění pánů plnění distribuované správy objednávek

Když je spuštěno zpracování distribuované správy objednávek, jsou vytvořeny plány plnění. V průběhu času bude systém obsahovat mnoho plánů plnění. Chcete-li spravovat počet plánů plnění, které systém obsahuje, můžete nakonfigurovat dávkovou úlohu, která odstraní starší plány plnění na základě hodnoty **Období zadržení ve dnech**.

1. Přejděte zpět na **Retail a Commerce \> Distribuovaná správa objednávek \> Dávkové zpracování \> Nastavení úlohy odstranění dat plnění DOM**. 
1. V poli **Skupina dávek** vyberte nakonfigurovanou skupinu dávek.
1. Zvolte **Opakování** a nadefinujte opakování dávkové úlohy.
1. Vyberte **OK**.

## <a name="more-information"></a>Další informace

Při používání funkce distribuované správy objednávek je nutné vzít v úvahu následující:

- Momentálně se distribuovaná správa objednávek dívá pouze na objednávky vytvořené z obchodní sítě. Prodejní objednávky jsou identifikovány jako prodejní objednávky, když je možnost **Obchodní prodej** nastavena na **Ano**.
- Společnost Microsoft netestovala distribuovanou správu objednávek s rozšířenými funkcemi správy skladu. Zákazníci a partneři se proto nemohou automaticky spoléhat na kompatibilitu mezi distribuovanou správou objednávek s rozšířenými funkcemi správy skladu a procesy, které používají. Rozšířené funkce skladu podporují konfigurovatelné dimenze (například stav zásob), které neposkytují přesné informace o dostupných zásobách. Distribuovaná správa objednávek poskytuje rozšiřitelnou metodu pro nastavení dostupných zásob, která podporuje implementaci rozšířené správy skladu. Ta umožňuje práci s přizpůsobenými hodnotami stavu zásob a dalšími dimenzemi.

    Rozšiřitelnost distribuované správy objednávek je omezená, protože optimalizace probíhá v předem sestaveném modelu MIP, který bere v úvahu optimalizaci a její omezení. Několik rozšiřitelných bodů je k dispozici už teď, konkrétně nastavení optimalizace zásob a následného zpracování. Profily distribuované správy objednávek se mohou lišit podle původu prodeje a způsobu doručení. Původ prodejní objednávky lze nastavit během ingestace objednávky a na základě těchto hodnot použít různé optimalizační strategie. Distribuovaná správa objednávek podporuje také vytváření vlastních dávkových úloh, které mohou použít úlohu procesoru distribuované správy objednávek jako vstup a umožnit předání profilu jako parametru. Tímto způsobem lze spouštět jednu optimalizaci za druhou v případě různých obchodních scénářů.

- Distribuovaná správa objednávek je k dispozici pouze v cloudové verzi aplikace Commerce. Není podporována v místních nasazeních.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
