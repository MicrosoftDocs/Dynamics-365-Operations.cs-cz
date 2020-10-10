---
title: Nové uživatelské rozhraní dokumentu v modulu Správa obchodních dokumentů
description: Toto téma obsahuje informace o tom, jak používat nové uživatelské rozhraní dokumentu (UI) ve funkci správy obchodních dokumentů rámce elektronického výkaznictví.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 015b595f85397fc1cf2c0368814ddc0369176f82
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893188"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Nové uživatelské rozhraní dokumentu v modulu Správa obchodních dokumentů

[!include [banner](../includes/banner.md)]

Správa obchodních dokumentů a umožňuje podnikovým uživatelům upravovat šablony obchodních dokumentů pomocí služby Microsoft 365 nebo příslušné desktopové aplikace Microsoft Office. Úpravy mohou zahrnovat změny návrhu nebo nová nasazení, nebo uživatelé mohou přidávat zástupné symboly, které budou zahrnovat další data, aniž by bylo nutné změnit zdrojový kód. Další informace o způsobu práce se správou obchodních dokumentů naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).

Nové uživatelské rozhraní pro dokumenty je jasnější a má pohodlnější používání. V oblasti **obchodního dokumentu** jsou zobrazeny pouze ty šablony, které jsou k dispozici pro aktuálního poskytovatele.

Tlačítko **Nový dokument** umožňuje uživatelům vytvářet a upravovat šablonu v konfiguraci formátu elektronického výkaznictví, kterou poskytuje jiný poskytovatel. V příkladu v tomto tématu je poskytovatelem Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Zpřístupnění nového uživatelského rozhraní dokumentu v modulu Správa obchodních dokumentů

Chcete-li začít používat nové uživatelské rozhraní dokumentu v modulu správa obchodních dokumentů, je třeba zapnout funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu** v pracovním prostoru **správy funkcí**.

Chcete-li tuto funkci zapnout pro všechny právnické osoby, postupujte podle následujících kroků.

1. V pracovním prostoru **Správa funkcí** na kartě **Nová** vyberte v seznamu funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu**.
2. Výběrem možnosti **Povolit nyní** zapněte vybranou funkci.
3. K nové funkci budete mít přístup po aktualizaci stránky.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Úprava šablon vlastněných ostatními poskytovateli

1. V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.

    ![Pracovní prostor správy obchodních dokumentů](./media/BDM_overview_new_template1.png)

2. V dialogovém okně vyberte dokument, který chcete použít jako šablonu, a poté vyberte možnost **Vytvořit dokument**.

    ![Dialogové okno obchodních dokumentů](./media/BDM_overview_new_template2.png)

3. V novém dialogovém okně v poli **Název** změňte požadovaným způsobem název. Text názvu se použije k pojmenování nové konfigurace formátu elektronického výkaznictví, která je automaticky vytvořena. Verze konceptu této konfigurace **(Kopie sestavy FTI odběratele (GER)**) bude obsahovat upravenou šablonu a bude automaticky označena pro spuštění tohoto formátu elektronického výkaznictví pro aktuálního uživatele. Původní šablona ze základní konfigurace formátu elektronického výkaznictví bude použita ke spuštění tohoto formátu elektronického výkaznictví pro každého jiného uživatele.
4. V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.
5. V poli **Komentář** aktualizujte poznámky pro revizi upravitelné šablony, která bude automaticky vytvořena.
6. Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.

    ![Dialogové okno vytvoření dokumentu](./media/BDM_overview_new_template3.png)

Tlačítko **Nový dokument** se používá pro vytváření úpravy šablony v konfiguraci formátu elektronického výkaznictví, kterou poskytuje jiný poskytovatel. V tomto příkladu je poskytovatelem Microsoft. Když vyberete **Nový dokument**, zobrazí se všechny šablony vlastněné aktuálními a jinými poskytovateli. Po výběru bude šablona otevřena pro úpravy. Upravená šablona bude poté uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.

Další informace naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).
