---
title: "Rozhraní Návrháře sestav"
description: "Tento článek vysvětluje, jak navigovat v návrháři sestav, a jak používat různé možnosti podle specifických požadavků."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 50 - 10
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59041
ms.assetid: 054de5b0-8618-4195-be12-f031b4bb4d74
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 58c56aca6f339a5ec13703605334dd45b208ab2c
ms.lasthandoff: 03/29/2017


---

# <a name="report-designer-interface"></a>Rozhraní Návrháře sestav

Tento článek vysvětluje, jak navigovat v návrháři sestav, a jak používat různé možnosti podle specifických požadavků. 

<a name="report-designer-menu-commands"></a>Příkazy nabídky Návrháře sestav
-----------------------------

V následujících tabulkách jsou popsány příkazy a možnosti nabídky, které lze použít při návrhu finančních sestav. Některé příkazy a možnosti nabídky jsou k dispozici pouze za zvláštních okolností. Například příkazy pro zvýšení a snížení úrovně vykazovacích jednotek jsou k dispozici pouze v případě, že měníte definici stromu výkaznictví.

### <a name="file-menu"></a>Nabídka Soubor

Nabídka **Soubor** je k dispozici všem uživatelům a obsahuje následující příkazy.

| Příkaz                           | Popis                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nový                               | Vytvořte novou definici sestavy, definici řádku, definici sloupce, definici stromu výkaznictví, definici skupiny výkaznictví nebo složku. Další možnosti jsou k dispozici v závislosti na vaší uživatelské roli. |
| Otevřené                              | Otevřete existující definici řádku, definici sloupce, definici stromu výkaznictví nebo definici sestavy.                                                                                             |
| Zavřít                             | Zavře aktuální stavební blok.                                                                                                                                                                |
| Zavřít vše                         | Zavře všechny stavební bloky.                                                                                                                                                                       |
| Uložit                              | Uloží aktuální definici řádku, definici sloupce, definici stromu výkaznictví nebo definici sestavy.                                                                                             |
| Uložit jako                           | Uloží aktuální definici řádku, definici sloupce, definici stromu výkaznictví nebo definici sestavy pod novým názvem.                                                                            |
| Vlastnosti                        | Otevře dialogové okno **Vlastnosti**, ve kterém můžete změnit název a popis sestavy.                                                                                                   |
| Vytvořit                          | Vygeneruje aktuální sestavu. Tento příkaz je k dispozici z definice sestavy.                                                                                                                 |
| Zobrazit sestavu                       | Poslední verze generovanou sestavu otevřete v 365 Dynamics pro operace. Tento příkaz je k dispozici z definice sestavy, pokud jste vygenerovali alespoň jednu sestavu.                                 |
| Poslední definice sestav         | Zobrazí seznam sestav, které byly naposledy vytvořeny nebo upraveny. Poté můžete vybrat sestavu ze seznamu.                                                                                    |
| Poslední definice řádků            | Zobrazí definic řádků, které byly naposledy vytvořeny nebo upraveny. Poté můžete vybrat definici řádku ze seznamu.                                                                    |
| Poslední definice sloupce         | Zobrazí seznam definice sloupce, které byly naposledy vytvořeny nebo upraveny. Poté můžete vybrat definici sloupce ze seznamu.                                                              |
| Poslední definice stromu výkaznictví | Zobrazí seznam definic stromů výkaznictví, které byly naposledy vytvořeny nebo upraveny. Poté můžete vybrat definici stromu výkaznictví ze seznamu.                                              |
| Ukončit                              | Ukončí Návrhář sestav.                                                                                                                                                                            |

### <a name="edit-menu"></a>Nabídka Upravit

Nabídka **Upravit** je k dispozici pro uživatele, kteří mají role **Návrhář** nebo **Správce**. Tato nabídka obsahuje následující příkazy:

| Příkaz                                | Popis                                                                                                                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zpět                                   | Vrátí zpět předchozí akci.                                                                                                                                                                                              |
| Znovu                                   | Zopakuje dříve vrácenou akci.                                                                                                                                                                                      |
| Vyjmout                                    | Vymaže vybraný text a zkopíruje ho do schránky.                                                                                                                                                            |
| Kopírovat                                   | Zkopíruje vybraný text do schránky.                                                                                                                                                                           |
| Vložit                                  | Vloží naposledy vyjmutý nebo zkopírovaný text ze schránky.                                                                                                                                                    |
| Vymazat                                  | Vymaže obsah vybrané buňky stavebního bloku.                                                                                                                                                           |
| Najít                                   | Otevře dialogové okno **Najít a nahradit**, kde můžete prohledávat text v podokně náhledu.                                                                                                                              |
| Nahradit                                | Otevře dialogové okno **Najít a nahradit**, kde můžete prohledávat a nahrazovat text v podokně náhledu.                                                                                                                  |
| Vložit řádky z dimenzí            | Otevře dialogové okno **Vložit řádky z dimenzí**, kde můžete vybrat hodnoty dimenze, které mají být zahrnuty v definici řádku. Tento příkaz je k dispozici z definice řádku.                                  |
| Přečíslovat řádky                          | Přečísluje všechny číselné kódy řádků. Tento příkaz je k dispozici z definice řádku.                                                                                                                                   |
| Odkazy řádků                              | Otevře dialogové okno **Odkazy řádků**, kde můžete určit zdroje pro datové odkazy v definicích řádků a definicích stromů výkaznictví. Tento příkaz je k dispozici z definice řádku.                            |
| Vyrovnání rozdílů po zaokrouhlení                    | Otevře dialogové okno **Vyrovnání rozdílů po zaokrouhlení**, kde můžete zadat parametry pro zaokrouhlování. Tento příkaz je k dispozici z definice řádku.                                                                  |
| Správa sad dimenzí                  | Otevře dialogové okno **Sady dimenzí**, ve kterém můžete vytvořit a upravit sady dimenzí. Tento příkaz je k dispozici v definici řádku nebo definici stromu výkaznictví.                                              |
| Vložit řádek                             | Vloží prázdný řádek do definice řádku nebo prázdný řádek záhlaví do definice sloupce. Tento příkaz je k dispozici v definici řádku nebo definici sloupce.                                               |
| Odstranit řádek                             | Odstraní vybraný řádek z definice řádku nebo vybraný řádek záhlaví z definice sloupce. Tento příkaz je k dispozici v definici řádku nebo definici sloupce.                                       |
| Vložit sloupec                          | Vloží prázdný sloupec do definice sloupce. Tento příkaz je k dispozici z definice sloupce.                                                                                                             |
| Odstranit sloupec                          | Odstraní vybraný sloupec z definice sloupce. Tento příkaz je k dispozici z definice sloupce.                                                                                                         |
| Vložit jednotky výkaznictví z dimenzí | Otevře dialogové okno **Vložit jednotky výkaznictví z dimenzí**, kde můžete vybrat hodnoty dimenze, které mají být zahrnuty v definici stromu výkaznictví. Tento příkaz je k dispozici z definice stromu výkaznictví. |
| Importovat hierarchii sady dimenzí         | Otevře dialogové okno **Hierarchie sady dimenzí**, kde můžete importovat hierarchii sady dimenzí z finančních dat. Tento příkaz je dostupný z definice stromu vykazování pro... \financial-dimensions\dimension-Based systém.  |
| Vložit jednotku výkaznictví                  | Vložte prázdný řádek do definice stromu výkaznictví. Tento příkaz je k dispozici z definice stromu výkaznictví.                                                                                                |
| Odstranit jednotku výkaznictví                  | Odstraní vybranou jednotku výkaznictví z definice stromu výkaznictví. Tento příkaz je k dispozici z definice stromu výkaznictví.                                                                             |

### <a name="view-menu"></a>Nabídka Zobrazení

Nabídka **Zobrazení** je k dispozici všem uživatelům a obsahuje následující příkazy.

| Příkaz         | Popis                                                            |
|-----------------|------------------------------------------------------------------------|
| Podokno Navigace | Zobrazí nebo skryje navigační podokno.                                      |
| Panely nástrojů        | Vyberte panely nástrojů, které jsou zobrazeny.                                  |
| Stavový řádek      | Zobrazí nebo skryje informace o stavu v okně **Návrhář sestav**. |
| Uvítací stránka    | Otevře stránku **Vítejte**.                                             |

### <a name="format-menu"></a>Nabídka Formát

Nabídka **Formát** je k dispozici pro uživatele, kteří mají role **Návrhář** nebo **Správce**. Tato nabídka obsahuje následující příkazy:

| Příkaz               | Popis                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Styly a formátování | Otevře dialogové okno **Styly a formátování**, ve kterém můžete vytvářet a upravovat styl textu v definicích řádků a definicích sloupců. Tento příkaz je k dispozici v definici řádku nebo definici sloupce. |
| Šířka sloupce          | Otevře dialogové okno **Šířka sloupce**, kde můžete nastavit šířku vybraného sloupce. Tento příkaz je k dispozici v definici řádku, definici sloupce nebo definici stromu výkaznictví.                      |
| Skrýt                  | Skryje vybraný sloupec. Tento příkaz je k dispozici v definici řádku, definici sloupce nebo definici stromu výkaznictví.                                                                                        |
| Zobrazit                | Zobrazí skryté sloupce mezi vybranými sloupci. Tento příkaz je k dispozici v definici řádku, definici sloupce nebo definici stromu výkaznictví.                                                      |

### <a name="company-menu"></a>Nabídka Společnost

Nabídka **Společnost** je k dispozici pro uživatele, kteří mají role **Návrhář** nebo **Správce**. Tato nabídka obsahuje následující příkazy:

| Příkaz               | Popis                                                                                                            |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Společnosti             | Otevře dialogové okno **Společnosti**, ve kterém můžete vytvářet a upravovat společnosti.                                          |
| Skupiny stavebních bloků | Otevře dialogové okno **Skupiny stavebních bloků**, kde můžete vytvořit, upravit, importovat a exportovat skupiny stavebních bloků. |

### <a name="go-menu"></a>Nabídka Přejít

Nabídka **Přejít** je k dispozici všem uživatelům a obsahuje následující příkazy. **Poznámka:** Tyto příkazy nemají žádný viditelný efekt, pokud není zobrazeno navigační podokno.

| Příkazy                   | Popis                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| Definice sestavy         | Zobrazí definice sestavy v navigačním podokně.                                    |
| Definice řádku            | Zobrazí definice řádku v navigačním podokně.                                       |
| Definice sloupce         | Zobrazí definice sloupce v navigačním podokně.                                    |
| Definice stromu výkaznictví | Zobrazí definice stromu výkaznictví v navigačním podokně.                            |
| Zabezpečení                   | Zobrazí informace o zabezpečení pro uživatele, skupiny a společnosti v navigačním podokně. |

### <a name="tools-menu"></a>Nabídka Nástroje

Nabídka **Nástroje** je k dispozici všem uživatelům, avšak některé příkazy mají omezenou dostupnost. Tato nabídka obsahuje následující příkazy:

| Příkaz                       | Popis                                                                                                                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chránit                       | Přiřadí aktuálnímu stavebnímu bloku heslo. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**.                                                                           |
| Stav fronty sestav           | Otevře dialogové okno **Stav fronty sestav**, v němž se zobrazí všechny nedávno vygenerované sestavy a podrobnosti jednotlivých sestav.                                                                                    |
| Informace o zdrojovém systému     | Zobrazí nastavení systému Microsoft Dynamics ERP. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**.                                                                 |
| Rezervované položky             | Zobrazí definice řádků, definice sloupců, definice stromu výkaznictví a definice sestav, které jsou právě otevřené. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**. |
| Aktualizovat finanční data uložená v mezipaměti | Aktualizuje data ve sloupci finanční dimenze.                                                                                                                                                               |
| Možnosti                       | Otevře dialogové okno **Možnosti**, kde můžete upravit uživatelské předvolby pro Návrhář sestav.                                                                                                                       |

### <a name="window-menu"></a>Nabídka Okno

Nabídka **Okno** je k dispozici všem uživatelům a obsahuje následující příkazy.

| Příkaz              | Popis                                                                                                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uspořádat vedle sebe    | Zobrazí vedle sebe všechna okna.                                                                                                                                                     |
| Uspořádat nad sebou      | Zobrazí všechna okna nad sebou.                                                                                                                                               |
| Na sebe              | Překryje přes sebe všechna otevřená okna tak, aby bylo viditelné záhlaví každého okna.                                                                                                                      |
| Ukotvit vodorovně    | Ukotví vybraný řádek tak, aby byl při posunování tento řádek stále viditelný v okně. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**.       |
| Ukotvit svisle      | Ukotví vybraný sloupec tak, aby byl při posunování tento sloupec stále viditelný v okně. Tento příkaz je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**. |
| Seznam otevřených oken | Zobrazí seznam oken, která jsou otevřená. Výběrem můžete okno přesunout dopředu.                                                                                                               |

### <a name="help-menu"></a>Nabídka Nápověda

Nabídka **Nápověda** je k dispozici všem uživatelům a obsahuje následující příkazy.

| Příkaz | popis                                                  |
|---------|--------------------------------------------------------------|
| Nápověda    | Otevřete 365 Dynamics operace nápovědy wiki stránky pro finanční vykazování. |
|         |                                                              |

## <a name="report-designer-toolbar-buttons"></a>Tlačítka panelu nástrojů Návrháře sestav
Následující tabulky popisují tlačítka na panelu nástrojů, která lze použít při navrhování sestav. Některá tlačítka panelu nástrojů jsou k dispozici pouze za zvláštních okolností. Například tlačítka pro zvýšení a snížení úrovně vykazovacích jednotek jsou k dispozici pouze v případě, že měníte definici stromu výkaznictví.

### <a name="standard-toolbar"></a>Standardní panel nástrojů

Standardní panel nástrojů poskytuje rychlý přístup k příkazům pro soubory a úpravy. Tento panel nástrojů obsahuje následující tlačítka.

| Tlačítko                                                                                                                                                                                   | Popis                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![New button](./media/rowc130389.png)](./media/rowc130389.png)                              | Můžete vytvořit novou (prázdnou) definici sestavy, definici řádku, definici sloupce nebo definici stromu výkaznictví.                                                                               |
| [![Tlačítko Otevřít](./media/openfolderc130389.png)](./media/openfolderc130389.png)               | Otevřete existující definici řádku, definici sloupce, definici stromu výkaznictví nebo definici sestavy.                                                                                   |
| [![Tlačítko Uložit](./media/savec130389.png)](./media/savec130389.png)                           | Uloží aktuální definici řádku, definici sloupce, definici stromu výkaznictví nebo definici sestavy.                                                                                   |
| [![Tlačítko Kopírovat](./media/copyc130389.png)](./media/copyc130389.png)                           | Zkopíruje vybraný text do schránky.                                                                                                                                               |
| [![Tlačítko Vyjmout](./media/cutc130389.png)](./media/cutc130389.png)                              | Vymaže vybraný text a zkopíruje ho do schránky.                                                                                                                                |
| [![Tlačítko Vložit](./media/pastec130389.png)](./media/pastec130389.png)                        | Vloží text ze schránky.                                                                                                                                                    |
| [![Tlačítko Zpět](./media/undoc130389.png)](./media/undoc130389.png)                           | Vrátí zpět předchozí akci.                                                                                                                                                                  |
| [![Tlačítko znovu](./media/redoc130389.png)](./media/redoc130389.png)                           | Zopakuje dříve vrácenou akci.                                                                                                                                                          |
| [![Tlačítko Najít](./media/findc130389.png)](./media/findc130389.png)                           | Otevře dialogové okno **Najít a nahradit**, kde můžete prohledávat a nahrazovat text v aktivním okně.                                                                                  |
| [![Vložit řádek tlačítko.](./media/insertrowc130389.png)](./media/insertrowc130389.png)           | Vloží prázdný řádek do definice řádku nebo prázdný řádek záhlaví do definice sloupce. Toto tlačítko je k dispozici v definici řádku nebo definici sloupce.                    |
| [![Můžete vložit sloupec](./media/insertcolumnc130389.png)](./media/insertcolumnc130389.png)  | Vloží prázdný sloupec do definice sloupce. Toto tlačítko je k dispozici z definice sloupce.                                                                                  |
| [![Tlačítko zámku](./media/lockc130389.png)](./media/lockc130389.png)                           | Přiřadí aktuálnímu stavebnímu bloku heslo. Toto tlačítko je k dispozici pro uživatele, kteří mají role **Návrhář** **Správce**.                                                 |
| [![Tlačítko propojit řádek](./media/rowlinkc130389.png)](./media/rowlinkc130389.png)                 | Otevře dialogové okno **Odkazy řádků**, kde můžete určit zdroje pro datové odkazy v definicích řádků a definicích stromů výkaznictví. Toto tlačítko je k dispozici z definice řádku. |
| [![Podporovat tlačítko](./media/promotec130389.png)](./media/promotec130389.png)                  | Zvýší úroveň jednotky definice stromu výkaznictví. Když vyberete podřízenou jednotku a kliknete na tlačítko **Zvýšit úroveň**, podřízená jednotka bude přesunuta na stejnou úroveň jako nadřazená jednotka.                |
| [![Tlačítko snížit úroveň](./media/demotec130389.png)](./media/demotec130389.png)                     | Sníží úroveň jednotky definice stromu výkaznictví. Pokud vyberete jednotku a kliknete na tlačítko **Snížit úroveň**, jednotka se stane podřízenou pro jednotku, která jí předchází.                               |
| [![Tlačítko Rozbalit](./media/expandtreebuttonc130389.png)](./media/expandtreebuttonc130389.png) | Rozbalte všechny jednotky definice stromu výkaznictví na úrovni vybrané jednotky.                                                                                                   |
| [![Tlačítko Sbalit](./media/collapsec130389.png)](./media/collapsec130389.png)               | Sbalí strom výkaznictví.                                                                                                                                                           |
| [![Tlačítko Nápověda](./media/helpc130389.png)](./media/helpc130389.png)                           | Otevřete nápovědu.                                                                                                                                                                             |

### <a name="formatting-toolbar"></a>Panel nástrojů formátování

Panel nástrojů formátování nabízí snadný přístup k příkazům stylů. Tento panel nástrojů obsahuje následující tlačítka.

| Tlačítko                                                                                                                                                                                                   | Popis                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [![Tlačítko styl písma](./media/formattingc130389.png)](./media/formattingc130389.png)                         | Použije vybraný styl písma na aktuální text.      |
| [![Tlačítko písmo](./media/fonttype.png)](./media/fonttype.png)                                                 | Nastaví aktuální text na vybrané písmo.              |
| [![Tlačítko velikost písma](./media/fontsize.png)](./media/fontsize.png)                                            | Nastaví aktuální text na vybranou velikost písma (v bodech). |
| [![Tlačítko Tučné](./media/boldc130389.png)](./media/boldc130389.png)                                           | Nastaví tučné písmo pro aktuální text.                             |
| [![Tlačítko Kurzíva](./media/italicsc130389.png)](./media/italicsc130389.png)                                   | Nastaví kurzívu pro aktuální text.                           |
| [![Tlačítko podtržení](./media/underlinec130389.png)](./media/underlinec130389.png)                            | Nastaví podtržení pro aktuální text.                             |
| [![Tlačítko Zmenšit odsazení](./media/outdentlsc130389.png)](./media/outdentlsc130389.png)                      | Zmenší odsazení aktuálního textu.                |
| [![Vzhled tlačítka Zvětšit odsazení](./media/indentlsc130389.png)](./media/indentlsc130389.png)                        | Zvětší odsazení aktuálního textu.                |
| [![Tlačítko Barva pozadí](./media/fillbackgroundcolorc130389.png)](./media/fillbackgroundcolorc130389.png) | Změní barvu pozadí aktuální buňky.        |
| [![Tlačítko Barva písma](./media/fontcolorc130389.png)](./media/fontcolorc130389.png)                           | Změní barvu aktuálního textu.                   |

### <a name="report-designer-toolbar"></a>Panel nástrojů návrháře sestav

Panel nástrojů návrháře sestav poskytuje rychlý přístup k příkazům navigace v návrháři sestav. Tento panel nástrojů obsahuje následující tlačítka.

| Tlačítko                                                                                                                                                                                          | Popis                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [![Tlačítko definice sestavy](./media/reportc130389.png)](./media/reportc130389.png)                 | Zobrazí definici sestavy uvedenou v nabídce **Okno**.                                                                                                            |
| [![Tlačítko definice řádku](./media/rowc130389.png)](./media/rowc130389.png)                          | Zobrazí definici řádku, která je přiřazena k aktivní definici sestavy.                                                                                                    |
| [![Tlačítko definice sloupce](./media/columnc130389.png)](./media/columnc130389.png)                 | Zobrazí definici sloupce, která je přiřazena k aktivní definici sestavy.                                                                                                 |
| [![Přídavné tlačítko definice stromu](./media/treec130389.png)](./media/treec130389.png)             | Zobrazí definici stromu výkaznictví, která je přiřazena k aktivní definici sestavy.                                                                                         |
| [![Tlačítko prohlížeče sestav](./media/reportviewerc130389.png)](./media/reportviewerc130389.png)         | Spustí aplikaci Report Viewer a zobrazí nejnovější verzi vygenerované sestavy. Toto tlačítko je k dispozici z definice sestavy, pokud jste vygenerovali alespoň jednu sestavu. |
| [![Generovat sestavu](./media/generate-to-ddvc130389.png)](./media/generate-to-ddvc130389.png) | Vygeneruje sestavu z aktivní definice sestavy. Toto tlačítko je k dispozici z definice sestavy.                                                                      |



<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví pro aplikaci Microsoft Dynamics ERP](financial-reporting-intro.md)

[Generate a financial report](\financials\general-ledger\generate-financial-report.md)


