---
title: Vytvoření konfigurací elektronického výkaznictví v RCS a jejich odeslání do globálního úložiště
description: Toto téma vysvětluje, jak vytvořit konfiguraci elektronického vykazování (ER) ve službě Microsoft Regulatory Configuration Services (RCS) a odeslat ji do globálního úložiště.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441216"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Vytvoření konfigurací v Regulatory Configuration Services (RCS) a jejich odeslání do globálního úložiště

[!include [banner](../includes/banner.md)]

Službu Microsoft Regulatory Configuration Services (RCS) můžete použít k navrhování konfigurací elektronického vykazování (ER) a jejich publikování, aby mohly být použity ve vaší organizaci.

Následující postupy vysvětlují, jak může uživatel v roli Správce systému nebo Návrháře elektronického výkaznictví vytvořit odvozenou verzi konfigurace ER, která byla nakonfigurována v instanci RCS, a poté odvozenou konfiguraci nahrát do globálního úložiště. 

Než budete moci tyto kroky dokončit, je nutné nejprve splnit následující předpoklady:

- Přistupte k RCS instanci.
- Vytvořte aktivního poskytovatele konfigurace. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Musíte se také ujistit, že je pro vaši společnost zajištěno prostředí RCS.

1. V aplikaci Finance and Operations přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, pro její zřízení klikněte na externí odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů.

Pokud již bylo pro vaši společnost zřízeno prostředí RCS, přistupte k ní pomocí adresy URL výběrem možnosti přihlášení.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Vytvoření odvozenou verzi konfigurace v RCS

1. V pracovním prostoru **Elektronické výkaznictví** ověřte, zda máte aktivního poskytovatele konfigurace pro vaši organizaci. 
2. Vyberte **Konfigurace vykazování**.
3. Vyberte konfiguraci, ze které chcete odvodit novou verzi. Pomocí pole filtru nad stromem můžete vyhledávání zúžit.
4. Vyberte **Vytvořit konfiguraci** \> **Odvodit z názvu**.
5. Zadejte jméno a popis a poté vyberte **Vytvořit konfiguraci** k vytvoření nové odvozené verze.
6. Vyberte nově odvozenou konfiguraci, přidejte popis verze a poté vyberte **OK**. Stav konfigurace na se změní na **Dokončeno**.

![Nová verze konfigurace v RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Při změně stavu konfigurace se může zobrazit chybová zpráva o ověření související s připojenými aplikacemi. Chcete-li validaci vypnout, v podokně Akce na kartě **Konfigurace** vyberte **Uživatelské parametry**, a poté nastavte **Přeskočit ověření při změně stavu konfigurace a přeskládat** možnost na **Ano** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Nahrajte konfiguraci do Globálního úložiště

Chcete-li s organizací sdílet novou nebo odvozenou konfiguraci, nahrajte ji do Globálního úložiště.

1. Vyberte dokončenou verzi konfigurace a poté vyberte **Nahrát do úložiště**.
2. Vyberte **Globální (Microsoft)** a poté vyberte **Nahrát**.

    ![Nahrání do možností úložiště](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. V dialogovém okně pro potvrzení vyberte **Ano**. 
4. Podle potřeby aktualizujte popis verze a poté vyberte **OK**. 

Stav konfigurace je aktualizován na **Sdílení** a konfigurace se nahraje do globálního úložiště. Odtud můžete s konfigurací pracovat následujícími způsoby:

- Importujte jej do instance Dynamics 365. Další informace získáte v tématu [(ER) Import konfigurací z RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Pro sdílení s třetí stranou nebo externí organizací, viz [RCS sdílení konfigurací elektronického výkaznictví (ER) s externími organizacemi](rcs-global-repo-share-configuration.md)

    ![Odvozená verze konfigurace Intrastat Contoso v globálním úložišti](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Odstranění konfigurace z globálního úložiště
Pomocí následujících kroků odstraňte konfiguraci, kterou vaše organizace vytvořila.

1. V pracovním prostoru **Elektronické výkaznictví** ověřte, že váš poskytovatel konfigurace je **Aktivní**. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. U vašeho aktivního poskytovatele konfigurace vyberte **úložiště**.
3. Vyberte typ úložiště **Globální** a vyberte **Otevřít**.
4. Na záložce s náhledem **Filtr** vyhledejte konfiguraci, kterou chcete odstranit, pomocí funkce **Filtr**.
5. Na záložce s náhledem **Verze** vyberte verzi konfigurace, kterou chcete odstranit, a poté vyberte **Odstranit**:

    ![Odstranění konfigurace z globálního úložiště](media/RCS_Delete_from_GlobalRepo.JPG)

6. V dialogovém okně pro potvrzení vyberte **Ano**.

    ![Odstranění zprávy s potvrzením o verzi konfigurace](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Verze konfigurace je odstraněna a zobrazí se potvrzovací zpráva. 

> [!NOTE]
> Konfigurace mohou být odstraněny pouze poskytovatelem konfigurace, který je vytvořil. Pokud byla konfigurace sdílena s jinou organizací, bude nutné ji před odstraněním zrušit.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]