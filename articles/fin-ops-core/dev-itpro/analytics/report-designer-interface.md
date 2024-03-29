---
title: Rozhraní Návrháře sestav
description: Tento článek vysvětluje, jak navigovat v Report Designer, a jak používat různé možnosti podle specifických požadavků.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.form: FinancialReports
ms.openlocfilehash: 25d913e6f5d4c95dceda1291a2c33abe37348574
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802735"
---
# <a name="report-designer-interface"></a>Rozhraní Návrháře sestav

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak navigovat v Report Designer, a jak používat různé možnosti podle specifických požadavků.

## <a name="report-designer-menu-commands"></a>Příkazy nabídky Report Designer

V následujících tabulkách jsou popsány příkazy a možnosti nabídky, které lze použít při návrhu finančních sestav. Některé příkazy a možnosti nabídky jsou k dispozici pouze za zvláštních okolností. Například příkazy pro zvýšení a snížení úrovně organizační jednotky jsou dostupné pouze pokud upravujete definice organizačního stromu.

### <a name="file-menu"></a>Nabídka Soubor

Nabídka **Soubor** je k dispozici všem uživatelům a obsahuje následující příkazy.

| Příkaz                           | Popis |
|-----------------------------------|-------------|
| Nová                               | Vytvořte novou definici sestavy, definici řádku, definici sloupce, definici stromu výkaznictví, definici skupiny výkaznictví nebo složku. Další možnosti jsou k dispozici v závislosti na vaší uživatelské roli. |
| Otevřené                              | Otevřete existující definici řádku, definici sloupce, definici stromu výkaznictví nebo definici sestavy. |
| Zavřít                             | Zavře aktuální stavební blok. |
| Zavřít vše                         | Zavře všechny stavební bloky. |
| Uložit                              | Uloží aktuální definici řádků, definici sloupců, definici organizačního stromu nebo definici sestavy. |
| Uložit jako                           | Uloží aktuální definici řádků, definici sloupců, definici organizačního stromu nebo definici sestavy pod novým názvem. |
| Vlastnosti                        | Otevře dialogové okno **Vlastnosti**, ve kterém můžete změnit název a popis sestavy. |
| Generovat                          | Vygeneruje aktuální sestavu. Tento příkaz je dostupný z definice sestavy. |
| Zobrazit sestavu                       | Otevře nejnovější verzi vygenerované sestavy. Tento příkaz je k dispozici z definice sestavy, pokud jste vygenerovali alespoň jednu sestavu. |
| Poslední definice sestav         | Zobrazí seznam zpráv, které byly nedávno vytvořeny nebo změněny. Zprávu pak můžete vybrat ze seznamu. |
| Poslední definice řádků            | Zobrazí seznam definicí řádků, které byly nedávno vytvořeny nebo změněny. Definici řádku pak můžete vybrat ze seznamu. |
| Poslední definice sloupců         | Zobrazí seznam definicí sloupců, které byly nedávno vytvořeny nebo změněny. Definici sloupce pak můžete vybrat ze seznamu. |
| Poslední definice organizačních stromů | Zobrazí seznam definicí organizačních stromů, které byly nedávno vytvořeny nebo změněny. Definici organizačního stromu pak můžete vybrat ze seznamu. |
| Konec                              | Ukončete Návrhář sestav. |

### <a name="edit-menu"></a>Nabídka Upravit

Nabídka **Upravit** je k dispozici pro uživatele, kteří mají role **Návrhář** nebo **Správce**. Tato nabídka zahrnuje následující příkazy.

| Příkaz                                | Popis |
|----------------------------------------|-------------|
| Zpět                                   | Vrátí zpět poslední akci. |
| Znovu                                   | Stornuje poslední akci vrácení. |
| Vyjmout                                    | Odstraní vybraný text a zkopíruje ho do schránky. |
| Kopírovat                                   | Zkopíruje vybraný text do schránky. |
| Vložit                                  | Vloží naposledy vyjmutý nebo zkopírovaný text ze schránky. |
| Vymazat                                  | Odstraní obsah vybrané buňky stavebního bloku. |
| Najít                                   | Otevře dialogové okno **Najít a nahradit**, kde můžete prohledávat text v podokně náhledu. |
| Nahradit                                | Otevře dialogové okno **Najít a nahradit**, kde můžete prohledávat a nahrazovat text v podokně náhledu. |
| Vložit řádky z dimenzí            | Otevře dialogové okno **Vložit řádky z dimenzí**, kde můžete vybrat hodnoty dimenze, které mají být zahrnuty v definici řádku. Tento příkaz je dostupný z definice řádků. |
| Přečíslovat řádky                          | Přečísluje všechny číselné kódy řádků. Tento příkaz je dostupný z definice řádků. |
| Odkazy na řádky                              | Otevře dialogové okno **Odkazy řádků**, kde můžete určit zdroje pro datové odkazy v definicích řádků a definicích stromů výkaznictví. Tento příkaz je dostupný z definice řádků. |
| Úprava zaokrouhlení                    | Otevře dialogové okno **Vyrovnání rozdílů po zaokrouhlení**, kde můžete zadat parametry pro zaokrouhlování. Tento příkaz je dostupný z definice řádků. |
| Spravovat sady dimenzí                  | Otevře dialogové okno **Sady dimenzí**, ve kterém můžete vytvořit a upravit sady dimenzí. Tento příkaz je dostupný z definice řádků nebo z definice organizačního stromu. |
| Vložit řádek                             | Vloží prázdný řádek do definice řádků nebo prázdný řádek záhlaví do definice sloupců. Tento příkaz je dostupný z definice řádků nebo sloupců. |
| Odstranit řádek                             | Odstraní vybraný řádek z definice řádků nebo vybraný řádek záhlaví z definice sloupců. Tento příkaz je dostupný z definice řádků nebo sloupců. |
| Vložit sloupec                          | Vloží prázdný sloupec do definice sloupců. Tento příkaz je dostupný z definice sloupců. |
| Odstranit sloupec                          | Odstraní vybraný sloupec z definice sloupců. Tento příkaz je dostupný z definice sloupců. |
| Vložit organizační jednotky z dimenzí | Otevře dialogové okno **Vložit jednotky výkaznictví z dimenzí**, kde můžete vybrat hodnoty dimenze, které mají být zahrnuty v definici stromu výkaznictví. Tento příkaz je dostupný z definice organizačního stromu. |
| Importovat hierarchii sad dimenzí         | Otevře dialogové okno **Hierarchie sady dimenzí**, kde můžete importovat hierarchii sady dimenzí z finančních dat. Tento příkaz je k dispozici z definice stromu výkaznictví pro systém ve složce. .\\financial-dimensions\\systém založený na dimenzích. |
| Vložit organizační jednotku                  | Vložte prázdný řádek do definice stromu výkaznictví. Tento příkaz je dostupný z definice organizačního stromu. |
| Odstranit organizační jednotku                  | Odstraní vybranou organizační jednotku z definice organizačního stromu. Tento příkaz je dostupný z definice organizačního stromu. |

### <a name="view-menu"></a>Nabídka Zobrazit

Nabídka **Zobrazení** je k dispozici všem uživatelům a obsahuje následující příkazy.

| Příkaz         | Popis                                                            |
|-----------------|------------------------------------------------------------------------|
| Navigační podokno | Zobrazí nebo skryje navigační podokno.                                      |
| Panely nástrojů        | Umožňuje vybrat panely nástrojů, které jsou viditelné.                                  |
| Stavový řádek      | Zobrazí nebo skryje informace o stavu v okně **Report Designer**. |
| Uvítací stránka    | Otevře **uvítací stránku**.                                             |

### <a name="format-menu"></a>Nabídka Formát

Nabídka **Formát** je k dispozici pro uživatele, kteří mají role **Návrhář** nebo **Správce**. Tato nabídka zahrnuje následující příkazy.

| Command               | popis |
|-----------------------|-------------|
| Styly a formátování | Otevře dialogové okno **Styly a formátování**, ve kterém můžete vytvářet a upravovat styl textu v definicích řádků a definicích sloupců. Tento příkaz je dostupný z definice řádků nebo sloupců. |
| Šířka sloupce          | Otevře dialogové okno **Šířka sloupce**, kde můžete nastavit šířku vybraného sloupce. Tento příkaz je dostupný z definice řádků, definice sloupců nebo definice organizačního stromu. |
| Skrýt                  | Skryje vybraný sloupec. Tento příkaz je dostupný z definice řádků, definice sloupců nebo definice organizačního stromu. |
| Zobrazit                | Zviditelní sloupce skryté mezi vybranými sloupci. Tento příkaz je dostupný z definice řádků, definice sloupců nebo definice organizačního stromu. |

### <a name="company-menu"></a>Nabídka Společnost

Nabídka **Společnost** je k dispozici pro uživatele, kteří mají role **Návrhář** nebo **Správce**. Tato nabídka zahrnuje následující příkazy.

| Příkaz               | Popis                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Společnosti             | Otevře dialogové okno **Společnosti**, ve kterém můžete vytvářet a upravovat společnosti.                                          |
| Skupiny stavebních bloků | Otevře dialogové okno **Skupiny stavebních bloků**, kde můžete vytvořit, upravit, importovat a exportovat skupiny stavebních bloků. |

### <a name="go-menu"></a>Nabídka Přejít

Nabídka **Přejít** je dostupná všem uživatelům a obsahuje následující příkazy.

> [!NOTE]
> Tyto příkazy nemají žádný viditelný vliv, pokud není zobrazeno navigační podokno.

| Příkazy                   | Popis                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Definice sestav         | Zobrazí v navigačním podokně definice sestav.                                    |
| Definice řádků            | Zobrazí v navigačním podokně definice řádků.                                       |
| Definice sloupců         | Zobrazí v navigačním podokně definice sloupců.                                    |
| Definice organizačních stromů | Zobrazí v navigačním podokně definice organizačních stromů.                            |
| Zabezpečení                   | Zobrazí v navigačním podokně informace o zabezpečení pro uživatele, skupiny a společnosti. |

### <a name="tools-menu"></a>Nabídka Nástroje

Nabídka **Nástroje** je k dispozici všem uživatelům, avšak některé příkazy mají omezenou dostupnost. Tato nabídka zahrnuje následující příkazy.

| Příkaz                       | Popis |
|-------------------------------|-------------|
| Zamknout                       | Uplatní heslo na aktuální stavební blok. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**. |
| Stav fronty sestav           | Otevře dialogové okno **Stav fronty sestav**, v němž se zobrazí všechny nedávno vygenerované sestavy a podrobnosti jednotlivých sestav. |
| Informace o zdrojovém systému     | Zobrazte nastavení pro systém Microsoft Dynamics ERP. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**. |
| Rezervované položky             | Zobrazí definice řádků, definice sloupců, definice organizačních stromů a definice sestav, které jsou momentálně otevřené. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**. |
| Aktualizovat finanční data v mezipaměti | Aktualizuje data ve sloupci finančních dimenzí. |
| Možnosti                       | Otevře dialogové okno **Možnosti**, kde můžete upravit uživatelské předvolby pro Návrhář sestav. |

### <a name="window-menu"></a>Nabídka Okno

Nabídka **Okno** je k dispozici všem uživatelům a obsahuje následující příkazy.

| Příkaz              | Popis |
|----------------------|-------------|
| Uspořádat vedle sebe    | Zobrazí všechna otevřená okna vedle sebe. |
| Uspořádat nad sebou      | Zobrazí všechna otevřená okna nad sebou. |
| Na sebe              | Zobrazí všechna otevřená okna ve vrstvách tak, aby bylo viditelné záhlaví každého okna. |
| Ukotvit vodorovně    | Ukotví vybraný řádek, takže při posouvání zůstane tento řádek zobrazen v okně. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**. |
| Ukotvit svisle      | Ukotví vybraný sloupec, takže při posouvání zůstane tento sloupec zobrazen v okně. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**. |
| Seznam otevřených oken | Zobrazí seznam oken, která jsou otevřena. Zvolením okna je přeneste do popředí. |

### <a name="help-menu"></a>Nabídka Nápověda

Nabídka **Nápověda** je k dispozici všem uživatelům a obsahuje následující příkazy.

| Příkaz | Popis                                                              |
|---------|--------------------------------------------------------------------------|
| Nápověda    | Otevřete stránku článku s nápovědou pro finanční výkaznictví. |
|         |                                                                          |

## <a name="report-designer-toolbar-buttons"></a>Tlačítka panelu nástrojů Report Designer
Následující tabulky popisují tlačítka na panelu nástrojů, která lze použít při navrhování sestav. Některá tlačítka na panelu nástrojů jsou dostupná pouze za určitých okolností. Například tlačítka pro zvýšení a snížení úrovně organizační jednotky jsou dostupná pouze pokud upravujete definice organizačního stromu.

### <a name="standard-toolbar"></a>Panel nástrojů Standardní

Tento panel nástrojů poskytuje rychlý přístup k příkazům pro práci se soubory a k editačním příkazům. Tento panel nástrojů obsahuje následující tlačítka.

| Tlačítko                                                                                       | popis |
|----------------------------------------------------------------------------------------------|-------------|
| [![Tlačítko Nový.](./media/rowc130389.png)](./media/rowc130389.png)                              | Vytvoří novou (prázdnou) definici sestavy, definici řádků, definici sloupců nebo definici organizačního stromu. |
| [![Tlačítko Otevřít.](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Otevřete existující definici řádku, definici sloupce, definici stromu výkaznictví nebo definici sestavy. |
| [![Tlačítko Uložit.](./media/savec130389.png)](./media/savec130389.png)                           | Uloží aktuální definici řádků, definici sloupců, definici organizačního stromu nebo definici sestavy. |
| [![Tlačítko Kopírovat.](./media/copyc130389.png)](./media/copyc130389.png)                           | Zkopíruje vybraný text do schránky. |
| [![Tlačítko Vyjmout.](./media/cutc130389.png)](./media/cutc130389.png)                              | Odstraní vybraný text a zkopíruje ho do schránky. |
| [![Tlačítko Vložit.](./media/pastec130389.png)](./media/pastec130389.png)                        | Vloží text ze schránky. |
| [![Tlačítko Zpět.](./media/undoc130389.png)](./media/undoc130389.png)                           | Vrátí zpět poslední akci. |
| [![Tlačítko Znovu.](./media/redoc130389.png)](./media/redoc130389.png)                           | Stornuje poslední akci vrácení. |
| [![Tlačítko Najít.](./media/findc130389.png)](./media/findc130389.png)                           | Otevře dialogové okno **Najít a nahradit**, kde můžete prohledávat a nahrazovat text v aktivním okně. |
| [![Tlačítko Vložit řádek.](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Vloží prázdný řádek do definice řádků nebo prázdný řádek záhlaví do definice sloupců. Toto tlačítko je dostupné z definice řádků nebo definice sloupců. |
| [![Tlačítko Vložit sloupec.](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Vloží prázdný sloupec do definice sloupců. Toto tlačítko je dostupné z definice sloupců. |
| [![Tlačítko Zámek.](./media/lockc130389.png)](./media/lockc130389.png)                           | Uplatní heslo na aktuální stavební blok. Toto tlačítko je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**. |
| [![Tlačítko Odkaz řádku.](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Otevře dialogové okno **Odkazy řádků**, kde můžete určit zdroje pro datové odkazy v definicích řádků a definicích stromů výkaznictví. Toto tlačítko je dostupné z definice řádků. |
| [![Tlačítko Zvýšit úroveň.](./media/promotec130389.png)](./media/promotec130389.png)                  | Zvýší úroveň jednotky v definici organizačního stromu. Když vyberete podřízenou jednotku a kliknete na tlačítko **Zvýšit úroveň**, podřízená jednotka bude přesunuta na stejnou úroveň jako nadřazená jednotka. |
| [![Tlačítko Snížit úroveň.](./media/demotec130389.png)](./media/demotec130389.png)                     | Sníží úroveň jednotky v definici organizačního stromu. Pokud vyberete jednotku a kliknete na tlačítko **Snížit úroveň**, jednotka se stane podřízenou pro jednotku, která jí předchází. |
| [![Tlačítko Rozbalit.](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Rozbalí všechny jednotky v definici organizačního stromu na úrovni vybrané jednotky. |
| [![Tlačítko Sbalit.](./media/collapsec130389.png)](./media/collapsec130389.png)               | Sbalí strom výkaznictví. |
| [![Tlačítko Nápověda.](./media/helpc130389.png)](./media/helpc130389.png)                           | Otevřete nápovědu. |

### <a name="formatting-toolbar"></a>Panel nástrojů formátování

Panel nástrojů formátování nabízí snadný přístup k příkazům stylů. Tento panel nástrojů obsahuje následující tlačítka.

| Tlačítko                                                                                                       | popis                                           |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [![Tlačítko Styl písma.](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Použije na aktuální text vybraný styl písma.   |
| [![Tlačítko Písmo.](./media/fonttype.png)](./media/fonttype.png)                                                 | Nastaví u aktuálního textu vybrané písmo.           |
| [![Tlačítko Velikost písma.](./media/fontsize.png)](./media/fontsize.png)                                            | Nastaví u aktuálního textu vybranou velikost písma (v bodech). |
| [![Tlačítko Tučné.](./media/boldc130389.png)](./media/boldc130389.png)                                           | Nastaví aktuální text jako tučný.                          |
| [![Tlačítko Kurzíva.](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Nastaví aktuální text jako kurzívu.                        |
| [![Tlačítko Podtržené.](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Podtrhne aktuální text.                          |
| [![Tlačítko Zmenšit odsazení.](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Zmenší odsazení aktuálního textu.             |
| [![Tlačítko Zvětšit odsazení.](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Zvětší odsazení aktuálního textu.             |
| [![Tlačítko Barva pozadí.](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Změní barvu pozadí aktuální buňky.     |
| [![Tlačítko Barva písma.](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Změní barvu aktuálního textu.                |

### <a name="report-designer-toolbar"></a>Panel nástrojů návrháře sestav

Panel nástrojů návrháře sestav poskytuje rychlý přístup k příkazům navigace v návrháři sestav. Tento panel nástrojů obsahuje následující tlačítka.

| Tlačítko                                                                                              | popis |
|-----------------------------------------------------------------------------------------------------|-------------|
| [![Tlačítko Definice sestavy.](./media/reportc130389.png)](./media/reportc130389.png)            | Zobrazí definici sestavy uvedenou v nabídce **Okno**. |
| [![Tlačítko Definice řádku.](./media/rowc130389.png)](./media/rowc130389.png)             | Zobrazí definici řádků, která je přiřazena k definici aktivní sestavy. |
| [![Tlačítko Definice sloupce.](./media/columnc130389.png)](./media/columnc130389.png)  | Zobrazí definici sloupců, která je přiřazena k definici aktivní sestavy. |
| [![Tlačítko Definice stromu výkaznictví.](./media/treec130389.png)](./media/treec130389.png)             | Zobrazí definici organizačního stromu, která je přiřazena k definici aktivní sestavy. |
| [![Tlačítko Report Viewer.](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Spustí Prohlížeč sestav s nejnovější verzí vygenerované sestavy. Toto tlačítko je dostupné z definice sestavy, pokud jste vygenerovali alespoň jednu sestavu. |
| [![Tlačítko Generovat sestavu.](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Vygeneruje sestavu z definice aktivní sestavy. Toto tlačítko je dostupné z definice sestavy. |

## <a name="additional-resources"></a>Další zdroje

[Finanční výkaznictví](financial-reporting-intro.md)

[Generování finančních sestav](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
