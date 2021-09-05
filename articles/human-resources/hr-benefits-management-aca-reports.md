---
title: Vytvářejte ve správě zaměstnaneckých výhod sestavy v rámci zákona Affordable Care Act
description: Toto téma popisuje, jak správa zaměstnaneckých výhod sleduje informace, které jsou hlášeny formuláři 1095-B a formuláři 1095-C pro mandát zaměstnavatele podle zákona Affordable Care Act (ACA).
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 99ac67795cd3f587e54a84361dd4744b79b4dbbd
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416247"
---
# <a name="generate-aca-reports-in-benefits-management"></a>Generujte zprávy ACA ve Správě zaměstnaneckých výhod

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Správa zaměstnaneckých výhod sleduje informace, které jsou hlášeny formuláři 1095-B a formuláři 1095-C pro mandát zaměstnavatele podle zákona Affordable Care Act (ACA). Stejně jako možnost ACA hlášení v minulosti v pracovním prostoru **zaměstnanecké výhody**, tato funkce se vztahuje pouze na právnické osoby ve Spojených státech.

Abyste mohli tuto funkci používat, musíte nejprve zapnout **Pokročilou správu zaměstnaneckých výhod**. Další informace, včetně důležitých upozornění na správu zaměstnaneckých výhod, viz [Povolení nebo zákaz správy zaměstnaneckých výhod](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> Sestavení ACA můžete použít pouze buď z pracovního prostoru **správa zaměstnaneckých výhod**, nebo staršího prostoru **zaměstnanecké výhody**, ne z obou. Například pokud jste přešli na správu zaměstnaneckých výhod, hlášení ACA je k dispozici pouze z prostoru **správa zaměstnaneckých výhod**, ne ze starého pracovního prostoru **zaměstnanecké výhody**.
>
> Pokud přepnete na správu zaměstnaneckých výhod uprostřed roku registrace, musíte správně nakonfigurovat data zaměstnanců pro celý rok ve správě výhod. Tímto způsobem zajistíte, že budete dostávat přesné informace o sestavách za celý rok.

## <a name="getting-started"></a>Začínáme

Chcete-li sledovat informace proformuláře 1095, nejprve vytvořte jednu nebo více skupin Affordable Care. Tyto skupiny označují následující informace:

- Nabídka krytí, která byla poskytnuta zaměstnanci
- Podíl zaměstnance na nejnižší měsíční prémii, pokud je cena nad federální hranicí chudoby
- Případně program Safe Harbor, který využívá zaměstnavatel

Skupiny pokrytí Affordable Care vám pomohou spravovat tyto informace pro více záznamů zaměstnanců, které mají stejné podmínky. Skupiny můžete snadno přiřadit jednomu nebo více zaměstnancům.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Vytvořte nebo upravte skupinu pokrytí Affordable Care

1. V pracovním prostoru **správa zaměstnaneckých výhod** vyberte **Skupina pokrytí Affordable Care**.

    ![Výběr skupiny pokrytí Affordable Care.](./media/hr-benefits-management-aca-coverage-group.png)

2. Vyberte **Nová** k vytvoření nové skupiny pokrytí Affordable Care nebo **Upravit** ke změně existující skupiny.

    ![Vyberte Nová nebo Upravit.](./media/hr-benefits-management-aca-new.png)

3. Nastavte následující pole.

    | Pole | popis |
    |---|---|
    | Jméno | Zadejte název skupiny. |
    | popis | Zadejte popis skupiny. |
    | Nabídka pokrytí | Krytí, které je nabízeno zaměstnancům, jejich manželům nebo partnerům a jejich závislým osobám. |
    | Podíl zaměstnance na nákladech | Množství, za které je zaměstnanec zodpovědný. |
    | Použitelná sekce 4980H Safe Harbor | Kód Safe Harbor 4980H nebo kód transition relief. |
    | Měsíc začátku plánu | Vyberte kalendářní měsíc, kdy začíná rok vašeho plánu dávek. |
    | Skupina platná od | První datum, kdy je tento záznam platný. |
    | Skupina platná do | Poslední datum, kdy je tento záznam platný. Pokud není datum vypršení platnosti, zadejte **Nikdy**. |

    ![Vytvoření skupiny disponibility.](./media/hr-benefits-management-aca-new-group.png)

4. Zvolte možnost **Uložit**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Přiřaďte více zaměstnanců do skupiny pokrytí Affordable Care

1. V pracovním prostoru **správa zaměstnaneckých výhod** vyberte **Skupina pokrytí Affordable Care**.
2. Vyberte skupinu, ke které chcete přiřadit zaměstnance.
3. Vyberte **Hromadné přiřazení**.

    ![Vyberte Hromadné přiřazení.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Vyberte zaměstnance v seznamu a poté vyberte **Přiřadit**.

    ![Přiřaďte vybrané zaměstnance ke skupině.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Správa několika verzí možností pokrytí

Můžete spravovat několik verzí skupin pokrytí. Když se ve vaší organizaci nebo ve výhodách, které nabízí, něco změní, můžete udržovat aktuální informace o skupině, aniž byste museli vytvářet novou skupinu a přiřazovat k ní zaměstnance.

Poté, co jste vytvořili skupiny pokrytí Affordable Care, můžete jim hromadně přiřadit zaměstnance. Můžete také jednotlivě přiřadit zaměstnance ke skupinám a určit, zda jsou sledovány a hlášeny informace ACA.

Pokud pro zaměstnance nemusíte sledovat a hlásit informace ACA, můžete nastavit **Zpráva o pokrytí** možnost **Ne**. Můžete mít například zaměstnance na částečný úvazek, kteří nevyžadují hlášení ACA.

### <a name="override-default-values-for-an-employee"></a>Přepsat výchozí hodnoty pro zaměstnance

U zaměstnanců, kteří jsou přiřazeni do skupiny pokrytí Affordable Care, můžete změnit následující možnosti pro měsíce, které vyžadují různé hodnoty:

- Nabídka pokrytí
- Podíl zaměstnance na nákladech
- Použitelná sekce 4980H Safe Harbor

> [!NOTE]
> U zpráv ACA 2020 musíte na formuláři 1095-C hlásit pracovní i domácí PSČ. Hodnoty se vyplňují automaticky na základě aktuálních aktivních míst. Pokud bylo kterékoli místo v kterékoli části roku jiné, musíte přepsat hodnotu. Pole **PSČ** (řádek 17) sestavy 1095-C se vyplní pouze pokud kód **Nabídka krytí** obsahuje od **1L** po **1Q** následovně:
>
> - **1L, 1M nebo 1N:** PSČ primární rezidence
> - **1O, 1P, 1Q:** Primární PSČ práce

Chcete-li zadat výjimky pro jakékoli hodnoty skupiny pokrytí Affordable Care, postupujte takto.

1. Ve **Správa zaměstnanců** pracovním prostoru vyberte **Odkazy** a poté vyberte **Pracovníci**.
2. V seznamu vyberte zaměstnance.
3. Na kartě **Zaměstnání** v sekci **Více informací** vyberte **Pokrytí Affordable Care**.

    ![Změna možností pro jednoho zaměstnance.](./media/hr-benefits-management-aca-change-single-employee.png)

4. Vyberte možnost **Upravit**.
5. U každého měsíce, který vyžaduje změny, zaškrtněte políčko **Přepsat výchozí** a poté podle potřeby změňte ostatní hodnoty.

    ![Přepsat výchozí hodnoty.](./media/hr-benefits-management-aca-override-default.png)

6. Zvolte možnost **Uložit**.

## <a name="report-health-care-coverage"></a>Vykazování pokrytí zdravotní péče

Musíte sledovat jakékoli pojištění zdravotní péče sponzorované zaměstnavatelem a pojištěné u zaměstnanců na plný i částečný úvazek. Zahrňte každého zaměstnance společně s jeho závislými osobami do zprávy 1095-C za měsíce, kdy byli pojištěni.

Chcete-li určit, zda je třeba nahlásit plán výhod, postupujte podle těchto kroků.

1. V pracovním prostoru **Správa zaměstnaneckých** výhod vyberte možnost **plány zaměstnaneckých výhod**.
2. Vyberte plán výhod, který chcete nahlásit.
3. Vyberte možnost **Upravit**.
4. Nastavte možnost **Hlášeno podle zákona Affordable Care** na **Ano**.

    ![Vykazování pokrytí zdravotní péče.](./media/hr-benefits-management-aca-report-coverage.png)

5. Zvolte možnost **Uložit**.

Pokud si zaměstnanec zvolí krytí zdravotní péče pro závislou osobu, doba jejího krytí se určí podle data, kdy byla závislá osoba zapsána nebo odstraněna. Data pokrytí závislých osob se automaticky počítají na základě období, kdy závislá osoba byla způsobilá a aktivní v plánu během roku registrace.

## <a name="generate-1095-b-and-1095-c-forms"></a>Generujte formuláře 1095-B a 1095-C

ACA formuláře 1095-B and 1095-C můžete vygenerovat a poté rozeslat všem zaměstnancům. Můžete také elektronicky vygenerovat formulář 1095-C a odpovídající přenosové soubory 1094-C a odeslat je do Internal Revenue Service (IRS).

1. V pracovním prostoru **správa zaměstnaneckých výhod** vyberte **Formulář ACA 1095-B** nebo **Formulář ACA 1095-C**.
2. Podle potřeby změňte parametry a poté vyberte **OK**.

    > [!NOTE]
    > Při tisku formulářů 1095-C pro více než 500 zaměstnanců obdržíte více než jeden soubor PDF. Doporučujeme zvýšit hodnotu pole **Maximální velikost souboru v megabajtech** na stránce **Parametry správy dokumentů** na **150**. (Chcete-li tuto stránku rychle otevřít, použijte vyhledávací pole na navigační liště.)
    >
    > ![Změna maximální velikosti souboru.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Chcete-li zkontrolovat stav svých přehledů a zobrazit je, otevřete vyhledávací pole na navigačním panelu stránky **Úlohy elektronického hlášení**.

    ![Hledání stránky úloh elektronického výkaznictví.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Vyberte sestavu, kterou chcete zobrazit, a poté vyberte **Zobrazit soubory**.

    ![Zobrazují se soubory.](./media/hr-benefits-management-aca-show-files.png)

5. Zvolte **Otevřít**.

    ![Otevření souboru.](./media/hr-benefits-management-aca-open-file.png)

6. Na oznamovací liště, která se zobrazí v dolní části okna prohlížeče, otevřete soubor zip a poté vyberte sestavu. Můžete zobrazit nebo vytisknout soubor PDF.

    ![Ukázkový formulář 1095-C.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>Zobrazit informace o pokrytí ACA

Stránka **Pokrytí Worker Affordable Care** zobrazuje následující informace:

- Zaměstnanci, kteří jsou přiřazeni ke každé skupině pokrytí
- Zaměstnanci, kteří nemusí být zahrnuti do zprávy
- Nepřiřazení zaměstnanci

Chcete-li tuto informaci zobrazit, postupujte takto.

1. V pracovním prostoru **správa zaměstnaneckých výhod** vyberte **Skupina pokrytí Worker Affordable Care**.
2. V poli **Název skupiny** vyberte skupinu.

    ![Prohlížení pokrytí ACA.](./media/hr-benefits-management-aca-view-coverage.png)

U případných přepsaných výchozích hodnot skupiny pokrytí ACA se vedle změněné hodnoty zobrazí hvězdička. Pokud jsou hodnoty u všech 12 měsíců stejné a nebyly přepsány, hodnota bude uvedena ve sloupci **Všech 12 měsíců**.

Můžete si prohlédnout zaměstnance, kteří jsou označeni jako nezodpovědní ACA a kteří nebudou vyžadovat formulář 1095-C. V poli **Filtrovat podle** vyberte **Není třeba hlásit ACA**.

Můžete zobrazit zaměstnance, kteří nejsou přiřazeni ke skupině nebo kterým je přiřazena skupina, jejíž platnost vypršela. V poli **Filtrovat podle** vyberte **Nepřiřazená nebo vypršela skupina**.

### <a name="export-to-excel"></a>Export do aplikace Excel

Chcete-li exportovat některý ze seznamů Microsoft Excel, postupujte takto.

1. Vyberte tlačítko **Otevřít Microsoft Office**.
2. Vyberte **Dočasná tabulka lidských zdrojů HCM pro interní použití**.
3. Vyberte **Stáhnout**.

### <a name="view-aca-reportable-dependents"></a>Zobrazit závislé osoby závislé na ACA

Pokud musíte hlásit kryté osoby, protože poskytujete pojištěné osoby, můžete zobrazit závislé osoby, na které se vztahují plány dávek, které jsou označeny jako **hlásitelné ACA**. V podokně akcí vyberte **Zobrazit data pokrytí rodinného příslušníka**.

![Zobrazení pokrytí rodinného příslušníka.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Zobrazí se informace o pokrytí závislých osob zaměstnance.

![Pokrytí závislých prvků.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Tato stránka zobrazuje pouze plány výhod, které jsou označeny jako **hlásitelné ACA**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
