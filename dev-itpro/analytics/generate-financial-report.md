---
title: "Generovat finanční sestavu"
description: "Toto téma obsahuje informace o generování finančních sestav."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="generate-a-financial-report"></a>Generovat finanční sestavu

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o generování finančních sestav. 

Chcete-li vygenerovat sestavu, otevřete definici sestavy a klikněte na tlačítko Generovat na panelu nástrojů. Otevře se okno Stav fronty sestav a označí umístění vaší sestavy ve frontě. Ve výchozím nastavení bude vygenerovaná sestava otevřena ve Webovém prohlížeči.
| ![Poznámka](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Poznámka")**Poznámka**        |
|------------------------------------------------------------------------------------------------|
| Můžete generovat sestavy pouze do složek a umístění, k nimž máte oprávnění pro přístup. |

Následující tabulka vysvětluje dostupné možnosti pro generování sestav.

| Možnost                                                                                | Získání dalších informací |
|---------------------------------------------------------------------------------------|----------------------|
| Nastavte plán pro generování sestavy nebo skupiny sestav automaticky              |                      |
| Kontrolujte chybějící účty nebo data v sestavách a ověřujte přesnost sestav |                      |

Při generování sestavy se používají možnosti, které jste zadali na kartě Definice sestavy. Karta Výstup a distribuce slouží k určení umístění knihovny sestav, což nabízí snadný způsob sdílení sestavy.

## <a name="schedule-report-generation"></a> Plánování generování sestavy
Mnoho společností má základní sadu sestav, které jsou spouštěny v plánovaných intervalech, aby odpovídaly obchodním procesům. Můžete naplánovat generování sestavy pravidelně, například denně, týdně, měsíčně nebo ročně. Může se jednat o jednu sestavu nebo skupinu sestav zahrnující více společností. Je nutné zadat vaše přihlašovací údaje pro všechny společnosti, které jsou určeny, například v definici stromu výkaznictví. Pokud přihlašovací údaje nejsou platné, sestava zobrazí pouze informace, pro přístup k nimž máte oprávnění, například pro společnost, ke které jste momentálně přihlášeni. Výstupní informace jsou nejprve přečteny ze skupiny sestav a poté z jednotlivých sestav.

Jak jsou plány sestav vytvářeny a ukládány, jsou zobrazovány v navigačním podokně v části Plány sestav. Můžete vytvářet složky pro uspořádání sestav. Pokud se nespustí jedna sestava v plánu, všechny ostatní sestavy budou spuštěny.
| ![Důležité](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Důležité")**Důležité**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abyste mohli vytvářet, upravovat a odstraňovat plány sestav, musíte mít roli návrháře nebo správce. Při spuštění sestavy jsou použity přihlašovací údaje uživatele, který plán vytvořil, k vygenerování sestavy. |

### <a name="create-a-report-schedule"></a>Vytvoření plánu sestavy

1.  V Návrháři sestav v nabídce Soubor klikněte na tlačítko Nový a vyberte možnost Plán sestavy. Zobrazí se dialogové okno Nový plán sestavy.
2.  V části Nastavení vyberte jednotlivou sestavu nebo skupinu sestav k naplánování. Pouze sestavy nebo skupiny sestav pro společnost nebo výběr stavebních bloků, ke kterým jste aktuálně přihlášeni, jsou k dispozici.
3.  Zaškrtnutím políčka Aktivní zapněte plán sestavy. Pouze uživatel, který vytvořil sestavu, nebo správce může aktivovat nebo deaktivovat plán sestavy.
4.  Kliknutím na tlačítko Oprávnění zadejte přihlašovací údaje pro společnost. Standardně budou vaše přihlašovací údaje použity pro společnost, ke které jste přihlášeni. Jsou-li zahrnuty jiné společnosti, například v definicích stromu výkaznictví, vyberte možnost Použít samostatné přihlašovací údaje a zadejte přihlašovací údaje pro jinou společnost, která je zahrnuta v plánu sestavy. Můžete vybrat možnost Ověřování systému Windows nebo zadejte uživatelské jméno a heslo pro každou společnost. Zaškrtnutím políčka Uložit přihlašovací údaje můžete uložit přihlašovací údaje pro tyto společnosti a pak kliknutím na tlačítko OK dialogové okno zavřít.
5.  V části Četnost v poli Počátek opakování vyberte datum, kdy má být plán spuštěn. Ve výchozím nastavení je zvoleno aktuální systémové datum klientského počítače.
6.  V poli Spustit sestavu v vyberte čas spuštění sestavy. Pokud zadáte čas, který předchází aktuálnímu systémovému času, sestava se spustí v další naplánované datum.
7.  V oblasti Způsob opakování  určete, jak často má být sestava spuštěna. Ve výchozím nastavení je vybraná možnost Denně s hodnotou intervalu (dny) 1. Další možnosti zahrnují týdenní, měsíční a roční.
8.  V oblasti Rozsah opakování zaškrtněte, kdy má sestava přestat být generovaná.
    -   Bez koncového data – plán sestavy bude probíhat neomezeně.
    -   Nastavení počtu výskytů – plán sestavy bude spuštěn s určeným počtem opakování a pak bude deaktivován.
    -   Konec do – plán sestavy skončí k určenému datu.

9.  Na panelu nástrojů klikněte na tlačítko Uložit. V dialogovém okně Uložit jako zadejte jedinečný název a popis pro plán sestavy.

Abyste mohli zkopírovat plán sestavy, musíte mít roli návrháře nebo správce. I v případě, že správce upraví plán sestavy, sestava si zachová přihlašovací údaje uživatele, který ji vytvořil.
### <a name="copy-a-report-schedule"></a>Zkopírování plánu sestavy

1.  V Návrháři sestav, klikněte na tlačítko Plány sestav v podokně navigace a otevřete plán sestavy ke zkopírování.
2.  V nabídce Soubor klikněte na tlačítko Uložit jako a zadejte nový název a popis pro plán v dialogovém okně Uložit jako. Klikněte na tlačítko OK a v navigačním podokně se zobrazí nový plán.
3.  Upravte pole a informace nového plánu podle potřeby a klikněte na tlačítko Uložit na panelu nástrojů nebo klikněte na tlačítko Uložit v nabídce Soubor.

Abyste mohli odstranit plán sestavy, musíte být vlastníkem plánu sestavy nebo mít úlohu správce.
### <a name="delete-a-report-schedule"></a>Odstranění plánu sestavy

1.  V Návrháři sestav v navigačním podokně klikněte na tlačítko Plány sestav.
2.  Vyberte plán sestavy k odstranění a klikněte na tlačítko Odstranit nebo stiskněte klávesu Delete.
3.  V dialogovém okně k ověření odstranění kliknutím na tlačítko Ano trvale odstraňte plán sestavy. Pokud nemáte oprávnění k odstranění plánu, bude zobrazena zpráva a sestava nebude odstraněna.

### <a name="credentials-and-report-schedules"></a>Přihlašovací údaje a plány sestav

Pokud nezadáte přihlašovací údaje, které jsou vyžadovány u všech společností zahrnutých do sestav, při uložení plánu sestav obdržíte následující zprávu: „Je nutné zadat vaše přihlašovací údaje pro společnosti, které jsou obsaženy v tomto plánu sestavy. Použijte tlačítko Oprávnění a zadejte své přihlašovací údaje.“

Například Pavla se přihlásí ke společnosti A pomocí svého přihlašovacího jména a hesla. Vytvoří plán pro sestavu, která používá definici stromu výkaznictví ke shromažďování dat z více společností. Při uložení tohoto plánu sestavy je Pavla vyzvána k zadání přihlašovacích údajů pro ostatní společnosti, které jsou určeny v definici stromu výkaznictví. Po vypršení platnosti vašich přihlašovacích údajů nebudou ovlivněné sestavy v plánu sestav generovány, dokud nebudou přihlašovací údaje aktualizovány. Zobrazí se zpráva ve frontě sestav informující o tom, že je nutné aktualizovat oprávnění. Provedená plánu sestavy se nezdaří, pokud nastane některá z následujících situací (kvůli vyžadovaným přihlašovacím údajům):
-   byla přidána nová společnost do stromu sestav pro jednotlivou sestavu;
-   sestava ve skupině sestav byla upravena;
-   byla přidána nová sestava pro další společnost do skupiny sestav.

Pokračujte kliknutím na tlačítko Oprávnění v dialogovém okně Plánování sestav a poté zadejte příslušné přihlašovací údaje.

## <a name="missing-account-analysis-feature"></a> Funkce analýzy chybějícího účtu
Můžete hledat finanční účty a dimenze, které mohou chybět v rámci všech definic řádků, definic stromu výkaznictví a definic sestav ve skupině stavebních bloků. To je užitečné při vytváření nebo aktualizaci více účtů nebo stavebních bloků v krátkém časovém období, když chcete ověřit, že všechny nové informace budou zahrnuty do sestav.

Chybějící účty se určují použitím nejnižší a nejvyšší hodnoty z definice řádku nebo definice stromu výkaznictví a zobrazí seznam účtů, které nejsou v definici řádku nebo definici stromu výkaznictví, ale jsou ve finančních datech. Pokud má chybějící účet vyšší nebo nižší hodnotu než hodnoty v definici řádku, tento účet nebude zahrnut do seznamu chybějících účtů.
| ![Tip](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Tip")**Tip**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Pro účely ověření by tento postup měl být spouštěn před generováním měsíčních sestav a při vytváření nových stavebních bloků. |

Sestavy, které mají rozsahy hodnot, mají menší pravděpodobnost chybějících účtů. Pokud je to možné, používejte rozsahy ve stavebních blocích, aby byly zahrnuty nově vytvořené účty. Pokud je jakákoli definice sestavy nastavena na hodnotu společnosti @ANY, můžete se přihlásit k určité společnosti a spustit analýzu chybějících účtů pro danou společnost.
| ![Poznámka](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Poznámka")**Poznámka**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pokud byla přidána nová společnost, je nutné přidat novou společnost do stromů výkaznictví ve všech existujících sestavách, jinak společnost nebude zahrnuta do analýzy chybějících účtů. |

### <a name="run-missing-account-analysis"></a>Spuštění analýzy chybějícího účtu

1.  V Návrháři sestav klikněte na tlačítko Nástroje a potom na tlačítko Analýza chybějícího účtu.
2.  V poli Filtr společnosti vyberte společnost k filtrování výsledků nebo vyberte možnost Všechny (žádný filtr) a zobrazí se výsledky ze všech dostupných společností.
3.  V poli Filtr dimenze vyberte dimenzi, podle které chcete filtrovat výsledky, nebo vyberte možnost Všechny (žádný filtr) k zobrazení všech informací ze všech dostupných dimenzí.
4.  V poli Seskupit podle vyberte možnost pro řazení výsledků. Výsledky můžete řadit podle stavebního bloku, který je ovlivněn, nebo lze výsledky seřadit podle sad dimenzí a hodnot.
5.  Zkontrolujte zobrazené výsledky. Když vyberete položku v horním podokně, zobrazí se další informace o výjimce v dolním podokně. Zahrnuty jsou související dimenze, hodnoty a sestavy.
6.  Chcete-li otevřít ovlivněnou položku, klikněte na přidruženou ikonu zobrazenou v podokně seznamu nebo pravým tlačítkem myši klikněte na položku a vyberte možnost Otevřít. Lze vybrat více položek – stiskněte a podržte klávesu Ctrl a vyberte položky v dolním podokně.
7.  Pokud je vrácena jakákoli hodnota, stavební blok či sestava, které nemají být zahrnuty do analýzy, klikněte pravým tlačítkem na položku a vyberte možnost Vyloučit nebo zaškrtněte políčko Vyloučit vedle položky k odstranění položky ze seznamu. Vyloučené položky nebudou zahrnuty při aktualizaci seznamu. Lze vybrat více položek – stiskněte a podržte klávesu Ctrl a vyberte položky v dolním podokně. Chcete-li zobrazit všechny položky, včetně všech výsledků, které jste označili k vyloučení z analýzy, zaškrtněte políčko Zobrazit vyloučené stavební bloky a hodnoty a poté klikněte na tlačítko Aktualizovat.
8.  Kliknutím na tlačítko Aktualizovat obnovíte výjimky, které byly adresovány. Kliknutím na tlačítko Ano proveďte úplnou aktualizaci všech výsledků nebo kliknutím na tlačítko Ne proveďte částečnou aktualizaci adresovaných položek.
    | ![Poznámka](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Poznámka")**Poznámka**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Formulář je aktualizován automaticky při otevření, pokud formulář nebyl otevřen během posledních 15 minut. |

9.  Po vyřešení potíží kliknutím na tlačítko OK dialogové okno zavřete.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Klávesové zkratky pro analýzu chybějícího účtu
Po spuštění analýzy chybějícího účtu jsou k dispozici následující klávesové zkratky.

| Akce                           | Použitá klávesová zkratka |
|--------------------------------------|----------------------------|
| Filtrování podle společnosti                    | Alt+C                      |
| Filtrování podle dimenze                  | Alt+D                      |
| Výběr pole Seskupit podle            | Alt+G                      |
| Zobrazení vyloučených bloků a hodnot      | Alt+S                      |
| Aktualizace výsledků                      | Alt+R                      |
| Vyloučení vybraných stavebních bloků  | Alt+X                      |
| Vyloučení vybrané definice řádku  | Ctrl+B                     |
| Vyloučení vybrané hodnoty dimenze | Ctrl+D                     |
| Otevření vybrané definice sestavy.  | Ctrl+R                     |
| Otevření vybrané definice řádku     | Ctrl+O                     |

 
<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví](financial-reporting-intro.md)

[Rozhraní Návrháře sestav](report-designer-interface.md)



