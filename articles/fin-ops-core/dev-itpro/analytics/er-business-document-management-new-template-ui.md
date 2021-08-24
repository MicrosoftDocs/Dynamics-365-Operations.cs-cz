---
title: Uživatelské rozhraní ve stylu Microsoft Office v modulu Správa obchodních dokumentů
description: Toto téma obsahuje informace o tom, jak používat nové uživatelské rozhraní ve funkci správy obchodních dokumentů v rozhraní elektronického výkaznictví (ER).
author: v-anamir
ms.date: 04/12/2021
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
ms.openlocfilehash: 4d4c256b2384f14fd8439c4a9263860f504113de369142d0913a2538f1f0939f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737944"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Uživatelské rozhraní ve stylu Microsoft Office v modulu Správa obchodních dokumentů

[!include [banner](../includes/banner.md)]

Správa obchodních dokumentů a umožňuje podnikovým uživatelům upravovat šablony obchodních dokumentů pomocí služby Microsoft 365 nebo příslušné desktopové aplikace Microsoft Office. Úpravy mohou zahrnovat změny návrhu nebo nová nasazení, nebo uživatelé mohou přidávat zástupné symboly, které budou zahrnovat další data, aniž by bylo nutné změnit zdrojový kód. Další informace o způsobu práce se správou obchodních dokumentů naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).

Nové uživatelské rozhraní pro dokumenty je jasnější a má pohodlnější používání. V oblasti **obchodního dokumentu** jsou zobrazeny pouze ty šablony, které jsou k dispozici pro aktuálního poskytovatele. V předchozím uživatelském rozhraní karta **Šablona** obsahovala všechny šablony, které byly k dispozici libovolným poskytovatelům. Také se zobrazily všechny šablony, které vytvořil a upravil jakýkoli uživatel, který měl stejnou roli.

Tlačítko **Nový dokument** můžete použít k vytváření a úpravě šablony v konfiguraci formátu elektronického výkaznictví, kterou poskytuje jiný poskytovatel. V příkladu v tomto tématu je poskytovatelem Microsoft. Alternativně můžete vytvořit šablonu nahráním vlastní šablony ve formátu Excel.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

Video [Vytvoření nového obchodního dokumentu pomocí správy obchodních dokumentů](https://youtu.be/gAIYl-mM_pw) (zobrazeno výše) je zahrnuto v souboru[seznamu skladeb Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), který je k dispozici na YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Zpřístupnění nového uživatelského rozhraní dokumentu v modulu Správa obchodních dokumentů

Chcete-li začít používat nové uživatelské rozhraní dokumentu v modulu správa obchodních dokumentů, je třeba zapnout funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu** v pracovním prostoru **správy funkcí**.

Chcete-li tuto funkci zapnout pro všechny právnické osoby, postupujte podle následujících kroků.

1. V pracovním prostoru **Správa funkcí** na kartě **Vše** vyberte v seznamu funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu**.
2. Výběrem možnosti **Povolit nyní** zapněte vybranou funkci.
3. K nové funkci budete mít přístup po aktualizaci stránky.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Úprava šablon vlastněných ostatními poskytovateli

1. V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.

    ![Pracovní prostor správy obchodních dokumentů.](./media/BDM_overview_new_template1.png)

2. Na kartě **Vybrat** vyberte dokument, který chcete použít jako šablonu, a poté vyberte možnost **Vytvořit dokument**.

    ![Dialogové okno obchodních dokumentů.](./media/BDM_overview_new_template2.png)

3. V novém dialogovém okně v poli **Název** změňte požadovaným způsobem název. Text názvu se použije k pojmenování nové konfigurace formátu elektronického výkaznictví, která je automaticky vytvořena. Verze konceptu této konfigurace **(Kopie sestavy FTI odběratele (GER)**) bude obsahovat upravenou šablonu a bude automaticky označena pro spuštění tohoto formátu elektronického výkaznictví pro aktuálního uživatele. Původní šablona ze základní konfigurace formátu elektronického výkaznictví bude použita ke spuštění tohoto formátu elektronického výkaznictví pro každého jiného uživatele.
4. V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.
5. V poli **Komentář** aktualizujte poznámky pro revizi upravitelné šablony, která bude automaticky vytvořena.
6. Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.

    ![Dialogové okno vytvoření dokumentu.](./media/BDM_overview_new_template3.png)

Tlačítko **Nový dokument** se používá pro vytváření úpravy šablony v konfiguraci formátu elektronického výkaznictví, kterou poskytuje jiný poskytovatel. V tomto příkladu je poskytovatelem Microsoft. Když vyberete **Nový dokument**, zobrazí se všechny šablony vlastněné aktuálními a jinými poskytovateli. Po výběru bude šablona otevřena pro úpravy. Upravená šablona bude poté uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Nahrajte šablonu, která používá existující formát aplikace Excel
Před odesláním šablony postupujte podle těchto pokynů a poskytněte požadované informace.

1. V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.

    ![Pracovní prostor správy obchodních dokumentů.](./media/BDM_overview_new_template1.png)
    
2. Na stránce **Vytvořit novou šablonu** na kartě **Nahrát** na kartě **Šablona** vyberte možnost **Procházet** k vyhledání a výběru souboru Excel, který chcete použít jako šablonu. V části **Šablona** se pole **Název** a **Popis** vyplňují automaticky. Určují název a popis nové konfigurace formátu ER, která se automaticky vytvoří. V případě potřeby můžete tato pole upravit.
3. V části **Typ dokumentu** do pole **Název** zadejte typ obchodního dokumentu. Tato hodnota se použije k vyhledání správného zdroje dat (tj. konfigurace modelu ER).

    ![Karta Šablona.](./media/BDM_overview_new_UI_import_21.jpg)

4. Na kartě **Zdroj dat** na rychlé kartě **Filtr** vyberte **Použít filtr**. V části **Zdroj dat** je pole **Název** vyplněno automaticky nebo můžete hodnotu vybrat ručně. Pomocí filtru můžete vyhledat název příslušného zdroje dat podle názvu, popisu, kódu země/oblasti a typu obchodního dokumentu.

    ![Karta zdroje dat.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > Karta **Filtr** se používá k vyhledání správného zdroje dat (tj. konfigurace modelu ER). Můžete upravit všechna pole filtru a vyhledat nejvhodnější zdroj dat pro dokument, který nahráváte.
    > 
    > Podmínky na kartě **Filtr** se používají jako podmínky **OR**.
    
5. Na kartě **Mapování** vyberte **Automaticky zjistit**. Pole **Definice kořene** je vyplněno automaticky nebo můžete hodnotu vybrat ručně. Tato karta zobrazuje mapování konce pro prvky ze šablony a modelu.

    ![Karta Mapování.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Mapování v části **Struktura šablony** používá úplnou shodu štítků nebo popisů ve zdroji dat v jazyce uživatele a v názvu buňky v šabloně.

6. Vyberte **Vytvořit dokument** k potvrzení, že chcete vytvořit šablonu a zahájit proces úprav.

Další informace naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).

Pokud v elektronickém vykazování není poskytovatel, můžete ho vytvořit. Pokud neexistuje žádný aktivní poskytovatel, můžete jej aktivovat.

- Chcete-li vytvořit poskytovatele, změňte název poskytovatele v poli **Název**, aktualizujte internetovou adresu nového poskytovatele v poli **Internetová adresa** a vyberte **OK** k potvrzení.

    ![Vytvoření nového poskytovatele v BDM.](./media/bdm_create_provider.png)
    
- Chcete-li aktivovat stávajícího poskytovatele, vyberte jeho jméno v poli **Poskytovatel konfigurace** a vyberte **OK** k nastavení poskytovatele jako aktivního.

    ![Aktivace poskytovatele v BDM.](./media/bdm_choose_provider.png)

> [!NOTE]
> Každá šablona BDM bude odkazovat na zprostředkovatele jako na autora konfigurace. Proto je pro šablonu vyžadován aktivní poskytovatel.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
