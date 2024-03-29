---
title: Sdílení konfigurací ER v RCS/globálním úložišti s externími organizacemi
description: Tento článek vysvětluje, jak sdílet konfigurace elektronického vykazování (ER) ve službě Microsoft Regulatory Configuration Services (RCS)/globálním úložišti přímo s externími organizacemi.
author: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
ms.openlocfilehash: d9400ffcede9924a01391a433b570651d3f0c5e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284808"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Sdílejte konfigurace elektronického vykazování (ER) v globálním úložišti služby Microsoft Regulatory Configuration Services (RCS) s externími organizacemi

[!include [banner](../includes/banner.md)]

Službu Microsoft Regulatory Configuration Services (RCS) můžete použít ke sdílení konfigurací elektronického vykazování (ER) a jejich publikování do externích organizací.

Následující postupy vysvětlují, jak uživatel RCS může sdílet verzi konfigurace ER, která byla nakonfigurována v instanci RCS, s externí organizací. Než budete moci tyto kroky dokončit, je nutné nejprve splnit následující předpoklady:

- Přistupte k RCS instanci.
- Vytvořte aktivního poskytovatele konfigurace. Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- Vytvořte a nahrajte novou verzi konfigurace ER. Pro další informace viz [Vytvoření a nahrání nových verzí konfigurace elektronického hlášení (ER)](rcs-global-repo-upload.md).

Musíte se také ujistit, že je pro vaši společnost zajištěno prostředí RCS.

1. Ve finanční a provozní aplikaci přejděte na **Správa organizace** \> **Pracovní prostory** \> **Elektronické vykazování**.
2. Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, pro její zřízení klikněte na externí odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů.

Pokud již bylo pro vaši společnost zřízeno prostředí RCS, přistupte k ní pomocí adresy URL výběrem možnosti přihlášení.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Ověřte konfiguraci, kterou chcete sdílet

Postupujte podle těchto kroků a ověřte, že konfigurace, kterou chcete sdílet, již byla nahrána do globálního úložiště.

1. V **Elektronickém výkaznictí** vyberte pracovní prostor **Úložiště** pro vašeho poskytovatele konfigurace.

    ![Poskytovatelé konfigurace.](media/1_RCS_Repo_for_config_provider.JPG)

2. Vyberte **Globální úložiště** \> **Otevřít**.
3. Vyhledejte konfiguraci, kterou chcete sdílet. Pomocí pole filtru můžete vyhledávání zúžit. Pokud nemůžete najít konfiguraci v globálním úložišti, postupujte podle těchto kroků: [Vytvořte a nahrajte novou verzi konfigurace elektronického výkaznictví (ER)](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>Sdílení konfigurací elektronického výkaznictví s externími organizacemi

Po vytvoření konfigurace u vašeho poskytovatele konfigurace ji můžete sdílet přímo s externími organizacemi pomocí pevné záložky **Sdíleno s** na stránce **Globální úložiště konfigurace**.

1. V **Elektronickém výkaznictí** vyberte pracovní prostor **Úložiště** pro vašeho poskytovatele konfigurace.
2. Vyberte **Globální úložiště** \> **Otevřít**. 
3. Vyberte konfiguraci, kterou chcete sdílet.
4. Na pevné kartě **Sdíleno s** vyberte **Organizace**.

    ![Sdíleno pomocí pevné záložky.](media/1_RCS_Repo_for_Share_with_org.JPG)

5. V dialogovém okně zadejte název domény pro externí organizaci a poté vyberte **OK**.

    ![Sdílejte konfigurační verzi pomocí dialogového okna externí organizace.](media/1_RCS_Repo_for_Share_with_form.JPG)

Konfigurace je sdílena s externí organizací a je k dispozici této organizaci v globálním úložišti. Odtud ji lze importovat do instance RCS organizace nebo do jejích instancí finančních a provozních aplikací.

6. Chcete-li zrušit sdílení konfigurace, která byla dříve sdílena s externí organizací, vyberte konfiguraci a klikněte na **Zrušit sdílení** a poté vyberte **OK**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
