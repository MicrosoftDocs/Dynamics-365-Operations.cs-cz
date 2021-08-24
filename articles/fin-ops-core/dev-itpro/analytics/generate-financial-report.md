---
title: Generovat finanční sestavy
description: Toto téma obsahuje informace o generování finančních sestav.
author: jinniew
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 101cf2b29bb6f91cec5a3dac0be30b53388905c96ecf481f5b7b3e90cda3f804
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740256"
---
# <a name="generate-financial-reports"></a>Generovat finanční sestavy

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o generování finančních sestav.

Chcete-li vygenerovat sestavu, otevřete definici sestavy a vyberte tlačítko **Generovat** na panelu nástrojů. Otevře se stránka **Stav fronty sestav** a označí umístění vaší sestavy ve frontě. Ve výchozím nastavení se generovaná sestava otevře ve Web Viewer.

Pro generování sestav jsou k dispozici následující možnosti:

- Nastavte plán pro generování sestavy nebo skupiny sestav automaticky
- Kontrolujte chybějící účty nebo data v sestavách a ověřujte přesnost sestav

Při generování sestavy se používají možnosti, které jste zadali na kartě Definice sestavy.

## <a name="generate-a-financial-report"></a>Generovat finanční sestavu

Chcete-li generovat finanční sestavu, přejděte na **Hlavní kniha** \> **Dotazy a sestavy** \> **Finanční sestavy**.

- Zvolte sestavu, kterou chcete generovat, a vyberte **Generovat**.
- Vyplňte pole **Datum sestavy** a vyberte tlačítko **OK**.

Po vygenerování sestavy bude sestava k dispozici pro zobrazení v oddílu **Sestavy**.

Sestavu můžete **Zobrazit** nebo **Odstranit**.

Pro generování sestavy pomocí **návrháře sestav** otevřete definici sestavy a vyberte tlačítko **Generovat** na panelu nástrojů. Otevře se stránka **Stav fronty sestav** a označí umístění vaší sestavy ve frontě. Ve výchozím nastavení se generovaná sestava otevře ve Web Viewer.

## <a name="report-groups"></a>Skupiny sestav

Skupiny sestav jsou účinným způsobem, jak generovat několik sestav současně. Předpokládejme například, že víte, že na konci měsíce generují uživatelé každý měsíc osm sestav. Vytvořte skupinu sestav a místo výběru **Generovat** pro každou z osmi sestav ve skupině můžete vybrat **Generovat** pro skupinu sestav a osm sestav bude vygenerováno v jednom kroku. Po vygenerování sestav ve vybrané skupině přehledů můžete přejít na **Finanční sestavy** (**Hlavní kniha> Dotazy a zprávy > Finanční sestavy**) pro zobrazení jednotlivých sestavy. Chcete-li vytvořit příklad skupinu sestav, proveďte následující kroky.

1. V návrháři sestav vyberte **Skupiny sestav**. 
2. Vyberte existující definice sestav, které chcete zahrnout do své skupiny sestav. 
3. Z každé sestavy, která bude zahrnuta do skupiny, vyberte přepsání nastavení společnosti, podrobností a data.
   Doporučujeme nastavit **Společnost**, **Doba**, **Rok**, a **Úroveň podrobností** pro každou sestavu. 
4. Uložte skupinu sestav.

## <a name="schedule-report-generation"></a>Plánování generování sestavy
Mnohé společnosti používají základní sadu sestav, které se spouštějí v naplánovaných intervalech, aby byly v souladu s jejich obchodními procesy. Můžete naplánovat generování sestavy pravidelně, například denně, týdně, měsíčně nebo ročně. Může se jednat o jednu sestavu nebo skupinu sestav zahrnující několik společností. Pro všechny zadané společnosti, které pocházejí například z definice organizačního stromu, je nutné zadat přihlašovací údaje. Pokud přihlašovací údaje nejsou platné, sestava zobrazí pouze informace, pro přístup k nimž máte oprávnění, například pro společnost, ke které jste momentálně přihlášeni. Výstupní informace jsou nejprve přečteny ze skupiny sestav a poté z jednotlivých sestav.

Jak jsou plány sestav vytvářeny a ukládány, jsou zobrazovány v navigačním podokně v části Plány sestav. Vytvořením složek můžete sestavy uspořádat. Pokud se jedna sestava v plánu nespustí, všechny ostatní sestavy se normálně spustí.

> [!IMPORTANT]
> Abyste mohli vytvářet, měnit a odstraňovat plány sestav, potřebujete roli návrháře nebo správce. Při spuštění sestavy jsou použity přihlašovací údaje uživatele, který plán vytvořil, k vygenerování sestavy.

### <a name="create-a-report-schedule"></a>Vytvoření plánu sestavy

1. V Návrháři sestav v nabídce **Soubor** vyberte tlačítko **Nový** a vyberte možnost **Plán sestavy**. Zobrazí se dialogové okno **Nový plán sestavy**.
2. V části **Nastavení** vyberte jednotlivou sestavu nebo skupinu sestav k naplánování. Jsou dostupné pouze sestavy nebo skupiny sestav pro vybranou společnost nebo stavební blok, ke kterému jste právě přihlášeni.
3. Zaškrtnutím políčka **Aktivní** zapněte plán sestavy. Plán sestavy může aktivovat nebo deaktivovat pouze autor sestavy nebo správce.
4. Vybráním tlačítka **Oprávnění** zadejte přihlašovací údaje pro společnost. Ve výchozím nastavení se použijí přihlašovací údaje pro společnost, ke které jste přihlášeni. Jsou-li zahrnuty jiné společnosti, například v definicích stromu výkaznictví, vyberte možnost **Použít samostatné přihlašovací údaje** a zadejte přihlašovací údaje pro jinou společnost, která je zahrnuta v plánu sestavy. Můžete vybrat možnost **Ověřování systému Windows** nebo zadejte uživatelské jméno a heslo pro každou společnost. Zaškrtnutím políčka **Uložit přihlašovací údaje** můžete uložit přihlašovací údaje pro tyto společnosti a pak zvolením tlačítka **OK** dialogové okno zavřít.
5. V části **Četnost** v poli **Počátek opakování** vyberte datum, kdy má být plán spuštěn. Ve výchozím nastavení se vybere aktuální systémové datum klientského počítače.
6. V poli **Spustit sestavu v** vyberte čas spuštění sestavy. Pokud zadáte čas před aktuálním systémovým časem, spustí se sestava v příští naplánované datum.
7. V oblasti **Způsob opakování** určete, jak často má být sestava spuštěna. Ve výchozím nastavení je vybraná možnost **Denně** s hodnotou intervalu (dny) 1. Další možnosti zahrnují týdenní, měsíční a roční.
8. V oblasti Rozsah opakování vyberte, kdy má být generování sestavy ukončeno.

    - **Bez koncového data** – plán sestavy bude probíhat neomezeně.
    - **Nastavení počtu výskytů** – plán sestavy bude spuštěn s určeným počtem opakování a pak bude deaktivován.
    - **Konec do** – plán sestavy skončí k určenému datu.

9. Zvolte **Uložit**. V dialogovém okně **Uložit jako** zadejte jedinečný název a popis pro plán sestavy.

Abyste mohli zkopírovat plán sestavy, musíte mít roli návrháře nebo správce. I v případě, že správce upraví plán sestavy, sestava si zachová přihlašovací údaje uživatele, který ji vytvořil.

### <a name="copy-a-report-schedule"></a>Zkopírování plánu sestavy

1. V Návrháři sestav vyberte tlačítko **Plány sestav** v podokně navigace a otevřete plán sestavy ke zkopírování.
2. V nabídce **Soubor** vyberte tlačítko **Uložit jako** a zadejte nový název a popis pro plán v dialogovém okně **Uložit jako**. Vyberte tlačítko **OK** a v navigačním podokně se zobrazí nový plán.
3. Upravte pole a informace nového plánu podle potřeby a vyberte tlačítko **Uložit** na panelu nástrojů nebo vyberte tlačítko **Uložit** v nabídce **Soubor**.

Abyste mohli odstranit plán sestavy, musíte být vlastníkem plánu sestavy nebo mít úlohu správce.

### <a name="delete-a-report-schedule"></a>Odstranění plánu sestavy

1. V Návrháři sestav v navigačním podokně vyberte tlačítko **Plány sestav**.
2. Vyberte plán sestavy k odstranění a vyberte tlačítko **Odstranit** nebo stiskněte klávesu **Delete**.
3. V dialogovém okně k ověření odstranění zvolením tlačítka **Ano** trvale odstraňte plán sestavy. Pokud nemáte oprávnění k odstranění plánu, bude zobrazena zpráva a sestava nebude odstraněna.

### <a name="credentials-and-report-schedules"></a>Přihlašovací údaje a plány sestav

Pokud nezadáte přihlašovací údaje, které jsou vyžadovány u všech společností zahrnutých do sestav, při uložení plánu sestav obdržíte následující zprávu: „Je nutné zadat vaše přihlašovací údaje pro společnosti, které jsou obsaženy v tomto plánu sestavy. Klikněte na tlačítko Oprávnění a zadejte přihlašovací údaje.“

Uživatel se například přihlásí ke společnosti A pomocí svého přihlašovacího jména a hesla. Uživatel vytvoří plán pro sestavu, která používá definici stromu výkaznictví ke shromažďování dat z více společností. Při uložení tohoto plánu sestavy je uživatel vyzván k zadání přihlašovacích údajů ostatních společností, které jsou zadány v definici organizačního stromu. Po vypršení platnosti vašich přihlašovacích údajů nebudou ovlivněné sestavy v plánu sestav generovány, dokud nebudou přihlašovací údaje aktualizovány. Zobrazí se zpráva ve frontě sestav informující o tom, že je nutné aktualizovat oprávnění. Provedená plánu sestavy se nezdaří, pokud nastane některá z následujících situací (kvůli vyžadovaným přihlašovacím údajům):

- byla přidána nová společnost do stromu sestav pro jednotlivou sestavu;
- Některá sestava ve skupině sestav byla změněna
- Do skupiny sestav byla přidána nová sestava pro další společnost

Pokračujte zvolením tlačítka **Oprávnění** v dialogovém okně **Plánování sestav** a poté zadejte příslušné přihlašovací údaje.

## <a name="missing-account-analysis-feature"></a>Funkce Analýza chybějících účtů
Můžete hledat finanční účty a dimenze, které mohou chybět v rámci všech definic řádků, definic stromu výkaznictví a definic sestav ve skupině stavebních bloků. To je užitečné při vytváření nebo aktualizaci více účtů nebo stavebních bloků v krátkém časovém období, když chcete ověřit, že všechny nové informace budou zahrnuty do sestav.

Chybějící účty se určují použitím nejnižší a nejvyšší hodnoty z definice řádku nebo definice stromu výkaznictví a zobrazí seznam účtů, které nejsou v definici řádku nebo definici stromu výkaznictví, ale jsou ve finančních datech. Pokud je chybějící účet větší nebo menší než hodnoty v definici řádku, nebude tento účet zahrnut do seznamu chybějících účtů.

> [!TIP]
> Pro účely ověření doporučujeme tento proces spustit před generováním měsíčních sestav a při vytváření nových stavebních bloků.

Sestavy, které mají rozsahy hodnot, mají menší pravděpodobnost chybějících účtů. Pokud je to možné, používejte ve stavebních blocích rozsahy. Budou tak do nich zahrnuty i nově vytvářené účty. Pokud je nějaká definice sestavy nastavena na společnost @ANY, můžete se k dané společnosti přihlásit a spustit pro ni analýzu chybějících účtů.

> [!NOTE]
> Pokud byla přidána nová společnost, je nutné přidat novou společnost do stromů výkaznictví ve všech existujících sestavách, jinak společnost nebude zahrnuta do analýzy chybějících účtů.

### <a name="run-missing-account-analysis"></a>Spuštění analýzy chybějícího účtu

1. V Návrháři sestav vyberte tlačítko **Nástroje** a potom tlačítko **Analýza chybějícího účtu**.
2. V poli **Filtr společnosti** vyberte společnost k filtrování výsledků nebo vyberte možnost **Všechny (žádný filtr)** a zobrazí se výsledky ze všech dostupných společností.
3. V poli **Filtr dimenze** vyberte dimenzi, podle které chcete filtrovat výsledky, nebo vyberte možnost **Všechny (žádný filtr)** k zobrazení všech informací ze všech dostupných dimenzí.
4. V poli **Seskupit podle** vyberte možnost pro řazení výsledků. Výsledky můžete řadit podle příslušného stavebního bloku nebo podle sad hodnot a dimenzí.
5. Projděte si zobrazené výsledky. Když vyberete položku v horním podokně, v dolním podokně se zobrazí další informace o výjimce. To zahrnuje související dimenze, hodnoty a sestavy.
6. Chcete-li otevřít ovlivněnou položku, vyberte přidruženou ikonu zobrazenou v podokně seznamu nebo pravým tlačítkem myši klikněte na položku a vyberte možnost **Otevřít**. Lze vybrat více položek – stiskněte a podržte klávesu **Ctrl** a vyberte položky v dolním podokně.
7. Pokud je vrácena jakákoli hodnota, stavební blok či sestava, které nemají být zahrnuty do analýzy, klikněte pravým tlačítkem na položku a vyberte možnost **Vyloučit** nebo zaškrtněte políčko **Vyloučit** vedle položky k odstranění položky ze seznamu. Vyloučené položky nebudou zahrnuty při aktualizaci seznamu. Lze vybrat více položek – stiskněte a podržte klávesu **Ctrl** a vyberte položky v dolním podokně. Chcete-li zobrazit všechny položky, včetně všech výsledků, které jste dříve z analýzy vyloučili, zaškrtněte políčko **Zobrazit vyloučené stavební bloky a hodnoty** a potom vyberte **Aktualizovat**.
8. Zvolením tlačítka **Aktualizovat** obnovíte výjimky, které byly vyřešeny. Zvolením tlačítka **Ano** proveďte úplnou aktualizaci všech výsledků nebo zvolením tlačítka **Ne** proveďte částečnou aktualizaci adresovaných položek.

    > [!NOTE]
    > Formulář je automaticky aktualizován při otevření, pokud nebyl otevřen v posledních 15 minutách.

9. Po vyřešení potíží zvolením tlačítka **OK** dialogové okno zavřete.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Klávesové zkratky pro analýzu chybějícího účtu
Po spuštění analýzy chybějícího účtu jsou k dispozici následující klávesové zkratky.

| Akce                           | Stiskněte tlačítko . |
|--------------------------------------|----------------------------|
| Filtrování podle společnosti                    | Alt+C                      |
| Filtr podle dimenze                  | ALT+D                      |
| Výběr pole Seskupit podle            | Alt+G                      |
| Zobrazení vyloučených stavebních bloků a hodnot      | Alt+S                      |
| Aktualizace výsledků                      | Alt+R                      |
| Vyloučení vybraného stavebního bloku  | Alt+X                      |
| Vyloučení vybrané definice řádku  | Ctrl+B                     |
| Vyloučení vybrané hodnoty dimenze | Ctrl+D                     |
| Otevření vybrané definice sestavy  | Ctrl+R                     |
| Otevření vybrané definice řádku     | Ctrl+O                     |


## <a name="additional-resources"></a>Další zdroje

[Finanční výkaznictví](financial-reporting-intro.md)

[Rozhraní Návrháře sestav](report-designer-interface.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
