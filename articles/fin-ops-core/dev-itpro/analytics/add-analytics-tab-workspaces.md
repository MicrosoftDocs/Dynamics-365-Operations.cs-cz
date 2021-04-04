---
title: Přidání analýz do pracovního prostoru pomocí Power BI Embedded
description: Toto téma popisuje, jak vložit sestavu Power BI na kartě Analýzy v pracovním prostoru.
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4e757ce585b16b23d65506068dcc337211107199
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568483"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Přidání analýz do pracovního prostoru pomocí Power BI Embedded

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tato funkce je podporována v Finance and Operations (verze 7.2 a novější).

## <a name="introduction"></a>Úvod
Toto téma popisuje, jak vložit sestavu Microsoft Power BI na kartě **Analýzy** v pracovním prostoru. V uvedeném příkladu rozšíříme pracovní prostor **Správa rezervací** v aplikaci Správa vozového parku na kartě **Analýzy** tak, aby zahrnovala analytický pracovní prostor.

## <a name="prerequisites"></a>Požadavky
+ Přístup k prostředí pro vývojáře, kde běží aktualizace Platform 8 nebo vyšší.
+ Analytická sestava (soubor .pbix) vytvořená pomocí Microsoft Power BI Desktop, která obsahuje datový model, jehož zdrojem je databáze úložiště Entity.

## <a name="overview"></a>Přehled
Ať rozšíříte existující pracovní prostor aplikace nebo zadáte nový pracovní prostor, můžete použít vložené analytické zobrazení ke kvalifikovaným a interaktivním zobrazením vašich obchodních údajích. Proces přidání karty analytického pracovního prostoru má čtyři kroky.

1. Přidejte soubor .pbix jako prostředek Dynamics 365.
2. Definujte kartu analytického pracovního prostoru.
3. Vložte prostředek .pbix prostředků na kartu pracovní prostor.
4. Volitelné: Přidejte rozšíření pro přizpůsobení zobrazení.

> [!NOTE]
> Další informace o postupu vytváření analytických sestav naleznete v tématu [Začínáme s Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/). Tato stránka je skvělý zdroj informací, které pomáhají vytvořit přinutit řešení generování analytických sestav.

## <a name="add-a-pbix-file-as-a-resource"></a>Přidejte soubor .pbix jako prostředek
Dříve než začnete, musíte vytvořit nebo získat sestavu Power BI, kterou vložíte do pracovního prostoru. Další informace o postupu vytváření analytických sestav naleznete v tématu [Začínáme s Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).

Tento postup slouží k přidání souboru .pbix jako artefaktů projektu Visual Studio.

1. Vytvořte nový projekt v příslušném modelu.
2. V Průzkumníku řešení vyberte projekt, klepněte pravým tlačítkem myši a poté vyberte **Přidat** \> **Nová položka**.
3. V dialogovém okně **Přidat novou položku**, v části **Operační artefakty**, vyberte šablonu **Prostředek**.
4. Zadejte název, který se použije k odkazování na sestavu v metadatech X ++ a klepněte na tlačítko **přidat**.

    ![Dialogové okno Přidat novou položku](media/analytical-workspace-add.png)

5. Najděte soubor .pbix, který obsahuje definici analytické sestavy, a klepněte na tlačítko **Otevřít**.

    ![Dialogové okno Vybrat soubor zdrojů](media/analytical-workspace-select-resource.png)

Poté, co jako prostředek Dynamics 365 nepřidáte .pbix soubor, můžete vložit sestavy pracovní prostory a přidat přímé odkazy pomocí položky nabídky.

## <a name="add-a-tab-control-to-an-application-workspace"></a>Přidat ovládací prvek karty s pracovním prostorem aplikace
V tomto příkladu doporučujeme rozšířit pracovní prostor **řízení rezervací** v modelu Správa vozového parku přidáním karty **Analýzy** kartu pro definici formuláře **FMClerkWorkspace**.

Následující obrázek znázorňuje, jak formulář **FMClerkWorkspace** vypadá v Návrháři v aplikaci Microsoft Visual Studio.

![Formulář FMClerkWorkspace před změnami](media/analytical-workspace-definition-before.png)

Pomocí následujícího postupu rozšířit definici formuláře pracovního prostoru **Řízení rezervací**.

1. Otevřete návrhář formuláře k rozšíření definice návrhu.
2. V definici návrhu vyberte nejvyšší prvek označený **Návrhu | Vzor: Pracovní prostor operační**.
3. Klepněte pravým tlačítkem myši a poté vyberte **Nová** \> **Karta** pro přidání nového ovládacího prvku s názvem **FormTabControl1**.
4. V návrháři formuláře vyberte **FormTabControl1**.
5. Klepněte pravým tlačítkem myši a poté vyberte **Stránka Nová karta**. Tím přidáte novou kartu.
6. Přejmenujte stránku karty, například na **Pracovní prostor**.
7. V návrháři formuláře vyberte **FormTabControl1**.
8. Klikněte pravým tlačítkem myši a poté vyberte **Stránka Nová karta**.
9. Přejmenujte stránku karty, například na **Analýza**.
10. V návrháři formuláře vyberte **Analýz (Stránka Karta)**.
11. Nastavte vlastnost **Titulky** na možnost **Analýza** a nastavte vlastnost **Auto deklarace** na hodnotu **Ano**.
12. Klepněte pravým tlačítkem myši na ovládací prvek a poté vyberte **Nová** \> **Skupina** pro přidání nové skupiny ovládacích prvků.
13. Přejmenujte skupinu formuláře, například na **powerBIReportGroup**.
14. V návrháři formuláře vyberte **PanoramaBody (karta)** a přetáhněte ovládací prvek na kartu **Pracovní prostor**.
15. V definici návrhu vyberte nejvyšší prvek označený **Návrhu | Vzor: Pracovní prostor operační**.
16. Klikněte pravým tlačítkem a vyberte **Odebrat vzor**.
17. Znovu klikněte pravým tlačítkem a vyberte **Přidat vzor** \> **Pracovní prostor s kartami**.
18. Vytvořit nové sestavení pro ověření provedených změn.

Následující obrázek znázorňuje, jak návrh vypadá poté, co tyto změny se projeví.

![FMClerkWorkspace po provedení změn](media/analytical-workspace-definition-after.png)

Poté, co jste přidali ovládací prvky formuláře, které budou použity pro sestavu pracovního prostoru, je nutné definovat velikost nadřazenému ovládacímu prvku tak, aby se přizpůsobilo rozvržení. Ve výchozím bude v sestavě viditelná stránka **Podokno Filtry** a **Karta**. Můžete však změnit viditelnost zobrazení těchto ovládacích prvků v závislosti na příjemci cílové sestavy.

> [!NOTE]
> Pro vložené pracovní prostory doporučujeme použití rozšíření ke skrytí stránky **Podokno Filtry** i **Karta**.

Nyní jste dokončili úlohu rozšíření definice formuláře aplikace. Další informace o tom, jak používáte rozšíření přizpůsobení naleznete v tématu [Přizpůsobení pomocí rozšíření a překrývání vrstev](../extensibility/customization-overlayering-extensions.md).

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>Přidání obchodní logiky X ++ pro vložení ovládacího prvku prohlížeče
Pomocí těchto kroků přidejte obchodní logiku, která inicializuje ovládací prvek prohlížeče sestav, který je vložen do pracovního prostoru **řízení rezervací**.

1. Otevřete návrhář formuláře **FMClerkWorkspace** k rozšíření definice návrhu.
2. Stisknutím klávesy F7 přejděte ke kódu za definicí kódu.
3. Přidejte následující kód X++:

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Vytvořit nové sestavení pro ověření provedených změn.

Nyní jste dokončili úkol přidání obchodní logiky v ovládacím prvku prohlížeče sestavy. Následující obrázek znázorňuje, jak pracovní prostor vypadá poté, co se tyto změny projeví.

![Sestava vložená do pracovního prostoru](media/analytical-workspace-final.png)

> [!NOTE]
> Můžete zobrazit stávající operační zobrazení pomocí záložek pracovního prostor pod nadpisem stránky.

## <a name="reference"></a>Odkaz

### <a name="pbireporthelperinitializereportcontrol-method"></a>Metoda PBIReportHelper.initializeReportControl
Tento oddíl obsahuje informace o pomocnících třídy, která se používá k vložení do ovládacího prvku skupiny sestavy Power BI (zdroj .pbix).

#### <a name="syntax"></a>Syntaxe
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>Parametry

| Jméno             | popis                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| resourceName     | Název zdroje .pbix                                                                               |
| formGroupControl | Ovládací prvek skupiny formuláře pro použití sestavy Power BI.                                              |
| defaultPageName  | Výchozí název stránky.                                                                                       |
| showFilterPane   | Logická hodnota, která určuje, zda má být podokno filtru zobrazené (**true**) nebo skryté (**false**).     |
| showNavPane      | Logická hodnota, která určuje, zda má být navigační podokno zobrazené (**true**) nebo skryté (**false**). |
| defaultFilters   | Výchozí filtry pro sestavu Power BI.                                                                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]