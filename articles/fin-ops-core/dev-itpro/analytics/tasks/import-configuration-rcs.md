---
title: (Elektronické výkaznictví) Import konfigurací z RSC
description: Toto téma obsahuje informace o tom, jak může uživatel importovat novou verzi konfigurace elektronického výkaznictví z RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143216"
---
# <a name="er-import-configurations-from-rcs"></a>(Elektronické výkaznictví) Import konfigurací z RSC

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Regulatory Configuration Services (RCS). V tomto příkladu vyberete verzi konfigurace elektronického výkaznictví, která byla nakonfigurována v instanci RCS, a importujte ji do aktuální instance pro vzorovou společnost, Litware, Inc. Tyto kroky lze provádět ve všech společnostech, protože konfigurace Felektronického výkaznictví je sdílena mezi společnostmi. K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). Chcete-li dokončit tento postup, musíte mít také přístup k instanci RCS, která obsahuje alespoň jednu konfiguraci elektronického výkaznictví ve stavu **dokončeno** nebo **sdíleno**.

1. Přejděte na **Správa organizace** > **Pracovní prostory** > **Elektronické výkaznictví**. 
2. Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). 
3. Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, klikněte na externí odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů pro zřízení RCS prostředí. 
4. Klikněte na **Parametry elektronického výkaznictví**. 
5. Klikněte na kartu **RCS**. 
6. Pokud jste již RCS prostředí pro vaši společnost zřídili, použijte pro přístup k ní uvedené adresy URL na stránce. 
7. Zavřete stránku. 

## <a name="register-a-new-er-repository"></a>Registrace nového úložiště elektronického výkaznictví 
1. Označte na seznamu vybraný řádek. 
2. Vyberte poskytovatele Litware, Inc. 
3. Klikněte na možnost Úložiště. 
4. Klepnutím na možnost Přidat otevřete dialogové okno. 
5. V poli Typ úložiště konfigurace zadejte RCS. 
6. Klikněte na Vytvořit úložiště. 
7. V poli zobrazovaného názvu prostředí RCS zadejte nebo vyberte hodnotu. 
8. Vyberte příslušnou instanci RCS. Všimněte si, že jich můžete mít několik. 
9. Klepněte na tlačítko OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Import konfigurací elektronického z úložiště založeného na RCS
1. Klikněte na **Zobrazit filtry**. 
2. Zadejte hodnotu filtru „RCS“ v poli **Název** za použití operátoru filtru **začíná na**. 
3. Po otevření vybraného úložiště na stránce **Připojit k Regulatory Configuration Services** klikněte na odkaz **Zde klikněte pro připojení k Regulatory Configuration Services**. 
4. Klikněte na **Otevřít**. 
5. Klepněte na tlačítko **Zavřít**. 
6. Vyberte požadovanou verzi konfigurace elektronického výkaznictví a kliknutím na **Import** ji převeďte do aktuální instance.

