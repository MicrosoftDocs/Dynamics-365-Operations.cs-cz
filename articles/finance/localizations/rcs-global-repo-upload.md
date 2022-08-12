---
title: Vytvoření konfigurací elektronického výkaznictví v RCS a jejich odeslání do globálního úložiště
description: Tento článek vysvětluje, jak vytvořit konfiguraci elektronického vykazování (ER) ve službě Microsoft Regulatory Configuration Services (RCS) a odeslat ji do globálního úložiště.
author: JaneA07
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f73f7189ad82d85169a4e0df573dd26dab8bb009
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070593"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Vytvoření konfigurací v Regulatory Configuration Services (RCS) a jejich odeslání do globálního úložiště

[!include [banner](../includes/banner.md)]

Službu Microsoft Regulatory Configuration Services (RCS) můžete použít k navrhování konfigurací elektronického vykazování (ER) a jejich publikování, aby mohly být použity ve vaší organizaci.

Následující postupy vysvětlují, jak může uživatel v roli Správce systému nebo Návrháře elektronického výkaznictví vytvořit odvozenou verzi konfigurace ER, která byla nakonfigurována v instanci RCS, a poté odvozenou konfiguraci nahrát do globálního úložiště. 

Než budete moci tyto kroky dokončit, je nutné nejprve splnit následující předpoklady:

- Získání přístupu k prostředí RCS pro vaši organizaci.
- Vytvořte aktivního poskytovatele konfigurace a aktivujte ho. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Musíte se ujistit, že je pro vaši organizaci zajištěno prostředí RCS. Pokud pro vaši organizaci nemáte zřízenou instanci RCS, můžete tak učinit pomocí následujících kroků:

1. Ve finanční a provozní aplikaci přejděte na **Správa organizace** \> **Pracovní prostory** \> **Elektronické vykazování**.
2. V části **Související odkazy / Externí odkazy** vyberte **Regulatory services – Konfigurace** a poté postupujte podle pokynů k **přihlášení** k jejímu ustanovení.

Pokud již bylo pro vaši organizaci zřízeno prostředí RCS, přistupte k ní pomocí adresy URL a vyberte možnost **přihlásit**.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Vytvoření odvozenou verzi konfigurace v RCS

> [!NOTE]
> Pokud je to poprvé, co používáte RCS, nebudete mít k dispozici žádnou konfiguraci, ze které byste mohli odvodit. Budete muset importovat konfiguraci z globálního úložiště. Další informace viz [Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Přihlaste se** k RCS a vyberte pracovní prostor **Elektronické vykazování**.
2. Ověřte, zda máte aktivního poskytovatele konfigurace pro vaši organizaci, který je nastaven na aktivní (viz předpoklady). 
3. Vyberte **Konfigurace vykazování**.
4. Vyberte konfiguraci, ze které chcete odvodit novou verzi. Pomocí pole filtru nad stromem můžete vyhledávání zúžit.
5. Vyberte **Vytvořit konfiguraci** \> **Odvodit z názvu**.
6. Zadejte jméno a popis a poté vyberte **Vytvořit konfiguraci** k vytvoření nové odvozené verze se stavem „Koncept“.
7. Vyberte nově odvozenou konfiguraci a v případě potřeby proveďte další změny formátu konfigurace. 
8. Po dokončení změn je třeba provést nastavení **Změnit stav** pro konfiguraci **Dokončeno**, aby jej bylo možné publikovat v úložišti. Vyberte **OK**.

![Nová verze konfigurace v RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Při změně stavu konfigurace se může zobrazit chybová zpráva o ověření související s připojenými aplikacemi. Chcete-li validaci vypnout, v podokně Akce na kartě **Konfigurace** vyberte **Uživatelské parametry**, a poté nastavte **Přeskočit ověření při změně stavu konfigurace a přeskládat** možnost na **Ano** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Nahrajte konfiguraci do Globálního úložiště

Chcete-li s organizací sdílet novou nebo odvozenou konfiguraci, nahrajte ji do Globálního úložiště následujícím postupem:

1. Vyberte dokončenou verzi konfigurace a poté vyberte **Nahrát do úložiště**.
2. Vyberte **Globální (Microsoft)** a poté vyberte **Nahrát**.

    ![Nahrání do možností úložiště.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. V dialogovém okně pro potvrzení vyberte **Ano**. 
4. Podle potřeby aktualizujte popis verze a poté vyberte **OK**. Verzi můžete také volitelně nahrát do připojené aplikace nebo do úložiště GIT.  

Stav konfigurace je aktualizován na **Sdíleno** a konfigurace se nahraje do globálního úložiště. Vytvoří se také verze konceptu konfigurace, kterou jste nahráli, a lze ji použít, pokud jsou vyžadovány následné změny.

Po nahrání konfigurace do globálního úložiště s ní můžete pracovat následujícími způsoby:

- Importujte jej do instance Dynamics 365. Další informace získáte v tématu [(ER) Import konfigurací z RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Pro sdílení s třetí stranou nebo externí organizací, viz [RCS sdílení konfigurací elektronického výkaznictví (ER) s externími organizacemi](rcs-global-repo-share-configuration.md)

    ![Odvozená verze konfigurace Intrastat Contoso v globálním úložišti.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Odstranění konfigurace z globálního úložiště
Pomocí následujících kroků odstraňte konfiguraci, kterou vaše organizace vytvořila.

1. V pracovním prostoru **Elektronické výkaznictví** ověřte, že váš poskytovatel konfigurace je **Aktivní**. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. U vašeho aktivního poskytovatele konfigurace vyberte **úložiště**.
3. Vyberte typ úložiště **Globální** a vyberte **Otevřít**.
4. Na záložce s náhledem **Filtr** vyhledejte konfiguraci, kterou chcete odstranit, pomocí funkce **Filtr**.
5. Na záložce s náhledem **Verze** vyberte verzi konfigurace, kterou chcete odstranit, a poté vyberte **Odstranit**:

    ![Odstranění konfigurace z globálního úložiště.](media/RCS_Delete_from_GlobalRepo.JPG)

6. V dialogovém okně pro potvrzení vyberte **Ano**.

    ![Odstranění zprávy s potvrzením o verzi konfigurace.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Verze konfigurace je odstraněna a zobrazí se potvrzovací zpráva. 

> [!NOTE]
> Konfigurace mohou být odstraněny pouze poskytovatelem konfigurace, který je vytvořil. Pokud byla konfigurace sdílena s jinou organizací, bude nutné ji před odstraněním zrušit.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

