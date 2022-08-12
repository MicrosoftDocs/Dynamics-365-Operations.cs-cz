---
title: Uživatelské rozhraní ve stylu Microsoft Office v modulu Správa obchodních dokumentů (obsahuje video)
description: Tento článek obsahuje informace o tom, jak používat nové uživatelské rozhraní ve funkci správy obchodních dokumentů v rozhraní elektronického výkaznictví (ER).
author: v-anamir
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 208cfc91f11d4893785538ce4874e85a5725e993
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109253"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Uživatelské rozhraní ve stylu Microsoft Office v modulu Správa obchodních dokumentů

[!include [banner](../includes/banner.md)]

Správa obchodních dokumentů a umožňuje podnikovým uživatelům upravovat šablony obchodních dokumentů pomocí služby Microsoft Office 365 nebo příslušné desktopové aplikace Microsoft Office. Úpravy mohou zahrnovat změny návrhu nebo nová nasazení, nebo uživatelé mohou přidávat zástupné symboly, které budou zahrnovat další data, aniž by bylo nutné změnit zdrojový kód. Další informace o způsobu práce se správou obchodních dokumentů naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).

Nové uživatelské rozhraní pro dokumenty je jasnější a má pohodlnější používání. Oblast **Obchodní dokument** zobrazuje pouze šablony, které vlastní aktuální [aktivní](tasks/er-configuration-provider-mark-it-active-2016-11.md) [poskytovatel](general-electronic-reporting.md#Provider) a nachází se v aktuální instanci Dynamics 365 Finance. V předchozím uživatelském rozhraní karta **Šablona** obsahovala všechny šablony, které byly k dispozici libovolným poskytovatelům. Také se zobrazily všechny šablony, které vytvořil a upravil jakýkoli uživatel, který měl stejnou roli.

Můžete použít tlačítko **Nový dokument** v pracovním prostoru **Správa obchodních dokumentů** k vytvoření a úpravě šablony v [konfiguraci](general-electronic-reporting.md#Configuration) formátu [Elektronické vykazování (ER)](general-electronic-reporting.md), kterou poskytuje jiný poskytovatel a nachází se v aktuální instanci Finance, nebo k nahrání nové šablony z excelového sešitu. Navíc ve verzi 10.0.25 a novějších můžete použít tlačítko **Nový dokument** pro vytvoření a úpravu šablony v konfiguraci formátu ER, která je uložena v [Globálním úložišti](general-electronic-reporting.md#Repository).

V příkladech v tomto článku je aktivním poskytovatelem Contoso a můžete jej použít k vytvoření šablony založené na šabloně poskytované společností Microsoft. Alternativně můžete vytvořit šablonu nahráním vlastní šablony ve formátu Excel.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Video [Vytvoření nového obchodního dokumentu pomocí správy obchodních dokumentů](https://youtu.be/gAIYl-mM_pw) (zobrazeno výše) je zahrnuto v [seznamu skladeb finance a provoz](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), který je k dispozici na YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Zpřístupnění nového uživatelského rozhraní dokumentu v modulu Správa obchodních dokumentů

Chcete-li začít používat nové uživatelské rozhraní dokumentu v modulu správa obchodních dokumentů, je třeba zapnout funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu** v pracovním prostoru **správy funkcí**.

Chcete-li tuto funkci zapnout pro všechny právnické osoby, postupujte podle následujících kroků.

1. V pracovním prostoru **Správa funkcí** na kartě **Vše** vyberte v seznamu funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu**.
2. Výběrem možnosti **Povolit nyní** zapněte vybranou funkci.
3. K nové funkci budete mít přístup po aktualizaci stránky.

## <a name="add-or-activate-a-provider"></a>Přidání nebo aktivace poskytovatele

Každá šablona obchodního dokumentu je uložena v konfiguraci formátu ER, která je označena jako vlastněná konkrétním poskytovatelem konfigurace. Když vytvoříte novou šablonu, vytvoří se nová konfigurace formátu ER, která ji podrží. Proto musí být pro tuto konfiguraci určen poskytovatel. K tomuto účelu slouží aktivní poskytovatel ER frameworku. Pokud v ER není žádný poskytovatel, můžete si ho vytvořit. Pokud neexistuje *aktivní* poskytovatel, můžete aktivovat jednoho ze stávajících poskytovatelů. V případě potřeby se otevře dialog pro přidání nebo aktivaci poskytovatele, zatímco začnete přidávat novou šablonu.

### <a name="add-a-new-provider"></a>Přidat nového poskytovatele

Chcete-li vytvořit nového poskytovatele, postupujte podle postupu v dialogovém okně **Poskytovatel konfigurace**:

1.  Na kartě **Vybrat poskytovatele konfigurace** v poli **Název** zadejte název nového poskytovatele.
2.  V poli **Internetová adresa** zadejte internetovou adresu (URL) nového poskytovatele. 
3.  Vyberte **OK**.

    ![Vytvoření nového poskytovatele ve správě obchodních dokumentů.](./media/bdm_create_provider.png)

Přidaný poskytovatel bude automaticky aktivován.

### <a name="activate-a-provider"></a>Aktivace poskytovatele

Chcete-li aktivovat poskytovatele, postupujte podle postupu v dialogovém okně **Poskytovatel konfigurace**:

1.  Na kartě **Vybrat poskytovatele konfigurace** v poli **Poskytovatel konfigurace** vyberte poskytovatele.
2.  Vyberte **OK**.

    ![Aktivace poskytovatele ve správě obchodních dokumentů.](./media/bdm_choose_provider.png)

Vybraný poskytovatel bude aktivován.

> [!NOTE]
> Každá šablona správy obchodních dokumentů je umístěna v konfiguraci formátu ER, která označuje poskytovatele jako autora konfigurace. Proto je pro každou šablonu vyžadován aktivní poskytovatel.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Úprava šablony vlastněné jiným poskytovatelem

Tento příklad ukazuje, jak použít tlačítko **Nový dokument** v pracovním prostoru **Správa obchodních dokumentů** k vytvoření a úpravě šablony v konfiguraci formátu ER, kterou poskytuje jiný poskytovatel a nachází se v aktuální instanci Finance. V tomto příkladu je aktivním poskytovatelem Contoso, který používá konfiguraci formátu ER poskytovanou společností Microsoft. Poté, co vyberete **Nový dokument**, karta **Vybrat** na stránce **Vytvořit novou šablonu** zobrazuje všechny šablony aktuální instance Finance, které vlastní aktuální poskytovatel a další poskytovatelé. Výběrem šablony ji otevřete. Poté můžete vytvořit novou upravitelnou kopii šablony. Upravená šablona je uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.

1. V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.

    ![Pracovní prostor správy obchodních dokumentů.](./media/BDM_overview_new_template1.png)

2. Na stránce **Vytvořit novou šablonu** na kartě **Vybrat** vyberte dokument, který chcete použít jako šablonu, a poté vyberte **Vytvořit dokument**.

    ![Dialogové okno obchodních dokumentů.](./media/BDM_overview_new_template2.png)

3. V novém dialogovém okně v poli **Název** změňte požadovaným způsobem název. Text názvu se použije k pojmenování nové konfigurace formátu elektronického výkaznictví, která je automaticky vytvořena. Verze konceptu této konfigurace **(Kopie sestavy FTI odběratele (GER)**) bude obsahovat upravenou šablonu a bude automaticky označena pro spuštění tohoto formátu elektronického výkaznictví pro aktuálního uživatele. Původní šablona ze základní konfigurace formátu elektronického výkaznictví bude použita ke spuštění tohoto formátu elektronického výkaznictví pro každého jiného uživatele.
4. V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.
5. V poli **Komentář** aktualizujte poznámky pro revizi upravitelné šablony, která bude automaticky vytvořena.
6. Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.

    ![Dialogové okno vytvoření dokumentu.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Nahrajte šablonu, která používá existující sešit Excel

Tento příklad ukazuje, jak použít tlačítko **Nový dokument** v pracovním prostoru **Správa obchodních dokumentů** k vytvoření a úpravě šablony v konfiguraci formátu ER na základě dostupného sešitu Excel. V tomto příkladu je aktivním poskytovatelem Contoso a vy používáte konfigurace [datového modelu](er-overview-components.md#data-model-component) ER a [mapování modelu](er-overview-components.md#model-mapping-component) ER poskytované společností Microsoft. Poté, co vyberete **Nový dokument**, vyberte kartu **Nahrát** na stránce **Vytvořit novou šablonu**. Zde můžete zadat podrobnosti o nahrání sešitu aplikace Excel. Po nahrání sešitu aplikace Excel se sešit transformuje na šablonu obchodního dokumentu, která se otevře pro úpravy. Upravená šablona bude uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.

Před odesláním šablony postupujte podle těchto pokynů a poskytněte požadované informace.

1. V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.
2. Na stránce **Vytvořit novou šablonu** na kartě **Nahrát** na kartě **Šablona** vyberte možnost **Procházet** k vyhledání a výběru souboru Excel, který chcete použít jako šablonu. V části **Šablona** se pole **Název** a **Popis** vyplňují automaticky. Určují název a popis nové konfigurace formátu ER, která se automaticky vytvoří. V případě potřeby můžete tato pole upravit.
3. V části **Typ dokumentu** do pole **Název** zadejte typ obchodního dokumentu. Tato hodnota se použije k vyhledání správného zdroje dat (tj. konfigurace modelu ER).

    ![Karta Šablona na kartě Nahrát na stránce Vytvořit novou šablonu.](./media/BDM_overview_new_UI_import_21.jpg)

4. Na kartě **Zdroj dat** na rychlé kartě **Filtr** vyberte **Použít filtr**. V části **Zdroj dat** je pole **Název** vyplněno automaticky nebo můžete hodnotu vybrat ručně. Pomocí filtru můžete vyhledat název příslušného zdroje dat podle názvu, popisu, kódu země/oblasti a typu obchodního dokumentu.

    ![Karta Zdroj dat na kartě Nahrát na stránce Vytvořit novou šablonu.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Karta **Filtr** se používá k vyhledání správného zdroje dat (tj. konfigurace modelu ER). Můžete upravit všechna pole filtru a vyhledat nejvhodnější zdroj dat pro dokument, který nahráváte.
    > 
    > Podmínky na kartě **Filtr** se používají jako podmínky **OR**.

5. Na kartě **Mapování** vyberte **Automaticky zjistit**. Pole **Definice kořene** je vyplněno automaticky nebo můžete hodnotu vybrat ručně. Tato karta zobrazuje mapování konce pro prvky ze šablony a modelu.

    ![Karta Mapování na kartě Nahrát na stránce Vytvořit novou šablonu.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Mapování v části **Struktura šablony** používá úplnou shodu štítků nebo popisů ve zdroji dat v jazyce uživatele a v názvu buňky v šabloně.

6. Vyberte **Vytvořit dokument** k potvrzení, že chcete vytvořit šablonu a zahájit proces úprav.

Další informace naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Nahrání šablony z globálního úložiště

Tento příklad ukazuje, jak použít tlačítko **Nový dokument** v pracovním prostoru **Správa obchodních dokumentů** k vytvoření a úpravě šablony v konfiguraci formátu ER, kterou poskytuje Microsoft a je umístěna v globálním úložišti. V tomto příkladu je aktivním poskytovatelem Contoso, který používá konfiguraci formátu ER poskytovanou společností Microsoft. Poté, co vyberete **Nový dokument**, karta **Import z globálního úložiště** na stránce **Vytvořit novou šablonu** zobrazuje všechny šablony obchodních dokumentů, které jsou uloženy v globálním úložišti, ale chybí v aktuální instanci Finance. Jakmile vyberete šablonu, bude importována z globálního úložiště do aktuální instance Finance, aby se vytvořila nová upravitelná kopie. Upravená šablona je uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.

1. V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.
2. Na stránce **Vytvořit novou šablonu** na kartě **Importovat z globálního úložiště** vyberte dokument, který chcete použít jako šablonu, a poté vyberte **Vytvořit dokument**.

    ![Import z globálního úložiště na stránce Vytvořit novou šablonu.](./media/BDM_overview_new_template22.png)

3. V okně zprávy vyberte **Ano** a potvrďte, že chcete importovat vybraný dokument z globálního úložiště do aktuální instance Finance. Pokud se zobrazí výzva k autorizaci, postupujte podle pokynů na obrazovce.
4. V novém dialogovém okně v poli **Název** změňte požadovaným způsobem název. Text názvu se použije k pojmenování nové konfigurace formátu elektronického výkaznictví, která je automaticky vytvořena. Verze konceptu této konfigurace(**Kopie upomínky inkasa (Excel)**) bude obsahovat upravenou šablonu a bude automaticky označena pro spuštění tohoto formátu elektronického výkaznictví pro aktuálního uživatele. Původní šablona ze základní konfigurace formátu elektronického výkaznictví bude použita ke spuštění tohoto formátu elektronického výkaznictví pro každého jiného uživatele.
5. V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.
6. V poli **Komentář** aktualizujte poznámky pro revizi upravitelné šablony, která bude automaticky vytvořena.
7. Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

